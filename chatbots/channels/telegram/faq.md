# FAQ Telegram

## На iPhone  тег не приходит при повторном входе по прямой ссылке?

Это особенность iPhone.

Если открыть диалог с ботом в Telegram и перейти по прямой ссылке с тегом из другого приложения, реакция не происходит. Однако, если закрыть либо диалог, либо само приложение Telegram, все работает корректно.

## Почему картинка приходит ссылкой?

Скорее всего вы не учли требования Bot API к файлам. Основные требования указаны в статье "[Отправка вложений](https://docs.salebot.pro/messendzhery-i-chaty/kak-sozdat-bota-v-telegram#dlya-informacii)".&#x20;

Таким образом, фото с большим разрешением отправляются ссылкой со значком 🚫

## Как удалить сообщение "Что умеет этот бот?" в Telegram

Если при создании бота вы вводите его ИМЯ и его username с окончанием bot, и не вводите ОПИСАНИЕ, то получите такой результат:

<figure><img src="https://lh7-rt.googleusercontent.com/docsz/AD_4nXfRy5FFuCfs10NYoCPxPnVvrfTR8YRt28rjEzTuOU1UdlU8VKtu2LphfBc9i-wUoHJ_kthndAoAINGFiOt14gQW_j50A8EijmETNwGrRNzkCxby2TurEuw9Ers8UKVyxzMoq5tM?key=ET92Byz3gZBtln2Fpf9spQGv" alt="" width="375"><figcaption></figcaption></figure>

На скриншоте нет сообщения "Что умеет этот бот", диалог пуст и есть только кнопка запуска.

Вывод: Если НЕ вводить описание (Edit Description), то сообщение перед запуском "Что умеет этот бот" не отображается.

В случае, когда описание бота уже введено, Edit Description можно только изменить, но не удалить. В качестве решения вопроса, можно удалить бот и создать с тем же именем:

1. команда newbot - создаем новый бот
2. ввод имени - указываем его имя (ник)&#x20;
3. ввод username for bot - указываем имя бота

<figure><img src="https://lh7-rt.googleusercontent.com/docsz/AD_4nXddTTConE1fop766DEbLnNyENLpu6qGHgMja-y3aErAfl8NeVo0h23iIBojHbqBo3--WLwCe-G86ikMuYREqecl2rrM38xrOSqK6WZiN3_9H2WC-5QcAcHs7xbMys0jpM3OTUI5?key=ET92Byz3gZBtln2Fpf9spQGv" alt="" width="375"><figcaption></figcaption></figure>

Поскольку речь идет о создании нового бота, то конечно клиенты старого бота не будут привязаны к новому. Продумайте изначально как переведете клиентов из одного бота в другой.

{% hint style="success" %}
Как поменять имя чата или его описание можно посмотреть[ тут](https://docs.salebot.pro/peremennye-1/api-v-kalkulyatore#kak-pomenyat-imya-chata-cherez-bot)
{% endhint %}

## Как сделать шрифт жирным?

Чтобы сделать шрифт жирным начертанием, нужно выделить нужное слово или текст с двух сторон звездочками: \*жирный\*

{% hint style="info" %}
Как сделать форматирование для Телеграма, [рассказали здесь](https://docs.salebot.pro/peremennye-1/api-v-kalkulyatore#ustanovki-parse_mode).&#x20;
{% endhint %}

## Как добавить реакции под постом в канале при помощи бота

1. Создаем новый бот для своего канала через @BotFather&#x20;
2. Добавляем наш бот в Администраторы канала (Telegram: Настройки канала - Администраторы - Добавить Администратора)
3. Производим настройку бота через @ControllerBot.&#x20;

<figure><img src="https://lh7-rt.googleusercontent.com/docsz/AD_4nXemQWo-YnaocDiykdQOkE6A_v0KMRCl1oJ1pm4gM_6a1y_-sr6uL6vKcdJL9HeU0X4jWSb6RIhtilVkzSVfUBz8TJ4CDQCmb0itPdW4MiDEv9p2xDhGsRoD_hs9yYQnnlIvYveHTQ?key=ET92Byz3gZBtln2Fpf9spQGv" alt=""><figcaption></figcaption></figure>

После запуска выбираем /addchannel. @ControllerBot предложит создать новый бот через @BotFather или ввести токен существующего. Поскольку мы создали бот в п.1, то указываем его токен:

<figure><img src="https://lh7-rt.googleusercontent.com/docsz/AD_4nXcJQq-wOjkmXcQowbOsNGMYbR8WV94ewR1hRMQJtvO5EeP1FMI4nX_cnZv5fijYc2_oof-AtyEmAhSURQgFtMmcWGs9Q_nOSobKrYARf1GAPdad5p1GuYzri68DLS8mF2nXd9yL?key=ET92Byz3gZBtln2Fpf9spQGv" alt="" width="563"><figcaption></figcaption></figure>

После ввода токена бота добавим наш канал:

<figure><img src="https://lh7-rt.googleusercontent.com/docsz/AD_4nXfrQkwrO5f1LQQGe8qYYA5xWy2kp-zpypn3UQWWggbXZk54Akd4Yu31AIwDrrluRW2cqmDOr9CG9526Z9eMxl6xtQOi4aHmR3xncy1xp3t1nWmuLCYauhtKGVYcz7NtNBxN7k7g?key=ET92Byz3gZBtln2Fpf9spQGv" alt="" width="563"><figcaption></figcaption></figure>

Для этого выполняем шаг 2 - пересылаем в @ControllerBot  любое сообщение из вашего канала (в администраторы, которого мы добавили вышеупомянутый бот):

<figure><img src="https://lh7-rt.googleusercontent.com/docsz/AD_4nXc3ku_kBVY6KByoRsIe3gFs04QForDDwBAd91B1G7pUrDfH0WL7n4A0V4G2CgCu-HILoM5axr_EJljLlB5_MCSwQP5RdwlMkDezqDCSaHNKBZdpkyTHMDEDE-i9ljyq1r9Z4bn_WQ?key=ET92Byz3gZBtln2Fpf9spQGv" alt="" width="375"><figcaption></figcaption></figure>

После подтверждения у нас появляется возможность создавать публикации:

<figure><img src="https://lh7-rt.googleusercontent.com/docsz/AD_4nXel6gXGSCSPlmD9ub5Sbm3xVipAUbKfoWOMLDyySAux_F1LwC2tLN0NXlbRMsViuMKqep7AepvyU_sHGXxtHTrZouCvh-eH4TFsn29N99rXduN1BG5QV4e0CT00lZlPXqArLDVicQ?key=ET92Byz3gZBtln2Fpf9spQGv" alt="" width="563"><figcaption></figcaption></figure>

Для этого перейдите в свой бот - запустите его! Появится меню:

<figure><img src="https://lh7-rt.googleusercontent.com/docsz/AD_4nXfDywHQ_46zvSJY6AghnI667alaItvGXHy4azmkYlXtdGTXH55zEI1occ5aRS9D5EavKPBL_xETTrvofJajK8B3UCJI8HHFkGWgjneVi6R3p2_iSlo_LB77wv1Ju5ggir-LHkRoww?key=ET92Byz3gZBtln2Fpf9spQGv" alt="" width="563"><figcaption></figcaption></figure>

Выбираем Создать пост, выбираем свой канал, настраиваем форматирование:

<figure><img src="https://lh7-rt.googleusercontent.com/docsz/AD_4nXeXdxMzGAtSgUI_hd571PyAlCYDF8J_Bp4lnLQgu2lv9OHdnx1ZAQfPGMy9KA9DX63Bn6pccu2oa5NjXAmanOw0IDZYoKrZTvszhMtqEV55LSFGmQ49QSDRiiY_T-McVv6OjE-Z3A?key=ET92Byz3gZBtln2Fpf9spQGv" alt="" width="563"><figcaption></figcaption></figure>

Отправляем боту текст будущего поста:

<figure><img src="https://lh7-rt.googleusercontent.com/docsz/AD_4nXe_izYDelmylVM_731semlEBSH40YuYr0Ii7S0F1-AFgkFFkxmyBYZvCB6HAIqdcpnQDme3Ee5VchHZoAj6RTWRJrWDHe_RIS03Z6aCHYmo7Ze8G6C-1C330dYabWSHY4NLGQZaxA?key=ET92Byz3gZBtln2Fpf9spQGv" alt="" width="375"><figcaption></figcaption></figure>

Добавляем реакции:

<figure><img src="https://lh7-rt.googleusercontent.com/docsz/AD_4nXcNJTD5Gf_Bk72kX4cOS3K_oslE7Gp6oSwtDv7e2lXgx6aSvRjBC4RTiLLYH1fnDHPEcEHcRQTuS1L3VaQr5m0ssTiZX0fa051L6cdBBae3_wMme7W-2zsyT8AWcpMdo1oTKyxjKQ?key=ET92Byz3gZBtln2Fpf9spQGv" alt="" width="375"><figcaption></figcaption></figure>

и нажимаем Далее. После небольшого ожидания бот предложит пост опубликовать прямо сейчас или разместить в отложенные:

<figure><img src="https://lh7-rt.googleusercontent.com/docsz/AD_4nXdErykiDPetjwnPdJx_J5vJC65O3sIxU2ExdLc5CSTigs48f8rsSWQEURy5y9m2LWF-Kl8fALNEiMDxBtZFo1LdQXGX6BRX-r1vFXx7rG8ZSvAa1GKlr9D9v0cZtGJ5wOGiJ7oBrw?key=ET92Byz3gZBtln2Fpf9spQGv" alt="" width="375"><figcaption></figcaption></figure>

Публикуем и получаем пост с введенными реакциями на нашем канале:

<figure><img src="https://lh7-rt.googleusercontent.com/docsz/AD_4nXd9iKJWPWPabNOJlMaKcC9hr_gNgva38oCbgFYF3uFFYoEsgR9K1bB1yaCRuO2ELdNiHvnlLsfTzMJBwM9GUil0UJoXoPehdb8mndt6P2perEU_FoYQLX9dDliY_wxrIxK1_S8GxQ?key=ET92Byz3gZBtln2Fpf9spQGv" alt="" width="375"><figcaption></figcaption></figure>

В реакцию можно добавить максимально 6 эмодзи.

## Как писать первым от имени бота при подаче заявки в закрытый канал

Для этого нужно создать:

1. Закрытый канал;
2. Бота, который будет иметь права Администратора в данном канале

Формируем ссылку Без ограничений, обязательно включите флаг Заявка на вступление:

<figure><img src="https://lh7-rt.googleusercontent.com/docsz/AD_4nXccB2tG3CUStGphlmJ6-O66Gt9uDUy7RzwGYj0KseLlb1ctYiQaYquPFN86J10UtNOlrSc4-i4NOB-nsYLkJrOePDNF9wCAM7-k_EaM6qQe1voF9Xx3seHBsB6n5dMsj96g3HklIA?key=ET92Byz3gZBtln2Fpf9spQGv" alt="" width="375"><figcaption></figcaption></figure>

Telegram: Управление группой - Пригласительные ссылки - Создать новую ссылку

Переходим к настройке воронки в нашем проекте:

Настраиваем блок, который будет ловить событие подачи заявки на вступление в группу от клиента  chat\_join\_request

В Калькуляторе блока прописываем принятие клиента в чат:

[tg\_approve\_chat\_join\_request(platform\_id, chat\_member\_id)](https://docs.salebot.pro/messendzhery-i-chaty/kak-sozdat-bota-v-telegram/api-telegram-funkcii-dlya-ispolzovaniya-vsekh-vozmozhnostei-telegram#kak-rabotat-s-zayavkami-v-chat-kanal-telegram), где

1. platform\_id - идентификатор нашей закрытой группы&#x20;
2. chat\_member\_id - идентификатор клиента, который подал заявку на вступление. Данная переменная формируется автоматически при подаче заявки.

А также настраиваем[ запуск бота по идентификатору Telegram](https://docs.salebot.pro/api-v-konstruktore-salebot.pro/api-konstruktora#zapusk-bota-po-identifikatoru-telegram)  при помощи запроса API-конструктора:

https://chatter.salebot.pro/api/#{api\_key}/tg\_callback, где прописываем параметры запроса:

1. message - текст callback-сообщения
2. user\_id - идентификатор клиента, которому шлем колбек. В нашем случае, это chat\_member\_id&#x20;
3. group\_id - имя нашего бота. В нашем случае, это значение я сохранила в константах проекта - mybot:
4. api\_key - Ключ доступа к API из раздела Настройки проекта.

<figure><img src="https://lh7-rt.googleusercontent.com/docsz/AD_4nXfNXuv2Tm9PBtWVxRIGTH7ssRnYjiuob04knRis3xx3Zna58PvA4V6TIbG8YHGq4hx6oL-H38TPyPPc7xQj6qtwtL72pmNyx-5zBStEl5pY9gCLP473_YKjpM8WLS8xRfugbD3-aA?key=ET92Byz3gZBtln2Fpf9spQGv" alt=""><figcaption></figcaption></figure>

Настройка запроса API-конструктора:

<figure><img src="../../../.gitbook/assets/Снимок экрана 2025-10-20 в 15.44.37.png" alt=""><figcaption></figcaption></figure>

<details>

<summary>Для копирования JSON параметров</summary>

{"message": "otpravka\_vbot", \
"user\_id": "#{chat\_member\_id}", \
"group\_id": "#{my\_bot}"\
}

</details>

Настраиваем второй блок с нашим колбеком otpravka\_vbot, который будет отправлять приветственное сообщение от бота нашему клиенту:

<figure><img src="../../../.gitbook/assets/Снимок экрана 2025-10-20 в 15.47.02.png" alt=""><figcaption></figcaption></figure>

Для этого скопируйте значение колбека параметра message (в примере — "Otpravka\_vbot") и вставьте колбек в поле Условие во втором блоке:

<figure><img src="../../../.gitbook/assets/Снимок экрана 2025-10-20 в 15.49.20.png" alt=""><figcaption></figcaption></figure>
