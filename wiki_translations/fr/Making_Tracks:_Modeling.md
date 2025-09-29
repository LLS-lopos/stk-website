---
title: 'Faire des Pistes: Modélisation'
toc: true
---
## Introduction à la modélisation

Passons maintenant à la modélisation de la piste. Grâce à quelques fonctionnalités avancées de Blender, les premières étapes seront simples et efficaces.

Cette approche est particulièrement adaptée aux circuits extérieurs, mais reste pertinente pour tout type de piste, notamment pour définir précisément la ligne de course. Pour les circuits intérieurs, vous pourrez ultérieurement remplacer cette structure par le bâtiment lui-même, mais cette étape initiale reste essentielle pour garantir une expérience de conduite optimale.

{% popup_info **Alternative avancée** :
- Utilisez l'outil de biseautage de courbe pour un meilleur contrôle de la géométrie
- Consultez ce [tutoriel](https://en.wikibooks.org/wiki/Blender_3D:_Noob_to_Pro/Bevelling_a_Curve) pour plus de détails
- Conversion requise avant l'export : **Objet > Convertir > Maillage**
- La méthode du modificateur de réseau reste utile pour définir la ligne de course
%}
<div><br/></div>

## Création du segment de base

1. **Préparation de la scène** :
   - Supprimez les objets par défaut (cube, lampe, caméra)
   - Créez un nouveau plan

2. **Dimensions du segment** :
   - Passez en mode édition (TAB)
   - Largeur (Y) : 10-12 unités Blender
   - Longueur (X) : 2-4 unités Blender

3. **Texturation (optionnelle)** :
   - Appliquez des coordonnées UV pour la texture de la route
   - Recommandé pour les pistes extérieures
   - Facilite grandement le travail d'édition UV ultérieur

## Création du tracé de la piste

### Configuration de la courbe de base

1. **Création** :
   - Ajoutez une courbe de Bézier
   - Nommez-la de manière explicite (ex: "Trace_Piste_Principale")

2. **Paramètres initiaux** :
   - Mode : **2D** pour une meilleure précision
   - Méthode de vrillage : **Z-Up** (essentiel pour éviter les inclinaisons indésirables)
   - Ces paramètres sont modifiables ultérieurement

3. **Conseils** :
   - Le mode 2D facilite le positionnement des points
   - Passez en 3D pour ajouter du relief (collines, dénivelés)
   - Vérifiez régulièrement l'orientation de la courbe

## Application des modificateurs

### 1. Configuration du modificateur Array (Réseau)

1. Sélectionnez votre segment de route
2. Ajoutez un modificateur **Array**
3. Paramètres :
   - Type d'ajustement : **Ajuster la courbe**
   - Courbe : sélectionnez votre courbe de Bézier
   - Cochez **Fusionner** pour un rendu continu

### 2. Configuration du modificateur Curve (Courbe)

1. Ajoutez un modificateur **Curve**
2. Paramètres :
   - Objet : sélectionnez votre courbe de Bézier
   - Vérifiez que la direction de la courbe est correcte

## Façonnage de la piste

### Édition de la courbe

1. **Mode édition** :
   - Sélectionnez la courbe
   - Passez en mode édition (TAB)

2. **Modification du tracé** :
   - Ajustez les poignées pour modifier les courbes
   - Ajoutez des points avec Ctrl+Clic gauche
   - La piste se met à jour en temps réel

3. **Fermeture de la boucle** :
   - Rapprochez les extrémités
   - Activez le mode cyclique : **Courbe > (Dés)activer Cyclique** (ou Alt+C)
   - Vérifiez la continuité du tracé

{%popup_info **Attention aux transformations** :
- **Ne jamais** mettre à l'échelle ou faire pivoter les courbes en mode objet
- Pour les modifications d'échelle, utilisez uniquement le mode édition

**Si vous avez déjà transformé l'objet** :
1. Sélectionnez la courbe et le segment
2. Ctrl+A > Appliquer > Rotation/Échelle
3. Si nécessaire, ajustez le rayon dans le panneau latéral (N)

**Conversion 2D/3D** :
- Passez temporairement en 3D pour les rotations
- Revenez en 2D après application%}

## Finalisation de la géométrie

Pour figer la géométrie tout en conservant la possibilité de modifications :

1. Sélectionnez le segment de route
2. En mode objet, appliquez successivement :
   - Le modificateur Array
   - Le modificateur Curve

**Important** : Cette opération est irréversible. Pensez à sauvegarder une copie de votre fichier .blend avant de procéder.

## Ajustement des jonctions

### Problèmes courants
- Chevauchement des extrémités
- Espace trop important
- Désalignement des bords

### Méthode de correction
1. Passez en mode édition (TAB)
2. Utilisez l'outil de sélection pour ajuster les points problématiques
3. Supprimez les doublons (M > Par distance)
4. Raccordez proprement les extrémités avec F
5. Vérifiez la continuité de la géométrie

## Optimisation de la jouabilité

Pour une expérience de conduite optimale :

1. **Inclinaison des virages** :
   - Ajoutez du dévers dans les courbes serrées
   - Ajustez progressivement pour un effet naturel

2. **Largeur de piste** :
   - Élargissez les zones de virage
   - Prévoyez de l'espace après les sauts
   - Créez des zones de dégagement

3. **Consultez le guide** :
   - [Directives de jouabilité](Making_Tracks:_Notes#gameplay)
   - Conseils pour le rythme de la piste
   - Équilibre entre difficulté et accessibilité

{% include art_portal %}
