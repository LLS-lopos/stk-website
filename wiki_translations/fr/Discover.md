---
title: Découvrir
---
{% capture heading -%}
..:: {%translate Bienvenue au Royaume des Mascottes !,Page title of discover page%} ::
{%- endcapture %}
{%main_title {{ heading }}%}

{% gallery widths=32%
/assets/wiki/STK1.3_1.jpg
/assets/wiki/STK1.3_2.jpg
/assets/wiki/STK1.3_3.jpg
%}

{%translate "Des karts. Du nitro. De l'action ! SuperTuxKart est un jeu de course d'arcade 3D open-source avec une variété de personnages, de circuits et de modes de jeu. Notre objectif est de créer un jeu plus amusant que réaliste, offrant une expérience agréable pour tous les âges."%}

{%translate "Dans le mode Histoire, vous devrez affronter le maléfique Nolok et le vaincre pour rendre le Royaume des Mascottes sûr à nouveau ! Vous pouvez courir seul contre l'ordinateur, participer à plusieurs coupes de Grand Prix ou tenter de battre votre meilleur temps en mode Contre-la-montre. Vous pouvez également faire la course, vous battre ou jouer au football avec jusqu'à huit amis sur un seul ordinateur, jouer en réseau local ou en ligne avec d'autres joueurs du monde entier."%}

{% gallery widths=32%
/assets/wiki/STK1.3_4.jpg
/assets/wiki/STK1.3_5.jpg
/assets/wiki/STK1.3_6.jpg
%}

{% capture main_characters -%}
{%translate Personnages principaux%}
{%- endcapture %}
{%main_title {{ main_characters }}%}

{% capture tux -%}
{%translate Tux%}
{%- endcapture -%}
{%- capture tux_desc -%}
{%translate "Le héros de SuperTuxKart. Tux est un manchot courageux qui doit sauver son ami Gnu des griffes maléfiques de Nolok. Tux est la mascotte de Linux."%}
{%- endcapture %}
{% include character_presentation name=tux type="odd" description=tux_desc icon="/assets/wiki/Character_tux_icon.png" %}

{% capture gnu -%}
{%translate Gnu%}
{%- endcapture -%}
{%- capture gnu_desc -%}
{%translate "Le sage mentor de Tux, Gnu se déplace sur un tapis volant et vit paisiblement dans une pagode. Lorsque Nolok le capture, tout le royaume tentera de le sauver. Gnu est la mascotte du projet GNU."%}
{%- endcapture %}
{% include character_presentation name=gnu type="even" description=gnu_desc icon="/assets/wiki/Character_gnu_icon.png" %}

{% capture nolok -%}
{%translate Nolok%}
{%- endcapture -%}
{%- capture nolok_desc -%}
{%translate "Le méchant de SuperTuxKart, Nolok élabore toujours des plans maléfiques dans son château de lave enflammé."%}
{%- endcapture %}
{% include character_presentation name=nolok type="odd" description=nolok_desc icon="/assets/wiki/Character_nolok_icon.png" %}

{% capture additional_characters -%}
{%translate Personnages additionnels%}
{%- endcapture %}
{%main_title {{ additional_characters }}%}

<table>
<tr>
{%- capture sara -%}
{%translate Sara%}
{%- endcapture -%}
{%- capture sara_desc -%}
{%translate "Sara est une puissante magicienne et la dirigeante du Royaume des Mascottes. Elle court en utilisant une motoneige spécialisée. Elle est la mascotte du site OpenGameArt."%}
{%- endcapture -%}
{% include character_presentation_small name=sara type="odd" description=sara_desc icon="/assets/wiki/Character_sara_icon.png" %}

{%- capture wilber -%}
{%translate Wilber%}
{%- endcapture -%}
{%- capture wilber_desc -%}
{%translate "Wilber est le caméraman officiel qui travaille pour WTXB-TV pour enregistrer les courses de kart, très populaires dans le Royaume des Mascottes. Il est la mascotte de GIMP."%}
{%- endcapture -%}
{% include character_presentation_small name=wilber type="even" description=wilber_desc icon="/assets/wiki/Character_wilber_icon.png" %}
</tr>
<tr>
{%- capture puffy -%}
{%translate Puffy%}
{%- endcapture -%}
{%- capture puffy_desc -%}
{%translate "Puffy participe aux courses principalement pour gagner assez d'argent pour réaliser son rêve : acheter un sous-marin. Il est la mascotte du projet OpenBSD."%}
{%- endcapture -%}
{% include character_presentation_small name=puffy type="odd" description=puffy_desc icon="/assets/wiki/Character_puffy_icon.png" %}

{%- capture pidgin -%}
{%translate Pidgin%}
{%- endcapture -%}
{%- capture pidgin_desc -%}
{%translate "La capacité de Pidgin à voler en fait le messager idéal pour diffuser les résultats du Grand Prix dans tout le Royaume des Mascottes. Il est la mascotte de Pidgin."%}
{%- endcapture -%}
{% include character_presentation_small name=pidgin type="even" description=pidgin_desc icon="/assets/wiki/Character_pidgin_icon.png" %}
</tr>
<tr>
{%- capture godette -%}
{%translate Godette%}
{%- endcapture -%}
{%- capture godette_desc -%}
{%translate "Godette est la mascotte de Godot et une véritable passionnée de technologie. On ne la voit jamais sans son ami GDBot, un robot qu'elle a construit et programmé elle-même. Ils courent même ensemble dans un kart tandem unique en son genre."%}
{%- endcapture -%}
{% include character_presentation_small name=godette type="odd" description=godette_desc icon="/assets/wiki/Character_godette_icon.png" %}

{%- capture amanda -%}
{%translate Amanda%}
{%- endcapture -%}
{%- capture amanda_desc -%}
{%translate "Amanda a été sauvée par des moines qui l'ont trouvée dans un panier alors qu'elle n'était qu'un petit. Elle enseigne maintenant l'art ancien de la course dans un monastère. Elle est la mascotte de Window Maker."%}
{%- endcapture -%}
{% include character_presentation_small name=amanda type="even" description=amanda_desc icon="/assets/wiki/Character_amanda_icon.png" %}
</tr>
<tr>
{%- capture emule -%}
{%translate Emule%}
{%- endcapture -%}
{%- capture emule_desc -%}
{%translate "Les connaissances supérieures d'Emule en génie mécanique lui ont permis de construire son propre kart avec un moteur suralimenté. Il est la mascotte d'eMule."%}
{%- endcapture -%}
{% include character_presentation_small name=emule type="odd" description=emule_desc icon="/assets/wiki/Character_emule_icon.png" %}

{%- capture suzanne -%}
{%translate Suzanne%}
{%- endcapture -%}
{%- capture suzanne_desc -%}
{%translate "La course est le rêve de Suzanne depuis son enfance. Elle a commencé sa carrière de pilote à la prestigieuse Académie de Kart de Val Verde. Elle est la mascotte de Blender."%}
{%- endcapture -%}
{% include character_presentation_small name=suzanne type="even" description=suzanne_desc icon="/assets/wiki/Character_suzanne_icon.png" %}
</tr>
<tr>
{%- capture gavroche -%}
{%translate Gavroche%}
{%- endcapture -%}
{%- capture gavroche_desc -%}
{%translate "Gavroche est un gobelin qui possède le manoir de Ravenbridge. Parfois, il fait des bruits effrayants pour faire croire aux gens que la maison est hantée. Il est la mascotte de MediaGoblin."%}
{%- endcapture -%}
{% include character_presentation_small name=gavroche type="odd" description=gavroche_desc icon="/assets/wiki/Character_gavroche_icon.png" %}

{%- capture hexley -%}
{%translate Hexley%}
{%- endcapture -%}
{%- capture hexley_desc -%}
{%translate "Les ancêtres d'Hexley ont commencé la course de karts il y a de nombreuses années, et de génération en génération, ils sont devenus très doués. Il est la mascotte de Darwin."%}
{%- endcapture -%}
{% include character_presentation_small name=hexley type="even" description=hexley_desc icon="/assets/wiki/Character_hexley_icon.png" %}
</tr>
<tr>
{%- capture xue -%}
{%translate Xue%}
{%- endcapture -%}
{%- capture xue_desc -%}
{%translate "Xue aime se démarquer de la foule, et son kart inhabituel reflète cette personnalité. Elle court avec un aéroglisseur spécial, assez petit pour être piloté par une souris. Elle est la mascotte de XFCE."%}
{%- endcapture -%}
{% include character_presentation_small name=xue type="odd" description=xue_desc icon="/assets/wiki/Character_xue_icon.png" %}

{%- capture konqi -%}
{%translate Konqi%}
{%- endcapture -%}
{%- capture konqi_desc -%}
{%translate "Bien que les ancêtres de Konqi aient été dangereux et craints, les dragons d'aujourd'hui sont inoffensifs... la plupart du temps. Il est la mascotte du projet KDE."%}
{%- endcapture -%}
{% include character_presentation_small name=konqi type="even" description=konqi_desc icon="/assets/wiki/Character_konqi_icon.png" %}
</tr>
<tr>
{%- capture adiumy -%}
{%translate Adiumy%}
{%- endcapture -%}
{%- capture adiumy_desc -%}
{%translate "Adiumy a commencé la course de karts quand il a réalisé que ses jambes étaient trop courtes pour devenir une star du football. Bien que les autres mascottes se moquent parfois de sa démarche chaloupée, il est très respecté comme l'un des pilotes de course les plus talentueux du royaume. Adiumy est la mascotte d'Adium."%}
{%- endcapture -%}
{% include character_presentation_small name=adiumy type="odd" description=adiumy_desc icon="/assets/wiki/Character_adiumy_icon.png" %}

{%- capture kiki -%}
{%translate Kiki%}
{%- endcapture -%}
{%- capture kiki_desc -%}
{%translate "Un utilisateur de Krita a d'abord dessiné Kiki pour un manuel de formation, mais dès que le manuel a été imprimé, Kiki a décidé de sauter des pages et de faire le tour du monde sur son avion à propulsion de stylo. Kiki est la mascotte du programme de peinture numérique Krita."%}
{%- endcapture -%}
{% include character_presentation_small name=kiki type="even" description=kiki_desc icon="/assets/wiki/Character_kiki_icon.png" %}
</tr>
<tr>
{%- capture pepper -%}
{%translate Pepper%}
{%- endcapture -%}
{%- capture pepper_desc -%}
{%translate "Pepper est une petite sorcière qui adore jouer avec son chat Carotte. Son enthousiasme pour la course a pris feu lorsque son amie Kiki l'a aidée à améliorer son balai avec un système d'injection de nitro et des pots d'échappement personnalisés. Pepper est le personnage principal du projet Pepper & Carrot."%}
{%- endcapture -%}
{% include character_presentation_small name=pepper type="odd" description=pepper_desc icon="/assets/wiki/Character_pepper_icon.png" %}
<td></td>
</tr>
</table>

{% capture many_more -%}
{%translate ...Et bien d'autres !%}
{%- endcapture %}
{%main_title {{ many_more }}%}

{%translate "Vous pouvez créer vos propres personnages, circuits et arènes et les partager avec la communauté SuperTuxKart ! Rendez-vous sur [online.supertuxkart-evolution.com](https://online.supertuxkart-evolution.com)."%}

{%translate Si vous êtes intéressé, vous pouvez jeter un œil à la page [communauté](Community).%}

[{%translate Conditions d'utilisation%}](Terms)
