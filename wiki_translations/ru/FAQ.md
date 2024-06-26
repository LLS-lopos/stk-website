---
title: ЧаВо
---
{% start_liquid main_title %}

Общие вопросы

{% end_liquid %}

{% start_liquid qa %}

Что такое SuperTuxKart?

SuperTuxKart — это трёхмерная гоночная игра с открытым исходным кодом. Она направлена на веселье игроков с разными навыками игры, с ящиками, дающими случайные предметы, нитро, заносами и многим другим. Правдоподобность не в почёте.

STK предлагает многопользовательский сетевой режим, режим одиночной многопользовательский игры, а также режим однопользовательской игры против компьютера с заездами на выбор и режимом истории, при прохождении которого окрываются новые машины и дороги. Также существует Гран-при, цель которого — набрать наибольшее количество очков за несколько заездов.

21 дорога перенесёт вас в самые разные места. От пляжей на солнечных островах до глубин старой шахты, от улиц города Кандэла до мирных сельских дорог, от космического судна до гор, вам предстоит многое исследовать и открывать.

В игре также предусмотрены дополнительные режимы игры: гонка на время, преследование лидера, футбол, захват флага и две разновидности режима битвы.

[Подробнее здесь](Discover)!

{% end_liquid %}

{% start_liquid qa %}

Кто стоит за SuperTuxKart?

Посетите страницу [Команда](Team), чтобы ознакомиться с информацией о людях, стоящих за SuperTuxKart!

{% end_liquid %}

{% start_liquid qa %}

Какие требования к требования к оборудованию?

**Видеокарта**

Графический процессор обычно ограничивает производительность STK. Видеокарты, соответствующие наименьшим требованиям, имеют поддержку OpenGL, но для плавной игры требуют низкого разрешения и низких настроек изображения. Видеоплаты, соответствующие желательным требованиям, могут запускать самую требовательную трассу в STK в 60FPS/1080p с современным конвейером отрисовки на настройках графики 4.

* **Желательные**: NVIDIA GeForce GTX 950, AMD Radeon RX 460, или производительнее; не менее 1 ГБ VRAM (видеопамяти).
* **Минимальные**: видеокарта NVIDIA GeForce 470 GTX, AMD Radeon 6870 HD или Intel HD Graphics 4000; как минимум 512 МБ VRAM (видеопамяти).

**Процессор**

Производительность ЦП может быть ограничением в зависимости от видеоплаты и настроек графики, в основном для сетевой игры, которая более усиленно использует ЦП. Хорошая производительность процессора обеспечивает высокую частоту кадров и, что важнее, плавность. Для STK однопоточная производительность первостепенна.

* **Желательные**: одноядерная производительность Core i5-2400 или выше. Сюда входят процессоры AMD Ryzen для компьютеров, большинство процессоров от Intel с 2012 года, а также последние мобильные процессоры среднего и высокого уровня.
* **Минимальные**: Любые двухъядерные процессоры Intel или AMD, Очень старые модели и модели с низкой тактовой частотой могут иметь проблемы, особенно в онлайн игре.

**Прочие требования**

* Минимум 1 ГБ свободной оперативной памяти
* Место на диске: 700 МБ

**Дополнительно**

* Джойстик с не менее чем 6 кнопками (если вы предпочитаете играть с помощью него).

{% end_liquid %}

{% start_liquid qa %}

Мой компьютер слишком стар для запуска SuperTuxKart. Что мне делать?

Вы можете попытать удачу и запустить игру. У STK есть запасной отрисовщик, использующий OpenGL 2.1 / GLES 2 / DirectX 9, которые должны работать на большинстве устройств, но не имеют современного конвейера отрисовки.

{% end_liquid %}

{% start_liquid qa %}

Какова история SuperTuxKart?

Изначально существовал [TuxKart](http://tuxkart.sourceforge.net). Работа над ним велась (примерно) с апреля 2000 г. до марта 2004. В июне 2004 г. проект «Game of the Month» [Linux Game Tome](https://web.archive.org/web/20040915081722/http://www.happypenguin.org/) решил поддержать TuxKart. Это происходило с июня по декабрь 2004 г. (Большинство ссылок на старые ветки форума испорчены, архивы здесь: [[1]](https://web.archive.org/web/20041109144934/http://www.happypenguin.org/forums/viewtopic.php?t=1407) [[2]](https://web.archive.org/web/20120607000453/http://www.happypenguin.org/forums/viewtopic.php?t=1407&postdays=0&postorder=asc&start=15&sid=e3789fa7035b89cbfc1ab2aa6366033c) [[3]](https://web.archive.org/web/20120606235857/http://www.happypenguin.org/forums/viewtopic.php?t=1407&postdays=0&postorder=asc&start=30&sid=e3789fa7035b89cbfc1ab2aa6366033c) [[4]](https://web.archive.org/web/20120607000143/http://www.happypenguin.org/forums/viewtopic.php?t=1407&postdays=0&postorder=asc&start=45&sid=e3789fa7035b89cbfc1ab2aa6366033c) [[5]](https://web.archive.org/web/20120607000320/http://www.happypenguin.org/forums/viewtopic.php?t=1407&postdays=0&postorder=asc&start=60&sid=e3789fa7035b89cbfc1ab2aa6366033c) [[6]](https://web.archive.org/web/20120606235853/http://www.happypenguin.org/forums/viewtopic.php?t=1407&postdays=0&postorder=asc&start=75&sid=e3789fa7035b89cbfc1ab2aa6366033c). К сожалению, этот проект закончился большими разногласиями, и наконец было принято решение сохранить текущее состояние как «SuperTuxKart». Несмотря на некоторые графические улучшения, сама кодовая база была очень нестабильной и почти неиграемой. Никто не работал над (Super)TuxKart несколько лет.

В 2006 году Joerg Henrichs (a.k.a. «Hiker») подхватил SuperTuxKart, исправил нерешённые ошибки и проблемы с производительностью без какого-либо участия первого игрового дизайнера или проекта Game of the Month. С помощью «Coz» в сентябре 2006 года был размещён первый выпуск STK.

В мае 2007 года была выпущена версия 0.3. В ней были добавлены списки рекордов, новая дорога (Остров), бомба замедленного действия, поддержка MacOSX, а также поддержка OpenAL.

В феврале 2008 года была выпущена версия 0.4. В этой версии использовалась «Bullet Physics» для улучшения обработки столкновений. «Auria» присоединилась и начала улучшать дороги (Зыбучие пески, Вокруг маяка).

Версия 0.5 была выпущена в мае 2008 года. Она включала много улучшенных дорог, открываемые испытания, режим Преследование лидера, а также множество переводов (Определитель языка ОС и сопоставление с ближайшим переводом).

Версия 0.6 была выпущена 22 января 2009 года. В ней был существенно улучшен ход игры; улучшена физика, добавлены нитро-ускорение и заносы. Также была улучшена звуковая система, было добавлено много любопытной музыки, а также много новых дорог и машин. Также была представлена первая многопользовательская арена для битвы до 3-х ударов и новые предметы и бонусы.

Версия 0.7 была выпущена 20 декабря 2010 года. Она содержала несколько значительных улучшений, включая: новый движок отрисовки трёхмерного мира «Irrlicht», новую пользовательскую оболочку, новые анимации машин, новые дороги, машины и предметы/усилители, а также поддержку коротких путей / других путей. Вскоре были выпущены версии: 0.7.1, 0.7.2, 0.7.3 с дополнительными  улучшениями.

Версия 0.8 была выпущена в декабре 2012 года, добавив сюжетный режим и новые испытания, улучшенный ИИ и заносы, режим обратного хода, новые трассы и музыку. Также было улучшено меню. За ней последовала версия 0.8.1, в которой были добавлены и обновлены трассы, добавлены режимы «Футбол» и «Охота за яйцами», а также внесены другие графические и игровые улучшения.

В 2015 году мы выпустили версию 0.9 — революционный релиз на новом игровом движке Antarctica, добавляющий расширенные графические возможности, которые были бы невозможны в предыдущих версиях. Среди этих возможностей: динамическое освещение, мгновенная отрисовка (позволяющая значительно увеличить количество растительности) и многое другое. За 0.9 последовали три точечных релиза, которые добавили дополнительные возможности и новые трассы.

В апреле 2019 года мы выпустили версию 1.0, в которой впервые появилась поддержка сетевого многопользовательского режима. Помимо этой важной особенности в игре появились новые и обновлённые трассы, добавлены задания SuperTux в сюжетном режиме, большое количество правок баланса, а также множество других улучшений и исправлений.

Затем Хайкер официально объявил о своём решении уйти из проекта после того, как возглавлял его в течение 13 лет. Аурия также отказалась от роли соруководителя, но продолжала участвовать в проекте.

Руководство проектом было передано Бенау, основному участнику проекта с 2017 года, и Алаяну, основному участнику проекта 1.0. Деви, важный участник проекта на протяжении нескольких лет и ответственный за версию для Android, остался в команде.

В январе 2020 года была выпущена версия 1.1. Игровой процес не был изменён, так что все версии 1.x совместимы. Основными изменениями в этой версии стали улучшенный сетевой код и значительные улучшения пользовательского интерфейса, особенно на больших разрешениях, а также множество исправлений и улучшений.

В августе 2020 года была выпущена версия 1.2. В ней была улучшена поддержку геймпадов через SDL2, который поддерживает горячее подключение и сопоставления манипуляторов геймпада.

В сентябре 2021 года вышла последняя версия под номером 1.3. В ней обновилось множество официальных картов.

Чтобы узнать подробности, обратитесь к [списку изменений](https://github.com/supertuxkart/stk-code/blob/master/CHANGELOG.md), [публикациям в блоге](https://blog.supertuxkart.net) или списку устранённых проблем в GitHub STK.

{% end_liquid %}

{% start_liquid qa %}

Является ли SuperTuxKart клоном Mario Kart?

Нет! Mario Kart — наиболее известная гоночная игра, но было и множество других.

Некоторые древние версии STK пытались подражать Mario Kart, но это уже прошло. Мы иногда пробуем её для вдохновения, как и другие игры про картинг, но не более.

Мало того, что в игровом процессе много существенных различий, SuperTuxKart развивается по-своему, и мы не пытаемся сделать её ближе к Mario Kart.

{% end_liquid %}

{% start_liquid qa %}

Как я могу помочь?

Для начала загляните на страницу [Сообщество](Community). Там должна содержаться вся информация, необходимая для того, чтобы выбрать занятие по душе: программирование, моделирование, проектирование и прочее.

Для начала вам следует связаться с текущими разработчиками и художниками через [IRC-канал](https://web.libera.chat/?channels=#supertuxkart), [канал Telegram](https://t.me/STKInternational) или [форум](https://forum.freegamedev.net/viewforum.php?f=16) и рассказать нам, чего вы хотите добиться. Это значительно повысит вероятность того, что ваш вклад будет принят.

{% end_liquid %}

{% start_liquid main_title %}

Вопросы по игровому процессу

{% end_liquid %}

{% start_liquid qa %}

Боты (искусственные игроки) могут стрелять назад, как я могу это повторить?

Большинство предметов (шар для боулинга, торт, вантуз) можно использовать в обратном направлении. Просто стреляйте ими, глядя назад.

{% end_liquid %}

{% start_liquid qa %}

Мухлюют ли боты?

Нет!

Ограничение скорости и ускорение абсолютно одинаковы для всех картов, будь то виртуальный соперник или человек. На низких уровнях сложности ИИ может даже специально замедляться. Вероятность получения бонусов при захвате подарочной коробки также одинакова. Есть небольшие различия в том, как быстро карты могут поворачивать с одного направления на другое, но это не даёт значимого преимущества ИИ и не предназначено для этого.

ИИ иногда проявляет нечеловеческие рефлексы при использовании бонусов, но если человек нажмёт нужную кнопку в нужное время, он сможет добиться того же результата. Кроме того, есть много возможностей перехитрить его.

Если вам трудно победить ИИ, сосредоточьтесь на улучшении вождения, чтобы как можно реже попадать в аварии при быстрой езде, и научитесь использовать заносы. На более высоких уровнях сложности занос просто необходим для победы над виртуальным гонщиком.

{% end_liquid %}

{% start_liquid qa %}

Могу ли я играть в STK по сети?

Да! Создав онлайн-аккаунт STK в игре и подключившись к нему, выберите в главном меню кнопку «В сети», а затем «Интернет», чтобы получить доступ игре по глобальной сети. Вы можете создать свой собственный сервер, на котором смогут играть другие, или присоединиться к серверам, размещённым сообществом. Для наилучшего опыта важно иметь стабильное соединение и низкий пинг до сервера.

{% end_liquid %}

{% start_liquid qa %}

Почему некоторые клавиши клавиатуры не работают при одновременном нажатии?

При игре с клавиатуры могут возникнуть проблемы с одновременным нажатием нескольких клавиш, например, при попытке использовать нитро при ускорении и поворотах. В таких ситуациях некоторые нажатия могут не регистрироваться. Однако это не ошибка SuperTuxKart, а физическое ограничение вашей клавиатуры: большинство клавиатур могут обрабатывать ограниченное количество одновременно нажатых клавиш (подробности вы можете найти [здесь](https://www.sjbaker.org/wiki/index.php?title=Keyboards_Are_Evil)).  Решением проблемы является использование игрового устройства ввода (геймпада или игровой клавиатуры), либо поиск и настройка клавиш таким образом, чтобы ваша текущая клавиатура смогла регистрировать их одновременно.

{% end_liquid %}

{% start_liquid qa %}

У меня странные проблемы с управлением

Это может быть постоянный поворот, случайное торможение или другие подобные странности, когда игра считает, что вы нажали клавишу, даже если это не так. Если это происходит, попробуйте зайти в меню настроек, на экран ввода и проверьте, есть ли у вас там геймпады. Попробуйте отключить все геймпады, кроме того, который вы используете. Иногда с геймпадов или других подобных устройств, которые ОС воспринимает как геймпад, поступают ложные данные.

{% end_liquid %}

{% start_liquid qa %}

Внезапно у меня на экране появился большой красный круг, что это?

Если в центре круга стоит пингвин, значит, кто-то метнул вантуз вам в лицо. Вы можете сделать это с другими, выстрелив вантузом в обратную сторону (см. раздел ЧаВо о бросках предметов в обратную сторону).

{% end_liquid %}

{% start_liquid qa %}

Можно ли использовать пульт Wii Remote с STK?

Да! Ищите подробности на странице [Wiimote](Wiimote).

{% end_liquid %}

{% start_liquid main_title %}

Технические вопросы

{% end_liquid %}

{% start_liquid qa %}

Я нашёл ошибку, как с вами связаться?

Сначала загляните в [баг-трекер STK](https://github.com/supertuxkart/stk-code/issues) и откройте новый вопрос, если ваша проблема ещё не сообщалась.

{% end_liquid %}

{% start_liquid qa %}

Где хранятся настройки?

* В **Windows**: он находится в `%APPDATA%/supertuxkart/config-0.10` (вы можете ввести этот адрес в Проводнике, и он приведёт вас туда).
* В **Linux**: Он либо в `$XDG_CONFIG_HOME/supertuxkart/config-0.10` (первый вариант), `~/.config/supertuxkart/config-0.10` (второй вариант) либо в `~/.supertuxkart/config-0.10` (третий вариант).
* На **macOS**: Он находится в каталоге `~/Library/Application Support/supertuxkart/config-0.10`. Обратите внимание, что этот каталог может быть скрыт.
* В **Android**: он находится в `/storage/emulated/0/Android/data/org.supertuxkart.stk/files/supertuxkart/home/supertuxkart/config-0.10`.
* В **Snap**: он находится в `~/snap/supertuxkart/current/.config/supertuxkart/config-0.10`.
* Во **Flatpak**: он находится в `~/.var/app/net.supertuxkart.SuperTuxKart/config/supertuxkart/config-0.10`.

Вы также можете посмотреть в выводе терминала заметку о том, где хранятся файлы конфигурации, или поискать файл под названием «config.xml».

{% end_liquid %}

{% start_liquid qa %}

Если версия из Git не будет собираться, что мне делать?

Такое иногда случается; разработчики должны быть в курсе, и это должно быть исправлено в ближайшее время. Если [GitHub Actions](https://github.com/supertuxkart/stk-code/actions) говорит, что текущая версия из Git компилируется, а у вас нет, то, вероятно, что-то не так с настройками вашего компилятора. (Проверьте наличие всех зависимостей, перезапустите CMake и пр.)

{% end_liquid %}

{% start_liquid qa %}

Как мне открыть все трассы?

Предполагаемый внутриигровой способ — играть в режиме истории и преодолевать все испытания.

Если же вы хотите открыть всё, не играя в режим истории, вы можете сжульничать, изменив конфигурационный файл. Откройте папку, упомянутую выше в вопросе «Где STK хранит пользовательский конфигурационный файл». Оттуда откройте папку «config-0.10», затем откройте файл «players.xml». Замените все вхождения «none» на «hard» («easy» или «medium», определяет максимальный уровень прохождения испытания).

{% end_liquid %}
