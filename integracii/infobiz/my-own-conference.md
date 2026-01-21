# My own CONFERENCE

* [Как настроить подключение ](my-own-conference.md#nastroika-podklyucheniya)
* [Как осуществлять поиск вебинаров ](my-own-conference.md#poisk-vebinarov)
* [Как проверить присутствует ли пользователь на активном вебинаре ](my-own-conference.md#proverka-prisutstvuet-li-polzovatel-na-aktivnom-vebinare)
* [Как получить данные истории пользователя по вебинару ](my-own-conference.md#poluchenie-dannykh-istorii-polzovatelya-po-vebinaru)
* [Как проверить есть ли пользователь в списке всех участников ](my-own-conference.md#proverka-est-li-polzovatel-v-spiske-vsekh-uchastnikov)
* [Как создать участника ](my-own-conference.md#sozdanie-uchastnika)
* [Как зарегистрировать участника на вебинар](my-own-conference.md#kak-zaregistrirovat-uchastnika-na-vebinar)

## Как настроить подключение

Для начала работы необходимо получить **ключ API**. Для этого зайдите в свой **личный кабинет** My own CONFERENCE, раздел **Профиль**:

![Личный кабинет my own Conference](https://lh4.googleusercontent.com/BVWwCBa2eG-8LmRwkMWvlDmyU-XhZWHiCUsrHrbnQR6CBj0JQCJVlc5zcYrYB0a88U-XIdh2rRIL12p6kEp0xKApdGKQwh09yOrTBKV--gZfaBkCyT1GKuMsDGLZX3tGHRss0sKp)

После получения API-ключа переходим в настройки проекта в **Salebot -> Константы проекта** и сохраняем его в переменную **myownconference\_api\_key**:

![Раздел Константы проекта в Настройках проекта Salebot](https://lh3.googleusercontent.com/MJMCBMs1zaof3EdhuQbfPsLGtFhcFa9_VAHkQ0oqM0Jg8EQRHfV_Iu2kSpTfh7QWN3hdYxvmRbDNZkFXKqDyfm2W5XzhAD1sSEWGobOOZMB6ewBO3fQsO8iM8_xhQx74ad89O_oN)

{% hint style="warning" %}
Каждая функция возвращает словарь, у которого есть параметр **status**, он может иметь два значения 0 и 1.

Если значение status=1, то запрос в myownconference прошел успешно и в параметре **result** будет результат запроса, например: \
{'status': '1', 'result': \[{'name': 'Super web', 'alias': 'csml-sjgf-cnjp-clkw', 'start': '2022-02-12 00:00:00'}]} \
или запрос в myownconference прошел успешно, но ничего не найдено: \
{'status': '1', 'result': \[]}

Если status=0 - то есть какая-то проблема и описание будет находиться в **error**, например: {"status":"0","error":"Webinar with alias "wenk-gjkc-teqp-nteh" not active"} {'status': '0', 'error': 'Missing required variables - email'}
{% endhint %}

## Как осуществлять поиск вебинаров

Для поиска вебинаров используется функция **myownconference\_find\_webinars(date, status)**, где:\
**date** - дата в формате дд.мм.гггг выбор всех вебинаров за определенный день \
**status** - значение 1 (активные или будущие вебинары), 0 - завершенные

**myownconference\_find\_webinars()** - без аргументов вернет массив всех найденных вебинаров.

**Функция возвращает словарь вида:** \
&#xNAN;**- в случае успеха:** \
{'status': '1', 'result': \[{'name': 'Super web', 'alias': 'csml-sjgf-cnjp-clkw', 'start': '2022-02-12 00:00:00'}]} \
&#xNAN;**- в случае ошибки, например:** \
{"status":"0","error":"Format not supported or date is not valid. Params must be yyyy-mm-dd"}

## **Как проверить присутствует ли пользователь на активном вебинаре**

**myownconference\_is\_online\_user(webinar\_id, email)**\
**webinar\_id** - идентификатор вебинара, другими словами значение 'alias' из запроса при поиске вебинара\
**email** - адрес электронной почты пользователя, если не передать, то будет использоваться адрес из переменной email, если она есть.

**Результат работы функции при успешном запросе:** \
{"status":"1","result":true} - пользователь присутствует в данный момент на вебинаре {"status":"1","result":false} - пользователь не на вебинаре

**В случае возникновения проблемы при выполнении запроса:**\
{"status":"0","error":"Webinar with alias "serg-dhpq-mznf-fwcb" not active"}

## **Как получить данные истории пользователя по вебинару**

**myownconference\_history\_user(webinar\_id, email)**\
**webinar\_id** - идентификатор вебинара, другими словами значение 'alias' из запроса при поиске вебинара\
**email** - адрес электронной почты пользователя - необязательный параметр, если есть адрес в переменной email, то значение будет взято из нее.

**Результат работы функции при успешном запросе:**\
в параметре **'result'** будет массив с данными о пользователе: \
{'status': '1', 'result': \['Вася Пупкин', 'exam@gmail.com', 'ua', '12:02:45', '12:12:15', 'G', '28%']} {"status":"1","result":false} - пользователь не найден

**В случае возникновения проблемы при выполнении запроса:**\
{'status': '0', 'error': 'Missing required variables - email'} - не передан адрес электронной почты и адрес не найден в переменной email

**Пример запроса и получении имени пользователя:**

![Пример оформления запроса на получение данных истории пользователя по вебинару](https://lh3.googleusercontent.com/eotTVaE1xBS_er0M6iafaJejxN6q8x5j5NiQrh2ZPY2xpEWvRevfoMxjfYZ9xB5hYbYB7-rXr43a0_w50i5KqQFsc89TUs-k1SoI65br6KX1_91WnCYdgSuf4Hzw3KQO0gh_1leE)

![Пример результата выполнения запроса](https://lh3.googleusercontent.com/000B5b3ld7K1N4n80J3SEipzZn1R9w2bP-uVbFd0ENQbY2UOZ-XhNYAjenB-kiKndGLViwBieRkVchxztxZx3pYwMkwhlYZrJAqhIiEyq9zz3jCn_1E_uMYFTf4qRhgDajmWmAV-)

## Как проверить е**сть ли пользователь в списке всех участников**

**myownconference\_is\_our\_user(email)**\
**email** - адрес электронной почты пользователя - необязательный параметр, если есть адрес в переменной email, то значение будет взято из нее.

**Результат работы функции при успешном запросе:** \
{"status":"1","result":true} - пользователь присутствует в Вашей базе \
{"status":"1","result":false} - нет такого пользователя в Вашей базе участников

**В случае возникновения проблемы при выполнении запроса:** \
{'status': '0', 'error': 'Missing required variables - email'} - не передан адрес электронной почты email и его значение не найдено в переменной email

## **Как создать участника**

Эта функция добавляет участника вебинара в общий список всех пользователей. После успешного создания, этого пользователя уже можно зарегистрировать на какой-то вебинар (об этом ниже).

**myownconference\_add\_user(email)**\
**email** - адрес электронной почты пользователя - необязательный параметр, если есть адрес  в переменной email, то значение будет взято из нее.

**Результат работы функции при успешном запросе :**\
{"status":"1","result":true} - пользователь добавлен в ваш список всех участников

**В случае возникновения проблемы при выполнении запроса:**  \
{'status': '0', 'error': 'Missing required variables - email'} - не передан адрес электронной почты email и его значение не найдено в переменной email

## **Как зарегистрировать участника на вебинар**

Для регистрации обязательно надо спрашивать у клиента email. Все остальное - по желанию.

**myownconference\_add\_user\_to\_webinar(webinar\_id, email)**\
**webinar\_id** - идентификатор вебинара, другими словами значение 'alias' из запроса при поиске вебинара \
**email** - адрес электронной почты пользователя - необязательный параметр, если есть адрес  в переменной email, то значение будет взято из нее.

**Результат работы функции при успешном запросе:**\
{"status":"1","result":true} - пользователь зарегистрирован  на вебинар

**В случае возникновения проблемы при выполнении запроса:** \
{"status":"0","error":"Webinar with alias \\"serg-dhpq-mznf-fwcb\\" not active"}
