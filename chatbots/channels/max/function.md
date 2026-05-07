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

<div data-with-frame="true"><figure><img src="../../../.gitbook/assets/IMAGE 2026-04-20 165639.jpg" alt=""><figcaption></figcaption></figure></div>

**`test = max_get_chat_member(-123456789876, id_user)`** - функция для проверки подписки.

Где -123456789876 это идентификатор чата/канала подписку на который Вы проверяете&#x20;

user\_id - это системная переменная, которая есть у клиентов

Ответ, если пользователь подписан:

{"last\_access\_time":1773919506455,"is\_owner":false,"is\_admin":false,"join\_time":1773919506455,"user\_id":5629219,"first\_name":"Tammy","last\_name":"Anw","is\_bot":false,"last\_activity\_time":1773919503000,"avatar\_url":"https://i.oneme.ru/i?r=BUFglOvkF6bn--g5U-BFgIkJ0mY5P8dF4T07z1RJjDqz22ee8G3r5tY7WE9sVySelj049w2aqEqPjDkS8j\_urqGG","full\_avatar\_url":"https://i.oneme.ru/i?r=BTFjO43w8Yr1OSJ4tcurq5HiKvNSlBkRpQUHL6c7ALhsGi3evqe\_\_2qMW2oV\_NMniqI","name":"Tammy Anw"}

Если пользователь не подписан, ответ None.

## Добавить пользователя в групповой чат

max\_add\_chat\_member(chat\_id, user\_id) - добавить пользователя в групповой чат

| Параметр                                           | Описание                 |
| -------------------------------------------------- | ------------------------ |
| <mark style="color:$danger;">**!**</mark> chat\_id | идентификатор чата в MAX |
| <mark style="color:$danger;">**!**</mark> user\_id | id пользователя          |

## Удалить пользователя из группового чата

max\_delete\_chat\_member(chat\_id, user\_id) - удалить пользователя из группового чата

| Параметр                                           | Описание                 |
| -------------------------------------------------- | ------------------------ |
| <mark style="color:$danger;">**!**</mark> chat\_id | идентификатор чата в MAX |
| <mark style="color:$danger;">**!**</mark> user\_id | id пользователя          |

## Отправить сообщение

max\_send\_message(platform\_id, text, enable\_markdown, enable\_html, disable\_link\_preview, disable\_notification, send\_by\_user\_id)

| Параметр                                               | Описание                                                                                                                                                                                                                                                                                 |
| ------------------------------------------------------ | ---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| <mark style="color:$danger;">**!**</mark> platfrom\_id | platfrom\_id клиента                                                                                                                                                                                                                                                                     |
| <mark style="color:$danger;">**!**</mark> text         | текст сообщения                                                                                                                                                                                                                                                                          |
| enable\_markdown                                       | включить разметку текста markdown. Необязательный параметр                                                                                                                                                                                                                               |
| enable\_html                                           | <p>включить разметку текста html. Необязательный параметр<br>Для включения нужно передать "1" или какое-нибудь значение, кроме 0 или False</p>                                                                                                                                           |
| disable\_link\_preview                                 | <p>выключить превью ссылок. Необязательный параметр<br>Для включения нужно передать "1" или какое-нибудь значение, кроме 0 или False</p>                                                                                                                                                 |
| disable\_notification                                  | <p>выключить уведомления при отправке сообщения. Необязательный параметр<br>Для включения нужно передать "1" или какое-нибудь значение, кроме 0 или False</p>                                                                                                                            |
| send\_by\_user\_id                                     | <p>использовать для отправки user_id клиента вместо platform_id. Чтобы отправить сообщение по user_id, нужно передать этот параметр, и вместо platfrom_id передать user_id. Необязательный параметр<br>Для включения нужно передать "1" или какое-нибудь значение, кроме 0 или False</p> |
| bot\_account\_id                                       | id аккаунта (бота), от имени которого нужно отправить сообщение. Необязательный параметр                                                                                                                                                                                                 |

## Отправить фото

max\_send\_photo(platform\_id, image\_url, caption, enable\_markdown, enable\_html, disable\_link\_preview, disable\_notification, send\_by\_user\_id)

<table><thead><tr><th width="284.9921875">Параметр</th><th>Описание</th></tr></thead><tbody><tr><td><mark style="color:$danger;"><strong>!</strong></mark> platfrom_id</td><td>platfrom_id клиента</td></tr><tr><td><mark style="color:$danger;"><strong>!</strong></mark> image_url</td><td>url изображения</td></tr><tr><td>caption</td><td>текст подписи. Необязательный параметр</td></tr><tr><td>enable_markdown</td><td>включить разметку текста markdown. Необязательный параметр<br>Для включения нужно передать "1" или какое-нибудь значение, кроме 0 или False</td></tr><tr><td>enable_html</td><td>включить разметку текста html. Необязательный параметр<br>Для включения нужно передать "1" или какое-нибудь значение, кроме 0 или False</td></tr><tr><td>disable_link_preview</td><td>выключить превью ссылок. Необязательный параметр<br>Для включения нужно передать "1" или какое-нибудь значение, кроме 0 или False</td></tr><tr><td>disable_notification</td><td>выключить уведомления при отправке сообщения. Необязательный параметр<br>Для включения нужно передать "1" или какое-нибудь значение, кроме 0 или False</td></tr><tr><td>send_by_user_id</td><td>использовать для отправки user_id клиента вместо platform_id. Чтобы отправить сообщение по user_id, нужно передать этот параметр, и вместо platfrom_id передать user_id. Необязательный параметр<br>Для включения нужно передать "1" или какое-нибудь значение, кроме 0 или False</td></tr><tr><td>bot_account_id</td><td>id аккаунта (бота), от имени которого нужно отправить сообщение. Необязательный параметр</td></tr></tbody></table>

## Отправить файл

max\_send\_document(platform\_id, file\_url, caption, enable\_markdown, enable\_html, disable\_link\_preview, disable\_notification, send\_by\_user\_id)

<table><thead><tr><th width="272.55859375">Параметр</th><th>Описание</th></tr></thead><tbody><tr><td><mark style="color:$danger;"><strong>!</strong></mark> platfrom_id</td><td>platfrom_id клиента</td></tr><tr><td><mark style="color:$danger;"><strong>!</strong></mark> file_url</td><td>url документа</td></tr><tr><td>caption</td><td>текст подписи. Необязательный параметр</td></tr><tr><td>enable_markdown</td><td>включить разметку текста markdown. Необязательный параметр. <br>Для включения нужно передать "1" или какое-нибудь значение, кроме 0 или False</td></tr><tr><td>enable_html</td><td>включить разметку текста html. Необязательный параметр.<br>Для включения нужно передать "1" или какое-нибудь значение, кроме 0 или False</td></tr><tr><td>disable_link_preview</td><td>выключить превью ссылок. Необязательный параметр<br>Для включения нужно передать "1" или какое-нибудь значение, кроме 0 или False</td></tr><tr><td>disable_notification</td><td>выключить уведомления при отправке сообщения. Необязательный параметр<br>Для включения нужно передать "1" или какое-нибудь значение, кроме 0 или False</td></tr><tr><td>send_by_user_id</td><td>использовать для отправки user_id клиента вместо platform_id. Чтобы отправить сообщение по user_id, нужно передать этот параметр, и вместо platfrom_id передать user_id. Необязательный параметр<br>Для включения нужно передать "1" или какое-нибудь значение, кроме 0 или False</td></tr><tr><td>bot_account_id</td><td>id аккаунта (бота), от имени которого нужно отправить сообщение. Необязательный параметр</td></tr></tbody></table>
