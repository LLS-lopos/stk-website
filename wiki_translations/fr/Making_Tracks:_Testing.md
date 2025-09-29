---
title: 'Faire des Pistes: Tests'
toc: true
---
Après avoir suivi les instructions des modules précédents, vous devriez maintenant être prêt à tester votre piste. Toutefois, vous voudrez également procéder à de nouveaux tests plus tard, au fur et à mesure que vous ajouterez des éléments à votre piste. Nous vous conseillons également de demander, si possible, l'avis de quelqu'un d'autre que vous sur votre piste. Cette personne sera moins susceptible d'être partiale et pourra souvent vous donner de meilleurs conseils. Essayez de poster votre piste sur le forum, ou demandez à un ami d'essayer votre prototype de piste.

## Exportation

1. Dans Blender, allez dans les propriétés de la scène (Scene Properties)
2. Localisez la section "Track Exporter"
3. Cliquez sur le bouton "Export Track"

Votre piste sera exportée dans un sous-dossier nommé "tracks" situé dans le même répertoire que votre fichier .blend. À l'intérieur du dossier "tracks", copiez le dossier portant le nom de votre piste vers le répertoire des extensions de SuperTuxKart :

* Sur Windows: %APPDATA%/supertuxkart/addons/tracks
* Sur Linux: ~/.local/share/supertuxkart/addons/tracks
* Sur macOS: ~/Library/Application Support/supertuxkart/addons/tracks

Veillez également à copier toutes les textures que vous avez utilisées et qui ne proviennent pas du dépôt multimédia.

Maintenant, lancez SuperTuxKart et trouvez votre circuit dans la section "Add-Ons" lorsque vous configurez une course.

## Recommandations

Lors des tests, vérifiez que votre piste respecte les [consignes de jouabilité](Making_Tracks:_Notes#gameplay) énoncées dans la section Notes.

## Gestion des problèmes

Pour faciliter les mises à jour futures de votre piste :

1. Modifiez la courbe de Bézier créée précédemment
2. Supprimez votre piste et ses lignes de conduite
3. Recréez-les en appliquant les modificateurs Array (réseau) et Curve (courbe)

Cette approche vous permettra de modifier facilement votre piste ultérieurement sans avoir à retravailler sa jouabilité.

## Conclusion

Bien que cet article soit concis, accordez une attention particulière aux tests de votre circuit. Une piste agréable à conduire est essentielle - les éléments décoratifs et paysagers que vous découvrirez dans les sections suivantes ne suffiront pas à compenser une piste mal conçue.

{% include art_portal %}
