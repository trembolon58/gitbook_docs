# Функции отправки вложений в сообщении

## Описание параметров функций

<details>

<summary>Отправить документ tg_send_document() </summary>

<mark style="color:red;">**!**</mark> Данные функции позволяют отправить файлы любого типа, рекомендуемые - **GIF**, **PDF** и **ZIP** весом до 2Гб.

<mark style="background-color:green;">**! Работает с бизнес-аккаунтом в Телеграм**</mark>

**tg\_send\_document(platform\_id, document, caption, reply\_markup, parse\_mode,reply\_to\_message\_id, protect\_content, disable\_notification**, **message\_thread\_id, entities)**&#x20;

Параметры:

<mark style="color:red;">**!**</mark>**&#x20;platform\_id** — идентификатор клиента в Telegram, которому необходимо прислать сообщение [**\***](attachments.md#gde-vzyat-platform_id-dlya-otpravki-uvedomlenii)

<mark style="color:red;">**!**</mark>**&#x20;document** - ссылка на документ с сервера Telegram. Получение ссылки через tg\_request рассмотрено [тут](https://docs.salebot.pro/messendzhery-i-chaty/kak-sozdat-bota-v-telegram/poluchit-polnyi-vebkhuk-webhook-ot-telegram)

**caption** - описание до 1024 символов

**reply\_markup** — настройки кнопок [**\*\***](attachments.md#kak-propisyvat-knopki-v-parametre-reply_markup)

**parse\_mode** — выделение текста в описании жирным или курсивом [**\*\*\***](https://docs.salebot.pro/messendzhery-i-chaty/kak-sozdat-bota-v-telegram/razmetka-markdown.-formatirovanie-soobsheniya-v-telegram)**.** Может иметь значения html, markdown, markdownV2.

**reply\_to\_message\_id -** идентификатор сообщения, которое необходимо процитировать

**protect\_content** — признак защиты контента от копирования. Чтобы включить передайте любое значение, кроме 0, False и пустых кавычек ''

**disable\_notification** —  признак отправки сообщения со звуковым уведомлением (по умолчанию 0)\
1 - отключить уведомление при получении, 0 - передать с уведомлением

**message\_thread\_id** —  идентификатор темы (доступно для супергрупп при наличии функционала форума)\
\
**entities** — c ним вы можете просто копировать сверстанный текст со всеми особенностями и просто указать с какого символа по какой он будет отображаться с тем или иным шрифтом. Пример можете подсмотреть в tg\_request в соответствующем поле. В параметре должен быть словарь. \
\
Пример передачи параметра: \
`entities = [{"offset":0,"length":5,"type":"bold"},{"offset":6,"length":4,"type":"text_link","url":"https://salebot.zmservice.ru"},{"offset":11,"length":9,"type":"strikethrough"},{"offset":21,"length":6,"type":"spoiler"},{"offset":29,"length":12,"type":"code"}]`  \
\
В примере показан только словарь, при этом сама переменная с текстом сообщения задана в переменной.

Для упрощения описания набора кнопок можно воспользоваться следующим [лайфхаком](/broken/pages/wISNJgxY6Z4qnHu9dd3P#lifehak)

</details>

<details>

<summary>Отправить несколько документов или другие файлы tg_send_some_document()</summary>

<mark style="color:red;">**!**</mark> Данные функции позволяют отправить файлы любого типа, рекомендуемые - **GIF**, **PDF** и **ZIP** весом до 2Гб.

**tg\_send\_some\_document(platform\_id, document\_list, disable\_notification, protect\_content, reply\_to\_message\_id, message\_thread\_id)**

Параметры:

<mark style="color:red;">**!**</mark>**&#x20;platform\_id** — идентификатор клиента в Telegram, которому необходимо прислать сообщение [**\***](attachments.md#gde-vzyat-platform_id-dlya-otpravki-uvedomlenii)

<mark style="color:red;">**!**</mark>**&#x20;document\_list** - массив документов, пример построения такого массива рассмотрен ниже

**disable\_notification** —  признак отправки сообщения со звуковым уведомлением (по умолчанию 0)\
1 - отключить уведомление при получении, 0 - передать с уведомлением

**protect\_content** — признак защиты контента от копирования. Чтобы включить передайте любое значение, кроме 0, False и пустых кавычек ''

**reply\_to\_message\_id -** идентификатор сообщения, которое необходимо процитировать

**message\_thread\_id** —  идентификатор темы (доступно для супергрупп при наличии функционала форума)

**Пример построения массива document\_list:** \
'\[\["Ссылка на документ1", "caption", "parse\_mode"], \["Ссылка на документ 2"], \["Ссылка на документ 3", "caption"]]'&#x20;

**Пример записи данных для одного документа:** \
\["Ссылка на документ", "caption", "parse\_mode"]&#x20;

<mark style="color:red;">**Важен порядок параметров**</mark><mark style="color:red;">!</mark> При построении массива документов кавычки "" могут быть опущены

**Описание параметров для массива document\_list:** \
<mark style="color:red;">**!**</mark>**&#x20;Ссылка на документ** - ссылка на документ с сервера Telegram. Получение ссылки через tg\_request рассмотрено [тут](/broken/pages/YVEk70VIBhfL7aUZFo9F#kak-pri-pomoshi-tg_request-poluchit-ssylku-na-kartinku-foto-animaciyu-video)\
**caption** — описание до 1024 символов\
**parse\_mode** — разметка описания, т.е. выделение текста в описании жирным или курсивом  [**\*\*\***](https://docs.salebot.pro/messendzhery-i-chaty/kak-sozdat-bota-v-telegram/razmetka-markdown.-formatirovanie-soobsheniya-v-telegram)

</details>

Пример как отправить документ с помощью API Telegram [здесь](attachments.md#dokumenty-primer-kak-otpravit-s-pomoshyu-api-telegram).

{% embed url="https://youtu.be/XqZ6nmxyaa4" %}

<details>

<summary>Отправить голосовое сообщение <strong>tg_send_voice(</strong>)</summary>

<mark style="color:red;">!</mark> Данная функция позволяет отправить голосовые файлы типа .OGG, закодированные с помощью OPUS, весом до 2Гб.

<mark style="background-color:green;">**! Работает с бизнес-аккаунтом в Телеграм**</mark>

**tg\_send\_voice(platform\_id, voice, caption, reply\_markup, parse\_mode, reply\_to\_message\_id, protect\_content, disable\_notification, message\_thread\_id, entities)**&#x20;

Параметры:

<mark style="color:red;">**!**</mark>**&#x20;platform\_id** — идентификатор клиента в Telegram, которому необходимо прислать сообщение [**\***](attachments.md#gde-vzyat-platform_id-dlya-otpravki-uvedomlenii)

<mark style="color:red;">**!**</mark>**&#x20;voice** - ссылка на голосовое сообщение в формате  .OGG

**caption** - описание до 1024 символов

**reply\_markup** — настройки кнопок [**\*\***](attachments.md#kak-propisyvat-knopki-v-parametre-reply_markup)

**parse\_mode** — выделение текста в описании жирным или курсивом [**\*\*\***](https://docs.salebot.pro/messendzhery-i-chaty/kak-sozdat-bota-v-telegram/razmetka-markdown.-formatirovanie-soobsheniya-v-telegram)**.** Может иметь значения html, markdown, markdownV2.

**reply\_to\_message\_id -** идентификатор сообщения, которое необходимо процитировать

**protect\_content** — признак защиты контента от копирования. Чтобы включить передайте любое значение, кроме 0, False и пустых кавычек ''

**disable\_notification** —  признак отправки сообщения со звуковым уведомлением (по умолчанию 0)\
1 - отключить уведомление при получении, 0 - передать с уведомлением

**message\_thread\_id** —  идентификатор темы (доступно для супергрупп при наличии функционала форума)\
\
**entities** — c ним вы можете просто копировать сверстанный текст со всеми особенностями и просто указать с какого символа по какой он будет отображаться с тем или иным шрифтом. Пример можете подсмотреть в tg\_request в соответствующем поле. В параметре должен быть словарь. \
\
Пример передачи параметра: \
`entities = [{"offset":0,"length":5,"type":"bold"},{"offset":6,"length":4,"type":"text_link","url":"https://salebot.zmservice.ru"},{"offset":11,"length":9,"type":"strikethrough"},{"offset":21,"length":6,"type":"spoiler"},{"offset":29,"length":12,"type":"code"}]`  \
\
В примере показан только словарь, при этом сама переменная с текстом сообщения задана в переменной.

Для упрощения описания набора кнопок можно воспользоваться следующим [лайфхаком](/broken/pages/wISNJgxY6Z4qnHu9dd3P#lifehak)

</details>

<details>

<summary>Отправить несколько аудиосообщений <strong>tg_send_some_audio()</strong></summary>

<mark style="color:red;">**!**</mark> Данная функция позволяет отправить аудиофайлы типа .MP3 or .M4A размером не больше 2Гб.

<mark style="background-color:green;">**! Работает с бизнес-аккаунтом в Телеграм**</mark>

**tg\_send\_some\_audio(platform\_id, audio\_list, disable\_notification, protect\_content, reply\_to\_message\_id, message\_thread\_id)**&#x20;

Параметры:

<mark style="color:red;">**!**</mark>**&#x20;platform\_id** — идентификатор клиента в Telegram, которому необходимо прислать сообщение [**\***](attachments.md#gde-vzyat-platform_id-dlya-otpravki-uvedomlenii)

<mark style="color:red;">**!**</mark>**&#x20;audio\_list** - массив аудио (подробнее ниже)&#x20;

**disable\_notification** —  признак отправки сообщения со звуковым уведомлением (по умолчанию 0)\
1 - отключить уведомление при получении, 0 - передать с уведомлением

**protect\_content** — признак защиты контента от копирования. Чтобы включить передайте любое значение, кроме 0, False и пустых кавычек ''

**reply\_to\_message\_id -** идентификатор сообщения, которое необходимо процитировать

**message\_thread\_id** —  идентификатор темы (доступно для супергрупп при наличии функционала форума)



**Пример построения массива аудио audio\_list:** \
'\[\["Ссылка на аудио1", "caption", "parse\_mode"], \["Ссылка на аудио 2"], \["Ссылка на аудио 3", "caption"]]'&#x20;

**Пример записи данных одного** **аудио**: \
\["Ссылка на аудио", "caption", "parse\_mode"]&#x20;

<mark style="color:red;">**Важен порядок параметров!**</mark> При построении массива аудиофайлов кавычки "" могут быть опущены

**Описание параметров:** \
<mark style="color:red;">**!**</mark>**&#x20;Ссылка на аудио** - ссылка на аудио в формате .OGG\
**caption** — описание до 1024 символов \
**parse\_mode** — выделение текста в описании жирным или курсивом [**\*\*\***](https://docs.salebot.pro/messendzhery-i-chaty/kak-sozdat-bota-v-telegram/razmetka-markdown.-formatirovanie-soobsheniya-v-telegram)

</details>

Пример как отправить голосовое сообщение с помощью API Telegram [здесь](attachments.md#golosovoe-soobshenie).

{% embed url="https://youtu.be/vyhhhJF-3FY" %}

<details>

<summary>Отправить анимацию <strong>tg_send_animation()</strong></summary>

<mark style="color:red;">**!**</mark> Данная функция позволяет отправить файл типа GIF или H.264/MPEG-4 AVC видео без звука весом до 2Гб.

<mark style="background-color:green;">**! Работает с бизнес-аккаунтом в Телеграм**</mark>

**tg\_send\_animation(platform\_id, animation, caption, reply\_markup, parse\_mode, reply\_to\_message\_id, protect\_content, has\_spoiler, disable\_notification, message\_thread\_id, entities, show\_caption\_above\_media)**

Параметры:

<mark style="color:red;">**!**</mark>**&#x20;platform\_id** — идентификатор клиента в Telegram, которому необходимо прислать сообщение [**\***](attachments.md#gde-vzyat-platform_id-dlya-otpravki-uvedomlenii)

<mark style="color:red;">**!**</mark>**&#x20;animation**- ссылка на анимацию. Получение ссылки через tg\_request рассмотрено [тут](https://docs.salebot.pro/messendzhery-i-chaty/kak-sozdat-bota-v-telegram/poluchit-polnyi-vebkhuk-webhook-ot-telegram)

**caption** - описание до 1024 символов

**reply\_markup** — настройки кнопок [**\*\***](attachments.md#kak-propisyvat-knopki-v-parametre-reply_markup)

**parse\_mode** — выделение текста в описании жирным или курсивом [**\*\*\***](https://docs.salebot.pro/messendzhery-i-chaty/kak-sozdat-bota-v-telegram/razmetka-markdown.-formatirovanie-soobsheniya-v-telegram)**.** Может иметь значения html, markdown, markdownV2.

**reply\_to\_message\_id -** идентификатор сообщения, которое необходимо процитировать

**protect\_content** — признак защиты контента от копирования. Чтобы включить передайте любое значение, кроме 0, False и пустых кавычек ''

**has\_spoiler** — создание спойлера. Чтобы включить,  передайте True

**disable\_notification** —  признак отправки сообщения со звуковым уведомлением (по умолчанию 0)\
1 - отключить уведомление при получении, 0 - передать с уведомлением

**message\_thread\_id** —  идентификатор темы (доступно для супергрупп при наличии функционала форума)\
\
**entities** — c ним вы можете просто копировать сверстанный текст со всеми особенностями и просто указать с какого символа по какой он будет отображаться с тем или иным шрифтом. Пример можете подсмотреть в tg\_request в соответствующем поле. В параметре должен быть словарь.&#x20;

**show\_caption\_above\_media** - принимает значение True, если указать этот параметр, то текст сообщения будет расположен над вложением\
\
Пример передачи параметра: \
`entities = [{"offset":0,"length":5,"type":"bold"},{"offset":6,"length":4,"type":"text_link","url":"https://salebot.zmservice.ru"},{"offset":11,"length":9,"type":"strikethrough"},{"offset":21,"length":6,"type":"spoiler"},{"offset":29,"length":12,"type":"code"}]`  \
\
В примере показан только словарь, при этом сама переменная с текстом сообщения задана в переменной.

Для упрощения описания набора кнопок можно воспользоваться следующим [лайфхаком](/broken/pages/wISNJgxY6Z4qnHu9dd3P#lifehak)

</details>

Пример как отправить анимацию с помощью API Telegram [здесь](attachments.md#animaciya-primer-kak-otpravit-s-pomoshyu-api-telegram).

{% embed url="https://youtu.be/A2dhfS_ltEQ" %}

<details>

<summary>Отправить видео с помощью API Telegram <strong>tg_send_video()</strong></summary>

<mark style="color:red;">**!**</mark> Данная функция позволяет отправить файл типа MPEG4  весом до 2Гб. \
(иные форматы можно отправить как файлы через tg\_send\_document())

<mark style="background-color:green;">**! Работает с бизнес-аккаунтом в Телеграм**</mark>

**tg\_send\_video(platform\_id, video, caption, reply\_markup, parse\_mode, reply\_to\_message\_id, protect\_content, has\_spoiler, disable\_notification, message\_thread\_id, entities,** show\_caption\_above\_media, cover **)**

Параметры:

<mark style="color:red;">**!**</mark>**&#x20;platform\_id** — идентификатор клиента в Telegram, которому необходимо прислать сообщение [**\***](attachments.md#gde-vzyat-platform_id-dlya-otpravki-uvedomlenii)

<mark style="color:red;">**!**</mark>**&#x20;video** - ссылка на видео. Получение ссылки через tg\_request рассмотрено [тут](https://docs.salebot.pro/messendzhery-i-chaty/kak-sozdat-bota-v-telegram/poluchit-polnyi-vebkhuk-webhook-ot-telegram)

**caption** - описание до 1024 символов

**reply\_markup** — настройки кнопок [**\*\***](attachments.md#kak-propisyvat-knopki-v-parametre-reply_markup)

**parse\_mode** — выделение текста в описании жирным или курсивом [**\*\*\***](https://docs.salebot.pro/messendzhery-i-chaty/kak-sozdat-bota-v-telegram/razmetka-markdown.-formatirovanie-soobsheniya-v-telegram)**.** Может иметь значения html, markdown, markdownV2.

**reply\_to\_message\_id -** идентификатор сообщения, которое необходимо процитировать

**protect\_content** — признак защиты контента от копирования. Чтобы включить передайте любое значение, кроме 0, False и пустых кавычек ''

**has\_spoiler** — создание спойлера. Чтобы включить,  передайте True

**disable\_notification** —  признак отправки сообщения со звуковым уведомлением (по умолчанию 0)\
1 - отключить уведомление при получении, 0 - передать с уведомлением

**message\_thread\_id** —  идентификатор темы (доступно для супергрупп при наличии функционала форума)\
\
**entities** — c ним вы можете просто копировать сверстанный текст со всеми особенностями и просто указать с какого символа по какой он будет отображаться с тем или иным шрифтом. Пример можете подсмотреть в tg\_request в соответствующем поле. В параметре должен быть словарь

show\_caption\_above\_media - принимает значение True, если указать этот параметр, то текст сообщения будет расположен над вложением

cover - обложка для видео в сообщении. Получение ссылки через tg\_request [тут](https://docs.salebot.pro/messendzhery-i-chaty/kak-sozdat-bota-v-telegram/poluchit-polnyi-vebkhuk-webhook-ot-telegram). \
\
Пример передачи параметра: \
`entities = [{"offset":0,"length":5,"type":"bold"},{"offset":6,"length":4,"type":"text_link","url":"https://salebot.zmservice.ru"},{"offset":11,"length":9,"type":"strikethrough"},{"offset":21,"length":6,"type":"spoiler"},{"offset":29,"length":12,"type":"code"}]`  \
\
В примере показан только словарь, при этом сама переменная с текстом сообщения задана в переменной.

Для упрощения описания набора кнопок можно воспользоваться следующим [лайфхаком](/broken/pages/wISNJgxY6Z4qnHu9dd3P#lifehak)

</details>

<details>

<summary>Отправить несколько видео с помощью API Telegram <strong>tg_send_some_video()</strong></summary>

<mark style="background-color:green;">**! Работает с бизнес-аккаунтом в Телеграм**</mark>

**tg\_send\_some\_video(platform\_id, video\_list, disable\_notification, protect\_content, reply\_to\_message\_id, has\_spoiler, message\_thread\_id)**&#x20;

Параметры:

<mark style="color:red;">**!**</mark>**&#x20;platform\_id** — идентификатор клиента в Telegram, которому необходимо прислать сообщение [**\***](attachments.md#gde-vzyat-platform_id-dlya-otpravki-uvedomlenii)

<mark style="color:red;">**!**</mark>**&#x20;video\_list** - массив видео (подробнее ниже)&#x20;

**disable\_notification** —  признак отправки сообщения со звуковым уведомлением (по умолчанию 0)\
1 - отключить уведомление при получении, 0 - передать с уведомлением

**reply\_to\_message\_id -** идентификатор сообщения, которое необходимо процитировать

**has\_spoiler** — создание спойлера (необязательный параметр, если требуется включить, то передайте True)

**message\_thread\_id** —  идентификатор темы (доступно для супергрупп при наличии функционала форума)



**Пример построения массива видео video\_list:** \
'\[\["Ссылка на видео1", "caption", "parse\_mode"], \["Ссылка на видео2"], \["Ссылка на видео3", "caption"]]'

**Пример записи данных одного видео:** \
\["Ссылка на видео", "caption", "parse\_mode"]&#x20;

<mark style="color:red;">**Важен порядок параметров!**</mark> При построении массива видео кавычки могут быть опущены

**Описание параметров:** \
<mark style="color:red;">**!**</mark>**&#x20;Ссылка на видео** — ссылка на видео внутрення Telegram. Получение ссылки через tg\_request рассмотрено [тут](/broken/pages/YVEk70VIBhfL7aUZFo9F#kak-pri-pomoshi-tg_request-poluchit-ssylku-na-kartinku-foto-animaciyu-video)\
**caption** — подпись до 1024 символов\
**parse\_mode** — выделение текста в описании жирным или курсивом [**\*\*\***](https://docs.salebot.pro/messendzhery-i-chaty/kak-sozdat-bota-v-telegram/razmetka-markdown.-formatirovanie-soobsheniya-v-telegram)**.** Может иметь значения html, markdown, markdownV2.

</details>

Пример как отправить видео с помощью API Telegram [здесь](attachments.md#video-primer-kak-otpravit-s-pomoshyu-api-telegram).

{% embed url="https://youtu.be/HBfOdIMhFSI" %}

<details>

<summary>Отправить геоточку <strong>tg_send_venue()</strong></summary>

<mark style="background-color:green;">**! Работает с бизнес-аккаунтом в Телеграм**</mark>

**tg\_send\_venue(platform\_id, latitude, longitude, title, address, protect\_content, disable\_notification, reply\_to\_message\_id, reply\_markup, message\_thread\_id)**&#x20;

Параметры:

<mark style="color:red;">**!**</mark>**&#x20;platform\_id** — идентификатор клиента в Telegram, которому необходимо прислать сообщение [**\***](attachments.md#gde-vzyat-platform_id-dlya-otpravki-uvedomlenii)

<mark style="color:red;">**!**</mark>**&#x20;latitude** —широта

<mark style="color:red;">**!**</mark>**&#x20;longitude** — долгота

<mark style="color:red;">**!**</mark>**&#x20;title** — название

<mark style="color:red;">**!**</mark>**&#x20;address** — адрес

**protect\_content** — признак защиты контента от копирования. Чтобы включить передайте любое значение, кроме 0, False и пустых кавычек ''

**disable\_notification** —  признак отправки сообщения со звуковым уведомлением (по умолчанию 0)\
1 - отключить уведомление при получении, 0 - передать с уведомлением

**reply\_to\_message\_id -** идентификатор сообщения, которое необходимо процитировать

**reply\_markup** — настройки кнопок [**\*\***](attachments.md#kak-propisyvat-knopki-v-parametre-reply_markup)

**message\_thread\_id** —  идентификатор темы (доступно для супергрупп при наличии функционала форума)

Для упрощения описания набора кнопок можно воспользоваться следующим [лайфхаком](/broken/pages/wISNJgxY6Z4qnHu9dd3P#lifehak)

</details>

Пример как отправить геоточку с помощью API Telegram [здесь](attachments.md#geotochka-primer-kak-otpravit-s-pomoshyu-api-telegram).

{% embed url="https://youtu.be/RorQNYodc2U" %}

<details>

<summary>Отправить контакт <strong>tg_send_contact()</strong></summary>

<mark style="background-color:green;">**! Работает с бизнес-аккаунтом в Телеграм**</mark>

В Telegram есть быстрый способ обменяться контактами из записной книжки. Мессенджер поддерживает отправку данных vCard — электронной визитной карточки.&#x20;

Функция tg\_send\_contact позволяет отправить контактный номер телефона с именем(названием организации). А также добавить к сообщению кнопки и настроить защиту контента для сообщения.



**tg\_send\_contact(platform\_id, phone, first\_name, last\_name, protect\_content, disable\_notification, reply\_to\_message\_id, reply\_markup, message\_thread\_id)**&#x20;

<mark style="color:red;">**! - обязательный параметр функции**</mark>

Параметры:

<mark style="color:red;">**!**</mark>**&#x20;platform\_id** — идентификатор клиента в Telegram, которому необходимо прислать сообщение [**\***](attachments.md#gde-vzyat-platform_id-dlya-otpravki-uvedomlenii)

<mark style="color:red;">**!**</mark>**&#x20;phone** — номер телефона в международном формате. Например, для РФ это +7XXXXXXXXXX

<mark style="color:red;">**!**</mark>**&#x20;first\_name** и **last\_name** - имя и фамилия, соответственно&#x20;

**protect\_content** — признак защиты контента от копирования. Чтобы включить передайте любое значение, кроме 0, False и пустых кавычек ''

**disable\_notification** —  признак отправки сообщения со звуковым уведомлением (по умолчанию 0)\
1 - отключить уведомление при получении, 0 - передать с уведомлением

**reply\_to\_message\_id -** идентификатор сообщения, которое необходимо процитировать

**reply\_markup** — настройки кнопок [**\*\***](attachments.md#kak-propisyvat-knopki-v-parametre-reply_markup)

**message\_thread\_id** —  идентификатор темы (доступно для супергрупп при наличии функционала форума)

Для упрощения описания набора кнопок можно воспользоваться следующим [лайфхаком](/broken/pages/wISNJgxY6Z4qnHu9dd3P#lifehak)

</details>

Пример как отправить контакт с помощью API Telegram [здесь](attachments.md#kontakt-primer-kak-otpravit-s-pomoshyu-api-telegram).

{% embed url="https://youtu.be/l-BxWtdjNz8" %}

<details>

<summary>Отправить стикер <strong>tg_send_sticker()</strong></summary>

<mark style="background-color:green;">**! Работает с бизнес-аккаунтом в Телеграм**</mark>

**tg\_send\_sticker(platform\_id, sticker\_id, protect\_content,  disable\_notification, reply\_to\_message\_id, reply\_markup, message\_thread\_id)**&#x20;

Параметры:

<mark style="color:red;">**!**</mark>**&#x20;platform\_id** — идентификатор клиента в Telegram, которому необходимо прислать сообщение [**\***](attachments.md#gde-vzyat-platform_id-dlya-otpravki-uvedomlenii)

<mark style="color:red;">**!**</mark>**&#x20;sticker\_id** - идентификатор стикера. Получение ссылки через tg\_request рассмотрено [тут](https://docs.salebot.pro/messendzhery-i-chaty/kak-sozdat-bota-v-telegram/poluchit-polnyi-vebkhuk-webhook-ot-telegram)

**protect\_content** — признак защиты контента от копирования. Чтобы включить передайте любое значение, кроме 0, False и пустых кавычек ''

**disable\_notification** —  признак отправки сообщения со звуковым уведомлением (по умолчанию 0)\
1 - отключить уведомление при получении, 0 - передать с уведомлением

**reply\_to\_message\_id -** идентификатор сообщения, которое необходимо процитировать

**reply\_markup** — настройки кнопок [**\*\***](attachments.md#kak-propisyvat-knopki-v-parametre-reply_markup)

**message\_thread\_id** —  идентификатор темы (доступно для супергрупп при наличии функционала форума)

Для упрощения описания набора кнопок можно воспользоваться следующим [лайфхаком](/broken/pages/wISNJgxY6Z4qnHu9dd3P#lifehak)

</details>

Пример как отправить стикер с помощью API Telegram [здесь](attachments.md#stiker-primer-kak-otpravit-s-pomoshyu-api-telegram).

{% embed url="https://youtu.be/OVHl5D4nFHM" %}

<details>

<summary>Отправить картинку <strong>tg_send_photo()</strong></summary>

<mark style="color:red;">**!**</mark> Фотография должна быть размером не более 10 МБ. Суммарная ширина и высота фотографии не должны превышать 10000. Соотношение ширины и высоты должно быть не более 20.

<mark style="background-color:green;">**! Работает с бизнес-аккаунтом в Телеграм**</mark>

**tg\_send\_photo(platform\_id, photo, caption, reply\_markup, parse\_mode, reply\_to\_message\_id, protect\_content, has\_spoiler, disable\_notification, message\_thread\_id, entities, show\_caption\_above\_media)**

Параметры:

<mark style="color:red;">**!**</mark>**&#x20;platform\_id** — идентификатор клиента в Telegram, которому необходимо прислать сообщение [**\***](attachments.md#gde-vzyat-platform_id-dlya-otpravki-uvedomlenii)

<mark style="color:red;">**!**</mark>**&#x20;photo** - ссылка на картинку. Получение ссылки через tg\_request рассмотрено [тут](https://docs.salebot.pro/messendzhery-i-chaty/kak-sozdat-bota-v-telegram/poluchit-polnyi-vebkhuk-webhook-ot-telegram)

**caption** - описание до 1024 символов

**reply\_markup** — настройки кнопок [**\*\***](attachments.md#kak-propisyvat-knopki-v-parametre-reply_markup)

**parse\_mode** — выделение текста в описании жирным или курсивом [**\*\*\***](https://docs.salebot.pro/messendzhery-i-chaty/kak-sozdat-bota-v-telegram/razmetka-markdown.-formatirovanie-soobsheniya-v-telegram)

**reply\_to\_message\_id -** идентификатор сообщения, которое необходимо процитировать

**protect\_content** — признак защиты контента от копирования. Чтобы включить передайте любое значение, кроме 0, False и пустых кавычек ''

**has\_spoiler** — создание спойлера. Чтобы включить,  передайте True

**disable\_notification** —  признак отправки сообщения со звуковым уведомлением (по умолчанию 0)\
1 - отключить уведомление при получении, 0 - передать с уведомлением

**message\_thread\_id** —  идентификатор темы (доступно для супергрупп при наличии функционала форума)\
\
**entities** — c ним вы можете просто копировать сверстанный текст со всеми особенностями и просто указать с какого символа по какой он будет отображаться с тем или иным шрифтом. Пример можете подсмотреть в tg\_request в соответствующем поле. В параметре должен быть словарь.&#x20;

show\_caption\_above\_media - принимает значение True, если указать этот параметр, то текст сообщения будет расположен над вложением\
\
Пример передачи параметра: \
`entities = [{"offset":0,"length":5,"type":"bold"},{"offset":6,"length":4,"type":"text_link","url":"https://salebot.zmservice.ru"},{"offset":11,"length":9,"type":"strikethrough"},{"offset":21,"length":6,"type":"spoiler"},{"offset":29,"length":12,"type":"code"}]`  \
\
В примере показан только словарь, при этом сама переменная с текстом сообщения задана в переменной.

Для упрощения описания набора кнопок можно воспользоваться следующим [лайфхаком](/broken/pages/wISNJgxY6Z4qnHu9dd3P#lifehak)

</details>

<details>

<summary>Отправить несколько картинок <strong>tg_send_some_photo()</strong></summary>

<mark style="color:red;">**!**</mark> Фотография должна быть размером не более 10 МБ. Суммарная ширина и высота фотографии не должны превышать 10000. Соотношение ширины и высоты должно быть не более 20.

<mark style="background-color:green;">**! Работает с бизнес-аккаунтом в Телеграм**</mark>

**tg\_send\_some\_photo(platform\_id, image\_list, disable\_notification=0**, **protect\_content=False, reply\_to\_message\_id=0, has\_spoiler=False,message\_thread\_id)**

Параметры:

<mark style="color:red;">**!**</mark>**&#x20;platform\_id** — идентификатор клиента в Telegram, которому необходимо прислать сообщение [**\***](attachments.md#gde-vzyat-platform_id-dlya-otpravki-uvedomlenii)

<mark style="color:red;">**!**</mark>**&#x20;image\_list** - массив картинок (подробнее ниже)&#x20;

**disable\_notification** —  признак отправки сообщения со звуковым уведомлением (по умолчанию 0)\
1 - отключить уведомление при получении, 0 - передать с уведомлением

**protect\_content** — для защиты от копирования (необязательный параметр, если нужно включить, то передайте в качестве параметра 1)

**reply\_to\_message\_id -** идентификатор сообщения, которое необходимо процитировать

**has\_spoiler** — создание спойлера (необязательный параметр, если требуется включить, то передайте True)

**message\_thread\_id** —  идентификатор темы (доступно для супергрупп при наличии функционала форума)<br>

**Пример image\_list:**

`'[["Ссылка на картинку 1", "caption", "parse_mode"], ["Ссылка на картинку 2"], ["Ссылка на картинку 3", "caption"]]'`

**Пример данных одной картинки:** \
\["Ссылка на картинку 1", "caption", "parse\_mode"]&#x20;

<mark style="color:red;">**Важен порядок параметров!**</mark> При построении массива картинок кавычки могут быть опущены

**Описание параметров:&#x20;**&#x20;

<mark style="color:red;">**!**</mark>**&#x20;Ссылка на картинку 1** - ссылка на картинку. Получение ссылки через tg\_request рассмотрено [тут](https://docs.salebot.pro/messendzhery-i-chaty/kak-sozdat-bota-v-telegram/poluchit-polnyi-vebkhuk-webhook-ot-telegram)

**caption** — подпись до 1024 символов &#x20;

**parse\_mode** — выделение текста в описании жирным или курсивом [**\*\*\***](https://docs.salebot.pro/messendzhery-i-chaty/kak-sozdat-bota-v-telegram/razmetka-markdown.-formatirovanie-soobsheniya-v-telegram)

</details>

{% hint style="warning" %}
Для понимания: Параметр caption это описание картинки (описание - краткое содержание или подпись с пояснением к изображению). Если caption указать при отправке одной картинке, то сообщение придет с текстом и вложением.&#x20;

В случае когда каждая картинка имеет описание, то к каждой картинке придет описание. Отображается при нажатии на картинку.&#x20;

Данную информацию и принцип работы функции вы можете так же узнать в официальной документации Telegram.&#x20;

\*Если выполняете настройки по видео-инструкции, то просмотрите ее, пожалуйста, внимательно.
{% endhint %}

Пример как отправить стикер с помощью API Telegram [здесь](attachments.md#kartinka-neskolko-kartinok-primer-kak-otpravit-s-pomoshyu-api-telegram).

{% embed url="https://youtu.be/LqX7tBk7brE" %}

<details>

<summary>Отправить круглое видео <strong>tg_send_video_note()</strong></summary>

<mark style="color:red;">**!**</mark> Начиная с версии 4.0, Telegram поддерживает отправку круглого видео в формате MPEG4 и длительностью не больше минуты.

<mark style="background-color:green;">**! Работает с бизнес-аккаунтом в Телеграм**</mark>

**tg\_send\_video\_note(platform\_id, video\_note,  reply\_markup, protect\_content, reply\_to\_message\_id, disable\_notification,  message\_thread\_id)** &#x20;

Параметры:

<mark style="color:red;">**!**</mark>**&#x20;platform\_id** — идентификатор клиента в Telegram, которому необходимо прислать сообщение [**\***](attachments.md#gde-vzyat-platform_id-dlya-otpravki-uvedomlenii)

<mark style="color:red;">**!**</mark>**&#x20;video\_note** - ссылка на видео. Получение ссылки через tg\_request рассмотрено [тут](https://docs.salebot.pro/messendzhery-i-chaty/kak-sozdat-bota-v-telegram/poluchit-polnyi-vebkhuk-webhook-ot-telegram)\
**reply\_markup** — настройки кнопок [**\*\***](attachments.md#kak-propisyvat-knopki-v-parametre-reply_markup)

**protect\_content** — признак защиты контента от копирования. Чтобы включить передайте любое значение, кроме 0, False и пустых кавычек ''

**reply\_to\_message\_id -** идентификатор сообщения, которое необходимо процитировать

**disable\_notification** —  признак отправки сообщения со звуковым уведомлением (по умолчанию 0)\
1 - отключить уведомление при получении, 0 - передать с уведомлением

**message\_thread\_id** —  идентификатор темы (доступно для супергрупп при наличии функционала форума)

Для упрощения описания набора кнопок можно воспользоваться следующим [лайфхаком](/broken/pages/wISNJgxY6Z4qnHu9dd3P#lifehak)

</details>



Пример как отправить круглое видео с помощью API Telegram [здесь](attachments.md#krugloe-video-primer-kak-otpravit-s-pomoshyu-api-telegram).

{% embed url="https://youtu.be/jAj13tPUcXQ" %}

<details>

<summary>Отправить эмодзи со случайным выбором (Dice) <strong>tg_send_dice()</strong> </summary>

**tg\_send\_dice(platform\_id, emoji, reply\_markup, disable\_notification, reply\_to\_message\_id, protect\_content, message\_thread\_id)**

<mark style="background-color:green;">**! Работает с бизнес-аккаунтом в Телеграм**</mark>

Параметры:

<mark style="color:red;">**!**</mark>**&#x20;platform\_id** — идентификатор клиента в Telegram, которому необходимо прислать сообщение [**\***](attachments.md#gde-vzyat-platform_id-dlya-otpravki-uvedomlenii)

**emoji** - эмодзи, которое требуется отправить.Если оставить параметр незаполненным, то по умолчанию отправит кубик. Вы можете передавать в этом параметре как эмодзи в виде строки, так и ключевое слово, используемое для его обозначения.

**reply\_markup** — настройки кнопок [**\*\***](attachments.md#kak-propisyvat-knopki-v-parametre-reply_markup)

**disable\_notification** —  признак отправки сообщения со звуковым уведомлением (по умолчанию 0)\
1 - отключить уведомление при получении, 0 - передать с уведомлением

**reply\_to\_message\_id -** идентификатор сообщения, которое необходимо процитировать

**protect\_content** — признак защиты контента от копирования. Чтобы включить передайте любое значение, кроме 0, False и пустых кавычек ''

**message\_thread\_id** —  идентификатор темы (доступно для супергрупп при наличии функционала форума)

Для упрощения описания набора кнопок можно воспользоваться следующим [лайфхаком](/broken/pages/wISNJgxY6Z4qnHu9dd3P#lifehak)

&#x20;

**Список возможных emoji:** \
1\) 'darts' или '🎯', для значений от 1 до 6 \
2\) 'dice' или '🎲', для значений от 1 до 6 \
3\) 'bowling' или '🎳', для значений от 1 до 6 \
4\) 'basketball' или '🏀', для значений от 1 до 5 \
5\) 'football' или '⚽', для значений от 1 до 5 \
6\) 'slots' или '🎰', для значений от 1 до 64 \
Также если клиент отправит боту одно из этих эмодзи, то вы получите коллбэк с информацией о количестве очков и какое использовалось эмодзи.

</details>

Пример как отправить эмодзи со случайным выбором [здесь](attachments.md#emodzi-primer-kak-otpravit-emodzi-so-sluchainym-vyborom-dice).

<details>

<summary>Отправить медиа группу tg_send_media_group()</summary>

<mark style="background-color:green;">**! Работает с бизнес-аккаунтом в Телеграм**</mark>

Метод, чтобы отправить группу фотографий, видео, документов или аудио в виде альбома. В случае успеха возвращается массив отправленных файлов.

<mark style="color:orange;">**Помните, что документы и аудиофайлы нельзя группировать с другим типами файлов!**</mark>

tg\_send\_media\_group(platform\_id, media\_list, disable\_notification, protect\_content, reply\_to\_message\_id, message\_thread\_id)

Параметры:

<mark style="color:red;">!</mark> platform\_id — идентификатор клиента в Telegram, которому необходимо отправить сообщение;

<mark style="color:red;">!</mark> media\_list - массив, содержащий от 2 до 10 фотографий, видео, документов или аудио (подробнее ниже);

disable\_notification — признак отправки сообщения со звуковым уведомлением (по умолчанию 0) 1 - отключить уведомление при получении, 0 - передать с уведомлением;

protect\_content — признак защиты контента от копирования. Чтобы включить передайте любое значение, кроме 0, False и пустых кавычек '';

reply\_to\_message\_id - идентификатор сообщения, которое необходимо процитировать;

message\_thread\_id — идентификатор темы (доступно для супергрупп при наличии функционала форума);

**Содержание элементов массива media\_list:**

<mark style="color:red;">!</mark> type - тип файла, “photo”, “video”, “audio” или ”document”

<mark style="color:red;">!</mark> media - Файл для отправки. Передайте file\_id для отправки файла, который существует на серверах Telegram (рекомендуется), передайте URL-адрес HTTP для Telegram, чтобы получить файл из Интернета, или передайте «attach://\<file\_attach\_name>», чтобы загрузить новый, используя multipart/form-data под именем \<file\_attach\_name>.

Подробнее: [https://core.telegram.org/bots/api#sending-files](https://core.telegram.org/bots/api#sending-files)

caption — Заголовок отправляемого файла, 0–1024 символа.

parse\_mode — Режим анализа сущностей в заголовке файла.

Подробнее: [https://core.telegram.org/bots/api#sending-files](https://core.telegram.org/bots/api#sending-files)

Пример массива media\_list:

\[{"type": "photo", "media": "AgACAgIAAxkBAAIKa2W6HqQG151EaWOKnCyy8feBi8p\_AAIH1zEbicvYSfi2QYj-CMreAQADAgADeAADNAQ", "caption": "фото приведений"}, {"type": "video", "media": "BAACAgIAAxkBAAIKpGW6P\_HGDoVz7u4blDF6925WO-hmAALVPQACicvYSYwIWCJKwKIWNAQ", “caption”: “видео с зайчиком”}]

</details>

{% embed url="https://youtu.be/nYnZaOPnDo4" %}

## Примеры работы с функциями

### **Документы: Пример как отправить с помощью API Telegram**

{% tabs %}
{% tab title="Пример" %}
Разберем пример с отправкой одного документа, добавим инлайн-кнопки и описание к  документу:

1. Для начала получите ссылку на Ваш документ. [Как это сделать подробно описано тут](/broken/pages/YVEk70VIBhfL7aUZFo9F#kak-poluchit-ssylku-na-media-s-pomoshyu-peremennoi).&#x20;
2.  Создаем блок, задаем переменные, как на скрине:<br>

    <figure><img src="../../../../.gitbook/assets/image (652).png" alt=""><figcaption></figcaption></figure>
3. Отправляем блок себе и видим результат нашей работы:

<figure><img src="../../../../.gitbook/assets/image (653).png" alt=""><figcaption></figcaption></figure>

Теперь разберем отправку нескольких документов

1. Тут также необходимо получит на каждый документ внутреннюю ссылку Telegram и сформировать массив\
   lnkdoc='\[\["BQACAgIAAxkBAAIQA2O8oEMNYPTgjLvglZ63HIYYOBwFAALvHwACtjXoSXFhhNvRN6MGLQQ", "Документ1"],\["BQACAgIAAxkBAAIQA2O8oEMNYPTgjLvglZ63HIYYOBwFAALvHwACtjXoSXFhhNvRN6MGLQQ", "Документ2"]]'
2. В окончании собираем функцию отправки документов:

<figure><img src="../../../../.gitbook/assets/image (654).png" alt=""><figcaption></figcaption></figure>

3\. Любуемся результатом нашего труда:

<figure><img src="../../../../.gitbook/assets/image (655).png" alt=""><figcaption></figcaption></figure>
{% endtab %}

{% tab title="Пример кода для копирования" %}
<mark style="color:red;">Не забывайте ссылки уникальны для каждого бота, поэтому не забудьте сформировать свои ссылки</mark>

Пример кода для отправки одного документа:

```
lnkdoc= "BQACAgIAAxkBAAIQA2O8oEMNYPTgjLvglZ63HIYYOBwFAALvHwACtjXoSXFhhNvRN6MGLQQ"
opts = {"inline_keyboard": [[{"text": "Отлично","callback_data":"Ответ1"}, {"text": "Не принято","callback_data":"Ответ2"}]]}
soob=tg_send_document(platform_id, lnkdoc, "Отправка документа", opts) 
```

Пример кода для отправки нескольких документов:

```
lnkdoc='[["BQACAgIAAxkBAAIQA2O8oEMNYPTgjLvglZ63HIYYOBwFAALvHwACtjXoSXFhhNvRN6MGLQQ", "Документ1"],["BQACAgIAAxkBAAIQA2O8oEMNYPTgjLvglZ63HIYYOBwFAALvHwACtjXoSXFhhNvRN6MGLQQ", "Документ2"]]'
soob=tg_send_some_document(platform_id, lnkdoc)
```
{% endtab %}
{% endtabs %}

Описание всех параметров для функции отправки документов [в этой статье.](attachments.md#otpravit-dokument-tg_send_document)

### Голосовое сообщение

{% tabs %}
{% tab title="Пример" %}
Как сказано в описании функция работает с файлами типа .OGG. Таким образом, первая задача - получение аудиозаписи в данном формате. \
Если у Вас файл .MP3, то Вы сможете его преобразовать в формат .OGG при помощи бота [https://t.me/mp3toolsbot](https://t.me/mp3toolsbot)

Далее полученный файл отправляете себе в бот для получения file\_id по алгоритму, который [описан тут.](attachments.md#dokumenty-primer-kak-otpravit-s-pomoshyu-api-telegram)

Собираем функцию:

<figure><img src="../../../../.gitbook/assets/image (656).png" alt=""><figcaption></figcaption></figure>

Отлично! Мы молодцы!
{% endtab %}

{% tab title="Пример для копирования" %}
<mark style="color:red;">Не забывайте ссылки уникальны для каждого бота, поэтому не забудьте сформировать свою ссылку</mark>

```
tg_send_voice(platform_id, "CQACAgIAAxkBAAER70Bi8VkgNhegB-msqDWXm2qHi3n9-AAC-iAAAk6giUvIXkW-XzBN0ikE")
```
{% endtab %}
{% endtabs %}

Описание всех параметров для функции отправки голосового сообщения [в этой статье.](attachments.md#otpravit-golosovoe-soobshenie-tg_send_voice)

### Ошибка при отправке голосовых сообщений

В случае, если сообщение не отправилось из-за настроек конфиденциальности, то возвращается следующая ошибка:

<mark style="color:red;">{"ok":false,"error\_code":400,"description":"Bad Request: user restricted receiving of voice messages"}</mark>

Суть ошибки: наличие в настройках конфиденциальности вашего пользователя "Не получать голосовые сообщения" (от всех или получать только от определенных пользователей):

<figure><img src="../../../../.gitbook/assets/Снимок экрана 2024-09-18 в 17.15.46.png" alt="" width="375"><figcaption></figcaption></figure>

Причем, если пользователь и отключит данную настройку конфиденциальности, то ошибка все равно будет приходить.&#x20;

Причем только полное удаление клиента из базы Salebot помогает преодолеть данную ошибку, хотя и пользователь уже включил разрешение.

<mark style="color:green;">**Решение:**</mark>&#x20;

После того, как пользователь изменил настройки конфиденциальности, нужно выждать паузу 30-60 секунд (пока сервера мессенджера обработают изменения), и после этого отправить ботом API запрос в Telegram:\
<mark style="color:green;">**https://api.telegram.org/bot\<TOKEN>/getChat?chat\_id=#{platform\_id}**</mark>

После этого данные о пользователе обновятся и голосовые сообщения уходят корректно.&#x20;

### **А**нимация: : **Пример как отправить** с помощью API Telegram&#x20;

{% tabs %}
{% tab title="Пример" %}
Давайте усложним задачу и отправим анимацию с защитой от копирования и со спойлером.

Итак, работа как всегда начинается с получения внутренний ссылки Telegram на выбранную нами анимацию ([подробно тут](/broken/pages/YVEk70VIBhfL7aUZFo9F#kak-poluchit-ssylku-na-media-s-pomoshyu-peremennoi))

<figure><img src="../../../../.gitbook/assets/image (657).png" alt=""><figcaption></figcaption></figure>

Собираем функцию:

<figure><img src="../../../../.gitbook/assets/image (658).png" alt=""><figcaption></figcaption></figure>

И проверяем нашу работу:

<figure><img src="../../../../.gitbook/assets/image (659).png" alt=""><figcaption></figcaption></figure>
{% endtab %}

{% tab title="Пример кода для копирования" %}
<mark style="color:red;">Не забывайте ссылки уникальны для каждого бота, поэтому не забудьте сформировать свою ссылку</mark>

```
animation="CgACAgIAAxkBAAIQDWO9Dbb0QODBmI_CUMhKHoWch7MDAAJBIQACtjXoScUjA-n5kGCYLQQ"
caption = "С Новым Годом!"
soob=tg_send_animation(platform_id, animation, caption, None, None, None, True,True)
```
{% endtab %}
{% endtabs %}

Описание всех параметров для функции отправки анимации [в этой статье.](attachments.md#otpravit-animaciyu-tg_send_animation)

### **Видео**: **Пример как отправить** с помощью API Telegram

{% tabs %}
{% tab title="Пример" %}
Итак,  начинаем работу с получения ссылки на отправляемый файл ([как получить ссылку, рассказали здесь](/broken/pages/YVEk70VIBhfL7aUZFo9F#kak-poluchit-ssylku-na-media-s-pomoshyu-peremennoi)) и после заполняем необходимые параметры функции:

<figure><img src="../../../../.gitbook/assets/image (660).png" alt=""><figcaption><p>Получение ссылки на видео через tg_request</p></figcaption></figure>

<figure><img src="../../../../.gitbook/assets/image (661).png" alt=""><figcaption><p>Функция отправки видео</p></figcaption></figure>

При проверке получим наше видео:

<figure><img src="../../../../.gitbook/assets/image (662).png" alt=""><figcaption></figcaption></figure>
{% endtab %}

{% tab title="Пример кода для копирования" %}
<mark style="color:red;">Не забывайте ссылки уникальны для каждого бота, поэтому не забудьте сформировать свою ссылку на видео</mark>

```
video="BAACAgIAAxkBAAIQFmO9Ycbt5JDIr9HKQh-XkhS9FqTxAALQIwACtjXoSXKlqfbH-I_gLQQ"
soob=tg_send_video(platform_id, video
```
{% endtab %}
{% endtabs %}

Описание всех параметров для функции отправки видео [в этой статье.](attachments.md#otpravit-video-s-pomoshyu-api-telegram)

### Геоточка: **Пример как отправить** с помощью API Telegram

{% tabs %}
{% tab title="Пример" %}
Итак, начнем с определения координат места. Получить их можно через [Google.Карты ](https://www.google.com/maps)

<figure><img src="../../../../.gitbook/assets/image (663).png" alt=""><figcaption></figcaption></figure>

Далее преобразовать полученные координаты из десятичных градусов в географические в любом [онлайн-конвертере](http://the-mostly.ru/konverter_geograficheskikh_koordinat.html):

<figure><img src="../../../../.gitbook/assets/image (664).png" alt=""><figcaption></figcaption></figure>

Итак, приступим к заполнению параметров функции и получению желаемого результата:

<figure><img src="../../../../.gitbook/assets/image (665).png" alt=""><figcaption><p>Заполнение параметров функции в поле Калькулятор</p></figcaption></figure>



<figure><img src="../../../../.gitbook/assets/image (666).png" alt=""><figcaption></figcaption></figure>
{% endtab %}

{% tab title="Пример кода для копирования" %}
```
soob=tg_send_venue(platform_id, "48°52′", "2°4′", "Мечта осуществима!", "Париж, Эйфелева башня") 
```
{% endtab %}
{% endtabs %}

Описание всех параметров для функции отправки геоточки [в этой статье](attachments.md#otpravit-geotochku-tg_send_venue).

### Контакт: **Пример как отправить** с помощью API Telegram

{% tabs %}
{% tab title="Пример" %}
Заполняем параметры телефон, имя и фамилия:

<figure><img src="../../../../.gitbook/assets/image (667).png" alt=""><figcaption><p>Пример заполнения параметров функции отправки контакта</p></figcaption></figure>

Результат выполнения:

<figure><img src="../../../../.gitbook/assets/image (668).png" alt=""><figcaption></figcaption></figure>
{% endtab %}

{% tab title="Пример кода для копирования" %}
```
soob=tg_send_contact(platform_id, "+79999999999", "Анна", "Тест", 1) 
```
{% endtab %}
{% endtabs %}

Описание всех параметров для функции отправки контакта [выше](attachments.md#otpravit-kontakt-tg_send_contact).

### Стикер: **Пример как отправить** с помощью API Telegram

{% tabs %}
{% tab title="Пример" %}
Отправка стикера ничем не отличается от отправки любого иного вложения:\
1\. Получаем внутреннюю ссылку Telegram ([подробнее тут](/broken/pages/YVEk70VIBhfL7aUZFo9F#kak-poluchit-ssylku-na-media-s-pomoshyu-peremennoi))\
2\. Заполняем параметры функции\
3\. Отправляем блок себе и смотрим результат

<figure><img src="../../../../.gitbook/assets/image (669).png" alt=""><figcaption><p>Отправка стикера</p></figcaption></figure>

Результат:

<figure><img src="../../../../.gitbook/assets/image (670).png" alt=""><figcaption></figcaption></figure>
{% endtab %}

{% tab title="Пример кода для копирования" %}
<mark style="color:red;">Не забывайте ссылки уникальны для каждого бота, поэтому не забудьте сформировать свою ссылку</mark>

```
soob=tg_send_sticker(platform_id, 'CAACAgIAAxkBAAEawJ5jmNeyat8uPGBMP3JzubRNXGjH3wACrw4AAsYg4UqePobN94_jkywE')
```
{% endtab %}
{% endtabs %}

Описание всех параметров для функции отправки стикера [в этой статье.](attachments.md#otpravit-stiker-tg_send_sticker)

### Круглое видео : **Пример как отправить** с помощью API Telegram

{% tabs %}
{% tab title="Пример" %}
Если у Вас квадратное видео, то получить круглое можно при помощи бота [https://t.me/roundNoteBot](https://t.me/roundNoteBot) :&#x20;

<figure><img src="../../../../.gitbook/assets/image (671).png" alt=""><figcaption><p>Получение круглого видео при помощи бота @roundNoteBot (https://t.me/roundNoteBot)</p></figcaption></figure>

Получив круглое видео, отправьте его себе в бот для получения ссылки (подробнее  [тут](attachments.md#kak-pri-pomoshi-tg_request-poluchit-ssylku-na-kartinku-foto-animaciyu-video)) и далее настройте функцию отправки круглого видео:

<figure><img src="../../../../.gitbook/assets/image (672).png" alt=""><figcaption></figcaption></figure>
{% endtab %}

{% tab title="Пример кода для копирования" %}
<mark style="color:red;">Не забывайте ссылки уникальны для каждого бота, поэтому не забудьте сформировать свою ссылку</mark>

```
tg_send_video_note(platform_id, 'DQACAgIAAxkBAAER6cVi6OzIezJo9FWu6WyZPzDgQX8B3QACcxsAArR3SUtRizDeiHWLNikE','','1')

```


{% endtab %}
{% endtabs %}

Описание всех параметров для функции отправки круглого[ в этой статье](attachments.md#otpravit-krugloe-video-tg_send_video_note).

### Картинка / несколько картинок : **Пример как отправить** с помощью API Telegram

{% tabs %}
{% tab title="Пример" %}
Разберем на примере функции для отправки нескольких картинок:

*   для начала сформируйте массив фото<br>

    <figure><img src="../../../../.gitbook/assets/image (673).png" alt=""><figcaption></figcaption></figure>
*   далее заполните параметры функции<br>

    <figure><img src="../../../../.gitbook/assets/image (674).png" alt=""><figcaption></figcaption></figure>
*   отправьте блок себе и любуйтесь результатом<br>

    <figure><img src="../../../../.gitbook/assets/image (675).png" alt=""><figcaption></figcaption></figure>
{% endtab %}

{% tab title="Пример кода для копирования" %}
<mark style="color:red;">Не забывайте ссылки уникальны для каждого бота, поэтому не забудьте сформировать свою ссылку на видео</mark>

```
image_list='[["https://faktoria-print.ru/wp-content/uploads/2022/07/syre-dlya-bumagi.jpg"], ["https://www.solbum.ru/upload/medialibrary/2d1/2d18bd473d50fe9c2fe6a1eb401b4fe3.JPG"], ["https://www.solbum.ru/upload/medialibrary/bb7/bb786b67b57d9ab44ef5f7b8400810bb.jpg"], ["https://obumage.net/wp-content/uploads/2017/05/tual_bumaga.jpg"]]'
soob=tg_send_some_photo(platform_id, image_list)
```
{% endtab %}
{% endtabs %}

Описание всех параметров для функции отправки картинок [в этой статье](attachments.md#otpravit-kartinku-tg_send_photo).

### **Эмодзи: пример как отправить эмодзи со случайным выбором (Dice)**

{% tabs %}
{% tab title="Пример" %}
Самый простой вариант - отправка функции только с одним обязательным параметром:

<figure><img src="../../../../.gitbook/assets/image (676).png" alt=""><figcaption></figcaption></figure>

В этом случае клиент получит кубик:

<figure><img src="../../../../.gitbook/assets/image (677).png" alt=""><figcaption></figcaption></figure>

Если клиент скинет кубик (клик по полученному эмодзи), то в бот прилетит колбек о выпавшем количестве очков:

<figure><img src="../../../../.gitbook/assets/image (678).png" alt=""><figcaption></figcaption></figure>

Можно поэкспериментировать в использовании данной функции. Например, давайте используем слот-машину, добавим кнопку Очки. При нажатии на кнопку будем получать общее колиество очков у клиента:

<figure><img src="../../../../.gitbook/assets/image (679).png" alt=""><figcaption><p>1е сообщение: предлагаем сыграть</p></figcaption></figure>

<figure><img src="../../../../.gitbook/assets/image (680).png" alt=""><figcaption><p>2е сообщение: ловим выпавшие очки</p></figcaption></figure>

<figure><img src="../../../../.gitbook/assets/image (681).png" alt=""><figcaption><p>3е сообщение: выдаем общее количество очков</p></figcaption></figure>

<figure><img src="../../../../.gitbook/assets/image (682).png" alt=""><figcaption><p>Пример работы бота</p></figcaption></figure>
{% endtab %}

{% tab title="Пример кода для копирования" %}
1й пример:

```
soob=tg_send_dice(platform_id)
```

2й пример:

<pre><code>/* 1й блок */
<strong>tg_send_message(platform_id,'Кликните по слот-машине, чтобы испытать удачу!')
</strong>opts='{"inline_keyboard": [[{"text": " 👓 ","callback_data":"Играем"}]]}'
soob=tg_send_dice(platform_id, 'slots', opts)

/* 2й блок - Текст Сообщение */
Выпало #{res[1]} очков
<strong>/* 2й блок - Калькулятор */
</strong>res=splitter('#{question}', ' ')
balls=if(balls==None,0,balls) + int(res[1])

/* 3й блок - Текст Сообщение */
У Вас всего #{balls} очков
</code></pre>
{% endtab %}
{% endtabs %}

Описание всех параметров для отправки эмодзи со случайным выбором [в этой статье.](attachments.md#otpravit-emodzi-so-sluchainym-vyborom-dice-tg_send_dice)

## Отправка "тяжелых" вложений

В телеграм (как в бизнес аккаунте, так и в обычном) можно отправлять вложения с помощью ссылки:

1. Можно отправлять вложения с любым размером, обходя ограничения;
2. Также направляются любые виды вложений, которые вам необходимы.

Как это сделать?

Скопируйте ссылку на вложение, которое уже существует в публичном доступе:

<figure><img src="../../../../.gitbook/assets/Снимок экрана 2024-06-25 в 16.05.01.png" alt="" width="563"><figcaption></figcaption></figure>

&#x20;Далее вставьте скопированную ссылку в функции вложения в блоке:

<figure><img src="../../../../.gitbook/assets/2024-06-25 16.07.45.jpg" alt=""><figcaption></figcaption></figure>

Готово. Таким образом вы можете направлять вложения любого вида и размера.
