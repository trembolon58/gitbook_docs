# Функции для отправки и редактирования сообщений

## Отправить сообщение в Telegram&#x20;

<mark style="background-color:green;">**! Работает с бизнес-аккаунтом в Телеграм**</mark>

**tg\_send\_message(platform\_id, text,client\_message\_id, reply\_markup, parse\_mode, disable\_web\_page\_preview, protect\_content, disable\_notification**, **message\_thread\_id, entities)**&#x20;

Параметры:

<table><thead><tr><th width="324.87890625">Параметр</th><th>Описание</th></tr></thead><tbody><tr><td><mark style="color:red;"><strong>!</strong></mark><strong> platform_id</strong></td><td>идентификатор клиента в Telegram, которому необходимо прислать сообщение <a href="messages.md#gde-vzyat-platform_id-dlya-otpravki-uvedomlenii"><strong>*</strong></a></td></tr><tr><td><mark style="color:red;"><strong>!</strong></mark><strong> text</strong></td><td>текст сообщения</td></tr><tr><td><strong>client_message_id</strong> </td><td>идентификатор сообщения, которое необходимо процитировать</td></tr><tr><td><strong>reply_markup</strong></td><td>настройки кнопок <a href="messages.md#kak-propisyvat-knopki-v-parametre-reply_markup"><strong>**</strong></a></td></tr><tr><td><strong>parse_mode</strong></td><td>выделение текста в описании жирным или курсивом <a href="https://docs.salebot.pro/messendzhery-i-chaty/kak-sozdat-bota-v-telegram/razmetka-markdown.-formatirovanie-soobsheniya-v-telegram"><strong>***</strong></a><strong>.</strong> Может иметь значения html, markdown, markdownV2.</td></tr><tr><td><strong>disable_web_page_preview</strong></td><td>отобразить превью ссылки. Чтобы отключить передайте 1, иначе 0 или оставьте пустое значение “”</td></tr><tr><td><strong>protect_content</strong></td><td>признак защиты контента от копирования. Чтобы включить передайте любое значение, кроме 0, False и пустых кавычек ''</td></tr><tr><td><strong>disable_notification</strong></td><td>признак отправки сообщения со звуковым уведомлением (по умолчанию 0)<br>1 - отключить уведомление при получении, 0 - передать с уведомлением</td></tr><tr><td><strong>message_thread_id</strong></td><td>идентификатор темы (доступно для супергрупп при наличии функционала форума)</td></tr><tr><td><strong>entities</strong></td><td>c ним вы можете просто копировать сверстанный текст со всеми особенностями и просто указать с какого символа по какой он будет отображаться с тем или иным шрифтом. Пример можете подсмотреть в tg_request в соответствующем поле. В параметре должен быть словарь. Пример можно посмотреть во вкладке с примером.</td></tr></tbody></table>

<details>

<summary><mark style="color:orange;"><strong>Подробный пример</strong></mark></summary>

Рассмотрим простой пример с набором обязательных параметров:

<figure><img src="../../../../.gitbook/assets/image (634).png" alt=""><figcaption></figcaption></figure>

В качестве platform\_id указывается идентификатор конкретного клиента

Тот  же пример, но с использованием переменных:

<figure><img src="../../../../.gitbook/assets/image (640).png" alt=""><figcaption></figcaption></figure>

В данном примере в переменной soob будет содержаться ответ сервера после отправки сообщения.&#x20;

<figure><img src="../../../../.gitbook/assets/image (641).png" alt=""><figcaption></figcaption></figure>

Если сохранить идентификатор сообщения message\_id из полученного ответа, то это позволит нам впоследствии работать с данным сообщением (редактировать, удалять, пересылать, комментировать).

Очень часто возникают сложности в использовании всех параметров. Давайте рассмотрим такой пример:

*   для начала объявите все параметры, используемые в функции. Не забывайте, что параметры можно передать не только значением, но и переменными, что чаще более удобно и наглядно.\
    Такие переменные, как  platform\_id и client\_message\_id Вы можете получить в карточке клиента \
    &#x20;**platform\_id** — идентификатор клиента в Telegram, которому необходимо прислать сообщение [**\***](messages.md#gde-vzyat-platform_id-dlya-otpravki-uvedomlenii)\
    <mark style="color:green;">>Будем отвечать в том же чате, где пишет клиент</mark>&#x20;

    **text** - текст сообщения. \
    <mark style="color:green;">>Используем форматирование текста - например, выделение жирным</mark>

    **client\_message\_id** - идентификатор сообщения, которое необходимо процитировать\
    <mark style="color:green;">>В чатах эта переменная получает свое значение автоматически.</mark> \
    **reply\_markup** — настройки кнопок [**\*\***](messages.md#kak-propisyvat-knopki-v-parametre-reply_markup)**.** \
    <mark style="color:green;">>Присвоим в переменную opts</mark>\
    **parse\_mode** — выделение текста в описании жирным или курсивом [**\*\*\***](messages.md#kak-ispolzovat-razmetku-teksta-markdown-v-parametre-parse_mode)**.** Может иметь значения html, markdown, markdownV2. Используемые символы для форматирования текста сообщения описаны[ тут](/broken/pages/KEcqTxiLh1QVQqHdo0eU)\
    <mark style="color:green;">>Используем markdown.</mark> \
    **disable\_web\_page\_preview -** отобразить превью ссылки. Чтобы отключить передайте 1, иначе 0 или оставьте пустое значение “”\
    <mark style="color:green;">>Мы можем передать любое значение, поскольку в тексте сообщения не указываем ссылку</mark>\
    **protect\_content** — признак защиты контента от копирования. Чтобы включить передайте любое значение, кроме 0, False и пустых кавычек ''\
    <mark style="color:green;">>Нам не требуется защита контента передадим ''</mark>\
    **disable\_notification** —  признак отправки сообщения с уведомлением (по умолчанию 0)\
    0 - отключить уведомление при получении, 1 - передать с уведомлением\
    <mark style="color:green;">>Уведомление - это всплывающее окно с содержимым текста сообщения. Давайте включим</mark>
* Далее собираем функцию. Не забывайте присваивать функцию переменной - это позволит отследить статус отправки сообщения

<figure><img src="../../../../.gitbook/assets/image (642).png" alt=""><figcaption><p>Поле Калькулятор</p></figcaption></figure>

Смотрим, что у нас получилось:\
После того, как клиент написал нам ключевое слово test, мы отвечаем ему, цитируя его сообщение<br>

<figure><img src="../../../../.gitbook/assets/image (643).png" alt=""><figcaption><p>Пример использования всех параметров функции отправки сообщения</p></figcaption></figure>

При этом в переменной soob видим следующий ответ сервера:<br>

<figure><img src="../../../../.gitbook/assets/image (644).png" alt=""><figcaption><p>Ответ сервера после отправки сообщения функцией API</p></figcaption></figure>

В ok мы как раз видим статус отправки, далее содержится информация о данном сообщении - его id, данные отправителя, содержимое отправления.\
\
Пример с передачей параметра **entities**\
Исходную строку можно поместить в переменную, как показано ниже: \
`text = "йцуав цйуа йуцайукап укцацу цйува31уцвац"` \
\
Параметр записываете в формате словаря с данными и указываете необходимое вам форматирование с указанием шрифтов.\
`entities = [{"offset":0,"length":5,"type":"bold"},{"offset":6,"length":4,"type":"text_link","url":"https://salebot.zmservice.ru"},{"offset":11,"length":9,"type":"strikethrough"},{"offset":21,"length":6,"type":"spoiler"},{"offset":29,"length":12,"type":"code"}]` \
\
Передайте параметр последним в используемой функции. Параметр можно передавать как в функции tg\_send\_message так и в функции tg\_send\_message\_1\
`x = tg_send_message(platform_id, text, None, None, None, False, False, False, None, entities`)<br>



</details>

{% hint style="info" %}
Чтобы в переменную записать текст с переносами строк, укажите значение следующим образом:

`text = "Текст первой строки" + "\n" + "Текст второй строки" + "\n" +"Третья строка"`
{% endhint %}

### Видеоинструкция

{% embed url="https://www.youtube.com/watch?v=ShqTZ_JCKE0" %}
Функции для отправки сообщения&#x20;
{% endembed %}

## Отправить сообщение с указанием конкретного бота в Telegram

tg\_send\_message\_1(token, platform\_id, text, client\_message\_id, reply\_markup, parse\_mode, disable\_web\_page\_preview, protect\_content, disable\_notification, message\_thread\_id, entities, business\_connection\_id)

<table><thead><tr><th width="288.94140625">Параметр</th><th>Описание</th></tr></thead><tbody><tr><td><mark style="color:red;"><strong>!</strong></mark><strong> token</strong></td><td>токен Telegram-бота, полученный в BotFather </td></tr><tr><td><mark style="color:red;"><strong>!</strong></mark><strong> platform_id</strong></td><td>идентификатор клиента в Telegram, которому необходимо прислать сообщение <a href="messages.md#gde-vzyat-platform_id-dlya-otpravki-uvedomlenii"><strong>*</strong></a></td></tr><tr><td><mark style="color:red;"><strong>!</strong></mark><strong> text</strong></td><td>текст сообщения</td></tr><tr><td><strong>client_message_id</strong></td><td>идентификатор сообщения, которое необходимо процитировать</td></tr><tr><td><strong>reply_markup</strong></td><td>настройки кнопок <a href="messages.md#kak-propisyvat-knopki-v-parametre-reply_markup"><strong>**</strong></a></td></tr><tr><td><strong>parse_mode</strong></td><td>выделение текста в описании жирным или курсивом <a href="https://docs.salebot.pro/messendzhery-i-chaty/kak-sozdat-bota-v-telegram/razmetka-markdown.-formatirovanie-soobsheniya-v-telegram"><strong>***</strong></a><strong>.</strong> Может иметь значения html, markdown, markdownV2.</td></tr><tr><td><strong>disable_web_page_preview</strong></td><td>отобразить превью ссылки. Чтобы отключить передайте 1, иначе 0 или оставьте пустое значение “”</td></tr><tr><td><strong>protect_content</strong></td><td>признак защиты контента от копирования. Чтобы включить передайте любое значение, кроме 0, False и пустых кавычек ''</td></tr><tr><td><strong>disable_notification</strong></td><td>признак отправки сообщения со звуковым уведомлением (по умолчанию 0)<br>1 - отключить уведомление при получении, 0 - передать с уведомлением</td></tr><tr><td><strong>message_thread_id</strong> </td><td>идентификатор темы (доступно для супергрупп при наличии функционала форума)</td></tr><tr><td><strong>entities</strong></td><td>c ним вы можете просто копировать сверстанный текст со всеми особенностями и просто указать с какого символа по какой он будет отображаться с тем или иным шрифтом. Пример можете подсмотреть в tg_request в соответствующем поле. В параметре должен быть словарь. </td></tr><tr><td><strong>business_connection_id</strong></td><td>значение при подключении бота - Business ID - отображается в каналах. Следует передавать, если в параметрах передается токен бота и надо отправить через подключенный к боту пользовательский аккаунт</td></tr></tbody></table>

<details>

<summary>Пример</summary>

Пример передачи параметра: \
`entities = [{"offset":0,"length":5,"type":"bold"},{"offset":6,"length":4,"type":"text_link","url":"https://salebot.zmservice.ru"},{"offset":11,"length":9,"type":"strikethrough"},{"offset":21,"length":6,"type":"spoiler"},{"offset":29,"length":12,"type":"code"}]`  \
\
В примере показан только словарь, при этом сама переменная с текстом сообщения задана в переменной.

</details>

## Редактировать текст в сообщении Telegram

{% hint style="warning" %}
Обращаем внимание!&#x20;

Функция для редактирования сообщений доступна только для новых и вновь отправленных сообщений.&#x20;

Время, в течение которого доступно редактирование сообщения, определяется самим мессенджером, причем зависит от нагруженности/активности вашего бота и может быть сокращено для редактирования.&#x20;

Оптимальное время для редактирования сообщения, как указывает техническая поддержка мессенджера, 48 часов.&#x20;
{% endhint %}

**tg\_edit\_message\_text(platform\_id, message\_id, text, reply\_markup, parse\_mode, disable\_web\_page\_preview, entities)**

<table><thead><tr><th width="270.03125">Параметр</th><th>Описание</th></tr></thead><tbody><tr><td><mark style="color:red;"><strong>!</strong></mark><strong> platform_id</strong></td><td>идентификатор клиента в Telegram, которому необходимо прислать сообщение <a href="messages.md#gde-vzyat-platform_id-dlya-otpravki-uvedomlenii"><strong>*</strong></a></td></tr><tr><td><mark style="color:red;"><strong>!</strong></mark><strong> message_id</strong></td><td>идентификатор сообщения, которое необходимо отредактировать. Предварительно id  нужно сохранять при отправке </td></tr><tr><td><mark style="color:red;"><strong>!</strong></mark><strong> text</strong></td><td>текст сообщения</td></tr><tr><td><strong>reply_markup</strong></td><td>настройки кнопок <a href="messages.md#kak-propisyvat-knopki-v-parametre-reply_markup"><strong>**</strong></a></td></tr><tr><td><strong>parse_mode</strong></td><td>выделение текста в описании жирным или курсивом <a href="https://docs.salebot.pro/messendzhery-i-chaty/kak-sozdat-bota-v-telegram/razmetka-markdown.-formatirovanie-soobsheniya-v-telegram"><strong>***</strong></a><strong>.</strong> Может иметь значения html, markdown, markdownV2.. Может иметь значения html, markdown, markdownV2.</td></tr><tr><td><strong>disable_web_page_preview</strong> </td><td>отобразить превью ссылки. Чтобы отключить передайте 1, иначе 0 или оставьте пустое значение “”</td></tr><tr><td><strong>entities</strong></td><td>c ним вы можете просто копировать сверстанный текст со всеми особенностями и просто указать с какого символа по какой он будет отображаться с тем или иным шрифтом. Пример можете подсмотреть в tg_request в соответствующем поле. В параметре должен быть словарь.</td></tr></tbody></table>

## Отправить реакцию на сообщение

tg\_set\_reaction(platform\_id, message\_id, reaction)

<table><thead><tr><th width="305.015625">Параметр </th><th>Описание</th></tr></thead><tbody><tr><td><mark style="color:red;"><strong>!</strong></mark> platform_id</td><td>идентификатор чата в телеграмм</td></tr><tr><td><mark style="color:red;"><strong>!</strong></mark> message_id</td><td>идентификатор сообщения</td></tr><tr><td><mark style="color:red;"><strong>!</strong></mark> reaction</td><td>передается необходимая реакция строкой</td></tr></tbody></table>

<details>

<summary>Пример</summary>

Пример кода для копирования:

react = tg\_set\_reaction(platform\_id, 1556, '👌')

Пример в калькуляторе:

<img src="../../../../.gitbook/assets/2024-02-19_11-15-40.png" alt="" data-size="original">

</details>

## Редактировать описание к вложению

**tg\_edit\_message\_caption(platform\_id, message\_id, caption, reply\_markup, parse\_mode, entities, show\_caption\_above\_media)**

<table><thead><tr><th width="305.015625">Параметр </th><th>Описание</th></tr></thead><tbody><tr><td><mark style="color:red;"><strong>!</strong></mark> platform_id</td><td>идентификатор клиента в Telegram, которому необходимо прислать сообщение <a href="messages.md#gde-vzyat-platform_id-dlya-otpravki-uvedomlenii"><strong>*</strong></a></td></tr><tr><td><mark style="color:red;"><strong>!</strong></mark> message_id</td><td>идентификатор сообщения, которое необходимо отредактировать</td></tr><tr><td><mark style="color:red;"><strong>!</strong></mark><strong> caption</strong></td><td>текст описания</td></tr><tr><td><strong>reply_markup</strong></td><td>настройки кнопок <a href="messages.md#kak-propisyvat-knopki-v-parametre-reply_markup"><strong>**</strong></a></td></tr><tr><td><strong>parse_mode</strong></td><td>выделение текста в описании жирным или курсивом <a href="https://docs.salebot.pro/messendzhery-i-chaty/kak-sozdat-bota-v-telegram/razmetka-markdown.-formatirovanie-soobsheniya-v-telegram"><strong>***</strong></a><strong>.</strong>  Может иметь значения html, markdown, markdownV2.</td></tr><tr><td><strong>entities</strong> </td><td>c ним вы можете просто копировать сверстанный текст со всеми особенностями и просто указать с какого символа по какой он будет отображаться с тем или иным шрифтом. Пример можете подсмотреть в tg_request в соответствующем поле. В параметре должен быть словарь.<br><br>Пример передачи параметра: <br><code>entities = [{"offset":0,"length":5,"type":"bold"},{"offset":6,"length":4,"type":"text_link","url":"https://salebot.zmservice.ru"},{"offset":11,"length":9,"type":"strikethrough"},{"offset":21,"length":6,"type":"spoiler"},{"offset":29,"length":12,"type":"code"}]</code>  <br><br>В примере показан только словарь, при этом сама переменная с текстом сообщения задана в переменной.</td></tr><tr><td><strong>show_caption_above_media</strong></td><td>принимает значение True, если указать этот параметр, то текст сообщения будет расположен над вложением</td></tr></tbody></table>



## Редактировать медиа вложения в сообщении

t**g\_edit\_message\_media(platform\_id, message\_id, media, reply\_markup)**

<table><thead><tr><th width="270.03125">Параметр</th><th>Описание</th></tr></thead><tbody><tr><td><mark style="color:red;"><strong>!</strong></mark><strong> platform_id</strong></td><td>идентификатор клиента в Telegram, которому необходимо прислать сообщение <a href="messages.md#gde-vzyat-platform_id-dlya-otpravki-uvedomlenii"><strong>*</strong></a></td></tr><tr><td><mark style="color:red;"><strong>!</strong></mark><strong> message_id</strong></td><td>идентификатор сообщения, которое необходимо отредактировать. Предварительно id  нужно сохранять при отправке </td></tr><tr><td><mark style="color:red;"><strong>!</strong></mark><strong> media</strong></td><td><p>словарь, описывающий медиа-файл: <br><em>Пример словаря в формате JSON для смены ранее отправленного фото:</em><br><code>media =</code> <code>'{"type": "photo", "media": "&#x3C;файл для отправки>"}'</code></p><p>где в качестве &#x3C;файл для отправки> рекомендуется указать file_id, полученный с помощью <a href="https://docs.salebot.pro/messendzhery-i-chaty/kak-sozdat-bota-v-telegram/poluchit-polnyi-vebkhuk-webhook-ot-telegram#kak-pri-pomoshi-tg_request-poluchit-ssylku-na-kartinku-foto-animaciyu-video">полного вебхука от Telegram</a></p><p>Подробнее параметры для словаря описаны в <a href="https://core.telegram.org/bots/api#inputmedia">официальной документации Telegram</a>.</p></td></tr><tr><td><strong>reply_markup</strong></td><td>настройки кнопок <a href="messages.md#kak-propisyvat-knopki-v-parametre-reply_markup"><strong>**</strong></a></td></tr></tbody></table>

## **Редактировать инлайн-клавиатуру в сообщении**

**tg\_edit\_message\_reply\_markup(platform\_id, message\_id, reply\_markup)**

<table><thead><tr><th width="270.03125">Параметр</th><th>Описание</th></tr></thead><tbody><tr><td><mark style="color:red;"><strong>!</strong></mark><strong> platform_id</strong></td><td>идентификатор клиента в Telegram, которому необходимо прислать сообщение <a href="messages.md#gde-vzyat-platform_id-dlya-otpravki-uvedomlenii"><strong>*</strong></a></td></tr><tr><td><mark style="color:red;"><strong>!</strong></mark><strong> message_id</strong></td><td>идентификатор сообщения, которое необходимо отредактировать. Предварительно id  нужно сохранять при отправке </td></tr><tr><td><mark style="color:red;"><strong>!</strong></mark><strong> reply_markup</strong></td><td>настройки кнопок <a href="messages.md#kak-propisyvat-knopki-v-parametre-reply_markup"><strong>**</strong></a></td></tr></tbody></table>

{% hint style="warning" %}
Редактировать можно только инлайн-клавиатуру.&#x20;
{% endhint %}

<details>

<summary>Пример редактирования сообщений с помощью API Telegram</summary>

Ниже в этой статье можно ознакомится с подробным примером работы с функциями API Telegram для редактирования сообщений&#x20;

</details>

## Копировать сообщение

**tg\_copy\_message(platform\_id, from\_chat\_id, message\_id, reply\_to\_message\_id, reply\_markup, parse\_mode, protect\_content, disable\_notification, caption, message\_thread\_id, entities, show\_caption\_above\_media)**

<table><thead><tr><th width="270.03125">Параметр</th><th>Описание</th></tr></thead><tbody><tr><td> <mark style="color:red;"><strong>!</strong></mark><strong> platform_id</strong> </td><td>идентификатор группы в Telegram, В КОТОРЫЙ будем копировать сообщение <a href="messages.md#gde-vzyat-platform_id-dlya-otpravki-uvedomlenii"><strong>*</strong></a></td></tr><tr><td><mark style="color:red;"><strong>!</strong></mark><strong> from_chat_id</strong> </td><td>идентификатор группы в Telegram, ИЗ КОТОРОЙ будем копировать сообщение <a href="messages.md#gde-vzyat-platform_id-dlya-otpravki-uvedomlenii"><strong>*</strong></a></td></tr><tr><td><mark style="color:red;"><strong>!</strong></mark><strong> message_id</strong></td><td>идентификатор сообщения, которое необходимо скопировать</td></tr><tr><td><strong>reply_to_message_id</strong> </td><td>идентификатор исходного сообщения, если копируемое сообщение является комментарием</td></tr><tr><td><strong>reply_markup</strong> </td><td>настройки кнопок <a href="messages.md#kak-propisyvat-knopki-v-parametre-reply_markup"><strong>**</strong></a></td></tr><tr><td><strong>parse_mode</strong></td><td>выделение текста в описании жирным или курсивом <a href="https://docs.salebot.pro/messendzhery-i-chaty/kak-sozdat-bota-v-telegram/razmetka-markdown.-formatirovanie-soobsheniya-v-telegram"><strong>***</strong></a><strong>.</strong> Может иметь значения html, markdown, markdownV2.</td></tr><tr><td><strong>protect_content</strong></td><td>признак защиты контента от копирования.  Чтобы включить передайте любое значение, кроме 0, False и пустых кавычек ''</td></tr><tr><td><strong>disable_notification</strong> </td><td>признак отправки сообщения со звуковым уведомлением (по умолчанию 0)<br>1 - отключить уведомление при получении, 0 - передать с уведомлением                           </td></tr><tr><td><strong>caption</strong> - </td><td>описание до 1024 символов</td></tr><tr><td><strong>message_thread_id</strong> </td><td>идентификатор темы (доступно для супергрупп при наличии функционала форума)</td></tr><tr><td><strong>entities</strong> </td><td>c ним вы можете просто копировать сверстанный текст со всеми особенностями и просто указать с какого символа по какой он будет отображаться с тем или иным шрифтом. Пример можете подсмотреть в tg_request в соответствующем поле. В параметре должен быть словарь.<br><br>Пример передачи параметра: <br><code>entities = [{"offset":0,"length":5,"type":"bold"},{"offset":6,"length":4,"type":"text_link","url":"https://salebot.zmservice.ru"},{"offset":11,"length":9,"type":"strikethrough"},{"offset":21,"length":6,"type":"spoiler"},{"offset":29,"length":12,"type":"code"}]</code>  <br><br>В примере показан только словарь, при этом сама переменная с текстом сообщения задана в переменной.</td></tr><tr><td><strong>show_caption_above_media</strong> </td><td>принимает значение True, если указать этот параметр, то текст сообщения будет расположен над вложением</td></tr></tbody></table>

## Переслать сообщение

**tg\_forward\_message(platform\_id, from\_chat\_id, message\_id, protect\_content, disable\_notification,** **message\_thread\_id)**&#x20;

<table><thead><tr><th width="312.0703125">Параметр</th><th>Описание</th></tr></thead><tbody><tr><td><mark style="color:red;"><strong>!</strong></mark><strong> platform_id</strong> </td><td> идентификатор клиента в Telegram, КУДА необходимо переслать сообщение <a href="messages.md#gde-vzyat-platform_id-dlya-otpravki-uvedomlenii"><strong>*</strong></a></td></tr><tr><td><mark style="color:red;"><strong>!</strong></mark><strong> from_chat_id</strong></td><td>идентификатор клиента в Telegram, ОТКУДА необходимо переслать сообщение <a href="messages.md#gde-vzyat-platform_id-dlya-otpravki-uvedomlenii"><strong>*</strong></a></td></tr><tr><td><mark style="color:red;"><strong>!</strong></mark><strong> message_id</strong></td><td>идентификатор пересылаемого сообщения</td></tr><tr><td><strong>protect_content</strong></td><td>признак защиты контента от копирования.  Чтобы включить передайте любое значение, кроме 0, False и пустых кавычек ''</td></tr><tr><td><strong>disable_notification</strong></td><td>признак отправки сообщения со звуковым уведомлением (по умолчанию 0)<br>1 - отключить уведомление при получении, 0 - передать с уведомлением</td></tr><tr><td><strong>message_thread_id</strong> </td><td>идентификатор темы (доступно для супергрупп при наличии функционала форума)</td></tr></tbody></table>

## Удалить сообщение

**tg\_delete\_message(platform\_id, message\_id)**&#x20;

<table><thead><tr><th width="294.3203125">Параметр</th><th>Описание</th></tr></thead><tbody><tr><td><mark style="color:red;"><strong>!</strong></mark><strong> platform_id</strong> </td><td>идентификатор клиента в Telegram <a href="messages.md#gde-vzyat-platform_id-dlya-otpravki-uvedomlenii"><strong>*</strong></a> </td></tr><tr><td><mark style="color:red;"><strong>!</strong></mark><strong> message_id</strong></td><td>идентификатор сообщения, которое необходимо удалить</td></tr></tbody></table>

{% hint style="warning" %}
<mark style="color:red;">**!**</mark> Используйте этот метод для удаления сообщения, в том числе служебного, со следующими ограничениями:

* Сообщение может быть удалено только в том случае, если оно было отправлено менее 48 часов назад.
* Сообщение с кубиками в приватном чате можно удалить только в том случае, если оно было отправлено более 24 часов назад.
* Боты могут удалять исходящие сообщения в приватных чатах, группах и супергруппах.
* Боты могут удалять входящие сообщения в приватных чатах.
* Боты с разрешениями can\_post\_messages могут удалять исходящие сообщения в каналах.
* Если бот является администратором группы, он может удалить там любое сообщение.
* Если у бота есть разрешение can\_delete\_messages в супергруппе или канале, он может удалить там любое сообщение.&#x20;
{% endhint %}

## **Удалить несколько сообщений**

tg\_delete\_messages(platform\_id, message\_ids)

<table><thead><tr><th width="288.06640625">Параметр</th><th>Описание</th></tr></thead><tbody><tr><td><mark style="color:red;"><strong>!</strong></mark> platform_id</td><td>идентификатор клиента в Telegram </td></tr><tr><td><mark style="color:red;"><strong>!</strong></mark> message_ids</td><td>массив с идентификаторами сообщений, которые необходимо удалить. Максимум 100 элементов</td></tr></tbody></table>

{% hint style="warning" %}
<mark style="color:red;">**!**</mark> Используйте этот метод для удаления сообщения, в том числе служебного, со следующими ограничениями:

* Сообщение может быть удалено только в том случае, если оно было отправлено менее 48 часов назад.
* Сообщение с кубиками в приватном чате можно удалить только в том случае, если оно было отправлено более 24 часов назад.
* Боты могут удалять исходящие сообщения в приватных чатах, группах и супергруппах.
* Боты могут удалять входящие сообщения в приватных чатах.
* Боты с разрешениями can\_post\_messages могут удалять исходящие сообщения в каналах.
* Если бот является администратором группы, он может удалить там любое сообщение.
* Если у бота есть разрешение can\_delete\_messages в супергруппе или канале, он может удалить там любое сообщение.&#x20;
{% endhint %}

{% embed url="https://www.youtube.com/watch?v=3V7z1j83y1I&t=655s" %}
Функция для редактирования сообщений
{% endembed %}

### **Пример отправки сообщения с помощью функции API Telegram**

{% tabs %}
{% tab title="Пример кода для копирования" %}
Пример 1

```
/*Текст удобно предварительно прописывать в переменной*/
text='Пишем-пишем-пишем текст'
/*Функция Отправить сообщение*/
soob=tg_send_message(platform_id, text)
/*Сохраняем ид отправленного сообщения*/
soob_id=soob['result']['message_id']

```

Пример 2

```
id_group=-1001847103100
text='Тестируем отправку сообщения API-методом. Например, *жирный текст*'
opts = {"inline_keyboard": [[{"text": "👍","callback_data":1}, {"text": "👎","callback_data":2}]]}
disable_web_page_preview=1
protect_content=''
disable_notification=1
parse_mode='markdown'
soob=tg_send_message(id_group, text,client_message_id, opts, parse_mode, disable_web_page_preview, protect_content, disable_notification) 


```
{% endtab %}
{% endtabs %}

### &#x20;**Пример редактирования сообщений с помощью API Telegram**&#x20;

{% tabs %}
{% tab title="Пример настройки" %}
Итак, отправим себе сообщение с инлайн-клавиатурой:

<figure><img src="../../../../.gitbook/assets/image (645).png" alt=""><figcaption></figcaption></figure>

далее отредактируем текст сообщения:

<figure><img src="../../../../.gitbook/assets/image (646).png" alt=""><figcaption></figcaption></figure>

теперь отредактируем кнопки:

<figure><img src="../../../../.gitbook/assets/image (647).png" alt=""><figcaption></figcaption></figure>

Попробуем отредактирвать сообщение с картинкой. Для этого отправим сообщение с картинкой и сохраним идентификатор отправленного сообщения. О том как получить ссылку на картинку подробно описано [тут](messages.md#kak-pri-pomoshi-tg_request-poluchit-ssylku-na-kartinku-foto-animaciyu-video):

<figure><img src="../../../../.gitbook/assets/image (648).png" alt=""><figcaption></figcaption></figure>

Редактируем картинку и описание:

<figure><img src="../../../../.gitbook/assets/image (649).png" alt=""><figcaption></figcaption></figure>
{% endtab %}

{% tab title="Пример кода для копирования" %}
```
/*Параметры удобно предварительно прописывать в переменной*/
text='Какой тариф желаете выбрать?'
opts = {"inline_keyboard": [[{"text": "Пакет 1","callback_data":1}, {"text": "Пакет 2","callback_data":2}]]}
/*Функция Отправить сообщение*/
soob=tg_send_message(platform_id, text, None, opts)
/*Сохраняем ид отправленного сообщения*/
soob_id=soob['result']['message_id']

/*Редактируем сообщение*/
text='Какой тариф Вас заинтересовал?'
tg_edit_message_text(platform_id, soob_id, text, opts)  

/*Редактируем инлайн-клавиатуру*/
opts = {"inline_keyboard": [[{"text": "Стандарт","callback_data":1}, {"text": "Премиум","callback_data":2}]]}
tg_edit_message_reply_markup(platform_id, soob_id, opts)


/*Отправляем картинку с описанием*/
soob=tg_send_photo(platform_id, "AgACAgIAAxkBAAIPpWO4T7jhOgYHq6uR8rjnq9rIvBs-AAJlwDEb5fHASaGdhzgWjyn7AQADAgADeAADLQQ", "Это картинка")
/*Сохраняем ид отправленного сообщения*/
soob_id=soob['result']['message_id']

/*Редактируем картинку*/
media='{"type": "photo", "media": "AgACAgIAAxkBAAIPrmO4UiH7Tazqn-3IbFVzPKNsVEZmAAJ1wDEb5fHASWcNXKah-egvAQADAgADeQADLQQ"}'
tg_edit_message_media(platform_id, soob_id, media)
/*Редактируем описание к картинке*/
tg_edit_message_caption(platform_id, soob_id, 'Вот он Я!')
```
{% endtab %}
{% endtabs %}

### Пример копирования сообщения с помощью API Telegram

{% tabs %}
{% tab title="Пример" %}
Отправим сообщение и сохраним его идентификатор:

<figure><img src="../../../../.gitbook/assets/image (650).png" alt=""><figcaption></figcaption></figure>

Скопируем ранее отправленное сообщение:

<figure><img src="../../../../.gitbook/assets/image (651).png" alt=""><figcaption></figcaption></figure>
{% endtab %}

{% tab title="Пример кода для копирования" %}
```
/*Параметры удобно предварительно прописывать в переменной*/
text='Какой тариф желаете выбрать?'
opts = {"inline_keyboard": [[{"text": "Пакет 1","callback_data":1}, {"text": "Пакет 2","callback_data":2}]]}
/*Функция Отправить сообщение*/
soob=tg_send_message(platform_id, text, None, opts)
/*Сохраняем ид отправленного сообщения*/
soob_id=soob['result']['message_id']


/*Копирование отправленного сообщения*/
tg_copy_message('5081438490', '1840834360', soob_id, None, opts, None, None, 1)
```
{% endtab %}
{% endtabs %}
