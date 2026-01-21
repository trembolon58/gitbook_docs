# Методы геймификации

## Методы геймификации в \*\*stagram\* и ВКонтакте&#x20;

{% hint style="danger" %}
\*Соц. сеть Instagram принадлежит Meta, деятельность которой признана в РФ экстремисткой и запрещена.
{% endhint %}

{% hint style="warning" %}
Для настройки работы функций рекомендуем опираться на шаблон геймификации в чатах \*\*stagram\*
{% endhint %}

Для работы нижеперечисленных функций требуется объявить общие переменные в Настройках проекта:

<table data-header-hidden><thead><tr><th width="270.3333333333333">Наименование переменной</th><th width="323">Назначение переменной</th><th align="center">Значение, пример</th></tr></thead><tbody><tr><td>comment_score</td><td>сколько начислять баллов за комментарии</td><td align="center">10</td></tr><tr><td>comment_max_actions </td><td>максимальное количество комментарий в день</td><td align="center">5</td></tr><tr><td>min_comment_len</td><td>минимальная длина комментария</td><td align="center">25</td></tr><tr><td>stories_score</td><td>сколько начислять баллов за реакции на сториз</td><td align="center">15</td></tr><tr><td>stories_max_actions</td><td>максимальное количество действий в день</td><td align="center">1</td></tr><tr><td>stories_mention_score</td><td>сколько начислять баллов за упоминания в сторис</td><td align="center">5</td></tr><tr><td>stories_mention_max_actions</td><td>максимальное количество действий в день</td><td align="center">2</td></tr><tr><td>post_mention_score</td><td>сколько начислять баллов за упоминания в посте</td><td align="center">10</td></tr><tr><td>post_mention_max_actions</td><td>максимальное количество действий в день</td><td align="center">3</td></tr><tr><td>end_game_date</td><td>дата завершения игры</td><td align="center">30.12.2021</td></tr></tbody></table>

**game\_add\_comment**(text=None) - добавляет очки за комментарий в инстаграм или вк, также можно передать любой текст

**game\_add\_stories**() - добавляет очки за реакции на сториз

**game\_add\_message**() - добавляет очки за сообщения в директ

**game\_add\_stories\_mention**() - добавляет очки за упоминание в истории

**game\_get\_user\_score**() - возвращает очки пользователя

**game\_get\_user\_place**() - показывает место пользователя в рейтинге

**game\_get\_leader\_score**() - возвращает очки лидера в рейтинге

**game\_get\_top(count=99999999, shift=0, humanize=False, delimiter=None, platform=None)** - вызов без аргументов вернет отсортированный рейтинг с массивом пользователей. На вход принимает следующие 4 параметра: count - сколько пользователей вернуть, shift - с какого места рейтинга сделать выборку (0 - список начнется с лидера и так по нисходящей по очкам, т.е. 3 - выборка будет с 4-го места в рейтинге и ниже), humanize - 0 - вернет массив со словарями пользователей, 1 вернет список для вывода пользователю, delimiter -  это разделитель между именем пользователя и его результатом (если предыдущий параметр humanize=1), platform - 1 - вместо имени выводит логин в инстаграм в формате @nik.&#x20;

Пример 1: game\_get\_top(10, 0, 1, ' - ') вернет: Вася - 40 Маша - 30 Петя - 10\
\
Пример 2: game\_get\_top(3, 0, 1, ' - ', 1) вернет: @vasya - 40 @masha - 30 @privet - 10&#x20;

**game\_add\_score**(count=1, client\_id=None) - добавляет пользователю очков

**game\_set\_score**(score, client\_id=None) - задает пользователю количество очков

**game\_ban\_player**() - блокирует пользователя

**game\_unban\_player**() - разблокирует пользователя

**game\_user\_banned**() - возвращает статус блокировки пользователя, заблокирован - True, не заблокирован -False

\# позволяет работать с произвольными значениями в турнирной таблице.&#x20;

**game\_add\_value**(val\_name, count=1, client\_id=None) -&#x20;

**game\_set\_value**(val\_name, value, client\_id=None)

{% hint style="info" %}
если не передавать client\_id, то функция работает с текущим клиентом
{% endhint %}

**game\_minus\_user\_score**(count =10) - отнимает очки у пользователя (count - сколько очков отнять)

**game\_get\_today\_user\_comment\_action**() - количество комментариев от пользователя за сегодня

**game\_get\_today\_user\_message\_actions**() - количество сообщений от пользователя за сегодня

**game\_get\_today\_user\_stories\_actions**() - количество сториз от пользователя за сегодня

**game\_get\_today\_user\_mention\_actions**() - количество активностей от пользователя за сегодня

**game\_get\_today\_user\_post\_mention\_actions**() - количество постов с упоминаниями от пользователя за сегодня

**game\_get\_total\_comment\_action**() - количество комментариев за все время игры

**game\_get\_total\_message\_actions**() -  количество сообщений за все время игры

**game\_get\_total\_stories\_actions**() - количество сториз за все время игры

**game\_get\_total\_stories\_mention\_actions()** - количество упоминаний в истории за все время игры

**game\_get\_total\_post\_mention\_actions()** - количество упоминаний в постах за все время игры

## Получение рейтинга в Telegram &#x20;

{% hint style="warning" %}
Для настройки работы функции рекомендуем опираться на [шаблон геймификации в чатах Телеграм](https://docs.salebot.pro/shablony/geimifikaciya-v-chatakh-telegram-igra-na-aktivnost-karmabot)
{% endhint %}

В общих переменных следует завести словарь **tg\_thanks\_score\_data**, в котором будут храниться сведения по клиентам в формате:

`{"total_thanks":20,"326659632":{"name":"Constantin","user_name":"сonstantin","score":5},"403051597":{"name":"Timm","user_name":"dbeing","score":15,"banned":false}}`

**tg\_get\_top(count=99999999, shift=0, humanize=False, delimiter=None)**&#x20;

Параметры:&#x20;

**count** - сколько пользователей вернуть\
**shift** - с какого места рейтинга сделать выборку (0 - список начинается с лидера и так по нисходящей по очкам, т.е. 3 - выборка будет с 4-го места в рейтинге и ниже)\
**humanize** - 0 - вернет массив со словарями пользователей, 1 вернет список для вывода пользователю\
**delimiter** -  это разделитель между именем пользователя и его результатом (если предыдущий параметр humanize=1)

**tg\_get\_user\_info()**

{'score': user\_score, 'place': place, 'name': name}
