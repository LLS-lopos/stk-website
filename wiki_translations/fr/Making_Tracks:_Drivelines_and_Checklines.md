---
title: 'Faire des Pistes: Lignes de conduite et de contrôle'
toc: true
---
{% popup_info "Cette page fournit des instructions pratiques pour la création de lignes de conduite. Pour plus de détails et une explication plus complexe, ainsi qu'une discussion sur les fonctionnalités non encore implémentées, voir la page [Discussion: Modèle théorique des lignes de conduite](Talk:Theoretical_Driveline_Model)." %}

Les lignes de conduite indiquent à SuperTuxKart où se trouve la piste. Elles sont représentées dans Blender par une série de quads connectés, avec le début marqué par une structure spéciale. Elles ne sont pas visibles pendant le jeu, sauf si vous activez le [mode débogage artiste](Artist_Debug_Mode).

## Création de la driveline principale

*Note : Les deux méthodes mentionnées recommandent de supprimer les faces de la ligne de conduite. Cette opération n'est en fait pas nécessaire, mais elle facilite la visualisation de la piste.*

### Si vous avez suivi le module précédent

Vous aurez déjà une piste plate composée de quads. Vous pouvez simplement dupliquer cette piste, passer en mode édition, sélectionner tous les points avec le raccourci clavier "a", taper sur la touche Suppr et supprimer **Faces Seulement**. Suivez ensuite les instructions ci-dessous pour créer une ligne de départ.

### Si vous avez fait une piste d'une autre manière

Commencez par un plan quadratique et supprimez uniquement sa face (en préservant les sommets et les arêtes). Ensuite, connectez des points pour former une série de quads le long de votre piste en boucle. Assurez-vous que la ligne de conduite tourne en douceur dans les virages, sans quoi les karts IA pourraient avoir des difficultés à suivre le tracé.

{% single_gallery "/assets/wiki/Driveline_bad.jpg" %}

### Création de la ligne de départ

La ligne de départ d'une piste dans SuperTuxKart est marquée par un espace entre deux quads déconnectés, avec des lignes "antennes" partant des extrémités du quad qui servira de ligne de départ. Voici une illustration :

{% single_gallery "/assets/wiki/Driveline_start.jpg" %}

### Rendre la driveline active

Pour que l'exportateur reconnaisse la ligne de conduite, sélectionnez l'objet de la ligne de conduite, puis dans les propriétés SuperTuxKart, définissez "Type" sur "Driveline (main)". Vous pouvez ignorer la propriété "Activate" pour l'instant.

## Création de transmissions secondaires/alternatives

Bien que chaque piste ne puisse avoir qu'une seule ligne de conduite principale, vous pouvez ajouter des lignes secondaires pour les raccourcis ou itinéraires alternatifs. Ces lignes secondaires suivent la même structure que la ligne principale, mais au lieu de former une boucle complète :

1. Placez les antennes près de deux points d'un quad de la ligne principale pour indiquer où les karts IA doivent quitter la piste principale.
2. Positionnez l'extrémité du dernier quad à l'endroit où l'itinéraire alternatif doit rejoindre la piste principale.
3. Dans les propriétés de l'objet, définissez le type sur "Driveline (additional)".

Voici une illustration :

{% single_gallery "/assets/wiki/Driveline_shortcut_entrance.jpg" %}

## Checklines

### Création de Checklines

Les lignes de contrôle servent à détecter le passage des karts et à empêcher les raccourcis. Pour en créer une :

1. Tracez un segment de ligne avec exactement deux points
2. Positionnez ce segment en travers de la piste

**Recommandations :**
* Utilisez les lignes de contrôle pour les raccourcis majeurs, pas pour les coupes de virage mineures
* Donnez une largeur suffisante pour détecter les karts légèrement hors-piste
* Évitez les emplacements où la ligne pourrait être manquée selon l'itinéraire emprunté
* Créez une chaîne de plusieurs lignes de contrôle pour assurer un ordre de passage cohérent
* Au minimum, prévoyez 3 lignes de contrôle par piste, en plus de la ligne d'arrivée

### Activation des lignes de contrôle

Pour configurer les lignes de contrôle :

1. Sélectionnez une ligne de contrôle
2. Dans les propriétés SuperTuxKart, définissez le type sur "Checkline"
3. Renseignez les paramètres :
   - **Nom** : Identifiant unique de la ligne (ex: "Controle1")
   - **Activate** : Nom de la prochaine ligne de contrôle à activer

**Cas particuliers :**
* Pour la dernière ligne avant la ligne d'arrivée, entrez "lap" dans le champ "Activate"
* Pour la première ligne, sélectionnez la **ligne de conduite principale** et définissez sa propriété "Activate" sur le nom de la première ligne de contrôle
* Pour les itinéraires alternatifs, utilisez le même nom de groupe pour les lignes concernées

## Lignes d'arrivée supplémentaires

Si la ligne de départ est trop étroite ou difficile à franchir, vous pouvez ajouter des lignes d'arrivée supplémentaires :

1. Créez une ligne avec exactement deux points
2. Dans les propriétés SuperTuxKart, définissez le type sur "Lap line"
3. Ces lignes seront activées par les lignes de contrôle configurées avec "lap"

{% popup_info "Important : Définissez la propriété 'Activate' de chaque ligne d'arrivée supplémentaire sur la prochaine ligne de contrôle !" %}

## Prochaines étapes

Votre piste est maintenant configurée avec :

* Des lignes de conduite principales et secondaires
* Un système de détection des passages
* Des lignes de contrôle pour valider les tours

Dans le prochain module, vous apprendrez à :
1. Exporter votre piste
2. La tester dans SuperTuxKart
3. Déboguer et affiner votre création

{% include art_portal %}
