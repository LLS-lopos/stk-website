---
title: Télécharger
---
{%- capture full_game -%}
{%translate Jeu complet,Installateur / paquets complets pour STK%}
{%- endcapture -%}
{%- capture x86_32 -%}
{%translate Intel / AMD 32 bits%}
{%- endcapture -%}
{%- capture x86_64 -%}
{%translate Intel / AMD 64 bits%}
{%- endcapture -%}
{%- capture arm_32 -%}
{%translate ARM 32 bits%}
{%- endcapture -%}
{%- capture arm_64 -%}
{%translate ARM 64 bits%}
{%- endcapture -%}
{%- capture all_archs -%}
{%translate toutes les architectures,Architectures tout-en-un pour l'installateur / les paquets STK%}
{%- endcapture -%}

{%- capture linux_link -%}
https://github.com/supertuxkart/stk-code/releases/download/{{ site.stk_version }}/SuperTuxKart-{{ site.stk_version }}-linux-x86_64.tar.xz
{%- endcapture -%}
{%- capture linux_content -%}
[**{{ full_game }}** (.tar.xz) {{ x86_32 }}](https://github.com/supertuxkart/stk-code/releases/download/{{ site.stk_version }}/SuperTuxKart-{{ site.stk_version }}-linux-x86.tar.xz)

[**{{ full_game }}** (.tar.xz) {{ x86_64 }}](https://github.com/supertuxkart/stk-code/releases/download/{{ site.stk_version }}/SuperTuxKart-{{ site.stk_version }}-linux-x86_64.tar.xz)

[**{{ full_game }}** (.tar.xz) {{ arm_32 }}](https://github.com/supertuxkart/stk-code/releases/download/{{ site.stk_version }}/SuperTuxKart-{{ site.stk_version }}-linux-armv7.tar.xz)

[**{{ full_game }}** (.tar.xz) {{ arm_64 }}](https://github.com/supertuxkart/stk-code/releases/download/{{ site.stk_version }}/SuperTuxKart-{{ site.stk_version }}-linux-arm64.tar.xz)

{%translate Extrayez et exécutez **run_game.sh** dans le dossier.%}
{%- endcapture -%}

{%- capture windows_link -%}
https://github.com/supertuxkart/stk-code/releases/download/{{ site.stk_version }}/SuperTuxKart-{{ site.stk_version }}-installer-x86_64.exe
{%- endcapture -%}
{%- capture windows_content -%}
[**{{ full_game }}** (.exe) {{ x86_32 }}](https://github.com/supertuxkart/stk-code/releases/download/{{ site.stk_version }}/SuperTuxKart-{{ site.stk_version }}-installer-i686.exe)

[**{{ full_game }}** (.exe) {{ x86_64 }}](https://github.com/supertuxkart/stk-code/releases/download/{{ site.stk_version }}/SuperTuxKart-{{ site.stk_version }}-installer-x86_64.exe)

[**{{ full_game }}** (.exe) {{ arm_64 }}](https://github.com/supertuxkart/stk-code/releases/download/{{ site.stk_version }}/SuperTuxKart-{{ site.stk_version }}-installer-aarch64.exe)

[**{%translate Archive sans installateur%}** (.zip) {{ all_archs }}](https://github.com/supertuxkart/stk-code/releases/download/{{ site.stk_version }}/SuperTuxKart-{{ site.stk_version }}-win.zip)
{%- endcapture -%}

{%- capture apple_link -%}
https://github.com/supertuxkart/stk-code/releases/download/{{ site.stk_version }}/SuperTuxKart-{{ site.stk_version }}-mac.zip
{%- endcapture -%}
{%- capture apple_content -%}
[**{{ full_game }}** (.zip) {{ all_archs }}](https://github.com/supertuxkart/stk-code/releases/download/{{ site.stk_version }}/SuperTuxKart-{{ site.stk_version }}-mac.zip)
{%- endcapture -%}

{%- capture android_link -%}
https://play.google.com/store/apps/details?id=org.supertuxkart.stk
{%- endcapture -%}
{%- capture android_content -%}
[**{%translate Obtenir sur le Google Play Store%}**](https://play.google.com/store/apps/details?id=org.supertuxkart.stk)

[**{%translate Télécharger l'APK%}** ({{ all_archs }})](https://github.com/supertuxkart/stk-code/releases/download/{{ site.stk_version }}/SuperTuxKart-{{ site.stk_version }}.apk)
{%- endcapture -%}

{%- capture switch_link -%}
https://github.com/supertuxkart/stk-code/releases/download/{{ site.stk_version }}/SuperTuxKart-{{ site.stk_version }}-switch.zip
{%- endcapture -%}
{%- capture switch_content -%}
[**{{ full_game }}** (.zip)](https://github.com/supertuxkart/stk-code/releases/download/{{ site.stk_version }}/SuperTuxKart-{{ site.stk_version }}-switch.zip)

{%translate Décompressez l'archive à la racine de la microSD pour l'installation.%}
{%- endcapture -%}

{%- capture source_code -%}
{%translate Code source%}
{%- endcapture -%}
{%- capture source_link -%}
https://github.com/supertuxkart/stk-code/releases/download/{{ site.stk_version }}/SuperTuxKart-{{ site.stk_version }}-src.tar.xz
{%- endcapture -%}
{%- capture source_content -%}
[**{{ full_game }}** (.tar.xz)](https://github.com/supertuxkart/stk-code/releases/download/{{ site.stk_version }}/SuperTuxKart-{{ site.stk_version }}-src.tar.xz)

{%translate "Pour obtenir le code le plus récent, consultez la page [Contrôle de version](Source_control)."%}
{%- endcapture -%}

{%- capture github_title -%}
..:: {%translate Télécharger depuis GitHub%} ::
{%- endcapture -%}
{%- main_title {{ github_title }}-%}

{%- include_relative_untranslated _Download.inc main_link=linux_link
os="linux" name="Linux" content=linux_content
-%}
{%- include_relative_untranslated _Download.inc main_link=windows_link
os="windows" name="Windows" content=windows_content
-%}
{%- include_relative_untranslated _Download.inc main_link=apple_link
os="apple" name="macOS" content=apple_content
-%}
{%- include_relative_untranslated _Download.inc main_link=android_link
os="android" name="Android" content=android_content
-%}
{%- include_relative_untranslated _Download.inc main_link=switch_link
os="switch" name="Switch Homebrew" content=switch_content
-%}
{%- include_relative_untranslated _Download.inc main_link=source_link
os="source" name=source_code content=source_content
-%}

{%translate Les liens de téléchargement principaux ci-dessus sont pour la dernière version stable, SuperTuxKart 1.4.

Vous pouvez trouver les versions 1.5 RC1 [ici](https://github.com/supertuxkart/stk-code/releases/tag/1.5-rc1).

Les versions d'aperçu automatisées sont disponibles [ici](https://github.com/supertuxkart/stk-code/releases/preview).

Les versions de test publiques pour SuperTuxKart Evolution ne sont pas encore disponibles. %}

{% capture rc_string -%}
{%translate Obtenir le dernier candidat de version :%}
{%- endcapture %}

{%- if site.stk_rc != '' -%}
{{ rc_string }}[{{ site.stk_rc }}](https://github.com/supertuxkart/stk-code/releases/{{ site.stk_rc }})
{%- endif -%}
<div class="download-content" style="font-size: 1rem; opacity: 1.0;">
<div class="download-left" style="text-align: center;">
</div>
<div class="download-right">
<i class="fa fa-download fa-fw fa-2x"></i>
</div>
</div>
