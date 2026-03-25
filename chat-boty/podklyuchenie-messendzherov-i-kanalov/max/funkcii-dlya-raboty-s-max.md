# Функции для работы с MAX

## Функции калькулятора

### Удалить сообщение

**max\_delete\_message(message id)** - удаляет указанное сообщение

| Параметр    | Описание                                                   |
| ----------- | ---------------------------------------------------------- |
| message\_id | id сообщения, которое нужно удалить. Обязательный параметр |

### Проверка подписки в групповом чате

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

### Добавить пользователя в групповой чат

max\_add\_chat\_member(chat\_id, user\_id) - добавить пользователя в групповой чат

| Параметр | Описание                 |
| -------- | ------------------------ |
| chat\_id | идентификатор чата в MAX |
| user\_id | id пользователя          |

### Удалить пользователя из группового чата

max\_delete\_chat\_member(chat\_id, user\_id) - удалить пользователя из группового чата

| Параметр | Описание                 |
| -------- | ------------------------ |
| chat\_id | идентификатор чата в MAX |
| user\_id | id пользователя          |
