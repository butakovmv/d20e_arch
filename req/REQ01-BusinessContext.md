# Бизнес-контекст, цели создания системы, неформализованные пожелания и требования

<!-- TOC -->
* [Бизнес-контекст, цели создания системы, неформализованные пожелания и требования](#бизнес-контекст-цели-создания-системы-неформализованные-пожелания-и-требования)
  * [Контекст](#контекст)
  * [Цели](#цели)
  * [Стейкхолдеры](#стейкхолдеры)
  * [Потребности](#потребности)
<!-- TOC -->

## Контекст

Есть культовая НРИ (настольно-ролевая игра) Dungeon & Dragons (D&D). У нее уже 5 редакций, сейчас идет бета-тестирование
6-й. 5-я редакция будет активно играемой около 2 лет.

Существует ответвление от 3.5 редакции - Pathfinder с более открытой лицензией. У Pathfinder есть 2 редакции, 2-я
редакция будет активно играемой около 4-5 лет.

Обе игры довольно похожи, есть небольшие различия в механике и наборе игровых сущностей. Правила игр описаны и
опубликованы в официальных книгах - в базовых и в книгах приключений. Также есть сайты с структурированными выдержками
из указанных книг. Примеры сайтов с правилами:

- https://ttg.club/
- https://roll20.net/compendium/dnd5e/CategoryIndex%3ARules#content
- https://pf2e-ru-translation.readthedocs.io/ru/latest/

Для проведения сеанса игры нужны:

- ведущий (Dungeon Master или ДМ);
- игроки с концепцией своего персонажа, описанной на листе персонажа;
- кубики (дайсы) с разным набором граней (20, 12, 10, 8, 6, 4) для внесения случайности в результат действий персонажей
  согласно правилам;
- сюжет с приключениями;
- в зависимости от способа ведения игры - опциональные дополнительные материалы: рисунки, письма, фигурки (миниатюры)
  действующих лиц;
- карты местности, для боя - с дюймовой сеткой, вне боя любой масштаб;
- справочники для игровых объектов;
- подсказки ДМ по импровизации, корректировке или созданию игровых объектов “на лету” при не прописанных в приключении
  реакции игрового мира на действия игроков;
- музыка для создания атмосферы;
- звуки для иллюстрации действий.

Минимальный, часто используемый вариант: бумага, карандаши, фантазия, кубики для бросков, ширма ДМ-а с подсказками для
скрытия от игроков результатов некоторых бросков, записи от руки.

Вариант посерьезнее - в дополнение к предыдущему списку добавляется ламинированная карта для рисования местности,
смываемые маркеры, распечатанные на 3d-принтере модельки
героев и монстров, bluetooth-колонка и телефон с плейлистами под нужные ситуации.

Существуют разрозненные инструменты для помощи ДМ, существуют инструменты для игры онлайн по скайпу/Discord, но нет
инструмента, который позволит использовать один и тот же инструмент для помощи ДМ, ведения игры как онлайн, так и
офлайн.

Нет инструмента, позволяющего имитировать стиль ведения игры определенного ДМ.

Основной конкурент - roll20.net. Его минусы - отсутствие локализации, базовые книги только платные, отсутствие
достаточного количества настраиваемого контента вместе с ограничением на размер загруженного пользователем контента.

## Цели

1. Повысить погружение игроков в игру, снизить затраты времени на рутинные операции.
2. Охватить игроков со слабым знанием английского.
3. Снизить затраты времени ДМ-а на подготовку к проведению игровых сессий.</br>Целевой показатель: затраты не более 30
   минут на сессию.
4. Дать ДМ-у удобный инструмент, избавляющий от необходимости держать информацию в голове или записывать на листочках,
   путаться и ошибаться на сеансах игры. </br>Целевой показатель: отсутствие бумажных записей в течение 5 сессий подряд
5. Автоматизировать часто используемые операции, особенно операции по созданию случайных игровых сущностей по заданным
   критериям.</br>Целевой показатель: отсутствие обращений к таблицам с параметрами создания предметов в течение
   кампании.
6. Иметь возможность обработать больше игроков с меньшими затратами;</br>Целевой показатель: количество игроков
   участвовавших в игровых сессиях за неделю >10, затраты на подготовку - от 2/3 до 1/2 от типичного для данного ДМ.
7. Дойти до 10 тысяч зарегистрированных пользователей в РФ, до 20 одновременно проводимых сессий в будни, до 50
   в выходные, до 500 одновременно активно играющих человек онлайн. Монетизация будет завязана на количество игровых
   сессий и количество пользователей онлайн.

## Стейкхолдеры

1. Заказчик - один ДМ, он же будет начальным владельцем системы
2. Пользователи - ДМ, игроки, наполнитель контента
3. Команда разработки - 2 fullstack разработчика, любят и владеют: js, vue, kotlin, spring, postgres, grafana,
   prometheus, sentry, junit, selenide, nginx, kubernetes
4. Команда сопровождения - заказчик, изредка один из разработчиков

## Потребности

1. Заказчик хочет создать более удобный инструмент для проведения онлайн и офлайн настольных игр, ориентированный в
   первую очередь на русскоязычное игровое сообщество.
2. Заказчик хочет сначала охватить систему D&D5, базовые книги и хотя бы одно из официально опубликованных приключений.
   В D&D 5 четко выделены несколько режимов игры: простой, отдых, исследование, столкновение. Характер запросов игроков
   для каждого режима игры свой.
3. Если инструмент окажется востребованным, народ попрет и будет соответствующий запрос со стороны пользователей - через
   какое-то время включить в систему механики сходных НРИ - Pathfinder2, Vampire the Masquerade. Предметная область
   каждой системы описана в официальных книгах игровой системы.
4. ДМ хочет быстро (30-60 секунд) добавлять в систему новые игровые объекты в процессе игры, с возможностью
   посмотреть позже, без необходимости в момент необходимости их долго записывать и запоминать с риском забыть.
5. ДМ хочет расширять систему плагинами с новым функционалом, например, генераторами для помощи в создании деталей
   малозначащих побочных персонажей или мира, которые добавляют детализацию игровому миру и погружение игрокам.
6. ДМ хочет создавать свои приключения (или описывать существующие официально опубликованные по Open Game License)
   и наполнять их содержимым - предметами, неигровыми персонажами, заданиями, картами локаций, библиотекой звуков и
   музыки.
7. Наполнение иногда можно делегировать стороннему человеку с меньшим набором прав, чтоб ничего не поломал.
8. ДМ хочет легко и просто в 2-3 клика переключать музыку для создания настроения (бой/кутеж в таверне/официальный
   прием/тайна/мистика/романтика/деревенская жизнь/etc), погодных эффектов (дождь, гром, буран, вой ветра), эффектов от
   действий (удары, выстрелы, смех, боевые крики, взрывы, вздохи, прикольные возгласы про неудачи или особо успешные
   действия типа “бадум-тссс”, “уа-уа-уа-уааааа….”, фанфары, звук оборванной струны или отсылки к другим мемчикам).
9. ДМ хочет предоставить игрокам возможность общаться текстом в реальном времени как от имени игрока, так и от
   имени персонажа. При общении от лица персонажа можно указать игровой язык реплик и форму сообщения - записка, шепот,
   разговор, крик. Чат должен поддерживать текст, смайлики, стикеры (картинки с эмоциями или мемами), реакции со
   значками эмоций на сообщения. Голосовое общение в реальном времени в системе не требуется, этот функционал закроет
   использование Discord-каналов.
10. ДМ хочет быстро переключать/менять локации без необходимости рисовать их маркерами/стирать на ламинированной карте,
    а также генерировать случайные или выбирать по каким-то признакам из набора сгенерированных (пример признаков -
    “дорога”, “лес”, “засада”, “привал”, “разграбленный караван” и т.д.) генерация или заранее, или вообще
    процедурно-случайная.
11. ДМ хочет активнее использовать настраиваемые переиспользуемые ресурсы - картинки персонажей, предметов,
    местности с возможностью изменять их размер, цвет, некоторые детали. При этом хочет чтобы эти ресурсы имели
    небольшой размер. Полагает, что этого можно добиться через использование SVG-изображений.
12. ДМ хочет для игроков конструктор персонажа, используемый при создании нового персонажа или повышении уровня у
    существующего. В реальности на бумаге такое занимает 1-2 часа (в зависимости от опыта игрока), хорошо бы это
    ускорить за счет автоматизированного помощника-подсказчика и сравнять в скорости опытных и новичков. Можно этот этап
    делегировать как “домашнее задание” с доступом вне игровой сессии.
13. ДМ хочет, чтобы у игроков была возможность переносить персонажей из других популярных платформ (генераторы
    персонажей, листы персонажей).
14. ДМ хочет предлагать автоподсказки в заполнении “дневников персонажа” - на основе деталей, фигурировавших в
    игре, и уже известных игрокам. Игроки не всегда записывают и запоминают детали, с учетом возможных перерывов между
    сессиями 1-2 недели, помощь в этом сместит фокус на погружение в игру и снизит число морщин у игроков при потугах
    что-то вспомнить.
15. ДМ хочет иметь возможность показать игрокам на экране красочные модельки/картинки/видео их персонажей,
    монстров, вместо 3д-отпечатанных моделек (так дешевле сгенерировать, проще раскрасить, труднее сломать, при замене
    на онлайн распечатанная офлайн 3д-моделька не поможет).
16. ДМ представляет это как:

    1) устройство у ведущего с расширенным набором функций и воспроизведением звуков;
    2) устройства у игроков с описанием его персонажа, просмотром дневника, подсказками или списком доступных действий
       (“заявка на действие”), чатом, картой/списком того, что видит вокруг конкретный персонаж;
    3) общее устройство (интерактивный стол/большой планшет/умный
       телевизор/проектор с потолка на стол) - с отображением карты, фигурок, квестовых предметов и загадок и всего что
       видит вся партия персонажей.
       В партии игроков обычно не более 6 (больше - падает темп игры, игроки больше ждут очереди, чем взаимодействуют),
       ДМ
       всегда один, музыка всегда одна, планшет с картой всегда один

17. Заказчик планирует использовать систему сначала самому, независимо водить несколько разных партий игроков по разным
    приключениям и мирам. Игроки не должны видеть игроков и предметы из “параллельной вселенной” других игроков. В
    перспективе появиться больше ДМ-ов, которым доступ к этой системе предоставляется “как сервис” за небольшую
    комиссию с каждой проведенной в ней игры. ДМ не должен иметь доступ к контенту другого ДМ, если тот не поделится им
    явно - с ограниченным кругом лиц или с неограниченным (т.е. со всеми).
18. Заказчик хочет, чтобы на этапе предоставления сервиса другим ДМ система предоставляла удобную информацию для
    сопровождения (поиск багов, отладка, реагирование на назревающие или проявившиеся проблемы) для максимально быстрого
    устранения.
19. Команда разработки хочет использовать привычные и популярные технологии.
20. Сопровождение хочет, чтобы оповещения по инцидентам приходили в мессенджер. Пользоваться возможностью по определению
    причины инцидента и выдачи в сообщении рекомендаций по исправлению, либо по возможности автоматизированно
    обрабатывать исправление. Возможность в свободное время просмотреть всю историю событий в системе за последние 2
    недели, возможность выгружать события для более долгого хранения.
21. Заказчик хочет иметь создание бэкапов игрового контента, прохождений, персонажей, чтобы при авариях можно было из
    чего-то восстановить состояние системы и вернуть пользователей. 
