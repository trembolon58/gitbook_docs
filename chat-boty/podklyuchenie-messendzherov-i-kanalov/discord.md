# Discord

## Подготовка к подключению

### Cоздание бота

Шаг 1. Создайте приложение ([перейдите по ссылке](https://discord.com/developers/applications))

Шаг 2. Добавьте бота (Add Bot)

<div data-with-frame="true"><figure><img src="../../.gitbook/assets/Снимок экрана 2026-03-10 в 13.30.29.png" alt=""><figcaption></figcaption></figure></div>

Шаг 2.1. В разделе Installation выберите Install Link -> None

<div data-with-frame="true"><figure><img src="../../.gitbook/assets/Снимок экрана 2026-03-10 в 13.31.30.png" alt=""><figcaption></figcaption></figure></div>

Шаг 2.2. В разделе Bot выключите Public Bot, далее включите Intents:

* Message Content Intent;
* Server memebrs intent;
* но можно и Presence Intent на будущее.

<div data-with-frame="true"><figure><img src="../../.gitbook/assets/Снимок экрана 2026-03-10 в 13.36.19.png" alt=""><figcaption></figcaption></figure></div>

<div data-with-frame="true"><figure><img src="../../.gitbook/assets/Снимок экрана 2026-03-10 в 13.37.50.png" alt=""><figcaption></figcaption></figure></div>

&#x20;3\. Получите токен (Reset Token)

&#x20;4\. Добавьте бота на сервер (OAuth2 → URL Generator, в Scopes отметить bot, в Bot Permissions выбрать Send Messages, Read Message History и другие нужные привилегии, перейти по полученной ссылке, выбрать сервер для добавления и согласиться)

<div data-with-frame="true"><figure><img src="../../.gitbook/assets/Снимок экрана 2026-03-10 в 13.39.07.png" alt=""><figcaption></figcaption></figure></div>

<div data-with-frame="true"><figure><img src="../../.gitbook/assets/Снимок экрана 2026-03-10 в 13.40.18.png" alt=""><figcaption></figcaption></figure></div>

Для получения полного вебхука от Дискорд достаточно присвоить любое значение переменной  save\_webhook

Если переменная задана, вебхук будет в сохранен в discord\_webhook

### Функции калькулятора

### Ответить на сообщение

discord\_reply\_to\_message(message\_id, text) - ответить на сообщение

| Параметр                                               | Описание                                |
| ------------------------------------------------------ | --------------------------------------- |
| <mark style="color:$danger;">**!**</mark> message\_id  | id сообщения, на которое нужно ответить |
| <mark style="color:$danger;">**!**</mark> text         | текст ответного сообщения               |

### Удалить сообщение

discord\_delete\_message(message\_id) - удалить сообщение

| Параметр                                               | Описание                            |
| ------------------------------------------------------ | ----------------------------------- |
| <mark style="color:$danger;">**!**</mark> message\_id  | id сообщения, которое нужно удалить |

### Изменить сообщение

discord\_edit\_message(message\_id, text) - изменить сообщение

| Параметр                                               | Описание                             |
| ------------------------------------------------------ | ------------------------------------ |
| <mark style="color:$danger;">**!**</mark> message\_id  | ID сообщение, которое нужно изменить |
| <mark style="color:$danger;">**!**</mark> text         | новый текст сообщения                |

### Закрепить сообщение

discord\_pin\_message(message\_id) - закрепить сообщение

| Параметр                                               | Описание                               |
| ------------------------------------------------------ | -------------------------------------- |
| <mark style="color:$danger;">**!**</mark> message\_id  |  ID сообщение, которое нужно закрепить |

### Открепить сообщение

discord\_unpin\_message(message\_id) - открепить сообщение

| Параметр                                               | Описание                               |
| ------------------------------------------------------ | -------------------------------------- |
| <mark style="color:$danger;">**!**</mark> message\_id  |  ID сообщения, которое нужно открепить |

### Отправить реакцию на сообщение

discord\_send\_reaction(message\_id, reaction) - отправить реакцию на сообщение

| Параметр                                               | Описание                                                                                                                                                          |
| ------------------------------------------------------ | ----------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| <mark style="color:$danger;">**!**</mark> message\_id  | сообщение, на которое нужно отправить реакцию                                                                                                                     |
| <mark style="color:$danger;">**!**</mark> reaction     | реакция, которую нужно отправить. Можно передать один эмодзи (Например ❤️), или id кастомного эмодзи на сервере. Где взять id кастомного эмодзи - информация ниже |

### Удалить реакцию на сообщение в канале

discord\_delete\_reaction(message\_id, reaction, user\_id) - удалить реакцию на сообщение в канале

| Параметр                                               | Описание                                                                                                                                                        |
| ------------------------------------------------------ | --------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| <mark style="color:$danger;">**!**</mark> message\_id  | сообщение, на котором нужно удалить реакцию                                                                                                                     |
| <mark style="color:$danger;">**!**</mark> reaction     | реакция, которую нужно удалить. Можно передать один эмодзи (Например ❤️), или id кастомного эмодзи на сервере. Где взять id кастомного эмодзи - информация ниже |
| user\_id                                               | id пользователя, чью реакцию нужно удалить. Необязательный параметр, если нужно удалить реакцию от текущего бота.                                               |

## Коллбеки

При отправке реакции от пользователя, в чат поступает коллбек вида:

new\_like ❤️ uid413984787162726410

<div data-with-frame="true"><figure><img src="../../.gitbook/assets/Снимок экрана 2026-03-10 в 13.20.47.png" alt="" width="546"><figcaption></figcaption></figure></div>

где <mark style="color:blue;">**uid413984787162726410**</mark> - id пользователя, отправившего реакцию.&#x20;

## Где взять id кастомной реакции?

Если в канале дискорда отправить кастомную реакцию на сообщение, придет колбек вида:

new\_like beer:1479419477396291696 uid413984787162726410

<div data-with-frame="true"><figure><img src="../../.gitbook/assets/Снимок экрана 2026-03-10 в 13.21.58.png" alt="" width="563"><figcaption></figcaption></figure></div>

где beer:1479419477396291696  - это id реакции. Его можно скопировать для использования в функциях с реакциями

## Где взять id сообщения?

Id сообщения клиента можно получить из вебхука, если save\_webhook включен. Пример:

data = discord\_webhook\["data"]

msg\_id = data\["id"]

result = discord\_reply\_to\_message(msg\_id, "This is a reply to a message")
