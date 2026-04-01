# Функции для работы с MAX

## Удалить сообщение

**max\_delete\_message(message id)** - удаляет указанное сообщение

| Параметр    | Описание                                                   |
| ----------- | ---------------------------------------------------------- |
| message\_id | id сообщения, которое нужно удалить. Обязательный параметр |

## Проверка подписки в групповом чате

max\_get\_chat\_member(chat\_id, user\_id) - проверить, состоит ли пользователь в групповом чате

| Параметр  | Описание                 |
| --------- | ------------------------ |
| chat\_id  | идентификатор чата в MAX |
| user\_id  | id пользователя          |

Если пользователь есть в чате, в ответе будет информация о нем. Если пользователя в чате нет, в ответе будет None

<div data-with-frame="true"><figure><img src="../../../.gitbook/assets/Снимок экрана 2026-03-19 в 17.29.23.png" alt=""><figcaption></figcaption></figure></div>

**`id_user = tt_request['message']['sender']['user_id']`** - необходимо прописать данную строк в калькуляторе, чтобы получить ID пользователя, который пишет в бот.

**`test = max_get_chat_member(-72227316929933, id_user)`** - функция для проверки подписки.

Ответ, если пользователь подписан:

{"last\_access\_time":1773919506455,"is\_owner":false,"is\_admin":false,"join\_time":1773919506455,"user\_id":5629219,"first\_name":"Tammy","last\_name":"Anw","is\_bot":false,"last\_activity\_time":1773919503000,"avatar\_url":"https://i.oneme.ru/i?r=BUFglOvkF6bn--g5U-BFgIkJ0mY5P8dF4T07z1RJjDqz22ee8G3r5tY7WE9sVySelj049w2aqEqPjDkS8j\_urqGG","full\_avatar\_url":"https://i.oneme.ru/i?r=BTFjO43w8Yr1OSJ4tcurq5HiKvNSlBkRpQUHL6c7ALhsGi3evqe\_\_2qMW2oV\_NMniqI","name":"Tammy Anw"}

Если пользователь не подписан, ответ None.

## Добавить пользователя в групповой чат

max\_add\_chat\_member(chat\_id, user\_id) - добавить пользователя в групповой чат

| Параметр | Описание                 |
| -------- | ------------------------ |
| chat\_id | идентификатор чата в MAX |
| user\_id | id пользователя          |

## Удалить пользователя из группового чата

max\_delete\_chat\_member(chat\_id, user\_id) - удалить пользователя из группового чата

| Параметр | Описание                 |
| -------- | ------------------------ |
| chat\_id | идентификатор чата в MAX |
| user\_id | id пользователя          |

## Отправить сообщение

max\_send\_message(platform\_id, text, enable\_markdown, enable\_html, disable\_link\_preview, disable\_notification, send\_by\_user\_id)

platfrom\_id - platfrom\_id клиента

text - текст сообщения

enable\_markdown - включить разметку текста markdown. Необязательный параметр

enable\_html - включить разметку текста html. Необязательный параметр

disable\_link\_preview - выключить превью ссылок. Необязательный параметр

disable\_notification - выключить уведомления при отправке сообщения. Необязательный параметр

send\_by\_user\_id - использовать для отправки user\_id клиента вместо platform\_id. Чтобы отправить сообщение по user\_id, нужно передать этот параметр, и вместо platfrom\_id передать user\_id. Необязательный параметр

## Отправить фото

max\_send\_photo(platform\_id, image\_url, caption, enable\_markdown, enable\_html, disable\_link\_preview, disable\_notification, send\_by\_user\_id)

platfrom\_id - platfrom\_id клиента

image\_url - url изображения

caption - текст подписи. Необязательный параметр

enable\_markdown - включить разметку текста markdown. Необязательный параметр

enable\_html - включить разметку текста html. Необязательный параметр

disable\_link\_preview - выключить превью ссылок. Необязательный параметр

disable\_notification - выключить уведомления при отправке сообщения. Необязательный параметр

send\_by\_user\_id - использовать для отправки user\_id клиента вместо platform\_id. Чтобы отправить сообщение по user\_id, нужно передать этот параметр, и вместо platfrom\_id передать user\_id. Необязательный параметр

## Отправить файл

max\_send\_document(platform\_id, file\_url, caption, enable\_markdown, enable\_html, disable\_link\_preview, disable\_notification, send\_by\_user\_id)

platfrom\_id - platfrom\_id клиента

file\_url - url документа

caption - текст подписи. Необязательный параметр

enable\_markdown - включить разметку текста markdown. Необязательный параметр

enable\_html - включить разметку текста html. Необязательный параметр

disable\_link\_preview - выключить превью ссылок. Необязательный параметр

disable\_notification - выключить уведомления при отправке сообщения. Необязательный параметр

send\_by\_user\_id - использовать для отправки user\_id клиента вместо platform\_id. Чтобы отправить сообщение по user\_id, нужно передать этот параметр, и вместо platfrom\_id передать user\_id. Необязательный параметр
