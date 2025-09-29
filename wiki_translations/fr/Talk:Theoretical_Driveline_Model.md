---
title: 'Discussion:Modèle théorique des lignes de conduite'
toc: true
---
## Concept des quads et des lignes de conduite

Les lignes de conduite (drivelines) sont utilisées pour indiquer à l'IA où conduire et pour déterminer l'ordre des karts : si un kart est sur la ligne de conduite, on sait quelle partie de la piste il a parcourue, ce qui permet de comparer la progression des karts. Si un kart sort de la ligne de conduite, le point de ligne de conduite le plus proche est sélectionné pour déterminer la distance parcourue par ce kart lors de la comparaison des distances, et pour déterminer où se diriger.

Tous les endroits où un kart est autorisé à rouler sont marqués par des quads. Les quads n'ont pas besoin d'être connectés (bien qu'ils le soient généralement). Une séquence de quads forme ensemble une ligne de conduite, indiquant dans quel ordre l'IA doit parcourir les quads. Exemple :

{% single_gallery /assets/wiki/New_driveline.jpg %}

Une *section de ligne de conduite* est une séquence de quads connectés entre eux. Ces sections de ligne de conduite sont ensuite connectées pour créer les lignes de conduite complètes d'une piste. Dans l'exemple ci-dessus, il y aurait deux sections de ligne de conduite : la ligne de conduite principale en noir qui crée le tour, et la ligne de conduite en rouge indiquant un raccourci (ou un chemin alternatif) pour les karts.

Dans Blender, les quads d'une section de ligne de conduite sont créés à partir d'un simple maillage :

{% single_gallery /assets/wiki/Driveline_blender.jpg %}

Le début d'une section de ligne de conduite est marqué par deux arêtes non connectées. Le *point de départ* d'une ligne de conduite est le point médian des deux sommets d'extrémité des arêtes. Le *point d'arrivée* est le point médian des quatre sommets du dernier quad. Les arêtes reliant les sommets correspondants des côtés gauche et droit sont facultatives. Donc, si vous voulez diviser un quad en deux (par exemple pour mieux modéliser la forme de la piste, ou pour aider l'IA), vous pouvez simplement ajouter les deux sommets, vous n'êtes pas obligé de les connecter. Il est cependant important que les deux côtés des lignes de conduite contiennent le même nombre de sommets (sinon les quads ne pourront pas être créés correctement). Si vous convertissez la piste principale comme décrit dans le tutoriel de création de piste, le maillage créé aura automatiquement le même nombre de points de chaque côté.

Il y a deux raisons pour lesquelles vous pourriez vouloir diviser une seule section de ligne de conduite en sections plus petites :

1. Une section de ligne de conduite peut être marquée comme 'invisible', c'est-à-dire qu'elle ne sera pas affichée dans la mini-carte. Cela doit être utilisé pour les raccourcis cachés qui doivent être découverts par le joueur. Ceci est fait en donnant à la ligne de conduite la propriété 'invisible' avec une valeur non nulle.
2. (pas encore implémenté) : une section de ligne de conduite peut être marquée comme 'désactivée', ce qui signifie qu'elle ne sera pas utilisée (ni affichée) dans le jeu. Cela peut être utilisé pour forcer l'IA à emprunter un certain chemin et ainsi s'assurer que l'IA peut rouler sur tous les chemins possibles.

Le script d'exportation de piste distingue deux types de sections de ligne de conduite :

### Sections de ligne de conduite principales

La ligne de conduite principale qui indique le chemin 'principal' que les karts doivent emprunter. Les quads de la ligne de conduite principale doivent former un seul tour. Une section de ligne de conduite est marquée comme faisant partie de la ligne de conduite principale en lui donnant le type "main-driveline".

{% single_gallery /assets/wiki/Main_driveline.jpg %}

L'exemple ci-dessus ne montre qu'une seule section de ligne de conduite. L'ordre dans lequel les sections de ligne de conduite principales sont connectées est déterminé comme suit :

1. La section de ligne de conduite principale dont le point de départ est le plus proche de (0,0,0) est sélectionnée en premier.
2. Parmi toutes les sections de ligne de conduite principales restantes, celle dont le point de départ est le plus proche du point d'arrivée de la dernière section de ligne de conduite principale sélectionnée est choisie ensuite.

Cette dernière étape est ensuite répétée jusqu'à ce que toutes les sections de ligne de conduite principales soient sélectionnées, et donc l'ordre dans lequel les sections de ligne de conduite principales sont connectées est déterminé. Les quads sont ensuite créés à partir des sections de ligne de conduite séparées, et un quad est ajouté de la dernière section de ligne de conduite ajoutée pour revenir à la première section de ligne de conduite. Cela crée le tour principal.

Note : Selon l'expérience, nous pourrions soit ajouter des quads pour connecter chaque section de ligne de conduite, soit ne pas ajouter la section de ligne de conduite entre la dernière et la première section.

### Sections de ligne de conduite normales

Les sections de ligne de conduite normales sont indiquées en donnant au maillage la propriété de type "driveline". Ces lignes de conduite sont utilisées pour créer des chemins 'alternatifs' sur lesquels rouler.

{% single_gallery /assets/wiki/Driveline.jpg %}

La procédure par laquelle ces sections de ligne de conduite sont ajoutées est similaire à la procédure ci-dessus :

1. Sélectionnez toutes les sections de ligne de conduite principales.
2. Parmi toutes les sections de ligne de conduite normales, celle dont le point de départ est le plus proche du point central de n'importe quel quad dans les lignes de conduite sélectionnées est choisie. Une nouvelle connexion est établie depuis le quad le plus proche vers la nouvelle section de ligne de conduite sélectionnée.

Cette procédure est ensuite répétée jusqu'à ce que tous les quads aient été ajoutés. Notez qu'en déplaçant les deux sommets de départ, vous pouvez contrôler exactement quel quad est sélectionné comme prédécesseur d'une section de ligne de conduite normale : il suffit de déplacer les deux sommets à proximité du centre du quad auquel vous voulez qu'il soit connecté.

FIXME : Qu'en est-il de la fin d'un quad nouvellement sélectionné ? Cela est-il également ajouté ???

## Concept détaillé : QuadGraph

Bien que la description jusqu'à présent corresponde exactement à ce qui est pris en charge par l'exportateur de piste, le concept réel implémenté dans STK permet une structure plus complexe. Ceci est réalisé en maintenant deux structures de données : une contenant la liste de tous les quads, et une décrivant comment les quads sont connectés entre eux, appelée graphe de quads. La principale différence entre les deux structures de données est qu'un quad dans la liste de tous les quads peut être utilisé plusieurs fois dans le graphe. Le graphe est constitué de nœuds - par défaut, chaque quad correspond à un nœud de graphe avec le même numéro - c'est exactement ce que suppose l'exportateur de piste. Mais ce n'est pas obligatoire : une partie de la piste pourrait ne pas être utilisée pour une course particulière (pensez à une piste de ville où plusieurs circuits de course différents peuvent être définis).

Le graphe définit pour chaque nœud de graphe à quel quad il appartient et quels sont ses successeurs possibles. Normalement, chaque quad n'aura qu'un seul successeur, mais en cas de raccourci ou de branche de la piste, il pourrait en avoir plusieurs.

Compte tenu des définitions de quads de l'image, les graphes suivants pourraient être définis :

### Boucle simple

Un graphe avec les nœuds 1 à 29, correspondant aux quads 1 à 29. L'ordre est alors

`1 → 2 → 3 → ... → 29 → 1. `

{% single_gallery /assets/wiki/Quad_graph_1.jpg %}

Cela définit une boucle simple, parcourue dans le sens des aiguilles d'une montre. Le raccourci n'est pas autorisé (pour l'IA, il n'y a pas de restriction sur l'endroit où les joueurs peuvent rouler).

### Boucle inverse

Un graphe avec les nœuds 1 à 29, correspondant aux quads 1 à 29 et le graphe :

`1 → 29 → 28 → ... → 2 → 1.`

Cela donne une boucle simple similaire à celle ci-dessus, mais elle est parcourue en sens inverse (c'est-à-dire dans le sens antihoraire).

### Boucle simple avec raccourci

{% single_gallery /assets/wiki/Quad_graph_2.jpg %}

Pour cela, nous avons besoin d'un graphe avec 34 nœuds, correspondant aux 34 quads. La boucle principale sera définie comme dans l'exemple 1, mais nous ajoutons en plus :

`15 → 30 → 31 ... → 34 → 23`

Cela permet à l'IA de choisir l'un ou l'autre des deux chemins (les critères de sélection du chemin ne sont pas encore définis - pour l'instant, c'est une sélection aléatoire).

Les nombres indiquent le numéro des quads. Cette partie ne définit pas dans quel ordre les quads doivent être parcourus, ni si le raccourci doit être utilisé ou non, elle définit uniquement quelle partie de la piste peut être utilisée.

### Une boucle à l'intérieur de la piste

La structure des lignes de conduite nous permet également de définir une boucle, c'est-à-dire de forcer l'IA à faire un cercle avant de continuer, voir l'image :

{% single_gallery /assets/wiki/Quad_graph_3.jpg %}

(Notez qu'il s'agit très probablement d'un exemple absurde uniquement - pour qu'une piste comme celle-ci soit équitable, les karts des joueurs devraient faire la même boucle, ce qui signifie qu'il doit y avoir un moyen d'indiquer cela au joueur, ce que nous n'avons pas actuellement).

Pour ce faire, nous avons besoin de nœuds de graphe supplémentaires pour les sections qui sont parcourues deux fois. Ainsi, les nœuds de graphe 1 à 34 correspondent aux quads 1 à 34, puis des nœuds de graphe supplémentaires 35 à 43 qui sont mappés aux quads 15 à 23 (à nouveau). Ainsi, les quads 15 à 23 ont chacun deux nœuds de graphe associés, mais chaque nœud de graphe a toujours exactement un quad. Ensuite, nous pouvons définir le graphe suivant :

`1 → 2 → ... 14 → 15 → 16 → ... → 23 → 34 → 33 → ... → 30 → ...`

Cela définit la première partie de la boucle : rouler à l'envers sur le raccourci jusqu'au nœud de graphe 30 (qui est le quad 30). Ensuite, nous utilisons le quad 15 pour la deuxième fois, nous utilisons donc les nœuds de graphe supplémentaires ici :

`... 30 → 35 [15] → 36 [16] → ... → 43 [23] → 24 → 25 → ... → 29 → 1`

Entre [] se trouvent les numéros de quad correspondants pour les nœuds de graphe 35 à 43. En ayant des couches de nœuds de graphe supplémentaires, l'IA suivra simplement le graphe jusqu'à la fin (il n'y a donc pas de boucles dans le graphe, sauf pour commencer un nouveau tour), mais les mappages des nœuds de graphe aux quads forcent l'IA à parcourir une boucle.
