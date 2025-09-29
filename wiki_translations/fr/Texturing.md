---
title: Texturation
toc: true
---
## Introduction à la texturation

La texturation est l'application d'images sur des objets 3D pour améliorer leur réalisme. Les méthodes varient selon la version de Blender utilisée. Ce guide complète les informations de la page [Matériaux](Materials) et fournit des instructions spécifiques à SuperTuxKart.

## Configuration pour Blender 2.80 et versions ultérieures

### Gestion des matériaux
- Les matériaux Blender sont obligatoires pour assigner des textures
- Deux méthodes d'accès :
  1. **Fenêtre Propriétés** > onglet **Matériau**
  2. **Éditeur de shaders** (plus avancé)

### Bonnes pratiques
- Créez toujours un matériau avant d'appliquer des textures
- Nommez clairement vos matériaux (ex: "route_asphalte", "herbe_paysage")

## Configuration pour Blender 2.63 à 2.79

### Approche recommandée
1. Utilisez uniquement les textures UV
2. Ignorez la section **Texture** des propriétés
3. Ne créez pas de matériaux complexes (non exportés)

### Étapes essentielles
1. Créez votre maillage
2. Définissez les coordonnées UV
3. Appliquez la texture via l'éditeur UV
4. SuperTuxKart gérera les matériaux automatiquement

**Important** : Les matériaux complexes et les nœuds de cycles ne seront pas exportés dans le jeu.

## Application des textures (Blender 2.80+)

### Configuration de base
- Les textures s'appliquent via les matériaux
- Une seule configuration de texture est prise en compte par matériau
- Priorité alphabétique : la configuration du matériau dont le nom vient en dernier dans l'ordre alphabétique est utilisée

### Paramètres recommandés
Dans le nœud **Principled BSDF** :
- **Spéculaire** : 0
- **Rugosité** : 1

Ces paramètres offrent un aperçu plus fidèle du rendu final dans SuperTuxKart, particulièrement en mode **Aperçu des matériaux** ou **Texture**.

### Méthode 1 : Fenêtre Propriétés

1. **Sélection du matériau**
   - Créez ou sélectionnez un matériau existant
   - Ajoutez un emplacement de matériau si nécessaire

2. **Configuration de la texture**
   - Allez dans **Couleur de base**
   - Cliquez sur le point jaune
   - Choisissez **Texture** > **Image Texture**
   - Sélectionnez ou importez une image

3. **Validation**
   - Le nom du fichier s'affiche à titre informatif
   - Le matériau est prêt pour une configuration avancée si nécessaire

### Méthode 2 : Éditeur de shaders (avancé)

#### Configuration initiale
1. Ouvrez l'**Éditeur de shaders**
2. Créez/sélectionnez un matériau
3. Vérifiez la présence des nœuds :
   - **Sortie de matériau**
   - **Principled BSDF**

#### Ajout d'une texture
1. **Insertion du nœud**
   - Raccourci : `Shift + A`
   - Menu : **Ajouter > Texture > Image Texture**
   - Placez-le de manière à ne pas obstruer les autres nœuds

2. Configuration de base
   - Sélectionnez une image existante ou importez-en une nouvelle
   - Connectez la sortie **Couleur** à **Couleur de base** du BSDF
   - (Optionnel) Connectez **Alpha** à **Alpha** pour la transparence

#### Aperçu dans Blender
- La connexion alpha n'affecte pas l'exportation
- Elle permet de visualiser la transparence dans Blender
- Le nom du fichier est affiché à titre informatif

## Sources recommandées pour les textures

### 1. Dépôt média officiel

#### Avantages
- Textures optimisées pour SuperTuxKart
- Effets graphiques avancés inclus :
  - Cartes de brillance (gloss)
  - Cartes normales (normal maps)
  - Autres effets spéciaux
- Pas besoin d'inclure les fichiers avec votre piste

#### Emplacement
- Dossier : `/stk_media_repo/textures/`
- Accessible depuis :
  1. Éditeur UV/Image
  2. Nœuds de texture
  3. Sélecteur de fichiers de Blender

{% popup_info "**Bonnes pratiques pour les chemins de textures**

### À FAIRE
- Utilisez des chemins relatifs
- Structurez votre projet comme suit :
  ```
  stk_media_repo/
  └── tracks/
      └── votre_piste/
          ├── models/
          └── textures/
  ```
- Référencez les textures depuis `stk_media_repo`

### À ÉVITER
- Chemins absolus
- Références à `stk-assets`
- Intégration des textures dans le fichier .blend
- Noms de fichiers avec espaces ou caractères spéciaux" %}

## Personnalisation des textures

### Coloration des vertex
Alternative puissante aux multiples textures :
- Appliquez différentes teintes sur un même matériau
- Idéal pour les variations de couleur
- Exemple : Le fond marin de Gran Paradiso utilise une texture rocheuse beige teintée en bleu-vert

### Types de cartes de texture
- **Texture de base** : Fichier principal (ex: `rock.png`)
- **Carte de brillance** : Se termine par `_gloss` (ex: `rock_gloss.png`)
- **Carte normale** : Se termine par `_normal` (ex: `rock_normal.png`)

{% popup_info "**Astuce** :
- Utilisez toujours la texture de base comme référence principale
- Les cartes de brillance et normales sont appliquées automatiquement
- Vérifiez les extensions des fichiers pour éviter les erreurs" %}

## Autres sources de textures

{% popup_info "**Chemin des textures**
Il est **très** important que les chemins vers les textures que vous utilisez soient corrects dans Blender, sans quoi personne ne pourra comprendre votre fichier. Placez toujours les fichiers de votre piste dans le dépôt média comme s'il s'agissait d'une partie du jeu de base. De plus :
- Ne créez pas de liens vers des textures dans **stk-assets**, utilisez uniquement **stk_media_repo**
- Ne jamais intégrer les textures dans votre fichier Blender
- Ne demandez jamais à Blender d'utiliser des chemins absolus" %}

### Textures personnalisées
#### Organisation recommandée
```Licensing#where-to-find-files
votre_piste/
├── models/
└── textures/
    ├── terrain/
    ├── batiments/
    └── details/
```
- Utilisez des chemins relatifs
- Suivez les [directives de nommage](Texture_Guidelines)
- Incluez toutes les textures nécessaires

### Banques d'images en ligne
#### Sources recommandées
- [Liste des sources libres de droits](Licensing#where-to-find-filesensing/#où-trouver-les-fichiers)
- Vérifiez toujours les licences
- Respectez les [directives de qualité](Texture_Guidelines)

### Bonnes pratiques
- Maintenez une résolution cohérente (1024x1024 ou 2048x2048)
- Utilisez des puissances de deux (256, 512, 1024...)
- Optimisez la taille des fichiers
- Testez les performances en jeu

## Coloration des vertex

### Avantages
- **Performances** : Très peu coûteux en ressources
- **Flexibilité** : Modifications en temps réel
- **Efficacité** : Alternative légère aux multiples textures

### Utilisations typiques
- Variations de couleur sur un même matériau
- Dégradés naturels
- Effets d'usure ou de salissure
- Marquages au sol personnalisés

### Ressources
- [Documentation officielle](https://docs.blender.org/manual/en/latest/sculpt_paint/vertex_paint/index.html)
- [Tutoriel vidéo](https://youtu.be/Ivb45iA5QT8) (ignorer la partie sur les matériaux)

## Configuration initiale

### Création d'un calque de couleurs
1. Sélectionnez l'objet à colorer
2. Onglet **Données** (icône en forme de triangle)
3. Section **Couleurs de sommet**
4. Cliquez sur **+** pour ajouter un calque

### Accès rapide
- Raccourci : `Tab` pour passer en mode édition, puis `Shift + Tab` pour la peinture
- Ou utilisez le sélecteur de mode en haut à gauche
- Un calque est créé automatiquement si nécessaire

## Techniques de peinture avancées

### 1. Outils de base

#### Sélecteur de couleur
- **Accès rapide** : Panneau latéral (touche `N`)
- **Fonctionnalités** :
  - Sélection RVB/HSV/Hexadécimal
  - Pipette (`S` pour activer)
  - Palettes personnalisables

#### Contrôles du pinceau
- **Taille** : `F` + glisser ou molette
- **Intensité** : `Shift + F` + glisser
- **Forme** : `Shift + F` (maintenu) + glisser
- **Verrouillage** : `Majuscule` pour contraindre aux axes X/Y

### 2. Modes de fusion

| Mode | Effet | Utilisation typique |
|------|-------|---------------------|
| Mélange | Mélange standard | Couches de peinture de base |
| Ajouter | Éclaircit les couleurs | Effets de lumière |
| Soustraction | Assombrit les couleurs | Ombres |
| Multiplier | Renforce les tons foncés | Usure et salissure |
| Éclaircir | Conserve les tons clés | Reflets |
| Assombrir | Conserve les tons foncés | Ombres profondes |

### 3. Bonnes pratiques

- **Subdivision** : 
  - `Ctrl + E` > Subdiviser pour plus de détails
  - Essentiel pour les zones nécessitant des dégradés précis
  - Attention à ne pas surcharger le maillage

- **Masquage** :
  - Utilisez le masquage par sélection
  - Protégez les zones adjacentes
  - Idéal pour les bords nets

### 4. Prévisualisation dans Blender

#### Blender 2.80+
1. Activez le mode **Aperçu matériel**
2. Configuration des nœuds :
   - Ajoutez un nœud **MixRGB**
   - Branchez la texture dans **Color1**
   - Branchez les couleurs de vertex dans **Color2**
   - Connectez la sortie à **Base Color** du BSDF

#### Blender 2.79
1. Activez **Solide texturé**
   - Raccourci : `N` pour ouvrir le panneau latéral
   - Section **Shading** > **Texture Solid**
2. Pour une meilleure prévisualisation :
   - Mode **Texture** dans la vue 3D
   - Activez **GLSL** dans les options d'affichage

## Décalcomanies (Decals)

### Introduction

Les décalcomanies permettent de superposer des textures supplémentaires sur un objet, comme des autocollants. Dans SuperTuxKart, cette technique est idéale pour ajouter des détails comme des marquages au sol, des graffitis ou des effets d'usure.

{% single_gallery "/assets/wiki/Decal_shader.jpg, Exemple de décalcomanie. La texture en bois utilise la première carte UV ; la texture transparente de la piste de terre utilise la deuxième carte UV." %}

### Configuration de base

1. **Préparation du maillage**
   - Sélectionnez l'objet cible
   - Allez dans l'onglet **Données** (icône en forme de triangle)
   - Section **UV Maps**
   - Cliquez sur **+** pour ajouter une nouvelle carte UV

2. **Création des UVs**
   - Sélectionnez la nouvelle carte UV
   - Passez en mode édition (`Tab`)
   - Activez l'option **Synchroniser la sélection**
   - Sélectionnez uniquement les faces à décorer
   - Créez un nouveau dépliage UV

3. **Application de la texture**
   - Assurez-vous que la bonne carte UV est sélectionnée
   - Appliquez la texture de décalcomanie
   - Ajustez le mapping UV selon vos besoins

## Configuration avancée : Décalcomanies (Decals)

### Prévisualisation dans Blender (2.80+)

1. **Configuration des nœuds** :
   - Ajoutez un nœud **MixRGB**
   - Branchements :
     - **Color1** : Texture principale (première UV)
     - **Color2** : Texture de décalcomanie (deuxième UV)
     - **Fac** : Sortie Alpha de la texture de décalcomanie
   - Connectez la sortie **Color** à **Base Color** du BSDF

2. **Ordre des calques** :
   - La texture principale sert de fond
   - La décalcomanie s'affiche par-dessus
   - L'alpha contrôle la transparence de la décalcomanie

{% popup_info **Limitations des décalcomanies** :
- Incompatibles avec les cartes normales
- Ne pas utiliser pour les effets de relief
- Privilégiez les textures avec canal alpha pour de meilleurs résultats
%}

{% include art_portal %}
