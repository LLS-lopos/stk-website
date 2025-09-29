---
title: 'Faire des Pistes: Annexe A: Dépannage'
display_title: true
---
Bien que le processus de construction de pistes soit généralement assez simple et que les exportateurs fonctionnent généralement bien, des problèmes peuvent survenir. Si vous ne trouvez rien d'utile sur cette page, n'hésitez pas à rechercher votre problème ou à demander de l'aide sur le [forum](https://forum.freegamedev.net/viewforum.php?f=16). N'oubliez pas de lire également la page [Communication](Communication) si vous postez des messages sur le forum.

{% start_liquid qa %}

Mes karts AI quittent la route !

Les raisons peuvent être multiples :

* Votre transmission est mal placée.
* Votre transmission présente une rupture. 
* Votre route prend un virage trop serré. 
* Votre route est trop étroite.

Essayez de corriger les problèmes qui se présentent et voyez si cela vous aide.

{% end_liquid %}

{% start_liquid qa %}

Les karts AI sont sauvés de façon aléatoire ou lorsqu'ils sont lancés par une fermeture éclair (zipper)

Pour décider s'il faut secourir un kart, SuperTuxKart effectue des raycasts pour déterminer si un kart est sur une surface ou non. Lorsqu'un kart est lancé par une fermeture éclair sans surface en dessous, STK détectera que le kart est hors piste et doit être secouru. Pour éviter cela, créez une surface basse polygone sous la surface de conduite principale ou la trajectoire de lancement pour que STK ne détecte pas un faux positif de besoin de sauvetage. Texturez la surface avec une texture transparente ou définissez-la comme "Physics only". Voir [Physique#interaction-kart-objet](Physics#kart-object-interaction) pour plus d'informations.

{% end_liquid %}

{% start_liquid qa %}

Les décorations transparentes ou translucides n'apparaissent pas correctement dans le jeu !

Il s'agit probablement d'un problème de tri. Essayez d'exporter les parties transparentes en tant qu'objets séparés ("Object" dans le panneau des propriétés de l'objet SuperTuxKart dans Blender). Si votre section transparente inclut une partie de la surface de conduite principale, assurez-vous de cocher la case "Drivable" dans le panneau des propriétés de l'objet SuperTuxKart. Assurez-vous également que "Désactiver l'écriture dans le Z-buffer" est coché pour toutes les textures transparentes ou partiellement transparentes dans le panneau des propriétés d'image SuperTuxKart.

{% end_liquid %}

{% start_liquid qa %}

Les objets transparents s'affichent bizarrement dans Blender !

C'est pour la même raison évoquée dans la question ci-dessus : problèmes de tri, et c'est un problème connu de Blender. Malheureusement, nous ne pouvons pas changer cela. Essayez de cocher la case "X-Ray" sous "Affichage" dans la section "Objet" de la fenêtre des propriétés de Blender pour vos objets transparents. Ce n'est pas une solution miracle, mais cela pourrait aider un peu.

{% end_liquid %}

{% start_liquid qa %}

Mon kart glisse partout et je ne peux pas bien diriger/accélérer !

C'est probablement dû à un lissage des normales. Désactivez le lissage des normales dans le panneau des propriétés de scène SuperTuxKart.

{% end_liquid %}

{% start_liquid qa %}

Mon kart s'envole dans les airs quand j'essaie de jouer sur ma piste !

Votre piste est probablement trop étroite ou vous avez trop de karts par rangée sur la ligne de départ. Lorsque le [Mode Débogage Artiste](Artist_Debug_Mode) est activé, si vous êtes placé dans les airs, vous commencerez à voler ; si le Mode Débogage Artiste n'est pas activé, le jeu plantera. Il existe trois façons de résoudre ce problème :

* Élargissez la piste au niveau de la ligne de départ.
* Réduisez la valeur **Karts par rangée** sur la ligne de départ sous **Positions de la ligne de départ** dans le panneau des propriétés de scène SuperTuxKart.
* Réduisez la valeur **Distance latérale de départ** dans la même section que ci-dessus.

Une autre possibilité est que votre piste a les normales du mauvais côté. Pour vérifier si c'est le problème, passez en mode édition sur votre maillage de piste, développez votre menu **Superposition de la vue** en haut à droite, tout en bas vous trouverez des boutons pour activer les superpositions de **Normales**. Si elles apparaissent sous le maillage, sélectionnez les faces que vous souhaitez corriger et allez dans **Maillage > Normales > Retourner**.

![Display_normals]({{ '/assets/wiki/Display_normals.jpg' | prepend: site.baseurl }})

{% end_liquid %}

{% include art_portal %}

{% end_liquid %}

{% start_liquid qa %}

Les objets transparents s'affichent bizarrement dans Blender!

Dans Blender pour voir la transparence, changé le "mode de fusion" dans **Paneau de propriété > Matériau > Réglage > mode de fusion**, choisir selon les cas "Mélange Alpha" -> alpha graduer ou "Seuil alpha" -> entre 1-0.5 transparent 100% et <0.5 100% Opaque

{% end_liquid %}

{% start_liquid qa %}

Mon kart glisse et je ne peux pas diriger/accélérer correctement!

Si ce n'est pas déjà fait activer "High tires adhesion" et/ou "Affect gravity"; Sinon il s'agit très probablement d'une conséquence du lissage des normales. Désactivez le lissage normal dans le panneau des propriétés de la scène de SuperTuxKart.

{% end_liquid %}

{% start_liquid qa %}

Mon kart s'envole en l'air lorsque j'essaie de jouer sur ma piste!

Il est probable que votre piste soit trop étroite ou que vous ayez trop de karts par rangée sur la ligne de départ. Lorsque le [Mode débogage artiste](Artist_Debug_Mode) est activé, si vous êtes placé en l'air, vous commencerez à voler ; si le Artist Debug Mode n'est pas activé, le jeu plantera. Il y a trois façons de résoudre ce problème :

* Élargir la piste au niveau de la ligne de départ.
* Réduisez la valeur de **Karts per row** au départ sous **Start line positions** dans le panneau des propriétés de scène SuperTuxKart.
* Réduisez la valeur de la **Start sideways distance** dans la même section que ci-dessus.

Une autre possibilité est que les normales de votre piste soient du mauvais côté. Pour vérifier si c'est le cas, passez en mode édition sur le maillage de votre piste, développez votre menu **Viewport Overlays** en haut à droite, tout en bas vous trouverez des boutons pour activer les recouvrements **Normals**. Aussi vous pouvez simplement coché **orientation des faces**, la partie qui sera visible en jeu apparait en bleu et la partie non-visible en rouge.
Si elles apparaissent (en bas du maillage/en rouge sur une suface praticable), sélectionnez le(s) face(s) que vous souhaitez corriger, et allez dans **Maillage > Normales > Inverser**.

![Display_normals]({{ '/assets/wiki/Display_normals.jpg' | prepend: site.baseurl }})

{% end_liquid %}

{% include art_portal %}
