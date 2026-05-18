---
description: >-
  бесплатный онлайн-офис, разрабатываемый компанией Google.  Позволяет работать
  с файлами
---

# Google Documents

## Как подготовить Google Документ

В нужном документе переходим в настройки доступа, где меняем общий доступ на “всех, у кого есть ссылка” и присваиваем право “редактор”.

<figure><img src="../../.gitbook/assets/image (84) (1).png" alt=""><figcaption></figcaption></figure>

<figure><img src="../../.gitbook/assets/image (85) (1).png" alt=""><figcaption></figcaption></figure>

## Как работать через свой сервисный аккаунт

По умолчанию конструктор работает с собственными сервисными аккаунтами для доступа к вашим документам. Поэтому вам необходимо выдавать доступ на редактирование по ссылке. Чтобы обеспечить достаточный уровень безопасности, вы можете передавать json с аутентификационными данными.&#x20;

{% hint style="info" %}
В Google Документах есть лимиты на количество запросов в единицу времени. Чтобы не зависеть от лимитов, вы можете использовать сервисный аккаунт.
{% endhint %}

Подробно процесс подключения сервисного аккаунта описан [тут](/broken/pages/AJyv5ldV9fJS174YJDVA#podgotovka-servisnogo-akkaunta)

Подключайте сервис Google Docs API и переходите к настройке самого документа

<figure><img src="../../.gitbook/assets/image (86) (1).png" alt=""><figcaption></figcaption></figure>

После [предоставления доступа через сервисный аккаунт](/broken/pages/AJyv5ldV9fJS174YJDVA#predostavlenie-dostupa-k-dokumentu) [нашему боту](/broken/pages/AJyv5ldV9fJS174YJDVA#predostavlenie-dostupa-k-failu-dokumentu-tablice-forme-i-td-botu-iz-proekta-salebot) создаем и подготавливаем к работе[ шаблон документа.](https://support.google.com/a/users/answer/9308885?hl=ru)

{% hint style="warning" %}
Функции для работы с Google-документами используйте только при работе через сервисный аккаунт. Это позволит избежать необходимость повторной авторизации
{% endhint %}

## Как создать новый Google-документ из бота

Для создания нового документа из Salebot воспользуйтесь функцией **gd\_create\_new\_doc(title, google\_email)**, где&#x20;

1. **title** - название нового документа, строка
2. **google\_email** - ваша почта google, с которой Вы будете просматривать документ, строка.&#x20;

Поскольку функция работает через сервисный аккаунт, то в результате выполнения функции права создателя документа будут у данного аккаунта. Функция автоматически выдаст права редактора указанному google\_email и новый документ будет доступен для редактирования.

**Пример:** gd\_create\_new\_doc('Новый документ. Да-да', 'googlemailtest@gmail.com')

<figure><img src="../../.gitbook/assets/image (87) (1).png" alt=""><figcaption></figcaption></figure>

В случае успешного исполнения функции будет создан новый документ, который вы увидите авторизовавшись под указанным в функции google\_email.&#x20;

<figure><img src="../../.gitbook/assets/image (88) (1).png" alt=""><figcaption></figcaption></figure>

Результат выполнения функции - словарь, содержащий статус исполнения функции, имя и ид вновь созданного документа

{"status":true,"message":"Google document Новый документ. Да-да, id 1UfOZ5-AXb-QRAs7Gev9tv\_H3Cx5JuWbFeeHq48CEyAY is created"}

## Как скопировать существующий Google-документ

Чтобы скопировать существующий документ, воспользуйтесь функцией \
**gd\_copy(doc\_id, google\_email)**, где:

1. **doc\_id** - идентификатор документа, строка (например, 1pgC9TFC6P6tUse6KwmFFzmAmj0bhU3fwW8hIvJwXJ\_M)&#x20;
2. **google\_email** - ваша почта google, с которой Вы будете просматривать документ, строка.

Поскольку функция работает через сервисный аккаунт, то в результате выполнения функции права создателя документа будут у данного аккаунта. Функция автоматически выдаст права редактора указанному google\_email  и новый документ будет доступен для редактирования.

**Пример:** result\_copy = gd\_copy('1UfOZ5-AXb-QRAs7Gev9tv\_H3Cx5JuWbFeeHq48CEyAY', 'googlemailtest@gmail.com')

<figure><img src="../../.gitbook/assets/image (89) (1).png" alt=""><figcaption></figcaption></figure>

В случае успешного исполнения функции будет создана копия документа, id которого вы указали. Документ вы увидите авторизовавшись под указанным в функции google\_email.&#x20;

<figure><img src="../../.gitbook/assets/image (90) (1).png" alt=""><figcaption></figcaption></figure>

Результат выполнения функции - словарь, содержащий статус исполнения функции и ид копии документа

{"status":true,"message":"document 13eufZJVlFT64tujOOInTZfAExOW1PpqSZhLupj\_PT1U successfully created"}

## Как вставить текст в конец Google-документа

Для вставки текста в конец документа используйте функцию \
**gd\_add\_text(doc\_id, text)**, где

1. **doc\_id** - идентификатор документа, строка (например, 1pgC9TFC6P6tUse6KwmFFzmAmj0bhU3fwW8hIvJwXJ\_M)&#x20;
2. **text** - текст для вставки. Если документ пустой, текст добавится в его начало. Если документ заполнен, текст вставится с нового абзаца в самом конце.&#x20;

**Пример:** result\_add\_text = gd\_add\_text('1UfOZ5-AXb-QRAs7Gev9tv\_H3Cx5JuWbFeeHq48CEyAY','Это же был чистый документ, верно? Ну вот, теперь здесь есть новая фраза!')

<figure><img src="../../.gitbook/assets/image (91) (1).png" alt=""><figcaption></figcaption></figure>

В случае успешного исполнения функции в ваш документ будет добавлен текст, указанный в функции.

Результат выполнения функции - словарь, содержащий уведомление об успехе\
{"status":true,"message":"document 1UfOZ5-AXb-QRAs7Gev9tv\_H3Cx5JuWbFeeHq48CEyAY successfully updated"}

<figure><img src="../../.gitbook/assets/image (92) (1).png" alt=""><figcaption></figcaption></figure>

## Как заменить части текста Google-документа

Эта функция будет полезна тем, у кого есть готовый шаблон документа, в котором нужно заменить некоторые части. \
**gd\_replace\_text(doc\_id, text\_array, match\_case)**, где:

1. **doc\_id** - идентификатор документа, строка(например, 1pgC9TFC6P6tUse6KwmFFzmAmj0bhU3fwW8hIvJwXJ\_M)&#x20;
2. **text\_array** - словарь, в котором ключи - это текст, который надо заменить, а значение - текст, которым заменяют&#x20;
3. **match\_case** - необязательная переменная. Если указать ее, равной 1, то поиск будет выполнен в строгом соответствии с указанным регистром. По умолчанию регистр не учитывается.&#x20;

{% hint style="warning" %}
<mark style="color:red;">**Обратите внимание!**</mark>  В словаре с данными для замены используются только двойные кавычки.
{% endhint %}

**Пример:** У нас есть текст-заготовка для анкетирования.

<figure><img src="../../.gitbook/assets/image (93) (1).png" alt=""><figcaption></figcaption></figure>

name ='Одинсон Локи Лафейсон' \
phone = 79004443322 \
\
array = {"company":"ООО АСГАРД","fio": "#{name}","phone\_number": "#{phone}","address":"Асгард, дворцовая улица, Палас 1","message":"Эй, пс. Не хочешь поговорить о Локи?"} \
\
new\_doc = gd\_replace\_text('1UfOZ5-AXb-QRAs7Gev9tv\_H3Cx5JuWbFeeHq48CEyAY',array, 0) \
new\_doc = gd\_replace\_text('1UfOZ5-AXb-QRAs7Gev9tv\_H3Cx5JuWbFeeHq48CEyAY',array, 0)&#x20;

<figure><img src="../../.gitbook/assets/image (94) (1).png" alt=""><figcaption></figcaption></figure>

Результат выполнения функции - словарь, содержащий уведомление об успехе

({"status":true,"message":"document 1UfOZ5-AXb-QRAs7Gev9tv\_H3Cx5JuWbFeeHq48CEyAY successfully updated"}) и видим, как изменился документ.&#x20;

<figure><img src="../../.gitbook/assets/image (95) (1).png" alt=""><figcaption></figcaption></figure>

{% hint style="info" %}
Совет! Если используете шаблон, сначала копируйте, а затем вносите изменения в копию - правки, которые вносятся через Salebot, нельзя откатить обратно через документы.&#x20;
{% endhint %}

## Как вставить изображение в конец Google-документа&#x20;

Воспользуйтесь функцией **gd\_add\_image(doc\_id, img\_url)**, где\
**doc\_id** - идентификатор документа, строка(например, 1pgC9TFC6P6tUse6KwmFFzmAmj0bhU3fwW8hIvJwXJ\_M) \
**img\_url** - ссылка на изображение, например, "https://cdn.sstatic.net/Sites/stackoverflow/company/img/logos/so/so-logo.png"&#x20;

**Пример:** add\_immage\_to\_doc= gd\_add\_image('1UfOZ5-AXb-QRAs7Gev9tv\_H3Cx5JuWbFeeHq48CEyAY','https://giknutye.r u/wp-content/uploads/2017/02/loki-6.jpg')&#x20;

<figure><img src="../../.gitbook/assets/image (96) (1).png" alt=""><figcaption></figcaption></figure>

Результат выполнения функции - словарь, содержащий уведомление об успехе

{"status":true,"message":"Image https://giknutye.ru/wp-content/uploads/2017/02/loki-6.jpg added to document 1UfOZ5-AXb-QRAs7Gev9tv\_H3Cx5JuWbFeeHq48CEyAY"}

<figure><img src="../../.gitbook/assets/image (97) (1).png" alt=""><figcaption></figcaption></figure>

## Как получить ссылку для сохранения Google-документа

Вы можете запросить ссылку на скачивание нужного документа в формате doc или pdf. Воспользуйтесь функцией **save\_google\_doc(doc\_id, type)**, где:

1. **doc\_id** - идентификатор документа, строка(например, 1pgC9TFC6P6tUse6KwmFFzmAmj0bhU3fwW8hIvJwXJ\_M)&#x20;
2. **type** - тип для скачивания, необязательный параметр. По умолчанию документ сформирует ссылку на скачивание в формате ‘.doc’. Если указать ‘pdf’, то документ сформирует ссылку на скачивание в формате ‘.pdf’&#x20;

**Пример:** save\_doc = save\_google\_doc('1UfOZ5-AXb-QRAs7Gev9tv\_H3Cx5JuWbFeeHq48CEyAY')

<figure><img src="../../.gitbook/assets/image (98) (1).png" alt=""><figcaption></figcaption></figure>

Результат выполнения функции - ссылка на документ

<figure><img src="../../.gitbook/assets/image (99) (1).png" alt=""><figcaption></figcaption></figure>

Остается его скачать.
