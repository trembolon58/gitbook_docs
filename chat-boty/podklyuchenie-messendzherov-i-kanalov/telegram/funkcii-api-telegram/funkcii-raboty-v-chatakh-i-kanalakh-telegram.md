# Функции работы в чатах и каналах Telegram

Так как внутри Salebot идентификаторы клиентов (пользователей, групп, каналов) внутри мессенджера записываются  в переменной platform\_id без каких-либо меток, к чему это принадлежит группе  или пользователю, то для работы с функциями принятия/отклонения заявки требуется единожды запомнить значения platform\_id чата и platform\_id пользователя в переменные с разными именами, например, chat\_id и user\_id.

## Как изменить настройки чата/канала **Telegram**

### <mark style="background-color:blue;">**Как поменять имя чата через бот в Telegram**</mark>

**tg\_set\_group\_title(platform\_id, title)**&#x20;

Параметры:

<table><thead><tr><th width="294.828125">Параметр</th><th>Описание</th></tr></thead><tbody><tr><td> <mark style="color:red;"><strong>!</strong></mark><strong> platform_id</strong> </td><td>идентификатор чата внутри Telegram <a href="funkcii-raboty-v-chatakh-i-kanalakh-telegram.md#gde-vzyat-platform_id-dlya-otpravki-uvedomlenii"><strong>*</strong></a>  </td></tr><tr><td><mark style="color:red;"><strong>!</strong></mark><strong> title</strong></td><td>новое название чата</td></tr></tbody></table>

### <mark style="background-color:blue;">**Как поменять описание чата через бот в Telegram**</mark>

**tg\_set\_chat\_description(platform\_id, description)**

<table><thead><tr><th width="294.828125">Параметр</th><th>Описание</th></tr></thead><tbody><tr><td> <mark style="color:red;"><strong>!</strong></mark><strong> platform_id</strong> </td><td>идентификатор чата внутри Telegram <a href="funkcii-raboty-v-chatakh-i-kanalakh-telegram.md#gde-vzyat-platform_id-dlya-otpravki-uvedomlenii"><strong>*</strong></a>  </td></tr><tr><td><mark style="color:red;"><strong>!</strong></mark><strong> description</strong></td><td>новое описание чата</td></tr></tbody></table>

### <mark style="background-color:blue;">**Как установить аватарку на группу/чат в Telegram**</mark>

**tg\_set\_chat\_photo(platform\_id, photo)**

<table><thead><tr><th width="294.828125">Параметр</th><th>Описание</th></tr></thead><tbody><tr><td> <mark style="color:red;"><strong>!</strong></mark><strong> platform_id</strong> </td><td>идентификатор чата внутри Telegram <a href="funkcii-raboty-v-chatakh-i-kanalakh-telegram.md#gde-vzyat-platform_id-dlya-otpravki-uvedomlenii"><strong>*</strong></a><strong>,</strong> в котором нужно установить аватарку </td></tr><tr><td><mark style="color:red;"><strong>!</strong></mark><strong>  photo</strong></td><td>ссылка на фото</td></tr></tbody></table>

### <mark style="background-color:blue;">**Как удалить аватарку группы/чата в Telegram**</mark>

**tg\_delete\_chat\_photo(platform\_id)**

<table><thead><tr><th width="294.828125">Параметр</th><th>Описание</th></tr></thead><tbody><tr><td> <mark style="color:red;"><strong>!</strong></mark><strong> platform_id</strong> </td><td>идентификатор чата внутри Telegram <a href="funkcii-raboty-v-chatakh-i-kanalakh-telegram.md#gde-vzyat-platform_id-dlya-otpravki-uvedomlenii"><strong>*</strong></a><strong>,</strong> в котором нужно установить аватарку </td></tr></tbody></table>

## Как забанить/разбанить группу **Telegram**

### <mark style="background-color:blue;">**Как забанить группу Telegram**</mark>

**tg\_ban\_chat\_sender\_chat(platform\_id, sender\_chat\_id)**&#x20;

Параметры:

<table><thead><tr><th width="294.828125">Параметр</th><th>Описание</th></tr></thead><tbody><tr><td> <mark style="color:red;"><strong>!</strong></mark><strong> platform_id</strong> </td><td>идентификатор чата внутри Telegram <a href="funkcii-raboty-v-chatakh-i-kanalakh-telegram.md#gde-vzyat-platform_id-dlya-otpravki-uvedomlenii"><strong>*</strong></a><strong>, который нужно забанить</strong></td></tr><tr><td><mark style="color:red;"><strong>!</strong></mark><strong> sender_chat_id</strong></td><td>идентификатор чата, который баним</td></tr></tbody></table>

При этом владелец забаненного чата не сможет писать и от имени других своих чатов до тех пор, пока не будет разбанен

### <mark style="background-color:blue;">**Как разбанить группу Telegram**</mark>

**tg\_unban\_chat\_sender\_chat(platform\_id, sender\_chat\_id)**

Параметры:

<table><thead><tr><th width="294.828125">Параметр</th><th>Описание</th></tr></thead><tbody><tr><td> <mark style="color:red;"><strong>!</strong></mark><strong> platform_id</strong> </td><td>идентификатор чата внутри Telegram <a href="funkcii-raboty-v-chatakh-i-kanalakh-telegram.md#gde-vzyat-platform_id-dlya-otpravki-uvedomlenii"><strong>*</strong></a><strong>,</strong> в котором разбаниваем </td></tr><tr><td><mark style="color:red;"><strong>!</strong></mark><strong> sender_chat_id</strong></td><td>идентификатор чата, который разбаниваем</td></tr></tbody></table>

## Как работать с ссылками на чат/канал **Telegram**

### <mark style="background-color:blue;">**Как создать ссылку на вступление в чат в Telegram**</mark>

**tg\_create\_chat\_invite\_link(platform\_id, member\_limit, hours, request, name)**&#x20;

Параметры:

<table><thead><tr><th width="282.87109375">Параметр</th><th>Описание</th></tr></thead><tbody><tr><td><mark style="color:red;"><strong>!</strong></mark><strong> platform_id</strong></td><td>идентификатор чата в Telegram <a href="funkcii-raboty-v-chatakh-i-kanalakh-telegram.md#gde-vzyat-platform_id-dlya-otpravki-uvedomlenii"><strong>*</strong></a> </td></tr><tr><td><strong>member_limit</strong></td><td>лимит на количество участников</td></tr><tr><td><strong>hours</strong></td><td>количество часов, которое будет действовать ссылка</td></tr><tr><td><strong>request</strong></td><td>признак того, что при переходе по ссылке должен формироваться запрос на вступление чат</td></tr><tr><td><strong>name</strong> </td><td>название ссылки</td></tr></tbody></table>

{% hint style="info" %}
При передаче параметра **member\_limit** значение параметра **request** автоматически заменится на **False**. Если же нужно принимать заявки на вступление, то параметр **member\_limit** оставляем пустым.
{% endhint %}

**Создание ссылки на вступление в чат:**

<figure><img src="../../../../.gitbook/assets/image (84) (1) (1).png" alt=""><figcaption></figcaption></figure>

### <mark style="background-color:blue;">**Как удалить ссылку на вступление в чат в Telegram**</mark>

**tg\_revoke\_chat\_invite\_link(platform\_id, invite\_link)**

Параметры:

<table><thead><tr><th width="294.828125">Параметр</th><th>Описание</th></tr></thead><tbody><tr><td> <mark style="color:red;"><strong>!</strong></mark><strong> platform_id</strong> </td><td>идентификатор чата внутри Telegram <a href="funkcii-raboty-v-chatakh-i-kanalakh-telegram.md#gde-vzyat-platform_id-dlya-otpravki-uvedomlenii"><strong>*</strong></a></td></tr><tr><td> <mark style="color:red;"><strong>!</strong></mark><strong> invite_link</strong></td><td>ссылка, которую надо удалить</td></tr></tbody></table>

### <mark style="background-color:blue;">**Как сделать неактивными все существующие ссылки и заменить их на одну**</mark>

{% hint style="warning" %}
Использовать с осторожностью. Все существующие ссылки для входа в вашу группу станут неактивными.
{% endhint %}

&#x20;**tg\_export\_chat\_link(platform\_id)**

Параметры:

<table><thead><tr><th width="294.828125">Параметр</th><th>Описание</th></tr></thead><tbody><tr><td> <mark style="color:red;"><strong>!</strong></mark><strong> platform_id</strong> </td><td>идентификатор чата внутри Telegram <a href="funkcii-raboty-v-chatakh-i-kanalakh-telegram.md#gde-vzyat-platform_id-dlya-otpravki-uvedomlenii"><strong>*</strong></a></td></tr><tr><td> <mark style="color:red;"><strong>!</strong></mark><strong> invite_link</strong></td><td>ссылка, которую надо удалить</td></tr></tbody></table>

Результат - ссылка, которая будет единственным способом попасть в группу до тех пор, пока не будут созданы дополнительные ссылки прочими способами.

## Как работать с заявками в чат/канал **Telegram**

### <mark style="background-color:blue;">**Как принять заявку и добавить пользователя в канал/чат в Telegram**</mark>

**tg\_approve\_chat\_join\_request(chat\_id, user\_id)**

Параметры:

<table><thead><tr><th width="279.9765625"></th><th></th></tr></thead><tbody><tr><td><mark style="color:red;"><strong>!</strong></mark><strong> chat_id</strong></td><td>идентификатор группы/канала внутри Telegram <a href="funkcii-raboty-v-chatakh-i-kanalakh-telegram.md#gde-vzyat-platform_id-dlya-otpravki-uvedomlenii"><strong>*</strong></a> </td></tr><tr><td><mark style="color:red;"><strong>!</strong></mark><strong> user_id</strong></td><td>идентификатор пользователя внутри Telegram <a href="funkcii-raboty-v-chatakh-i-kanalakh-telegram.md#gde-vzyat-platform_id-dlya-otpravki-uvedomlenii"><strong>*</strong></a> </td></tr></tbody></table>

Прием заявки:

<figure><img src="../../../../.gitbook/assets/image (132) (1) (1).png" alt=""><figcaption></figcaption></figure>

### <mark style="background-color:blue;">**Как отклонить заявку в канал/чат**</mark> <mark style="background-color:blue;">**в Telegram**</mark>

**tg\_decline\_chat\_join\_request(chat\_id, user\_id)**&#x20;

Параметры:

<table><thead><tr><th width="279.9765625"></th><th></th></tr></thead><tbody><tr><td><mark style="color:red;"><strong>!</strong></mark><strong> chat_id</strong></td><td>идентификатор группы/канала внутри Telegram <a href="funkcii-raboty-v-chatakh-i-kanalakh-telegram.md#gde-vzyat-platform_id-dlya-otpravki-uvedomlenii"><strong>*</strong></a> </td></tr><tr><td><mark style="color:red;"><strong>!</strong></mark><strong> user_id</strong></td><td>идентификатор пользователя внутри Telegram <a href="funkcii-raboty-v-chatakh-i-kanalakh-telegram.md#gde-vzyat-platform_id-dlya-otpravki-uvedomlenii"><strong>*</strong></a> </td></tr></tbody></table>

Отклонение заявки

<figure><img src="../../../../.gitbook/assets/image (133) (1).png" alt=""><figcaption></figcaption></figure>

## Как работать с подписчиками чата/канала **Telegram**

### <mark style="background-color:blue;">**Как заблокировать пользователя в Telegram**</mark>

**tg\_ban\_chat\_member(chat\_id, user\_id, hours)**&#x20;

Параметры:

<table><thead><tr><th width="283.67578125">Параметр</th><th>Описание</th></tr></thead><tbody><tr><td><mark style="color:red;"><strong>!</strong></mark><strong> chat_id</strong></td><td>идентификатор чата внутри Telegram <a href="funkcii-raboty-v-chatakh-i-kanalakh-telegram.md#gde-vzyat-platform_id-dlya-otpravki-uvedomlenii"><strong>*</strong></a> </td></tr><tr><td><mark style="color:red;"><strong>!</strong></mark><strong> user_id</strong></td><td>идентификатор пользователя внутри Telegram <a href="funkcii-raboty-v-chatakh-i-kanalakh-telegram.md#gde-vzyat-platform_id-dlya-otpravki-uvedomlenii"><strong>*</strong></a> для блокировки</td></tr><tr><td><strong>hours</strong></td><td>длительность блокировки в часах. По умолчанию блокировка навечно. При указании длительности блокировки свыше 366 дней блокировка будет установлена навечно</td></tr></tbody></table>

### <mark style="background-color:blue;">**Как разблокировать пользователя в Telegram**</mark>

**tg\_unban\_chat\_member(chat\_id, user\_id)** &#x20;

Параметры:

<table><thead><tr><th width="283.67578125">Параметр</th><th>Описание</th></tr></thead><tbody><tr><td><mark style="color:red;"><strong>!</strong></mark><strong> chat_id</strong></td><td>идентификатор чата внутри Telegram <a href="funkcii-raboty-v-chatakh-i-kanalakh-telegram.md#gde-vzyat-platform_id-dlya-otpravki-uvedomlenii"><strong>*</strong></a> </td></tr><tr><td><mark style="color:red;"><strong>!</strong></mark><strong> user_id</strong></td><td>идентификатор пользователя внутри Telegram <a href="funkcii-raboty-v-chatakh-i-kanalakh-telegram.md#gde-vzyat-platform_id-dlya-otpravki-uvedomlenii"><strong>*</strong></a><strong>,</strong> которого необходимо разблокировать</td></tr></tbody></table>

### <mark style="background-color:blue;">**Как проверить наличие подписки в Telegram**</mark>

**tg\_get\_chat\_member(chat\_id, user\_id)**&#x20;

Параметры:

<table><thead><tr><th width="283.67578125">Параметр</th><th>Описание</th></tr></thead><tbody><tr><td><mark style="color:red;"><strong>!</strong></mark><strong> chat_id</strong></td><td>идентификатор чата внутри Telegram <a href="funkcii-raboty-v-chatakh-i-kanalakh-telegram.md#gde-vzyat-platform_id-dlya-otpravki-uvedomlenii"><strong>*</strong></a> </td></tr><tr><td><mark style="color:red;"><strong>!</strong></mark><strong> user_id</strong></td><td>идентификатор пользователя внутри Telegram <a href="funkcii-raboty-v-chatakh-i-kanalakh-telegram.md#gde-vzyat-platform_id-dlya-otpravki-uvedomlenii"><strong>*</strong></a><strong>,</strong> подписку которого проверяем</td></tr></tbody></table>

### <mark style="background-color:blue;">**Как определить число участников в канале/чате**</mark>

**tg\_get\_chat\_member\_count(platform\_id)**

Параметры:

<table><thead><tr><th width="283.67578125">Параметр</th><th>Описание</th></tr></thead><tbody><tr><td><mark style="color:red;"><strong>!</strong></mark><strong> platform_id</strong></td><td>идентификатор чата в Telegram <a href="funkcii-raboty-v-chatakh-i-kanalakh-telegram.md#gde-vzyat-platform_id-dlya-otpravki-uvedomlenii"><strong>*</strong></a></td></tr></tbody></table>

### <mark style="background-color:blue;">**Как проверить, состоит ли участник чата в определенном списке**</mark>

**some\_client\_in\_list(list\_id, recepient)**

Параметры:

<table><thead><tr><th width="283.67578125">Параметр</th><th>Описание</th></tr></thead><tbody><tr><td><mark style="color:red;"><strong>!</strong></mark><strong> list_id</strong></td><td>номер списка</td></tr><tr><td><mark style="color:red;"><strong>!</strong></mark><strong> recepient</strong></td><td>идентификатор пользователя внутри Telegram <a href="funkcii-raboty-v-chatakh-i-kanalakh-telegram.md#gde-vzyat-platform_id-dlya-otpravki-uvedomlenii"><strong>*</strong></a>. Для клиентов чата данное значение в переменной chat_member_id.</td></tr></tbody></table>

{% embed url="https://www.youtube.com/watch?v=PajSl8clgVk" %}
Проверка подписки на канал Телеграм
{% endembed %}

## Как показать действия в чате/канале **Telegram**

### <mark style="background-color:blue;">**Как показать пользователю действия бота (печатает/выбирает стикер и т.д)**</mark>

**tg\_send\_chat\_action(platform\_id, bot\_action,  message\_thread\_id)**

<mark style="background-color:green;">**! Работает с бизнес-аккаунтом в Телеграм**</mark>

Параметры:

<table><thead><tr><th width="286.74609375">Параметр</th><th>Описание</th></tr></thead><tbody><tr><td><mark style="color:red;"><strong>!</strong></mark><strong> platform_id</strong></td><td>идентификатор чата в Telegram <a href="funkcii-raboty-v-chatakh-i-kanalakh-telegram.md#gde-vzyat-platform_id-dlya-otpravki-uvedomlenii"><strong>*</strong></a>  </td></tr><tr><td><mark style="color:red;"><strong>!</strong></mark><strong> bot_action</strong></td><td>действие бота из списка.</td></tr><tr><td><strong>message_thread_id</strong> </td><td>идентификатор темы (доступно для супергрупп при наличии функционала форума).</td></tr></tbody></table>

<details>

<summary><mark style="color:orange;">Список возможных действий <strong>bot_action</strong></mark></summary>

_**typing**_ для текстовых сообщений, \
&#xNAN;_**upload\_photo**_ для фотографий, \
&#xNAN;_**record\_video**_ или _**upload\_video**_ для видео , \
&#xNAN;_**record\_voice**_ или _**upload\_voice**_ для голосовых заметок, \
&#xNAN;_**upload\_document**_ для общих файлов, \
&#xNAN;_**choose\_sticker**_ для стикеров, \
&#xNAN;_**find\_location**_ для данных о местоположении, \
&#xNAN;_**record\_video\_note**_ или _**upload\_video\_note**_ для видеозаметки.&#x20;

</details>

{% hint style="info" %}
Данное уведомление будет отображаться, пока не будет получен  какой-либо ответ от бота, но не более 5 секунд.
{% endhint %}

### <mark style="background-color:blue;">**Как показывать пользователю Alert-уведомления**</mark>

**tg\_answer\_callback\_query(callback\_query\_id, text,show\_alert,cache\_time)**&#x20;

<table><thead><tr><th width="309.5234375">Параметр</th><th>Описание</th></tr></thead><tbody><tr><td><mark style="color:red;"><strong>!</strong></mark><strong> callback_query_id</strong> <strong>(обязательный)</strong></td><td>данный идентификатор позволяет определить нажавшего кнопку и продемонстрировать ему Alert-уведомление</td></tr><tr><td><mark style="color:red;"><strong>!</strong></mark><strong> text (обязательный)</strong> </td><td>текст Alert-уведомления.</td></tr><tr><td><strong>show_alert</strong></td><td>признак исчезающего уведомления (False - исчезающее уведомление (подсказка), True - уведомление в окне)</td></tr><tr><td><strong>cache_time</strong></td><td>Максимальное количество времени в секундах, в течение которого результат запроса обратного вызова может быть кэширован на стороне клиента. Приложения Telegram будут поддерживать кэширование, начиная с версии 3.14. Значение по умолчанию равно 0</td></tr></tbody></table>

<details>

<summary>Пример</summary>

Alert-уведомления показываются только в результате нажатия на callback-кнопку в телеграмме.&#x20;

Для примера используем следующие кнопки:

\[{"line":0,"index\_in\_line":0,"text":"111","type":"inline","callback":"первая"}, {"line":1,"index\_in\_line":0,"text":"222","type":"inline","callback":"вторая"}, {"line":2,"index\_in\_line":0,"text":"333","type":"inline","callback":"третья"}]&#x20;

<figure><img src="../../../../.gitbook/assets/Снимок экрана 2025-05-06 в 14.34.18.png" alt="" width="563"><figcaption></figcaption></figure>

После нажатия на такую кнопку приходит callback с текстом, содержащимся в соответствующем поле. При нажатии на кнопку “111” придет callback с текстом “первая”.

<figure><img src="../../../../.gitbook/assets/Снимок экрана 2025-05-06 в 14.35.43.png" alt="" width="563"><figcaption></figcaption></figure>

Создадим блок с первостепенной проверкой условия и в условие пишем желаемый текст. В нашем случае “первая”:

<figure><img src="../../../../.gitbook/assets/Снимок экрана 2025-05-06 в 14.37.43.png" alt="" width="563"><figcaption></figcaption></figure>

Если в поле **Выбор соответствия** выбрать **Игнорируя ошибки и неточности**, то в дальнейшем можно будет такой блок использовать для всех вариантов, которые отличаются на 1-2 символа. Например, благодарить за поставленную такой кнопкой оценку работы.&#x20;

Далее в калькуляторе используйте функцию **tg\_answer\_callback\_query** и в нее поместите такие параметры: \
**callback\_query\_id** - данный id позволяет идентифицировать нажавшего кнопку и продемонстрировать ему Alert-уведомление, \
**text** - текст Alert-уведомления.

<figure><img src="../../../../.gitbook/assets/Снимок экрана 2025-05-06 в 14.40.00.png" alt="" width="563"><figcaption></figcaption></figure>

Пример кода для копирования:

`tg_answer_callback_query('#{callback_query_id}', "Вы нажали кнопку 111")`

{% hint style="warning" %}
Важно! Параметр callback\_query\_id нужно передавать так, как показано в примере, т.е. в '#{}'
{% endhint %}

Если все подготовлено правильно, то результатом нажатия на кнопку будет Alert-уведомление с заданным текстом. В мобильной версии имя бота будет как заголовок над текстом.

<figure><img src="../../../../.gitbook/assets/Снимок экрана 2025-05-06 в 14.41.07.png" alt="" width="563"><figcaption></figcaption></figure>

Если же вы хотите показать простое всплывающее сообщение, то передайте третьим параметром False, как в примере ниже: \
tg\_answer\_callback\_query('#{callback\_query\_id}', "Вы нажали кнопку 222", False)

<figure><img src="../../../../.gitbook/assets/Снимок экрана 2025-05-06 в 14.43.18.png" alt="" width="375"><figcaption><p>В случае нажатия на кнопку при таких <br>параметрах на несколько секунд появится <br>уведомление такого вида. </p></figcaption></figure>

</details>

### <mark style="background-color:blue;">**Как в реакции на callback-кнопку добавить переход в бота с тэгом**</mark>

**tg\_callback\_url\_open(callback\_query\_id, url, cache\_time)**

Параметры:

<table><thead><tr><th width="309.5234375">Параметр</th><th>Описание</th></tr></thead><tbody><tr><td><mark style="color:red;"><strong>!</strong></mark><strong> callback_query_id</strong></td><td>данный идентификатор позволяет определить нажавшего кнопку и продемонстрировать ему Alert-уведомление</td></tr><tr><td><mark style="color:red;"><strong>!</strong></mark><strong> url</strong> </td><td>URL-адрес, указывающий бота и параметр (выглядит так: t.me/your_bot?start=XXXX, вместо your_bot - имя бота)</td></tr><tr><td><strong>cache_time</strong></td><td>Максимальное количество времени в секундах, в течение которого результат запроса обратного вызова может быть кэширован на стороне клиента. Приложения Telegram будут поддерживать кэширование, начиная с версии 3.14. Значение по умолчанию равно 0</td></tr></tbody></table>

<details>

<summary>Пример</summary>

В реакции на callback-кнопку можно добавить переход в бота с тегом tg\_callback\_url\_open('#{callback\_query\_id}', 't.me/bot\_name?start=XXXX')

Для примера используем следующие кнопки:

\[{"line":0,"index\_in\_line":0,"text":"111","type":"inline","callback":"первая"}, {"line":1,"index\_in\_line":0,"text":"222","type":"inline","callback":"вторая"}, {"line":2,"index\_in\_line":0,"text":"333","type":"inline","callback":"третья"}]&#x20;

<figure><img src="../../../../.gitbook/assets/Снимок экрана 2025-05-06 в 14.34.18.png" alt="" width="563"><figcaption></figcaption></figure>

После нажатия на такую кнопку приходит callback с текстом, содержащимся в соответствующем поле. При нажатии на кнопку “111” придет callback с текстом “первая”.

<figure><img src="../../../../.gitbook/assets/Снимок экрана 2025-05-06 в 14.35.43.png" alt="" width="563"><figcaption></figcaption></figure>

Создадим блок с первостепенной проверкой условия и в условие пишем желаемый текст. В нашем случае “первая”:

<figure><img src="../../../../.gitbook/assets/Снимок экрана 2025-05-06 в 14.37.43.png" alt="" width="563"><figcaption></figcaption></figure>

Если в поле **Выбор соответствия** выбрать **Игнорируя ошибки и неточности**, то в дальнейшем можно будет такой блок использовать для всех вариантов, которые отличаются на 1-2 символа. Например, благодарить за поставленную такой кнопкой оценку работы.

Далее в калькуляторе блока укажем tg\_callback\_url\_open('#{callback\_query\_id}', 't.me/bot\_name?start=XXXX'):

<figure><img src="../../../../.gitbook/assets/Снимок экрана 2025-05-06 в 15.08.46.png" alt=""><figcaption></figcaption></figure>

</details>

## Как настроить права  в чате/канале **Telegram**

### <mark style="background-color:blue;">**Как повысить пользователя до администратора в супергруппе или канале в Telegram**</mark>

**tg\_promote\_user(platform\_id, user\_id, promote\_options\_list)**

Параметры:

<table><thead><tr><th width="269.9765625">Параметр</th><th width="515.17578125">Описание</th></tr></thead><tbody><tr><td><mark style="color:red;"><strong>!</strong></mark><strong> platform_id</strong></td><td>идентификатор супергруппы или, если используете в канале, имя канала вида @channelusername, внутри Telegram <a href="funkcii-raboty-v-chatakh-i-kanalakh-telegram.md#gde-vzyat-platform_id-dlya-otpravki-uvedomlenii"><strong>*</strong></a></td></tr><tr><td><mark style="color:red;"><strong>!</strong></mark><strong> user_id</strong></td><td>идентификатор пользователя внутри Telegram <a href="funkcii-raboty-v-chatakh-i-kanalakh-telegram.md#gde-vzyat-platform_id-dlya-otpravki-uvedomlenii"><strong>*</strong></a> </td></tr><tr><td><mark style="color:red;"><strong>!</strong></mark><strong> promote_options_list</strong></td><td>список прав, которые нужно включить. </td></tr></tbody></table>

<details>

<summary><mark style="color:red;"><strong>Списки прав обязательного параметра promote_options_list</strong></mark></summary>

В списке прав **promote\_options\_list** можно указать следующие права:

1. **is\_anonymous** — присутствие администратора в чате скрыто,&#x20;
2. **can\_manage\_chat** — администратор может получить доступ к журналу событий чата, статистике чата, статистике сообщений в каналах, видеть участников канала, видеть анонимных администраторов в супер-группах и игнорировать медленный режим. Этот уровень прав выдается по умолчанию, в случае указания любой из последующих привилегий.&#x20;
3. **can\_post\_messages** — администратор может создавать сообщения канала, <mark style="color:red;">только для каналов</mark>&#x20;
4. **can\_edit\_messages** — администратор может редактировать сообщения других пользователей и может закреплять сообщения, <mark style="color:red;">только для каналов</mark>
5. **can\_delete\_messages** — администратор может удалять сообщения других пользователей
6. **can\_manage\_video\_chats** — администратор может управлять видеочатами,
7. **can\_restrict\_members** — администратор может ограничивать, ставить/отменять бан участникам чата,&#x20;
8. **can\_promote\_members** — администратор может добавлять новых администраторов с подмножеством их собственных привилегий или понижать в должности администраторов, которых он повысил, прямо или косвенно (повысили администраторы, которые были им назначены)
9. **can\_change\_info** — администратор может изменить название чата, фото и другие настройки&#x20;
10. **can\_invite\_users** — администратор может приглашать новых пользователей в чат
11. **can\_pin\_messages** — администратор может закреплять сообщения, <mark style="color:red;">только для супергруппы</mark>.

</details>

<details>

<summary>Пример</summary>

Разберем пример как повысить пользователя до администратора в супергруппе:

<figure><img src="../../../../.gitbook/assets/image (134) (1).png" alt=""><figcaption></figcaption></figure>

В данном примере помимо перечисленных прав будут по умолчанию выданы права can\_manage\_chat.

<figure><img src="../../../../.gitbook/assets/image (135) (1).png" alt=""><figcaption><p>Назначение прав пользователю</p></figcaption></figure>

<figure><img src="../../../../.gitbook/assets/image (136) (1).png" alt=""><figcaption><p>Установка титула администратору</p></figcaption></figure>

Пример кода для копирования

<pre data-full-width="false"><code><strong>Пример 1. 
</strong><strong>promote_options_list = ‘[“can_promote_members”,”can_change_info”,”can_invite_users”]’ 
</strong>tg_promote_user(platform_id, user_id, promote_options_list)

Пример 2. 
promote_options_list = '["can_manage_chat","can_post_messages","can_edit_messages","can_delete_messages","can_manage_video_chats","can_promote_members","can_restrict_members","can_invite_users","can_pin_messages"]' 
result=tg_promote_user(platform_id, reply_from, promote_options_list)  
</code></pre>

</details>

### <mark style="background-color:blue;">**Как изменить титул администратора с помощью бота в Telegram**</mark>

**tg\_set\_administrator\_title(platform\_id, user\_id, title)** &#x20;

Параметры:&#x20;

<table><thead><tr><th width="303.94921875">Параметр</th><th>Описание</th></tr></thead><tbody><tr><td><mark style="color:red;"><strong>!</strong></mark><strong> platform_id</strong></td><td>идентификатор супергруппы внутри Telegram <a href="funkcii-raboty-v-chatakh-i-kanalakh-telegram.md#gde-vzyat-platform_id-dlya-otpravki-uvedomlenii"><strong>*</strong></a> </td></tr><tr><td><mark style="color:red;"><strong>!</strong></mark><strong> user_id</strong></td><td>идентификатор пользователя внутри Telegram <a href="funkcii-raboty-v-chatakh-i-kanalakh-telegram.md#gde-vzyat-platform_id-dlya-otpravki-uvedomlenii"><strong>*</strong></a>  </td></tr><tr><td><mark style="color:red;"><strong>!</strong></mark><strong> title</strong></td><td>титул администратора. <br>Для титула есть следующие ограничения: 0-16 символов, эмодзи не разрешены.</td></tr></tbody></table>

{% hint style="warning" %}
ВАЖНО!&#x20;

Работает только на пользователях, которых администраторами супергруппы назначил бот
{% endhint %}

Пример кода для копирования:

```
result=tg_set_administrator_title(platform_id, reply_from, "огоньтитул")
```

### <mark style="background-color:blue;">**Ограничения для пользователей**</mark>

#### <mark style="background-color:blue;">**Общие ограничения для обычных пользователей чата или для отдельных пользователей  Telegram**</mark>

**tg\_chat\_permission(platform\_id, permission, media\_permissions)**

Параметры:

<table><thead><tr><th width="318.76171875">Параметр</th><th>Описание</th></tr></thead><tbody><tr><td><mark style="color:red;"><strong>!</strong></mark><strong> platform_id</strong></td><td>идентификатор чата внутри Telegram <a href="funkcii-raboty-v-chatakh-i-kanalakh-telegram.md#gde-vzyat-platform_id-dlya-otpravki-uvedomlenii"><strong>*</strong></a> </td></tr><tr><td><mark style="color:red;"><strong>!</strong></mark><strong> permission</strong></td><td>массив значений для списка ограничений, приведенного ниже. <br>В массиве значение 1 разрешает действие, а 0 - запрещает. <br>Порядковый номер соответствует позиции в массиве</td></tr><tr><td><mark style="color:red;"><strong>!</strong></mark><strong> media_permissions</strong></td><td>список значений прав для работы с медиа (подробнее ниже). <br>В списке значение 1 разрешает действие, а 0 запрещает. Порядковый номер соответствует позиции в списке. </td></tr></tbody></table>

<details>

<summary><strong>Список ограничений для обязательного параметра </strong><mark style="color:red;"><strong>permission</strong></mark></summary>

Список ограничений **permission:**\
1\. <mark style="color:red;">**!**</mark>**&#x20;can\_send\_messages** - разрешение отправлять текстовые сообщения, контакты, местоположения и места проведения\
2\. <mark style="color:red;">**!**</mark>**&#x20;can\_send\_media\_messages** - разрешение отправлять аудио, документы, фотографии, видео, видеозаметки и голосовые заметки, подразумевается наличие разрешения **can\_send\_messages**\
3\. <mark style="color:red;">**!**</mark>**&#x20;can\_send\_polls** - разрешение отправлять опросы, подразумевается наличие разрешения **can\_send\_messages**\
4\. <mark style="color:red;">**!**</mark>**&#x20;can\_send\_other\_messages** - разрешение отправлять анимацию, игры, стикеры и использовать встроенных ботов, подразумевается наличие разрешения **can\_send\_media\_messages**\
5\. <mark style="color:red;">**!**</mark>**&#x20;can\_add\_web\_page\_previews** - разрешение добавлять превью веб-страницы к своим сообщениям, подразумевается наличие разрешения **can\_send\_media\_messages**\
6\. <mark style="color:red;">**!**</mark>**&#x20;can\_change\_info** - разрешение изменять название чата, фото и другие настройки. Игнорируется в публичных супергруппах\
7\. <mark style="color:red;">**!**</mark>**&#x20;can\_invite\_users** - разрешение приглашать пользователей\
8\. <mark style="color:red;">**!**</mark>**&#x20;can\_pin\_messages** - разрешение закреплять сообщения. Игнорируется в публичных супергруппах\
9\. **can\_manage\_topics** - разрешение создавать темы в группах-форумах. Если пытаться применить в группах неподходящего типа, то функция  не сработает и вернет ошибку.&#x20;

</details>

<details>

<summary><strong>Список значений для обязательного параметра </strong><mark style="color:red;"><strong>media_permissions</strong></mark></summary>

#### **Список значений для выдачи прав по работе с медиа media\_permissions:**&#x20;

1\. **can\_send\_audios** - разрешение отправлять аудиофайлы\
2\. **can\_send\_documents** -разрешение отправлять документы\
3\. **can\_send\_photos** - разрешение отправлять фото\
4\. **can\_send\_videos**  - разрешение отправлять видео\
5\. **can\_send\_video\_notes** - разрешение отправлять круглое видео\
6\. **can\_send\_voice\_notes** - разрешение отправлять голосовые сообщения

</details>

#### <mark style="background-color:blue;">**Персональные ограничения для обычных пользователей чата или для отдельных пользователей  Telegram**</mark>

**tg\_restrict\_chat\_member(platform\_id, user\_id, minutes, permission, media\_permissions).**

Параметры:

| Параметр                                                    | Описание                                                                                                                                                                                                                    |
| ----------------------------------------------------------- | --------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| <mark style="color:red;">**!**</mark>**&#x20;platform\_id** | идентификатор чата внутри Telegram [**\***](funkcii-raboty-v-chatakh-i-kanalakh-telegram.md#gde-vzyat-platform_id-dlya-otpravki-uvedomlenii)                                                                                |
| <mark style="color:red;">**!**</mark>**&#x20;user\_id**     | идентификатор пользователя внутри Telegram [**\***](funkcii-raboty-v-chatakh-i-kanalakh-telegram.md#gde-vzyat-platform_id-dlya-otpravki-uvedomlenii)                                                                        |
| **minutes**                                                 | кол-во минут, в течении которого будет действовать ограничение (если не указать явно, по умолчанию будет применено значение 3600, что соответствует 60 часам, а если указать 0, то ограничения будут действовать бессрочно) |
| **permission**                                              | массив значений [для списка ограничений](funkcii-raboty-v-chatakh-i-kanalakh-telegram.md#spisok-ogranichenii-permission)                                                                                                    |
| **media\_permissions**                                      | список значений для выдачи прав по работе с медиа                                                                                                                                                                           |

<details>

<summary><strong>Список ограничений для параметра </strong><mark style="color:red;"><strong>permission</strong></mark></summary>

Список ограничений **permission:**\
1\. <mark style="color:red;">**!**</mark>**&#x20;can\_send\_messages** - разрешение отправлять текстовые сообщения, контакты, местоположения и места проведения\
2\. <mark style="color:red;">**!**</mark>**&#x20;can\_send\_media\_messages** - разрешение отправлять аудио, документы, фотографии, видео, видеозаметки и голосовые заметки, подразумевается наличие разрешения **can\_send\_messages**\
3\. <mark style="color:red;">**!**</mark>**&#x20;can\_send\_polls** - разрешение отправлять опросы, подразумевается наличие разрешения **can\_send\_messages**\
4\. <mark style="color:red;">**!**</mark>**&#x20;can\_send\_other\_messages** - разрешение отправлять анимацию, игры, стикеры и использовать встроенных ботов, подразумевается наличие разрешения **can\_send\_media\_messages**\
5\. <mark style="color:red;">**!**</mark>**&#x20;can\_add\_web\_page\_previews** - разрешение добавлять превью веб-страницы к своим сообщениям, подразумевается наличие разрешения **can\_send\_media\_messages**\
6\. <mark style="color:red;">**!**</mark>**&#x20;can\_change\_info** - разрешение изменять название чата, фото и другие настройки. Игнорируется в публичных супергруппах\
7\. <mark style="color:red;">**!**</mark>**&#x20;can\_invite\_users** - разрешение приглашать пользователей\
8\. <mark style="color:red;">**!**</mark>**&#x20;can\_pin\_messages** - разрешение закреплять сообщения. Игнорируется в публичных супергруппах\
9\. **can\_manage\_topics** - разрешение создавать темы в группах-форумах. Если пытаться применить в группах неподходящего типа, то функция  не сработает и вернет ошибку.&#x20;

</details>

<details>

<summary><strong>Список значений для параметра </strong><mark style="color:red;"><strong>media_permissions</strong></mark></summary>

#### **Список значений для выдачи прав по работе с медиа media\_permissions:**&#x20;

1\. **can\_send\_audios** - разрешение отправлять аудиофайлы\
2\. **can\_send\_documents** -разрешение отправлять документы\
3\. **can\_send\_photos** - разрешение отправлять фото\
4\. **can\_send\_videos**  - разрешение отправлять видео\
5\. **can\_send\_video\_notes** - разрешение отправлять круглое видео\
6\. **can\_send\_voice\_notes** - разрешение отправлять голосовые сообщения

</details>

<details>

<summary>Пример</summary>

Пример применения функции, в котором пользователю запретили все на 3 минуты:

<figure><img src="../../../../.gitbook/assets/image (137) (1).png" alt=""><figcaption></figcaption></figure>

При входе в чат пользователю будет показано уведомление о невозможности писать в чат и если ограничение по времени было выставлено, то он увидит срок действия данного ограничения.



<figure><img src="../../../../.gitbook/assets/image (138) (1).png" alt=""><figcaption></figcaption></figure>

Код для копирования:

```
permission = [0, 0, 0, 0, 0, 0, 0, 0] 
tg_restrict_chat_member(-1001607137668, 473737685, 3, permission)
```

</details>

## Как работать с сообщениями в чате/канале **Telegram**

### <mark style="background-color:blue;">**Как закрепить сообщение**</mark>

**tg\_pin\_chat\_message(platform\_id, message\_id, disable\_notification)**&#x20;

Параметры:

<table><thead><tr><th width="311.3359375">Параметр</th><th>Описание</th></tr></thead><tbody><tr><td><mark style="color:red;"><strong>!</strong></mark><strong> platform_id</strong></td><td>идентификатор чата внутри Telegram <a href="funkcii-raboty-v-chatakh-i-kanalakh-telegram.md#gde-vzyat-platform_id-dlya-otpravki-uvedomlenii"><strong>*</strong></a></td></tr><tr><td><strong>message_id</strong></td><td>идентификатор сообщения, которое нужно закрепить</td></tr><tr><td><strong>disable_notification</strong></td><td>параметр определяет нужно ли отправлять уведомление всем участникам чата о новом закрепленном сообщении (уведомления всегда отключены в каналах и приватных чатах).<br>Если не нужно отправлять уведомления, то в качестве значения параметра <strong>disable_notification</strong> передайте 1, иначе - 0.</td></tr></tbody></table>

### <mark style="background-color:blue;">**Как открепить сообщение**</mark>

**tg\_unpin\_chat\_message(platform\_id, message\_id)**&#x20;

Параметры:

<table><thead><tr><th width="311.3359375">Параметр</th><th>Описание</th></tr></thead><tbody><tr><td><mark style="color:red;"><strong>!</strong></mark><strong> platform_id</strong></td><td>идентификатор чата внутри Telegram <a href="funkcii-raboty-v-chatakh-i-kanalakh-telegram.md#gde-vzyat-platform_id-dlya-otpravki-uvedomlenii"><strong>*</strong></a></td></tr><tr><td><strong>message_id</strong></td><td>идентификатор сообщения, которое нужно открепить. Если <strong>message_id</strong> не указан, то будет откреплено самое последнее (по дате отправки) закрепленное сообщение.</td></tr></tbody></table>

### <mark style="background-color:blue;">**Как открепить все закрепленные сообщения**</mark>

**tg\_unpin\_all(platform\_id)**

Параметры:

<table><thead><tr><th width="311.3359375">Параметр</th><th>Описание</th></tr></thead><tbody><tr><td><mark style="color:red;"><strong>!</strong></mark><strong> platform_id</strong></td><td>идентификатор чата внутри Telegram <a href="funkcii-raboty-v-chatakh-i-kanalakh-telegram.md#gde-vzyat-platform_id-dlya-otpravki-uvedomlenii"><strong>*</strong></a></td></tr></tbody></table>

{% hint style="warning" %}
ВНИМАНИЕ!

В Telegram существует ограничение для функций закрепить/открепить сообщение.&#x20;

Сроки возможности использования функций **tg\_pin\_chat\_message / tg\_unpin\_chat\_message / tg\_unpin\_all ограничиваются&#x20;**<mark style="color:red;">**НЕ системой Сейлбота**</mark>**.**&#x20;

**Если срок обращения к сообщению для закрепления прошел, то функция хотя и вернет true, но для самого Телеграм настройки не будет применены.**

Также важно учитывать, что закрепленные сообщения могут сохраниться в кеше и визуально удалиться не сразу.&#x20;
{% endhint %}

## Как создать/закрыть опрос в чате/канале **Telegram**

### <mark style="background-color:blue;">**Как создать простой опрос в Telegram**</mark>

**tg\_send\_poll(platform\_id, question, options, is\_anonymous, allows\_multiple\_answers, reply\_markup, disable\_notification, protect\_content, token, reply\_to\_message\_id,  message\_thread\_id, business\_connection\_id)**

Параметры:

<table><thead><tr><th width="214.46875">Параметр</th><th>Описание</th></tr></thead><tbody><tr><td><mark style="color:red;"><strong>!</strong></mark><strong> platform_id</strong></td><td>идентификатор чата внутри Telegram <a href="funkcii-raboty-v-chatakh-i-kanalakh-telegram.md#gde-vzyat-platform_id-dlya-otpravki-uvedomlenii"><strong>*</strong></a> </td></tr><tr><td><mark style="color:red;"><strong>!</strong></mark><strong> question</strong> </td><td>вопрос </td></tr><tr><td><mark style="color:red;"><strong>!</strong></mark><strong> options</strong></td><td>массив вариантов ответов</td></tr><tr><td><strong>is_anonymous</strong></td><td>1 - анонимный опрос, '' - не анонимный </td></tr><tr><td><strong>allows_multiple_answers</strong></td><td>1 - возможны несколько ответов, '' - один ответ </td></tr><tr><td><strong>reply_markup</strong> </td><td>клавиатура или '' - без клавиатуры </td></tr><tr><td><strong>disable_notification</strong></td><td>признак отправки со звуковым уведомлением (по умолчанию 0)<br>1 - отключить уведомление при получении, 0 - передать с уведомлением</td></tr><tr><td><strong>protect_content</strong></td><td>1 защитить от копирования и скриншотов, '' - без защиты </td></tr><tr><td><strong>token</strong></td><td>токен бота, если не передан используется текущий</td></tr><tr><td><strong>reply_to_message_id</strong></td><td>идентификатор цитируемого сообщения</td></tr><tr><td><strong>message_thread_id</strong></td><td>идентификатор темы (доступно для супергрупп при наличии функционала форума)</td></tr><tr><td><strong>business_connection_id</strong></td><td>значение при подключении бота - Business ID - отображается в каналах. Следует передавать, если в параметрах передается токен бота и надо отправить через подключенный к боту пользовательский аккаунт</td></tr></tbody></table>

<details>

<summary>Важно учитывать!</summary>

Примечания

1\. Функция возвращает ответ от телеграма, в котором есть **message\_id**, его лучше сохранять, так как с его помощью можно будет завершить опрос функцией **tg\_stop\_poll** (описание ниже) и получить результат.

2\. Если опрос добавлен пользователем в канал, то в диалог придет колбек:&#x20;

**poll\_added** - неизменная часть \
**Вопрос** - текст вопроса из опроса

<figure><img src="../../../../.gitbook/assets/image (139) (1).png" alt=""><figcaption></figcaption></figure>

<figure><img src="../../../../.gitbook/assets/image (140) (1).png" alt=""><figcaption><p>Пример колбека при добавлении опроса в канал</p></figcaption></figure>

<figure><img src="../../../../.gitbook/assets/image (141) (1).png" alt=""><figcaption><p>Пример колбека при добавлении опроса в чат</p></figcaption></figure>

Второй колбек после poll\_added содержит цифры - это не что иное, как идентификатор  пользователя в Telegram, который добавил опрос.

{% hint style="warning" %}
**При создании опроса ботом колбек не приходит.**
{% endhint %}

&#x33;**.** В канале можно создавать только анонимные опросы

{% hint style="info" %}
**Внимание, рекомендуется отправлять в группу только анонимные опросы!**
{% endhint %}

4\. После создания опроса в переменную сохраните его идентификатор, чтобы понимать на какой опрос пришел колбек.

</details>

<details>

<summary>Пример в боте</summary>

В своей работе мы часто задаемся вопросами, на которые могли бы ответить наши клиенты. Опросы очень помогают получить обратную связь от клиентов и сделать определенные выводы.

Пример кода для копирования:

<pre><code><strong>/*Пример создания простого опроса*/
</strong>options = ["белый", "красный", "синий", "зеленый"] 
opros1=tg_send_poll(platform_id, 'Ваш любимый цвет?', options, 1, '', '', 1, '')
</code></pre>

<figure><img src="../../../../.gitbook/assets/image (142) (1).png" alt=""><figcaption><p>Функция создания опроса в Telegram</p></figcaption></figure>

<figure><img src="../../../../.gitbook/assets/image (143) (1).png" alt=""><figcaption><p>Созданный нами опрос в Telegram</p></figcaption></figure>

</details>

### <mark style="background-color:blue;">**Как создать викторину в Telegram**</mark>

**tg\_send\_quiz\_poll(platform\_id, question, options, explanation, correct\_option\_id, is\_anonymous, reply\_markup, parse\_mode, protect\_content, disable\_notification, token, reply\_to\_message\_id, message\_thread\_id )**

Параметры:

<table><thead><tr><th width="311.25">Параметр</th><th>Описание</th></tr></thead><tbody><tr><td><mark style="color:red;"><strong>!</strong></mark><strong> platform_id</strong> </td><td>идентификатор чата внутри Telegram <a href="funkcii-raboty-v-chatakh-i-kanalakh-telegram.md#gde-vzyat-platform_id-dlya-otpravki-uvedomlenii"><strong>*</strong></a> </td></tr><tr><td><mark style="color:red;"><strong>!</strong></mark><strong> question</strong> </td><td>вопрос </td></tr><tr><td><mark style="color:red;"><strong>!</strong></mark><strong> options</strong></td><td>массив вариантов ответов</td></tr><tr><td><mark style="color:red;"><strong>!</strong></mark><strong> explanation</strong></td><td>текст, который отображается, когда пользователь выбирает неправильный ответ или нажимает на значок лампы в опросе в стиле викторины, 0–200 символов с не более, чем двумя переводами строки после разбора сущностей. </td></tr><tr><td><mark style="color:red;"><strong>!</strong></mark><strong> correct_option_id</strong></td><td>номер правильного ответа, нумерация с 1</td></tr><tr><td><strong>is_anonymous</strong></td><td>1 - анонимный опрос, '' - неанонимный </td></tr><tr><td><strong>reply_markup</strong></td><td>клавиатура или '' - без клавиатуры </td></tr><tr><td><strong>parse_mode</strong></td><td>markdown или html для explanation или '' - без форматирования </td></tr><tr><td><strong>protect_content</strong></td><td>1 защитить от копирования и скриншотов, '' - без защиты</td></tr><tr><td><strong>disable_notification</strong></td><td>признак отправки со звуковым уведомлением (по умолчанию 0)<br>1 - отключить уведомление при получении, 0 - передать с уведомлением</td></tr><tr><td><strong>token</strong></td><td>токен бота, если не передан используется текущий</td></tr><tr><td><strong>reply_to_message_id</strong></td><td>ID цитируемого сообщения</td></tr><tr><td><strong>message_thread_id</strong></td><td>идентификатор темы (доступно для супергрупп при наличии функционала форума)</td></tr></tbody></table>

<details>

<summary><mark style="color:orange;">Важно учитывать!</mark></summary>

#### **Примечания**

1\. Функция возвращает ответ от Telegram, в котором есть **message\_id**, его лучше сохранять, так как с его помощью можно будет завершить викторину функцией **tg\_stop\_poll** (описание ниже) и получить результат.

2\. Если опрос добавлен пользователем в канал, то в диалог придет колбек: \
**poll\_added** - неизменная часть \
**Вопрос** - вопрос опроса

<figure><img src="../../../../.gitbook/assets/image (144) (1).png" alt=""><figcaption><p>Пример колбека в </p></figcaption></figure>

Если опрос создан в чате, то колбек дополнительно будет содержать  цифры - это идентификатор пользователя в Telegram, который добавил опрос.

<figure><img src="../../../../.gitbook/assets/image (145) (1).png" alt=""><figcaption></figcaption></figure>

{% hint style="warning" %}
При создании опроса ботом колбек не приходит.
{% endhint %}

3\. В канале можно создавать только анонимные викторины

4\. Если викторина была отправлена в диалог пользователя с ботом или в чат группы, то колбек о выбранном ответе придет в диалог бота с клиентом и будет иметь следующий вид:

Нумерация ответов начинается с 0. \
**poll\_answer 5325838371359031648** \
**\[3]**

**poll\_answer** - неизменяемая часть \
**5325838371359031648** - идентификатор викторины \
&#xNAN;**\[3]** - ответ

<figure><img src="../../../../.gitbook/assets/image (146) (1).png" alt=""><figcaption><p>Колбек на выбор ответа в Викторине </p></figcaption></figure>

5\. Если неанонимный опрос был создан в группе (неважно функцией или пользователем), в которой состоит в качестве администратора бот, то на каждый голос будет отправлен вебхук, при получении которого в диалог бота с клиентом будет отправлен колбек из пункта&#x20;

6\. Если клиент не контактировал с ботом, то отправить ему что-либо в ответ не получится, пока клиент не активирует бота.

{% hint style="info" %}
**Внимание рекомендуется отправлять в группу только анонимные викторины!**
{% endhint %}

7\. После создания викторины сохраните в переменную его идентификатор, чтобы понимать на какой опрос пришел колбек.

</details>

<details>

<summary>Пример в калькуляторе</summary>

Пример кода для копирования:

```
/*Пример создание Викторины*/
options = ["белый", "красный", "синий", "зеленый"] 
r = tg_send_quiz_poll(platform_id, 'Какого цвета крокодил?', options, 'Вот такое вот объяснение.', 4, '', '', '', '', 1)
```

Пример создания Викторины:

![](https://lh5.googleusercontent.com/-AJ26Ib4ocV45TIizFY1PoA2-NsPCHGhF2tiPFY1NeC5CEovR9H5Mk0_QUa_sZpfqwm1p0oIRN-NqjIj6KoZrGV2jtYEBFziHDm3lQ3z0mG2zxKvoFYsU2yGqEGgTh-pkA)

</details>

### <mark style="background-color:blue;">**Как завершить опрос**</mark>

{% hint style="info" %}
Когда опрос или викторина завершаются этой функцией в ответ приходит словарь с результатом опроса.
{% endhint %}

**tg\_stop\_poll(platform\_id, message\_id)**

Параметры:

<table><thead><tr><th width="303.45703125">Параметр</th><th>Описание</th></tr></thead><tbody><tr><td><mark style="color:red;"><strong>!</strong></mark><strong> platform_id</strong></td><td>идентификатор чата внутри Telegram <a href="funkcii-raboty-v-chatakh-i-kanalakh-telegram.md#gde-vzyat-platform_id-dlya-otpravki-uvedomlenii"><strong>*</strong></a></td></tr><tr><td><mark style="color:red;"><strong>!</strong></mark><strong> message_id</strong></td><td>идентификатор сообщения с опросом или викториной. Этот идентификатор можно получить из вебхука</td></tr></tbody></table>

## Как **работать с Форумами/Темами Telegram**

### 1. Как работать с главной темой **Telegram**

{% hint style="warning" %}
<mark style="color:red;">**Важно!**</mark>

Главная тема группы не имеет id и для работы с ней есть отдельные функции.
{% endhint %}

### <mark style="background-color:blue;">**Как переименовать главную Тему группы**</mark>

**tg\_edit\_general\_forum\_topic(platform\_id, topic\_name, bot\_name)**

Параметры:

<table><thead><tr><th width="185.921875">Параметр</th><th>Описание</th></tr></thead><tbody><tr><td><mark style="color:red;"><strong>!</strong></mark><strong> platform_id</strong></td><td>идентификатор Темы внутри Telegram <a href="funkcii-raboty-v-chatakh-i-kanalakh-telegram.md#gde-vzyat-platform_id-dlya-otpravki-uvedomlenii"><strong>*</strong></a></td></tr><tr><td><mark style="color:red;"><strong>!</strong></mark><strong> topic_name</strong></td><td>новое имя темы.</td></tr><tr><td>bot_name</td><td>необязательный параметр, наименование бота.<br>При работе с темами можно указать наименование бота, от имени которого нужно выполнить функцию. Это может пригодиться, если к проекту подключены более одного телеграм бота. Наименование бота можно найти в разделе "Каналы", поле "Group ID"</td></tr></tbody></table>

<details>

<summary>Пример для бота</summary>

Изменить Главную тему группы можно при помощи функции **tg\_edit\_general\_forum\_topic()**. Здесь 2 обязательных параметра - это идентификатор чата и новое наименование для Темы группы:&#x20;

<figure><img src="../../../../.gitbook/assets/image (147) (1).png" alt=""><figcaption><p>Изменение названия главной Темы</p></figcaption></figure>

<figure><img src="../../../../.gitbook/assets/image (148) (1).png" alt=""><figcaption></figcaption></figure>

</details>

<details>

<summary>Пример кода для копирования</summary>

_переименовать чат главной Темы_/\
`answer = tg_edit_general_forum_topic(-1001839380031, 'General')`

</details>

### <mark style="background-color:blue;">**Как закрыть главную Тему**</mark>

**tg\_close\_general\_forum\_topic(platform\_id)**

Параметры:

<table><thead><tr><th width="169.1484375">Параметр</th><th>Описание</th></tr></thead><tbody><tr><td><mark style="color:red;"><strong>!</strong></mark><strong> platform_id</strong> </td><td>идентификатор Темы внутри Telegram <a href="funkcii-raboty-v-chatakh-i-kanalakh-telegram.md#gde-vzyat-platform_id-dlya-otpravki-uvedomlenii"><strong>*</strong></a></td></tr><tr><td>bot_name</td><td>необязательный параметр, наименование бота.<br>При работе с темами можно указать наименование бота, от имени которого нужно выполнить функцию. Это может пригодиться, если к проекту подключены более одного телеграм бота. Наименование бота можно найти в разделе "Каналы", поле "Group ID"</td></tr></tbody></table>

<details>

<summary>Пример кода для копирования</summary>

/_закрыть чат главной Темы_/\
`answer = tg_close_general_forum_topic(-1001839380031)`

</details>

### <mark style="background-color:blue;">**Как открыть ранее закрытую главную Тему**</mark>

**tg\_reopen\_general\_forum\_topic(platform\_id,** bot\_nam&#x65;**)**&#x20;

Параметры:

<table><thead><tr><th width="181.796875">Параметр</th><th>Описание</th></tr></thead><tbody><tr><td><mark style="color:red;"><strong>!</strong></mark><strong> platform_id</strong> </td><td>идентификатор Темы внутри Telegram <a href="funkcii-raboty-v-chatakh-i-kanalakh-telegram.md#gde-vzyat-platform_id-dlya-otpravki-uvedomlenii"><strong>*</strong></a></td></tr><tr><td>bot_name</td><td>необязательный параметр, наименование бота.<br>При работе с темами можно указать наименование бота, от имени которого нужно выполнить функцию. Это может пригодиться, если к проекту подключены более одного телеграм бота. Наименование бота можно найти в разделе "Каналы", поле "Group ID"</td></tr></tbody></table>

<details>

<summary>Пример кода для копирования</summary>

/_открыть чат главной Темы_/\
`answer = tg_reopen_general_forum_topic(-1001839380031)`

</details>

### <mark style="background-color:blue;">**Как скрыть главную Тему**</mark>

**tg\_hide\_general\_forum\_topic(platform\_id,** bot\_nam&#x65;**)**&#x20;

Параметры:

<table><thead><tr><th width="315.3203125">Параметр</th><th>Описание</th></tr></thead><tbody><tr><td><mark style="color:red;"><strong>!</strong></mark><strong> platform_id</strong> </td><td>идентификатор Темы внутри Telegram <a href="funkcii-raboty-v-chatakh-i-kanalakh-telegram.md#gde-vzyat-platform_id-dlya-otpravki-uvedomlenii"><strong>*</strong></a></td></tr><tr><td>bot_name</td><td>необязательный параметр, наименование бота.<br>При работе с темами можно указать наименование бота, от имени которого нужно выполнить функцию. Это может пригодиться, если к проекту подключены более одного телеграм бота. Наименование бота можно найти в разделе "Каналы", поле "Group ID"</td></tr></tbody></table>

Суть данной операции в том, что чат Главной темы будет закрыт для участников Темы (можно читать, но нельзя писать) и скрыт из общего списка чатов Telegram для новых пользователей.&#x20;

<details>

<summary>Пример кода для копирования</summary>

/скрыть чат главной Темы/\
`answer = tg_hide_general_forum_topic(-1001839380031)`

</details>

### <mark style="background-color:blue;">**Как отобразить главную Тему или вернуть её видимость**</mark>&#x20;

**tg\_unhide\_general\_forum\_topic(platform\_id,** bot\_nam&#x65;**)**&#x20;

Параметры:

<table><thead><tr><th width="315.3203125">Параметр</th><th>Описание</th></tr></thead><tbody><tr><td><mark style="color:red;"><strong>!</strong></mark><strong> platform_id</strong> </td><td>идентификатор Темы внутри Telegram <a href="funkcii-raboty-v-chatakh-i-kanalakh-telegram.md#gde-vzyat-platform_id-dlya-otpravki-uvedomlenii"><strong>*</strong></a></td></tr><tr><td>bot_name</td><td>необязательный параметр, наименование бота.<br>При работе с темами можно указать наименование бота, от имени которого нужно выполнить функцию. Это может пригодиться, если к проекту подключены более одного телеграм бота. Наименование бота можно найти в разделе "Каналы", поле "Group ID"</td></tr></tbody></table>

{% hint style="warning" %}
<mark style="color:red;">**Важно!**</mark>&#x20;

Данная функция не открывает главную тему, а только делает ее видимой
{% endhint %}

<details>

<summary>Пример кода для копирования</summary>

/_отобразить чат главной Темы_/\
`answer = tg_unhide_general_forum_topic(-1001839380031)`

</details>

### **2. Как работать с дополнительными темами Telegram**

### <mark style="background-color:blue;">**Как создать новую тему Telegram**</mark>

**tg\_create\_forum\_topic(platform\_id, name, icon, icon\_color,** bot\_nam&#x65;**)**&#x20;

Параметры:

<table><thead><tr><th width="312.953125">Параметр</th><th>Описание</th></tr></thead><tbody><tr><td><mark style="color:red;"><strong>!</strong></mark><strong> platform_id</strong></td><td>идентификатор чата внутри Telegram <a href="funkcii-raboty-v-chatakh-i-kanalakh-telegram.md#gde-vzyat-platform_id-dlya-otpravki-uvedomlenii"><strong>*</strong></a> </td></tr><tr><td><mark style="color:red;"><strong>!</strong></mark><strong> name</strong></td><td>название новой темы</td></tr><tr><td><strong>icon</strong></td><td>идентификатор эмодзи, которое будет установлено на тему. Передается в виде строки. Можно использовать только те эмодзи, что есть в списке, полученном функцией <a href="funkcii-raboty-v-chatakh-i-kanalakh-telegram.md#kak-poluchit-spisok-emodzi-dlya-temy-telegram">tg_get_forum_icon</a> </td></tr><tr><td><strong>icon_color</strong></td><td>цвет эмодзи  из списка: 7322096, 16766590, 13338331, 9367192, 16749490, 16478047. Изменить цвет можно далеко не у всех эмодзи. </td></tr><tr><td>bot_name </td><td>необязательный параметр, наименование бота.<br>При работе с темами можно указать наименование бота, от имени которого нужно выполнить функцию. Это может пригодиться, если к проекту подключены более одного телеграм бота. Наименование бота можно найти в разделе "Каналы", поле "Group ID"</td></tr></tbody></table>

{% hint style="info" %}
Изменить установленный цвет нельзя, цвет задается только в момент создания темы
{% endhint %}

В результате исполнения функция вернет ответ, содержащий параметры новой темы, в том числе идентификатор темы (нужен для различных функций)

<details>

<summary>Пример для бота</summary>

Давайте создадим чат дополнительной темы:

<figure><img src="../../../../.gitbook/assets/image (149) (1).png" alt=""><figcaption><p>Создание новой темы</p></figcaption></figure>

Переменная answer будет содержать ответ следующего содержания: \
{"ok":true,"result":{"message\_thread\_id":254,"name":"second\_bot\_topic","icon\_color":7322096\}}

Здесь нам важно сохранить значение message\_thread\_id, оно нам понадобится в дальнейшем для работы с созданной темой:

<figure><img src="../../../../.gitbook/assets/image (150) (1).png" alt=""><figcaption><p>Сохраняем из ответа функции по созданию идентификатор дополнительной темы </p></figcaption></figure>

<figure><img src="../../../../.gitbook/assets/image (151) (1).png" alt=""><figcaption><p>Скрин Карточки клиента, раздел Переменные</p></figcaption></figure>

</details>

<details>

<summary>Пример кода для копирования</summary>

Создаем чат дополнительной темы\
`answer = tg_create_forum_topic(-1001839380031, 'second_bot_topic', None, 7322096)`

Сохраняем идентификатор чата созданной дополнительной темы\
`answer={"ok":true,"result":{"message_thread_id":254,"name":"second_bot_topic","icon_color":7322096}}/`\
`idtema1=answer['result']['message_thread_id']`

</details>

### <mark style="background-color:blue;">**Как изменить тему. Как переименовать и/или поменять эмодзи для темы**</mark>

**tg\_edit\_forum\_topic(platform\_id, message\_thread\_id, name, icon,** bot\_nam&#x65;**)**&#x20;

Параметры:

<table><thead><tr><th width="301.7578125">Параметр</th><th>Описание</th></tr></thead><tbody><tr><td><mark style="color:red;"><strong>!</strong></mark><strong> platform_id</strong></td><td>идентификатор чата внутри Telegram <a href="funkcii-raboty-v-chatakh-i-kanalakh-telegram.md#gde-vzyat-platform_id-dlya-otpravki-uvedomlenii"><strong>*</strong></a> </td></tr><tr><td><mark style="color:red;"><strong>!</strong></mark><strong> message_thread_id</strong></td><td>идентификатор чата дополнительной темы</td></tr><tr><td><strong>name</strong></td><td>название новой темы</td></tr><tr><td><strong>icon</strong></td><td>идентификатор эмодзи, которое будет установлено на тему. Передается в виде строки. Можно использовать только те эмодзи, что есть в списке, полученном функцией tg_get_forum_icon </td></tr><tr><td>bot_name</td><td>необязательный параметр, наименование бота.<br>При работе с темами можно указать наименование бота, от имени которого нужно выполнить функцию. Это может пригодиться, если к проекту подключены более одного телеграм бота. Наименование бота можно найти в разделе "Каналы", поле "Group ID"</td></tr></tbody></table>

<details>

<summary>Пример кода для копирования</summary>

`answer = tg_edit_forum_topic(-1001839380031, 254)`

</details>

### <mark style="background-color:blue;">**Как закрыть выбранную тему**</mark>

Закрыть тему - это значит оставить ее только для чтения, писать в закрытую тему нельзя

**tg\_close\_forum\_topic(platform\_id, message\_thread\_id,** bot\_nam&#x65;**)**&#x20;

Параметры:

<table><thead><tr><th width="300.9765625">Параметр</th><th>Описание</th></tr></thead><tbody><tr><td><mark style="color:red;"><strong>!</strong></mark><strong> platform_id</strong></td><td>идентификатор чата внутри Telegram <a href="funkcii-raboty-v-chatakh-i-kanalakh-telegram.md#gde-vzyat-platform_id-dlya-otpravki-uvedomlenii"><strong>*</strong></a> </td></tr><tr><td><mark style="color:red;"><strong>!</strong></mark><strong> message_thread_id</strong></td><td>идентификатор чата дополнительной темы</td></tr><tr><td>bot_name</td><td>необязательный параметр, наименование бота.<br>При работе с темами можно указать наименование бота, от имени которого нужно выполнить функцию. Это может пригодиться, если к проекту подключены более одного телеграм бота. Наименование бота можно найти в разделе "Каналы", поле "Group ID"</td></tr></tbody></table>

<details>

<summary>Пример кода для копирования</summary>

`answer = tg_close_forum_topic(-1001839380031, 254)`

</details>

### <mark style="background-color:blue;">**Как открыть ранее закрытую тему**</mark>

**tg\_reopen\_forum\_topic(platform\_id, message\_thread\_id,** bot\_nam&#x65;**)**&#x20;

Параметры:

<table><thead><tr><th width="300.9765625">Параметр</th><th>Описание</th></tr></thead><tbody><tr><td><mark style="color:red;"><strong>!</strong></mark><strong> platform_id</strong></td><td>идентификатор чата внутри Telegram <a href="funkcii-raboty-v-chatakh-i-kanalakh-telegram.md#gde-vzyat-platform_id-dlya-otpravki-uvedomlenii"><strong>*</strong></a> </td></tr><tr><td><mark style="color:red;"><strong>!</strong></mark><strong> message_thread_id</strong></td><td>идентификатор чата дополнительной темы</td></tr><tr><td>bot_name</td><td>необязательный параметр, наименование бота.<br>При работе с темами можно указать наименование бота, от имени которого нужно выполнить функцию. Это может пригодиться, если к проекту подключены более одного телеграм бота. Наименование бота можно найти в разделе "Каналы", поле "Group ID"</td></tr></tbody></table>

<details>

<summary>Пример кода для копирования</summary>

`answer = tg_reopen_forum_topic(-1001839380031, 254)`

</details>

### <mark style="background-color:blue;">**Как удалить тему со всеми сообщениями**</mark>

**tg\_delete\_forum\_topic(platform\_id, message\_thread\_id,** bot\_nam&#x65;**)**&#x20;

Параметры:

<table><thead><tr><th width="300.9765625">Параметр</th><th>Описание</th></tr></thead><tbody><tr><td><mark style="color:red;"><strong>!</strong></mark><strong> platform_id</strong></td><td>идентификатор чата внутри Telegram <a href="funkcii-raboty-v-chatakh-i-kanalakh-telegram.md#gde-vzyat-platform_id-dlya-otpravki-uvedomlenii"><strong>*</strong></a> </td></tr><tr><td><mark style="color:red;"><strong>!</strong></mark><strong> message_thread_id</strong></td><td>идентификатор чата дополнительной темы</td></tr><tr><td>bot_name</td><td>необязательный параметр, наименование бота.<br>При работе с темами можно указать наименование бота, от имени которого нужно выполнить функцию. Это может пригодиться, если к проекту подключены более одного телеграм бота. Наименование бота можно найти в разделе "Каналы", поле "Group ID"</td></tr></tbody></table>

<details>

<summary>Пример кода для копирования</summary>

`answer = tg_delete_forum_topic(-1001839380031, 254)`

</details>

### <mark style="background-color:blue;">**Как открепить все сообщения темы**</mark>

**tg\_unpin\_topic\_messages(platform\_id, message\_thread\_id,** bot\_nam&#x65;**)**&#x20;

Параметры:

<table><thead><tr><th width="300.9765625">Параметр</th><th>Описание</th></tr></thead><tbody><tr><td><mark style="color:red;"><strong>!</strong></mark><strong> platform_id</strong></td><td>идентификатор чата внутри Telegram <a href="funkcii-raboty-v-chatakh-i-kanalakh-telegram.md#gde-vzyat-platform_id-dlya-otpravki-uvedomlenii"><strong>*</strong></a> </td></tr><tr><td><mark style="color:red;"><strong>!</strong></mark><strong> message_thread_id</strong></td><td>идентификатор чата дополнительной темы</td></tr><tr><td>bot_name</td><td>необязательный параметр, наименование бота.<br>При работе с темами можно указать наименование бота, от имени которого нужно выполнить функцию. Это может пригодиться, если к проекту подключены более одного телеграм бота. Наименование бота можно найти в разделе "Каналы", поле "Group ID"</td></tr></tbody></table>

<details>

<summary>Пример кода для копирования</summary>

`answer = tg_unpin_topic_messages(-1001839380031, 254)`

</details>

### Как получить список эмодзи для Темы Telegram

**tg\_get\_forum\_icon()** - функция вернет какие эмодзи можно ставить на иконки тем форумов. Необходимо присвоить функцию переменной, так как в ответ будет словарь, в котором ключом будет эмодзи, а значением идентификатор этого эмодзи id

Параметры: <mark style="color:green;">**без параметров.**</mark>&#x20;

<details>

<summary>Содержание списка эмодзи</summary>

Для получения списка эмодзи для чата Темы отправьте команду в необходимый чат:

<figure><img src="../../../../.gitbook/assets/image (152) (1).png" alt=""><figcaption><p>Получение списка эмодзи</p></figcaption></figure>

В ответ функция вернет список эмодзи, т.е. переменная answer будет иметь в качестве значения словарь:

{'📰': '5434144690511290129', '💡': '5312536423851630001', '⚡️': '5312016608254762256', '🎙': '5377544228505134960', '🔝': '5418085807791545980', '🗣': '5368697802761185083', '🆒': '5420216386448270341', '❗️': '5379748062124056162', '📝': '5357193964787081133', '📆': '5433614043006903194', '📁': '5357315181649076022', '🔎': '5309965701241379366', '📣': '5309984423003823246', '🔥': '5312241539987020022', '❤️': '5312138559556164615', '❓': '5377316857231450742', '📈': '5350305691942788490', '📉': '5350713563512052787', '💎': '5309958691854754293', '💰': '5350452584119279096', '💸': '5309929258443874898', '\U0001fa99': '5377690785674175481', '💱': '5310107765874632305', '⁉️': '5377438129928020693', '🎮': '5309950797704865693', '💻': '5350554349074391003', '📱': '5409357944619802453', '🚗': '5312322066328853156', '🏠': '5312486108309757006', '💘': '5310029292527164639', '🎉': '5310228579009699834', '‼️': '5377498341074542641', '🏆': '5312315739842026755', '🏁': '5408906741125490282', '🎬': '5368653135101310687', '🎵': '5310045076531978942', '🔞': '5420331611830886484', '📚': '5350481781306958339', '👑': '5357107601584693888', '⚽️': '5375159220280762629', '🏀': '5384327463629233871', '📺': '5350513667144163474', '👀': '5357121491508928442', '\U0001fae6': '5357185426392096577', '🍓': '5310157398516703416', '💄': '5310262535021142850', '👠': '5368741306484925109', '✈️': '5348436127038579546', '\U0001f9f3': '5357120306097956843', '🏖': '5310303848311562896', '⛅️': '5350424168615649565', '🦄': '5413625003218313783', '🛍': '5350699789551935589', '👜': '5377478880577724584', '🛒': '5431492767249342908', '🚂': '5350497316203668441', '🛥': '5350422527938141909', '🏔': '5418196338774907917', '🏕': '5350648297189023928', '🤖': '5309832892262654231', '\U0001faa9': '5350751634102166060', '🎟': '5377624166436445368', '🏴\u200d☠️': '5386395194029515402', '🗳': '5350387571199319521', '🎓': '5357419403325481346', '🔭': '5368585403467048206', '🔬': '5377580546748588396', '🎶': '5377317729109811382', '🎤': '5382003830487523366', '🕺': '5357298525765902091', '💃': '5357370526597653193', '\U0001fa96': '5357188789351490453', '💼': '5348227245599105972', '\U0001f9ea': '5411138633765757782', '👨\u200d👩\u200d👧\u200d👦': '5386435923204382258', '👶': '5377675010259297233', '🤰': '5386609083400856174', '💅': '5368808634392257474', '🏛': '5350548830041415279', '\U0001f9ee': '5355127101970194557', '🖨': '5386379624773066504', '👮\u200d♂️': '5377494501373780436', '\U0001fa7a': '5350307998340226571', '💊': '5310094636159607472', '💉': '5310139157790596888', '\U0001f9fc': '5377468357907849200', '\U0001faaa': '5418115271267197333', '🛃': '5370947704199323325', '🍽': '5350344462612570293', '🐟': '5384574037701696503', '🎨': '5310039132297242441', '🎭': '5350658016700013471', '🎩': '5357504778685392027', '🔮': '5350367161514732241', '🍹': '5350520238444126134', '🎂': '5310132165583840589', '☕️': '5350392020785437399', '🍣': '5350406176997646350', '🍔': '5350403544182694064', '🍕': '5350444672789519765', '\U0001f9a0': '5312424913615723286', '💬': '5417915203100613993', '🎄': '5312054580060625569', '🎃': '5309744892677727325'}

</details>

<details>

<summary>Пример кода для копирования</summary>

```
answer = tg_get_forum_icon()
```

</details>
