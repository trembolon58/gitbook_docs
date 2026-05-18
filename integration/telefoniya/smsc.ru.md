# Smsc.ru

### Как подготовить аккаунт

Для работы с сервисом [SMSC.ru](https://smsc.ru/?ppsalebotpro) надо заключить договор - [ТУТ ](https://smsc.ru/contract/info/?ppsalebotpro)

После того как вы зарегистрировались на сервисе, перейдите в настройки и укажите номер телефона, с которого будут идти звонки и смс, настройте имя отправителя:

![](https://lh6.googleusercontent.com/HfL7jP0sR8SdAOt5UUxdmEFIiQn8TH3zPkyXEZIdmaI_MRnkVufZY9Woe2xpHV-1YiC_Iirlc00yJfeIj2AQpxvPNNSAZiCNaAoLqO2PTx4RTg_P0nErohO3lIdlilI_Wbq1W4P4)

Дополнительно в настройках можно включить автоматическое сокращение ссылок в смс и отслеживание номеров абонентов, которые кликнули по ссылке:

![](https://lh4.googleusercontent.com/G62Ur2mkuXNqOINoxYyAUK36gZM1UktfYlI4f_TBP4X52tuTVHFGQR-tha2ovRu7TQg7v-zpv1LvEYMJmyWmbw3NToDbblt3S1fTY3RjiuXxy1q1ng6hHb3hsv0efI120cdPV3Nb)

{% hint style="info" %}
В настройках API можно включить “Режим тестирования (виртуальная отправка без оплаты)”. Остальные настройки просмотрите самостоятельно и настройте под себя!
{% endhint %}

{% hint style="info" %}
Большинство ответов на ваши вопросы можно найти в документации: https://smsc.ru/faq/
{% endhint %}

На этом подготовка аккаунта окончена. Переходим к интеграции. Для интеграции используем этот раздел документации: [https://smsc.ru/api/](https://smsc.ru/api/?ppsalebotpro)

### Как сделать интеграцию

#### Отправляем СМС

Для отправки SMS формируем ссылку:

**https://smsc.ru/sys/send.php?login=ваш логин\&psw=ваш пароль\&phones=#{phone}\&mes=#{text}**

Обязательные параметры:&#x20;

ваш **логин** - логин, указанный при регистрации

ваш **пароль** - пароль указанный при регистрации

**phone** - телефон пользователя, кому уходит смс (номера могут передаваться без знака "+". Если номер передан без знака "+", то он может быть исправлен автоматическим форматированием и приведен к правильному международному формату. Таким образом, некоторые ошибки при вводе номеров телефонов могут быть исправлены автоматически. Для отключения автоисправления передайте номер со знаком "+".)

**text** - сообщение (Максимальный размер – 1000 символов. Сообщение при необходимости будет разбито на несколько SMS, отправленных абоненту и оплаченных по отдельности. Размер одного SMS – 160 символов в латинице или 70 символов в кириллице. При разбивке сообщения на несколько SMS в каждую часть добавляется заголовок для объединения частей в одно сообщение на телефоне получателя, и максимальная длина становится 67 для кириллицы и 153 для латинских букв).

{% hint style="info" %}
Дополнительные параметры передаются также в ссылке. С ними можно ознакомится в документации: [https://smsc.ru/api/](https://smsc.ru/api/?ppsalebotpro)
{% endhint %}

Пример блока с отправкой смс:

Тип запроса - GET

URL запроса - ссылка, описанная выше

В калькуляторе в переменной text записано сообщение для отправки

![](https://lh6.googleusercontent.com/5YHyFiX6qRz7Xj7t14PSxN2HijqM9J8ZrPcLzfQucAxyfbpk10q2ad758pfxh9jRLX2hqlWT0d347oPbTCAZh2gA4zm1qpkyx9yL8yHVLEBlCe8uucBtmggJ-mRln6WuWLDtecUY)

{% hint style="warning" %}
Размер одного SMS – 160 символов в латинице или 70 символов в кириллице.
{% endhint %}

#### Отправка голосового сообщения (звонок) <a href="#docs-internal-guid-cba5d49d-7fff-13b5-9214-f4c7179757b0" id="docs-internal-guid-cba5d49d-7fff-13b5-9214-f4c7179757b0"></a>

Для отправки голосового сообщения формируем ссылку:

**https://smsc.ru/sys/send.php?login=ваш логин\&psw=ваш пароль\&phones=#{phone}\&fileurl=#{audio}\&call=1**

Обязательные параметры:&#x20;

ваш **логин** - логин, указанный при регистрации

ваш **пароль** - пароль указанный при регистрации

**phone** - телефон пользователя, кому уходит смс (номера могут передаваться без знака "+". Если номер передан без знака "+", то он может быть исправлен автоматическим форматированием и приведен к правильному международному формату. Таким образом, некоторые ошибки при вводе номеров телефонов могут быть исправлены автоматически. Для отключения автоисправления передайте номер со знаком "+".)

**audio** - голосовой файл, загруженный на сервис

**call** - признак голосового сообщения. При формировании голосового сообщения можно передавать как текст, так и прикреплять файлы. Файлы, добавляемые к сообщению, должны передаваться методом POST в теле http-запроса. ( 0 (по умолчанию) – обычное сообщение, 1 – голосовое сообщение)

{% hint style="info" %}
При создании сообщения можно вставлять в текст http(s)-ссылки ранее загруженных файлов, узнать которые можно в личном кабинете на странице отправки, нажав последовательно ссылки "прикрепить файл" – "Загруженные файлы". Также можно указывать локальные ссылки на загруженные файлы на нашем сервере в виде "\<file/upload/files/sms/каталог\_загрузки/название\_файла>". Для загрузки файла из внешнего источника можно в запросе передавать дополнительный параметр fileurl, содержащий полный http(s)-адрес файла.
{% endhint %}

Пример блока с автодозвоном:

п запроса - GET

URL запроса - ссылка, описанная выше

В калькуляторе в переменной audio записано сообщение для отправки (как получить ссылку описано ниже)

![](https://lh6.googleusercontent.com/acONs1gy89H9g48gwP8yjkAZSUd7qROBFvXRONHQsVPzZrWBV6xUwH04yDXduEBEj0gB8JQ5iI6hbgbXc3LVHHj6vYhorapvIYwsM1pRuGXnc0UV3Yqc4vb24rm8kzkvZgOAgcKD)

**Загружаем аудио для отправки через fileurl:**

Идем в Настройки -> Медиа файлы -> Создать

<br>

![](https://lh5.googleusercontent.com/pP2Y8xpvDiItF3s-GijEZIg4fY7gEy5SttvZ3gkQ5vwbwNJ8k7hycpuny_c_yK8WGESu2gvj1GwGKiPnbI5-SqtXJ9NU1XfR9ZffnD8UpgmdfLc44_W9ztcRz_9yeAga_tJgRttb)

![](https://lh4.googleusercontent.com/ejfxr4eLu-jSAo2HcayQxFVB5AzwojdL4baJhKxN10MTH73zUwGvH9bOlaBHnObkJLBPmZoNlsXyoXUAnTbqYO_QzKcXDZKOte5I6T7e7qXRvHf18zVAA_B1p1DvsWwgZJy2jSpp)

![](https://lh6.googleusercontent.com/vHrnynXD5hUphmkQo2ysQnFJ922nPLHYIlPHeAIpun6JcC9Gd1tN0aT_RkgKhUOK9KGdwX1d_EBjBUzlk2WPnaa7GT8Jk1X0nm3NSRib7SykyrCtZB5QdHunBKLeps9rNQBKEd2r)

После того как мы загрузим и сохраним файл, нам надо его еще раз открыть, кликнув по названию:

![](https://lh4.googleusercontent.com/gCQ86YptbxOYTEKCNJpHtP-bCKqQG1p0SGtx7SIn_U289FfR5FBsTCrVexjV6QSxdrFsVuH6GjnVwbPpbpo1cxwTTzdab5lg9t0Fxy0Cu6ISNSYESqTLz2uwz59C2lXgYjaVm3wb)

Скопировать путь файла:

![](https://lh5.googleusercontent.com/xMItlsz9twRdwzd2dyaXT5Qq4Yh0pYUXIWuo66N3wV4KTZu810EOfp1I5xNicDNS4MjlCJvuRcwDueIHhcaWxYJWQnNTCLWCkufaTUlpcQSu7AXRRxZqTlryktL2QsL2eEGcAPRE)

Прикрепить к ссылке в калькуляторе Сейлбот:

![](https://lh6.googleusercontent.com/IUahE1k8TtiTViUpQFeVRC3N2w1fdT-h0NBb0MM4IR29B3dpSDIJ0YTrzD-79_VnqQ8ufy91qviidJs7lgFj6ndEa4Y-P4vAiWncCDaFuYF9sfJg0PxEM8igTmN0x1RA_4QqYY59)

### Ошибки

На этапе тестирования в поле “Текст сообщения” пишем #{custom\_answer} и смотрим, что нам ответит бот

![](https://lh3.googleusercontent.com/N-KwVD33E3hZunmLHypw_bru9VxhU6E-0hpDxU34Wt7Ulb-7KhDHi9vdq77UVRJ-7DH8lDERvFgXH13uATEfoZlUfR-cQqMjkSF5X6cIgQXeOPh3HydrMJiS6AjS6uE-nq7lbfdi)

**В случае успешной доставки сообщения или звонка мы получим в ответ от бота: «OK - 1 SMS, ID - 3»**

![](https://lh3.googleusercontent.com/oZ-Dv6IvPsZg7Woz5IJKmJ941BMaKwcZRq8rGNNQtzg3bpBxYo6yrXQkFWsXyVZWKp8fBNB85rnVlgy-batq78zPhTV__bBiiIoYdFDMpGMefyRJbvlDYx5riTX0vLUR1dPiz9o6)

Доставленное сообщение без настроенного “Имя отправителя” выглядит таким образом:

![](https://lh6.googleusercontent.com/RmZCRxHjJ8wnc-fiCtk85aQg8VuhhKzdLQPLF-5E2qeNtQrfcKkSssucX5goy19k5Xf60_RolGJPwTBK9WeiWTd27tX_ib98ifvHsdRdajh5UOue3UjAxmzojy74QBrWUzyUSiby)

