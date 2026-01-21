# Отправка заявок в мессенджеры и на электронную почту

В данной статье мы рассмотрим:

* Как оформить текст заявки
* Как отправить заявки в Мессенджеры
* Как отправить заявки/уведомления на электронную почту

Все боты, созданные на конструкторе Salebot, умеют отправлять заявки не только на электронную почту, но и в различные мессенджеры.

### Как оформить текст заявки <a href="#kak-oformit-tekst-zayavki" id="kak-oformit-tekst-zayavki"></a>

В качестве текста заявки вы можете использовать встроенную переменную #{order}:

<figure><img src="https://docs.salebot.pro/~gitbook/image?url=https%3A%2F%2F4216716816-files.gitbook.io%2F%7E%2Ffiles%2Fv0%2Fb%2Fgitbook-x-prod.appspot.com%2Fo%2Fspaces%252F-LxKl4rC_EcwBAz40Qn_%252Fuploads%252F2Z6TQE0AXbzaBDToWajX%252FScreenshot%25202025-12-04%2520at%252009.35.44.png%3Falt%3Dmedia%26token%3D9c14519c-4d26-476d-94b3-78e9fc2d035b&#x26;width=768&#x26;dpr=4&#x26;quality=100&#x26;sign=f56d5279&#x26;sv=2" alt=""><figcaption></figcaption></figure>

Но также можно составить и собственный текст.

### **Как отправить заявки в Мессенджеры** <a href="#kak-otpravit-zayavki-v-messendzhery" id="kak-otpravit-zayavki-v-messendzhery"></a>

Настройка отправки заявок в мессенджеры идентична для каждого.

Заявку можно отправить от любого мессенджера, который подключен к Salebot

Для отправки заявки в мессенджер используйте следующую функцию:

**message(client\_id, text, message\_id, timeout)**

Параметры:

**client\_id** —ID клиента в Salebot, которому нужно отправить сообщение. Взять его можно из карточки клиента:

<figure><img src="https://docs.salebot.pro/~gitbook/image?url=https%3A%2F%2F4216716816-files.gitbook.io%2F%7E%2Ffiles%2Fv0%2Fb%2Fgitbook-x-prod.appspot.com%2Fo%2Fspaces%252F-LxKl4rC_EcwBAz40Qn_%252Fuploads%252FHgyjyGUgS6EgDzbBpzDi%252FScreenshot%25202025-12-04%2520at%252009.37.13.png%3Falt%3Dmedia%26token%3Db1fccf03-7c50-4be7-97bb-f2e0c3c9d9b9&#x26;width=768&#x26;dpr=4&#x26;quality=100&#x26;sign=3714f60c&#x26;sv=2" alt="" width="375"><figcaption></figcaption></figure>

**text** — текст сообщения. Можно указать как переменную (не забудьте перед этим ее назначить) или записать нужный текст в кавычках.

**message\_id** — id отправляемого блока (необязательный параметр)

<figure><img src="https://docs.salebot.pro/~gitbook/image?url=https%3A%2F%2F4216716816-files.gitbook.io%2F%7E%2Ffiles%2Fv0%2Fb%2Fgitbook-x-prod.appspot.com%2Fo%2Fspaces%252F-LxKl4rC_EcwBAz40Qn_%252Fuploads%252FMcco4EZbL5bmo0L9Jeb5%252FScreenshot%25202025-12-04%2520at%252009.40.37.png%3Falt%3Dmedia%26token%3D524756d8-d071-459e-9bcd-d38e39a6c9d1&#x26;width=768&#x26;dpr=4&#x26;quality=100&#x26;sign=5408407b&#x26;sv=2" alt=""><figcaption></figcaption></figure>

**time\_out** - время отправки или задержка, необязательный параметр. Если нужно отправить сообщение с задержкой, укажите время в секундах:

* 1 час равен 3600 секунд; 1 минута равна 60 секундам.

Если вам необходимо отправить через несколько часов, то количество часов умножается на 3600 секунд. Например, отправить через 3 часа, в параметре указываем 10800 (3 \* 3600);

Если вам необходимо указать промежуток, равный минутам, то количество минут умножается на 60 секунд. Например, отправить нужно спустя 35 минут. Тогда в параметре укажите 2100 секунд (35 \* 60)

Если указано отрицательное число, сообщение отправится мгновенно. Например, timeout = 50.

* дату отправки в виде дд.мм.гггг чч:мм, например: timeout = ‘03.04.2022 15:00’. Если указать уже прошедшее время, то сообщение отправится мгновенно.

<details>

<summary>Пример с text</summary>

Настройки блока для отправки заявки:

<figure><img src="https://docs.salebot.pro/~gitbook/image?url=https%3A%2F%2F4216716816-files.gitbook.io%2F%7E%2Ffiles%2Fv0%2Fb%2Fgitbook-x-prod.appspot.com%2Fo%2Fspaces%252F-LxKl4rC_EcwBAz40Qn_%252Fuploads%252Fg0Tf4l6tL18Zep8KAQ29%252FScreenshot%25202025-12-04%2520at%252009.44.16.png%3Falt%3Dmedia%26token%3D170a9ba9-9067-46fe-83c0-3a4db10a2484&#x26;width=768&#x26;dpr=4&#x26;quality=100&#x26;sign=271dda9d&#x26;sv=2" alt="" width="375"><figcaption></figcaption></figure>

Результат выполнения метода отправки:

<figure><img src="https://docs.salebot.pro/~gitbook/image?url=https%3A%2F%2F4216716816-files.gitbook.io%2F%7E%2Ffiles%2Fv0%2Fb%2Fgitbook-x-prod.appspot.com%2Fo%2Fspaces%252F-LxKl4rC_EcwBAz40Qn_%252Fuploads%252FpPR2HoZeT5oFy4kKMbea%252FScreenshot%25202025-12-04%2520at%252009.44.02.png%3Falt%3Dmedia%26token%3D36e2120b-fab1-4c26-85d8-453a31885abf&#x26;width=768&#x26;dpr=4&#x26;quality=100&#x26;sign=3ba18a2&#x26;sv=2" alt="" width="563"><figcaption></figcaption></figure>

</details>

<details>

<summary>Пример с message_id</summary>

Блок с уведомлением о заявке:

<figure><img src="https://docs.salebot.pro/~gitbook/image?url=https%3A%2F%2F4216716816-files.gitbook.io%2F%7E%2Ffiles%2Fv0%2Fb%2Fgitbook-x-prod.appspot.com%2Fo%2Fspaces%252F-LxKl4rC_EcwBAz40Qn_%252Fuploads%252FYugm11QgVnrPYdnxuVmX%252FScreenshot%25202025-12-04%2520at%252009.50.34.png%3Falt%3Dmedia%26token%3D0396854b-b0e3-48f0-924d-0ea1d1d1c3c6&#x26;width=768&#x26;dpr=4&#x26;quality=100&#x26;sign=5ce86593&#x26;sv=2" alt="" width="375"><figcaption></figcaption></figure>

Настройки блока для отправки заявки:

<figure><img src="https://docs.salebot.pro/~gitbook/image?url=https%3A%2F%2F4216716816-files.gitbook.io%2F%7E%2Ffiles%2Fv0%2Fb%2Fgitbook-x-prod.appspot.com%2Fo%2Fspaces%252F-LxKl4rC_EcwBAz40Qn_%252Fuploads%252FHGT5PVih4bfou4fz8Bwt%252FScreenshot%25202025-12-04%2520at%252009.48.16.png%3Falt%3Dmedia%26token%3D128810a5-2170-49c4-bda2-bcbac484d13b&#x26;width=768&#x26;dpr=4&#x26;quality=100&#x26;sign=e64cade9&#x26;sv=2" alt=""><figcaption></figcaption></figure>

Пример отправки заявки

<figure><img src="https://docs.salebot.pro/~gitbook/image?url=https%3A%2F%2F4216716816-files.gitbook.io%2F%7E%2Ffiles%2Fv0%2Fb%2Fgitbook-x-prod.appspot.com%2Fo%2Fspaces%252F-LxKl4rC_EcwBAz40Qn_%252Fuploads%252FGyqUS2pFPAZD2OqxKm5A%252FScreenshot%25202025-12-04%2520at%252009.51.37.png%3Falt%3Dmedia%26token%3Dd434afc5-b0d4-49ce-b2d0-9d0695b3052d&#x26;width=768&#x26;dpr=4&#x26;quality=100&#x26;sign=eeadc400&#x26;sv=2" alt="" width="563"><figcaption></figcaption></figure>



</details>

<details>

<summary>Пример с timeout</summary>

Настройки блока для отправки заявки:

<figure><img src="https://docs.salebot.pro/~gitbook/image?url=https%3A%2F%2F4216716816-files.gitbook.io%2F%7E%2Ffiles%2Fv0%2Fb%2Fgitbook-x-prod.appspot.com%2Fo%2Fspaces%252F-LxKl4rC_EcwBAz40Qn_%252Fuploads%252FobimLSLF2qxJJghBie8e%252FScreenshot%25202025-12-04%2520at%252009.52.45.png%3Falt%3Dmedia%26token%3Ddffb6231-9129-4c4a-a100-744dd643cf09&#x26;width=768&#x26;dpr=4&#x26;quality=100&#x26;sign=41b26d44&#x26;sv=2" alt=""><figcaption></figcaption></figure>

</details>

Для отправки сообщения в whatsapp через номер телефона используйте функцию **whatsapp\_message(phone, text, message\_id)** Параметры:

**phone** — номер телефона в кавычках

**text** — текст сообщения. Можно указать как переменную (не забудьте перед этим ее назначить) или записать нужный текст в кавычках.

**message\_id** — id отправляемого блока (необязательный параметр)

#### Как отправить заявки в Telegram <a href="#kak-otpravit-zayavki-v-telegram" id="kak-otpravit-zayavki-v-telegram"></a>

В поле "Калькулятор указываем функцию API Telegram:

**tg\_send\_message(platform\_id, text, client\_message\_id, reply\_markup, parse\_mode)**

**platform\_id**— id клиента (чата, группы, канала) в Телеграм, куда нужно прислать уведомление

**client\_message\_id** — идентификатор сообщения, которое необходимо процитировать (необязательный параметр)

**reply\_markup** — настройки кнопок (необязательный параметр)

**parse\_mode** — выделение текста в описании жирным или курсивом (необязательный параметр)

<figure><img src="https://docs.salebot.pro/~gitbook/image?url=https%3A%2F%2F4216716816-files.gitbook.io%2F%7E%2Ffiles%2Fv0%2Fb%2Fgitbook-x-prod.appspot.com%2Fo%2Fspaces%252F-LxKl4rC_EcwBAz40Qn_%252Fuploads%252FHD7ZfUXLnMr5Z7j0i0HJ%252FScreenshot%25202025-12-04%2520at%252009.58.03.png%3Falt%3Dmedia%26token%3D48a234c6-c402-4ba1-bd53-12a1e4222620&#x26;width=768&#x26;dpr=4&#x26;quality=100&#x26;sign=3905dcc4&#x26;sv=2" alt="" width="563"><figcaption></figcaption></figure>

Где взять **platform\_id** для отправки уведомлений:

1. У вас должен быть подключен к проекту Telegram-бот
2. В этого бота нужно прислать любое сообщение с того Telegram-аккаунта, куда должны приходить сообщения о заявках. Если уведомления хотите присылать в Канал, бот должен быть администратором канала с возможностью писать сообщения.
3. Далее переходите в раздел Клиенты в Salebot:

<figure><img src="https://docs.salebot.pro/~gitbook/image?url=https%3A%2F%2F4216716816-files.gitbook.io%2F%7E%2Ffiles%2Fv0%2Fb%2Fgitbook-x-prod.appspot.com%2Fo%2Fspaces%252F-LxKl4rC_EcwBAz40Qn_%252Fuploads%252Fqdy5gwcqGHva4o32pAnh%252FScreenshot%25202025-12-04%2520at%252009.59.30.png%3Falt%3Dmedia%26token%3Df9c55754-3d53-44b7-aefa-79227d153f17&#x26;width=768&#x26;dpr=4&#x26;quality=100&#x26;sign=39e297f8&#x26;sv=2" alt="" width="375"><figcaption></figcaption></figure>

1. Откройте диалог с Telegram-аккаунтом, которому будете отправлять заявки.
2. Копируете значение ID в мессенджере (platform\_id):

<figure><img src="https://docs.salebot.pro/~gitbook/image?url=https%3A%2F%2F4216716816-files.gitbook.io%2F%7E%2Ffiles%2Fv0%2Fb%2Fgitbook-x-prod.appspot.com%2Fo%2Fspaces%252F-LxKl4rC_EcwBAz40Qn_%252Fuploads%252FSZ4mPk0QhK3vGTmygNeQ%252FScreenshot%25202025-12-04%2520at%252010.01.59.png%3Falt%3Dmedia%26token%3De81b366e-827f-448b-94ac-751a393d3a2b&#x26;width=768&#x26;dpr=4&#x26;quality=100&#x26;sign=eb54cc2c&#x26;sv=2" alt="" width="563"><figcaption></figcaption></figure>

И вставляете его вместо platform\_id в параметр функции.

Если вам необходимо настроить отправку нескольким пользователям Telegram, то продублируйте функцию и там вставьте другой айди.

### **Как отправить заявки/уведомления на электронную почту** <a href="#kak-otpravit-zayavki-uvedomleniya-na-elektronnuyu-pochtu" id="kak-otpravit-zayavki-uvedomleniya-na-elektronnuyu-pochtu"></a>

Перейдите в настройки проекта и в поле Email впишите адрес своей электронной почты. После этого все заявки из красного блока (блок "Закрыть сделку") будут отправляться вам на email.

<figure><img src="https://docs.salebot.pro/~gitbook/image?url=https%3A%2F%2F4216716816-files.gitbook.io%2F%7E%2Ffiles%2Fv0%2Fb%2Fgitbook-x-prod.appspot.com%2Fo%2Fspaces%252F-LxKl4rC_EcwBAz40Qn_%252Fuploads%252FkmTn4NnOTLw5mJ7w2Vnk%252FScreenshot%25202025-12-04%2520at%252010.03.43.png%3Falt%3Dmedia%26token%3Df7458f43-210c-4533-bffb-29dde0098a11&#x26;width=768&#x26;dpr=4&#x26;quality=100&#x26;sign=49e41ad9&#x26;sv=2" alt=""><figcaption></figcaption></figure>

{% hint style="success" %}
[О блоке "Закрыть сделку" рассказали здесь](../../chat-boty/kak-sozdat-chat-bot-dlya-biznesa/tipy-blokov/bloki-bez-usloviya.md#blok-zakryt-sdelku)
{% endhint %}
