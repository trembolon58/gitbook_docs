# Аналитика сайта

Данная вкладка необходима для настройки аналитики на сайте:

<div data-with-frame="true"><figure><img src="../../.gitbook/assets/image (452).png" alt=""><figcaption><p>Настройки сайта → Аналитика</p></figcaption></figure></div>

## Аналитика маркетинга и продаж

**Добавить клиенту метку.** При запуске бота со страницы сайта клиенту будет установлена метка. Её можно увидеть в разделе Клиенты в диалоге. По наличию метки можно фильтровать клиентов и работать в разделе Списки → вкладка Метки.

**Добавить клиента в список.** При запуске бота со страницы сайта клиент будет добавлен в указанный в настройках страницы сайта список. Увидеть списки, в которых есть клиент, можно в разделе Клиенты в диалоге. По наличию клиента в списках можно фильтровать клиентов и работать в разделе Списки. Выдавать различные доступы и настраивать работу бота

Пример настройки добавления клиентам метки и списка:

<div data-with-frame="true"><figure><img src="../../.gitbook/assets/image (453).png" alt=""><figcaption><p>Настройки сайта</p></figcaption></figure></div>

Где смотреть наличия у клиента меток и в какие списках состоит:

<div align="left" data-with-frame="true"><figure><img src="../../.gitbook/assets/2023-03-29_12-17-30 (2).png" alt=""><figcaption></figcaption></figure></div>

**Идентификатор сайта CoMagic.**&#x20;

Подключение к сайту сквозной аналитики через сервис CoMagic. Подробнее про настройку на стороне CoMagic можно найти на стороне сервиса. В настройках сайта достаточно указать Идентификатор сайта, полученный в  CoMagic

<div data-with-frame="true"><figure><img src="../../.gitbook/assets/image (454).png" alt=""><figcaption></figcaption></figure></div>

**Сохранение в переменные клиента значений из куки.** &#x20;

Для создания сквозной аналитики  можно включить на минилендинге передачу в бота значений куки клиента. И дальше передавать их в системы сквозной аналитики. \
\
Доступные варианты:

<div data-with-frame="true"><figure><img src="../../.gitbook/assets/image (455).png" alt=""><figcaption></figcaption></figure></div>

Пример переменных клиента, который запустил бота с сайта:

<div align="center" data-with-frame="true"><figure><img src="../../.gitbook/assets/image (456).png" alt="" width="439"><figcaption><p>Пример переменных клиента в диалоге в разделе Клиенты</p></figcaption></figure></div>

В переменные клиента записались данные из куки: Google Client ID, Yandex Client ID, Client IP address, User agent. Остальные сервисы к сайту не подключены.

**Пиксель ВКонтакте.** К сайту также можно подключить пиксель ВКонтакте. В данном поле укажите код пикселя.&#x20;

<div align="left"><figure><img src="../../.gitbook/assets/image (457).png" alt=""><figcaption><p>Настройка сайта</p></figcaption></figure></div>

**Пиксель Facebook\*.**  К сайту можно подключить пиксель Facebook. В данном поле укажите код пикселя. &#x20;

<div align="left"><figure><img src="../../.gitbook/assets/image (458).png" alt=""><figcaption><p>Настройка сайта</p></figcaption></figure></div>

{% hint style="danger" %}
\*Facebook принадлежит компании Meta Platform inc., деятельность которой признана экстремистской на территории РФ и запрещена.
{% endhint %}

## Сквозная аналитика сторонними сервисами

Для создания сквозной аналитики на сайте отметьте галочками чекбоксы для передачи в бота значений куки клиента.&#x20;

И дальше можно передавать значения из этих куки в системы сквозной аналитики. Например, в Roistat.

<figure><img src="../../.gitbook/assets/image (459).png" alt="" width="563"><figcaption></figcaption></figure>

Описание доступных интеграций с сервисами аналитики и инструкции по их настройке можно узнать в разделе[ Интеграции - > Аналитика.](../../analitika-dlya-biznesa/integracii-dlya-analitiki/)

## Google Аналитика

К сервису, созданному в Salebot, можно подключить Google Аналитику. Для этого создайте поток данных с указанием домена вашего сайта в Google Аналитике, создайте событие-конверсию и укажите данные в настройках сайта:

<div data-with-frame="true"><figure><img src="../../.gitbook/assets/image (460).png" alt=""><figcaption><p>Настройки сайта</p></figcaption></figure></div>

{% hint style="info" %}
[Подробнее о том как подключить и настроить Google Аналитику рассказано в статье.](../../analitika-dlya-biznesa/integracii-dlya-analitiki/google-analytics.md)
{% endhint %}

_**Создайте событие конверсии для каждой кнопки отдельно или одну цель для всех кнопок.**_

Если вы передадите название события в виде "button\_" со знаком "\_" в конце, то конверсия будет отправлена для каждой кнопки мессенджера разная.\
Например: \
"button\_vk" - для ВКонтакте \
"button\_telegram" - для Телеграм.

В конец будет добавлено: \
vk - Вконтакте \
telegram - Телеграм \
viber - Viber \
facebook\* - FaceBook\*\
whatsapp\* - WhatsApp\*\
ok - Одноклассники \
instagram\* - Instagram\*

{% hint style="danger" %}
\*Facebook, WhatsApp, Instagram принадлежат Meta platform Inc., деятельность которой признана в РФ экстремистской и запрещена.
{% endhint %}

Если вы передадите идентификатор без нижнего подчеркивания в конце, для всех кнопок будет действовать одинаковое событие конверсии, название которого передано в данное поле.

_<mark style="color:green;">Пример настроек Google Аналитики  на клики по кнопкам каждого мессенджера по отдельности:</mark>_

<div align="left" data-with-frame="true"><figure><img src="../../.gitbook/assets/image (461).png" alt=""><figcaption></figcaption></figure></div>

_Настройка конверсий на стороне Google Аналитики:_

<div data-with-frame="true"><figure><img src="../../.gitbook/assets/image (462).png" alt=""><figcaption></figcaption></figure></div>

## Пиксель ВКонтакте

Для того чтобы использовать пиксель ВК, нужно создать его в рекламном кабинете, раздел Ретаргетинг.

<div data-with-frame="true"><img src="https://lh4.googleusercontent.com/RzMNK7_WmycGXmMjqNPL617q5aXBphVARPeNguXoYKiixqaPAW3HGdyouDyBf65NHdjt9gVM49zkqxI6KMif5HMpjFO7YE6th10NAiwDT0EZp0s0DdYVkhu-c4bVDTyv3uJPgeoi" alt=""></div>

Переходим во вкладку Пиксели и нажимаем кнопку Создать пиксель.

<div data-with-frame="true"><img src="https://lh4.googleusercontent.com/Ct-xbMKgbruCesASq1X7xv-7YXWhga07bQmfOkIx071eWPXGIrKk7NvoVvE768aumBaASe880Fv7ZJfskQa-JZL95HF2UeDcky9HJSy_KVSAybPvwm3bobNSWFClTBVykQcpwEc_" alt=""></div>

Называем пиксель как удобно, выбираем тематику и, возможно, убираем (или оставляем, в зависимости от ваших потребностей) птичку с Автоматически создать аудиторию.

После нажатия кнопки создать, появится окно, в котором нам нужно скопировать код пикселя для вставки на сайт.

Переходим в настройки сайта в salebot и вставляем этот код, выделенный жирным.

Теперь добавим аудиторию для сбора клиентов, которые посетили лендинг. Переходим во вкладку Аудитории и нажимаем кнопку Создать аудиторию.

Вводим название и выбираем подключенный пиксель.

<div data-with-frame="true"><img src="https://lh4.googleusercontent.com/43UA1hVYE4CPzWs6wBMEj47iFuIceqvhc32VYSo7I4rImVGEQ08OzaVCim29PRyV4tmEmuDpJ5bjRyG38z98sFfUj_zh9raB92PMOSWi3zAlN51OaUSRxz5YZZ2TjZH5QrMKn47e" alt=""></div>

Создаем и переходим на лендинг, после этого статус пикселя в течение 10 минут станет **"**&#x420;аботает".

<div data-with-frame="true"><img src="https://lh5.googleusercontent.com/K7dEzKUWE7NEsXahNNg_OF9o-iUPQ5E4UDm4lXABUUX2CovNW0vZmMFMAbmyQJ-Shm3xteEWjeQdLiud6BiZVUURFwfCRusuCaxzrTCnWWosv88MylUqWGx8DJIjFRLFnlre0mmq" alt=""></div>

Salebot автоматически отправляет события открытия минилендинга и подписки на минилендинг.

**View** - открытие/просмотр подписной \
**Subscribe** - подписался

## Пиксель Facebook<mark style="color:red;">\*</mark>

{% hint style="danger" %}
<mark style="color:red;">**\***</mark>**На территории Российской Федерации&#x20;**<mark style="color:red;">**запрещена деятельность**</mark>**&#x20;социальных сетей&#x20;**<mark style="color:red;">**Facebook**</mark>**&#x20;и&#x20;**<mark style="color:red;">**Instagram**</mark>**, принадлежащих компании Meta Platforms Inc**., признанная экстремистской!
{% endhint %}

Пиксель Facebook<mark style="color:red;">\*</mark> можно установить на сайт, созданный в Salebot.&#x20;

{% hint style="warning" %}
&#x20;Для использования пикселя Facebook<mark style="color:red;">\*</mark> у вас <mark style="color:green;">должен быть установлен свой домен</mark> на минилендинг!
{% endhint %}

Ниже разберем как это сделать.

#### **Регистрируем пиксель в facebook**<mark style="color:red;">**\***</mark>**&#x20;ads**

[Переходим на страницу Events Manager.](https://www.facebook.com/events_manager2)\
Открываем меню и выбираем пункт Events Manager

<div data-with-frame="true"><img src="https://lh4.googleusercontent.com/6YCehjamLo_BK_-CKxPZf8nMZS_3_c0xjjhdFCwOpq3MhGvTLYMlf4YEBUij_xtuFjyMDH-xPW8TUrf_MNhlLcTsd6xVrJjYPRLjeZPadDOeTM2-iMa3W1ba9EhNbtkkF-vZ8Dy4" alt=""></div>

Далее нажимаем на зеленый крестик слева и выбираем:

1. Подключение нового источника данных - Интернет
2. Выберите способ подключения - Пиксель Facebook<mark style="color:red;">\*</mark>
3. Вводим название пикселя и адрес вашего сайта.

<div data-with-frame="true"><img src="https://lh6.googleusercontent.com/1lAN43HYjX_8_5XXtjyiDTiNhKzCiodZalmqHxxy0tQx-xS2Hl1S-TVBj63EGZeVm9e1PKeVGP83FoSRo0-7UwPNMqwnA3jWrbL9tSuTEYUD-mDkRkJxk9t5Mqq15DkesftKNTN2" alt=""></div>

Далее выбираем **Добавить код пикселя на сайт вручную**

<div data-with-frame="true"><img src="https://lh4.googleusercontent.com/jwTFAbz0pX2AN4ke589GK6jJTArg9q1dHs1XrFrUVMz5dYyW15Vc7cuRHKQ1UjurrZx6-SQ_t2fFOQ3iR24sPwJZRukI_P0SLzfNpM_Vk3f7uVRgHFCAcYbOuUA_WzUD8O336s30" alt=""></div>

Копируем код пикселя

<div data-with-frame="true"><img src="https://lh3.googleusercontent.com/f8QZvSupECTQ24JugJ7SxlypuZ-sR5tIyRIL7tnMafsKocYWJG-M1ehyVPWK916PMVAkAV2FOOgFaBeSiaPcsD6ohaRi-oQr0rd4VtZnHp_nLtTNdft_AteUkkbeSMS8-qclbXlD" alt=""></div>

<div data-with-frame="true"><img src="https://lh5.googleusercontent.com/9TYr-gODjHbWkK0zyg54u8DG7tiRRrNJvyKaRpi8JrcQPDo0r95ICNv2_nMaDByNB_pcd6vTfhtf33Iw6JrjqRi6JsHQxT-NkkchoRDnXwTwynN7IvmkaLTrHoiacFvs5dsLVIQP" alt=""></div>

Также его можно скопировать после создания, вот здесь:

<div data-with-frame="true"><img src="https://lh6.googleusercontent.com/0Gg4ZLcyRVgF4hn3kHdu-eaUklAyt5QvAh2Un0AZiapLH0N9YbtzJixuWY5L3bBQ5BM8K56BH1jOBD6fyhxnwBHJFi2MlC0PAVTUSofSdlhbK8m_FXv-PKPSq6B8-PGCsQSjyAXv" alt=""></div>

Далее переходим в настройки сайта и вставляем этот номер в соответствующее поле.

На этом настройка завершена. Теперь в фейсбук<mark style="color:red;">\*</mark> будет приходить два события:

**PageView** - просмотр страницы сайта\
**Лид** - при нажатии на одну из кнопок мессенджеров

После настройки пикселя и перехода на страницу, где он установлен (или нажатия на кнопку какого-то мессенджера), можно посмотреть тестовые события. Если они есть, то пиксель установлен верно.

<div data-with-frame="true"><img src="https://lh5.googleusercontent.com/KKqw_wSp3400pfIfPJSR1PIXbdW5sJ2a8RM0HSwicVzsS6DGnzNEQ267aFggGltgY1iEVUddta3Dbtm3r2MBy-iJKQYI-Zs0JQjZ7xmjjUon1VlUEIAyGKNMLPxCKsJu7WN2195h" alt=""></div>

## Как отследить события по заявкам и переходам в бота с сайта?

Теперь вы можете отследить события по заявкам и(или) переходам в бота с сайта.

Для этого вам нужно перейти в настройки сайта, в котором создана форма отправки заявки или с кнопками на мессенджеры:

<div data-with-frame="true"><figure><img src="../../.gitbook/assets/Снимок экрана 2026-04-09 в 16.00.31.png" alt=""><figcaption></figcaption></figure></div>

Далее наведите на блок "Форма" и найдите кнопку "Настройки":

<div data-with-frame="true"><figure><img src="../../.gitbook/assets/Снимок экрана 2026-04-09 в 16.01.49.png" alt=""><figcaption></figcaption></figure></div>

Раскройте настройки кнопок:

<div data-with-frame="true"><figure><img src="../../.gitbook/assets/Снимок экрана 2026-04-09 в 16.02.33.png" alt=""><figcaption></figcaption></figure></div>

Здесь вы увидите поле, где нужно вставить название события, настроенное в Яндекс Метрике:

<div data-with-frame="true"><figure><img src="../../.gitbook/assets/Снимок экрана 2026-04-09 в 16.03.36.png" alt="" width="563"><figcaption></figcaption></figure></div>

Чтобы отправка событий работала, [нужно вставить скрипт счетчика Метрики на сайт](analitika-saita.md#kak-sozdat-schetchik-yandeks.metriki), или вставить скрипт счетчика [Гугл Аналитики](analitika-saita.md#google-analitika) или [Facebook\* Pixel](analitika-saita.md#piksel-facebook).

Аналогично можно проставить название событий для каждой кнопки мессенджера.

<div data-with-frame="true"><figure><img src="../../.gitbook/assets/Снимок экрана 2026-04-09 в 16.06.55.png" alt=""><figcaption></figcaption></figure></div>

<div data-with-frame="true"><figure><img src="../../.gitbook/assets/Снимок экрана 2026-04-09 в 16.07.28.png" alt=""><figcaption></figcaption></figure></div>

<div data-with-frame="true"><figure><img src="../../.gitbook/assets/Снимок экрана 2026-04-09 в 16.07.47.png" alt="" width="375"><figcaption></figcaption></figure></div>
