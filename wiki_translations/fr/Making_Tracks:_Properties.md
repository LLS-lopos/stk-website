---
title: 'Faire des Pistes: Propriétés'
display_title: true
---
Après l'installation des extensions SuperTuxKart dans Blender, de nouveaux menus sont disponibles :

1. Dans la fenêtre Propriétés, sous l'onglet **Scène**, vous trouverez :
   - **Kart Exporter** (Exportation des karts)
   - **Track Exporter** (Exportation des pistes)
   - **SuperTuxKart Scene Properties** (Propriétés de la scène)
   - **SuperTuxKart Image Properties** (Propriétés des images)

2. Toujours dans la fenêtre Propriétés, sous l'onglet **Objet**, vous trouverez :
   - **SuperTuxKart Object Properties** (Propriétés des objets)

Si ces options ne sont pas visibles, consultez le guide d'[installation des outils](Installing_Tools).

## Configuration initiale de la piste

Pour commencer, cochez la case **Is a SuperTuxKart track** dans les propriétés de la scène. Cette action débloque des options supplémentaires dans le panneau des propriétés.

### Paramètres essentiels

Ces paramètres sont nécessaires pour l'exportation de votre piste :

1. **Chemin des ressources** (dans le panneau **Track Exporter**) :
   - Cliquez sur l'icône de dossier
   - Sélectionnez le répertoire `stk-assets`, `data` ou `addons`
   - Un dossier `tracks` sera automatiquement créé à cet emplacement lors de l'export

2. **Informations de base** (dans **SuperTuxKart Scene Properties**) :
   - **Nom de la piste** : Le nom qui s'affichera dans le jeu
   - **Nom du dossier** : Identifiant technique (sans espaces ni caractères spéciaux)
   - **Groupe** :
     - `Add-Ons` pour une piste téléchargeable
     - `standard` pour une potentielle intégration officielle
   - **Auteur** : Votre nom ou pseudonyme

### Paramètres avancés

Ces paramètres peuvent être configurés plus tard dans le processus de création :

1. **Musique** :
   - Spécifiez un fichier `.music` pour la bande-son
   - Consultez les [directives audio](Music_and_SFX_Guidelines) pour plus de détails

2. **Capture d'écran** :
   - Image d'aperçu dans le menu de sélection
   - Format recommandé : 4:3 redimensionné sur 1024×1024 px
   - Les cartes graphiques préfèrent les dimensions en puissance de deux

3. **Distance de rendu** (Camera far clip) :
   - Définit la visibilité des objets éloignés
   - Ajustez selon le type de piste :
     - **Intérieure** : Distance réduite pour de meilleures performances
     - **Extérieure** : Augmentez pour les décors lointains (nuages, etc.)
   - Note : Sans brouillard, la coupure est nette (pas de fondu progressif)

4. **Paramètres de course** :
   - **Conduite en arrière** :
     - Activez uniquement si la piste est praticable en sens inverse
     - Désactivez en présence d'obstacles unidirectionnels
   - **Nombre de tours** :
     - Pistes courtes : augmentez le nombre de tours (ex: 5-8)
     - Pistes longues : réduisez (ex: 2-3 tours)

5. **Position de départ** :
   - Ajustez l'espacement entre les karts si nécessaire
   - Si le jeu plante au démarrage, élargissez la zone de départ
   - Modifiez le nombre de karts par ligne si nécessaire

{%popup_info **Conseil important** :
- Explorez les différentes options pour comprendre leur fonctionnement
- Évitez de modifier les paramètres non documentés
- Notez toutes les modifications que vous apportez
- Une configuration incorrecte peut entraîner des problèmes difficiles à diagnostiquer plus tard%}

{% include art_portal %}
