# UISCOM

## **Как подключить сервис**

### **1.**&#x41F;одключение компонента

Для настройки интеграции UISCOM c Salebot.pro в кабинете UIS необходимо подключить компонент API Оптимальный. Подключить компонент можно только под правами Администратора.

Для этого необходимо в верхнем правом углу нажать "Администратор - Аккаунт". Слева в меню выбрать раздел "Тарифы и опции", в предоставленном списке опций найти "API Оптимальный" и нажать кнопку "Подключить".

![](https://lh5.googleusercontent.com/xxv6aaSq1gWbysZu5wnQ7BH9BIyk0sw5R0bVfcDMCAWVKat1ZV49dQ02HK5KAuRJovbepPaPmk-Y9kZtDCkumW3x9zek0p_gBqMItPUFdaHm7xPCLhGangWpvvk9KUX_WD4_jrjTFy6c8N-7-A)

### 2. Настройка доступов API

Для работы интеграции необходимо сформировать ключ API, а также добавить IP-адрес salesbot.pro в список разрешенных.

Для формирования ключа API  в верхнем правом углу  перейдите в "Администратор - Управление пользователями".

Можно редактировать либо уже имеющегося пользователя, либо создать нового.

![](https://lh4.googleusercontent.com/J0mm26cHnYssOXiU8-S3leDJYHJFFWk1msWuSS_aiYUiKJZaOAr67K_B71jTdon2XGbu_usHmC0GvI8H147TWvVpDF-ocj0UR6PPMHckQ__ioEZtD3RuiPZVNA40rV16zw8UeNySS9E95-PiNA)

При редактировании или создании пользователя внизу должны быть выбраны следующие пункты:

1. Data API
2. Call API
3. Использовать ключ API - бегунок в положении включен&#x20;
4. Время жизни - Вечно

![](https://lh3.googleusercontent.com/C27d0rz-c51J_wH5DJ2ADY2klsR-fFl-YdLYGT13hJyrC46qaO9LcpcUeVTSKet5yHr058V82dX5ogPKVAfQ5A1qLmiVfiaPsL4CazpsKf6Zr-uZNgZNKe-B3SfWybr-WTBJxp-Ir2CsRs77JA)

При проставлении галочки _Использовать ключ A&#x50;_&#x49; генерируется сразу ключ, который нужно скопировать. Ключ отображается один раз: до момента сохранения данных при редактировании или создании пользователя. Если вы не скопировали сразу ключ, то можно сгенерировать новый. Полученный ключ API укажите в настройках подключения телефонии UISCOM в вашем проекте Salebot:

![](https://lh6.googleusercontent.com/tulI00TDhtXri71QTiBZuZYAw8MuaEPEXoIHX_9zHvuPmCGi2PcMmNJ6Dg57-QPowBU_YMPBaVBUeGpFy3hrrzSE35cTBxBsF80mTwLbwQyh1bV_Ph3XEsvzmMCGzg1TssvDIPwJ5os9OJ9AEw)

![](https://lh6.googleusercontent.com/6KDUL8VFShN9a5CcwEQ05-T6xZo0Ilh3TMguasVHtYt-N_YzjE5V4bGWw-W7RGP9ojkusNg5rLVdAI_agGhAAb415i3ksmVqNDtHnB0tKj0hAs0tPH_ojCra2skVk7FSdmAJXxNsZniVX_eFFw)

В Uiscom после создания пользователя нужно перейти в "Администратор - Аккаунт", слева выбрать раздел "Правила и настройки безопасности", вкладка API. Нажать кнопку "Добавить", ввести в поле IP/Маска <mark style="color:red;">**ДВА IP-адреса: 158.160.42.134 и 62.84.125.172 (адрес salesbot.pro)**</mark><mark style="color:red;">;</mark> и нажать на дискету, чтобы сохранить указанный адрес.

![](https://lh6.googleusercontent.com/a7XzIofcRfMVZJZ-ZtbteRszLkJyxV0qkz_Im8iGDp8lUHnuodY1Dyu6VeB6crQ8d6QyckAGuXSGF3iVO3GDhtHElZhAXX_9ytQwXKxJJHHnBmK5clGGQrKAnalvUYIT4GVqbPhUc1-h--GfoQ)

{% hint style="info" %}
Внимание!&#x20;

**IP-адреса для добавления при настройке интеграции:**

1\)  158.160.42.134

2\) 62.84.125.172

Необходимо добавить оба IP адреса в настройках безопасности во вкладке АPI на стороне Uiscom.&#x20;
{% endhint %}

{% hint style="success" %}
При необходимости, можно разрешить в ЛК  запросы с любого ip через 0.0.0.0/0.&#x20;
{% endhint %}

### 3. Настройка телефонии

Если у вас еще не подключен номер UISCOM, то его можно подключить, перейдя "Администратор - Аккаунт", слева выбрать раздел "Управление номерами" и нажать кнопку "Подключить".

![](https://lh3.googleusercontent.com/xoiHkdcEerFgXQoehMcAAsj4oY74RZUbNsIa0b0xeKnX8gtDl9KY7ZnbX7IWx3LeNp7_usKCV1p01hwWi9yhjodDqWk_fzWAEnmeZPXuiAq5NAsYog12etC7CFONis4iJe_ah9_u5cX3Nrxkww)

Во всплывающем окне выбрать понравившийся номер, проставить галочку "Согласен с условиями" и нажать кнопку "Подключить".

![](https://lh4.googleusercontent.com/IA2-Scve35On7j_ZIh3Iy3jTkVr6Pch7n5EuQW7l0lYSsCqxPL6EDZZV2nYEBZPjXS0RulUUS6iLUHQwfHpdiwKIgkfa8D9Wj7WVv5xlxdRPnFTOmKnvPdUk8CA56h6Q55jNS-GtAjH_zbsQ1Q)

Для совершения звонков по сценарию, требуется создать сценарий в разделе "Виртуальная АТС - Сценарии".

![](https://lh3.googleusercontent.com/68Q_DS-jtdQyYVjcYClbm24DJiSPx38zxkGRC7iAm8Xkfvlb3WQUIytnOiCokuiRmJ8qmVVNYZT4qXr6w2zs3Y2e_47WChneUNC-JLTXXeuEfoJgSS3wcuhWYXN5Gg3q0LBn8aAo0yvHrz4KHQ)

После создания сценария необходимо получить id сценария, по которому должны обрабатываться звонки. Для этого нужно перейти в редактирование сценария и в адресной строке найти значение параметра "controller.params=xxxxxx" (вам нужны цифры, которые в дальнейшем понадобятся для настроек в salesbot.pro)

![](https://lh6.googleusercontent.com/55-btMlxSYPYApTq52El6Ui9c-X9vqv_6QkqE8INDlIexSCVlqnTSav8oNrervAyzBHHPLYGph1fajHN6-MVfymGg6QlJEHLmhVP9gyKdxfqXOxRmIHkrbbm8xazWdONVEVGZd66aagC1huyog)

Для того чтобы звонки поступали конкретному сотруднику требуется создать соответствующего сотрудника в разделе "Сотрудники".

![](https://lh4.googleusercontent.com/Ja-HGOfV1KHXsnb4W8YnDusiHq5wlaBY1O3KDoQU1u4bGU-P2O0lYToBnGNfKgIpPULTV1MbvD2zZ5_JK44K4_R_-SKpwC9bPLxT7ASVcrPomHtEgVtVqVgw-wLqDN-92JCW5Fr_kKcLlem9Iw)

После создания сотрудника необходимо получить id сотрудника, на которого должны поступать звонки. Для этого нужно перейти в редактирование сотрудника и в адресной строке найти значение параметра "controller.params.recorId=xxxxxxx" (вам нужны цифры, которые в дальнейшем понадобятся для настроек в salebot.pro)

![](https://lh3.googleusercontent.com/zzv2MdGa_3SOaA90r_CpVsl-jazxuGLzToZeZMsLzKY97vuz425JUDffPTGRNkFRjfL0pSLsMEY5jOW-cMZa-TSBpC7LuSnkwISZrTePgu5QHLZ13pGTFXwQpfI_HL-YuqHztSkzE89CeVx49Q)

## Как получить полный вебхук от UISCOM

{% hint style="info" %}
Вебхук - это уведомление о произошедшем событии. Такое уведомление содержит значения измененных переменных.
{% endhint %}

Для получения полного вебхука от UISCOM достаточно присвоить любое значение переменной  **save\_webhook** \
Переменная может быть как константой проекта, так и переменной сделки.

<div align="center"><figure><img src="../../.gitbook/assets/2023-03-20_17-35-37.png" alt=""><figcaption><p>Переменная сделки: присваиваем<br>в Калькуляторе блока </p></figcaption></figure></div>

<div align="center"><figure><img src="../../.gitbook/assets/image (14).png" alt=""><figcaption><p>Константы проекта</p></figcaption></figure></div>

При этом ответ UISCOM будет записываться в переменную **`uiscom_request`**, которую вы найдете в карточке клиента среди переменных сделки.

<div align="center"><figure><img src="../../.gitbook/assets/image (15).png" alt=""><figcaption><p>Пример значения переменной <strong><code>uiscom_request</code></strong></p></figcaption></figure></div>

## **Как происходит сопоставление клиента**

Для работы с телефонией используются номера в формате 71234567890 (должен начинаться с 7, состоять из 11 цифр и не иметь лишних знаков и отступов).&#x20;

Последовательность сопоставления данных о клиенте:

1\. Осуществляется поиск клиента Телефонии. Если клиент не найден, то происходит поиск по значениям всех переменных по всему списку клиентов проекта. Первая найденная запись о клиенте считается тем самым "искомым" клиентом.

2\. Если клиент не найден среди клиентов Телефонии и:\
\- к проекту подключен любой мессенджер, например, Whatsapp, то будет создан клиент Whatsapp с данным номером телефона. \
\- к проекту не подключены иные виды мессенджеров (Whatsapp, Viber, Instagram и т.д.), то будет создан клиент Телефонии. Такому клиенту Вы сможете совершать только звонки с получением информации о них. Написать такому клиенту возможности нет.

## **Функция звонок сотруднику в Salebot**

Для того, чтобы совершить звонок сотруднику из бота, необходимо использовать функцию **uiscom\_employee\_call(virtual\_phone, client\_phone, employee\_id)**, которая принимает на вход следующие параметры: \
virtual\_phone - виртуальный номер, строка, пример - '78001002752' \
client\_phone - номер клиента, которому должен быть совершен звонок, строка, пример - '79004443322'. \
employee\_id - идентификатор сотрудника, которому будет направлен звонок клиента, строка, пример - ‘2339292’.

Пример бота:

![](https://lh6.googleusercontent.com/6eTYSv2fEOI0_5a-CkY8S_sw5_DvCopKvyNRQLIONsMVOjZa80DanR9v4kt_VfO0EWJqIRhnbQCpStivb8veSf4hmX38OHBMlnejxsnqYnx4xSFvFXdzGJqNbZpzf6lqsze1k1Gos_TflsxNLQ)

<figure><img src="../../.gitbook/assets/2023-12-01_18-37-04.png" alt="" width="563"><figcaption></figcaption></figure>

## Функция звонок по сценарию в Salebot

Для того чтобы совершить звонок сотруднику из бота, необходимо использовать функцию **uiscom\_scenario\_call( virtual\_phone, client\_phone, scenario\_id)** , которая принимает на вход следующие параметры: \
virtual\_phone - виртуальный номер, строка, пример - '78001002752' \
client\_phone - номер клиента, которому должен быть совершен звонок, строка, пример - '79004443322'. \
scenario\_id - идентификатор сценария, по которому будет распределен звонок клиента, строка, пример - ‘328746’. \
Пример реализации функции в боте:

<figure><img src="../../.gitbook/assets/2023-12-01_18-27-42.png" alt="" width="560"><figcaption></figcaption></figure>

## **Настройка звонков из карточки клиента**

Чтобы настроить осуществление звонков непосредственно из карточки клиента. Для этого в систему Salebot вы должны внести своих сотрудников. После того, как вы зарегистрировали сотрудника, зайдите в редактирование его данных.

![](https://lh6.googleusercontent.com/iANl6NFNGBL9cWOjSQtlNDOWSe3xqzh3DSN1-FCZ3c7FI_qgLDMY6xboUQQ5LX7KDEvzF9SxP5kXLXc8KQrmciIJnrnfRpxJmZ1Z83v8jPowq60wxGQ0o5bOVz4MrhVZf8LABDMOOR7mdN6Ihg)

В позиции “Способ совершения телефонных звонков” выберите звонки по API Uiscom.&#x20;

* Если выбрать пункт **Отключить звонки**, то этот сотрудник не сможет совершать звонки и иконка телефона возле номеров телефона у него не будет отображаться.&#x20;
* **Звонки через приложение** - при нажатии на иконку телефона звонок будет перенаправлен в приложение, установленное для звонков на Вашем устройстве (Zopier и тд).&#x20;
* **Звонки по API Uiscom** - при клике на иконку телефона АТС звонок поступит сначала сотруднику, чей id вы указали в карточке, а затем перенаправляет звонок клиенту.

![](https://lh6.googleusercontent.com/pqfbWRNcSO0YK-B0j-vkQKg6uPN14omVxwUgthBWaXDA0Mo8z70BunergMZZwdxnbHDrRp1nsuzTJn6tKN37OmPn6to09FbpecabXbRxK5dYLGQJ1-2h1-XACze0sZ1mkJEVITGt7upi0Jd4Hw)

Далее потребуется указать виртуальный номер, зарегистрированный в Uiscom, а также id данного сотрудника в системе Uiscom.

![](https://lh4.googleusercontent.com/wkZiuEHfupS2bnk2sCv2BsUGoXQv5GuCR96m39LWiwT-b5-Js9HKZoWqZDka_14VCZv9_aeJ30lUy1wIDjx6CVIFqYGCOXnQw0dJ-XWR_0P4Onid1mVjCk1Jw7rg6Pd01Gfr8PEUh2I5RkL63w)

Для осуществления звонка выбранным методом достаточно в карточке клиента нажать на иконку телефонной трубки рядом с его номером телефона:

![](https://lh6.googleusercontent.com/pYuaVM0lxhF3JNeA4XOiaRab_NalUVXeBIHTws-b4iq7gvF53DSuORe8fPxN0_WoPqAil4uesAhMVZurDzapPbLOa_riXYR_aIwjMPbN9jT-TKPY5vzOHjzj2EqwmeaO_LrclNn1IK3aCDYuMQ)

## **Настройка вебхуков**

Чтобы настроить прием вебхуков с сервиса UIS, необходимо перейти в личный кабинет в раздел "Уведомления":

<figure><img src="../../.gitbook/assets/Снимок экрана 2024-10-22 в 16.03.38.png" alt=""><figcaption></figcaption></figure>

Далее нажмите на "Добавить уведомление":

![](https://lh3.googleusercontent.com/p7mA_eBn5tITymeWFj4xvRLZIWsR9rfwU-BwIYXJXJLkLNdqNXzNlbRPyOBESVEZY2ieGXXEvhKa6SzYNymR2oXcUpvXDxItQpYnfnCHGlp27y8Nx_XXZEx01jqrf4qQDYGKHjTSmvnCTuW0Sw)

Вы перейдете в настройки для добавления уведомлений:

<figure><img src="../../.gitbook/assets/Снимок экрана 2024-10-22 в 16.08.25.png" alt="" width="563"><figcaption></figcaption></figure>

Поставьте свитчер HTTP  в положение ВКЛ, метод - POST, а URL прописать вида [https://chatter.salebot.pro/uiscom\_webhook/](https://chatter.salebot.pro/uiscom_webhook/9xd99uobn9efrkjlx9ybsuz99c9m9nmz9fossm93)<апи-ключ>, например, **https://chatter.salebot.pro/uiscom\_webhook/9xd99uobn9efrkjlx9ybsuz99c9m9nmz9fossm93**

<figure><img src="../../.gitbook/assets/Снимок экрана 2024-10-22 в 16.09.48.png" alt=""><figcaption></figcaption></figure>

В тело запроса следует вставить следующий список: \
{ "external\_id":\{{external\_id\}}, \
"notification\_name":\{{notification\_name\}}, \
"virtual\_phone\_number":\{{virtual\_phone\_number\}}, \
"notification\_time":\{{notification\_time\}}, \
"scenario\_name": \{{scenario\_name\}}, \
"wait\_time\_duration" : \{{wait\_time\_duration\}}, \
"employee\_ids":\{{employee\_ids\}}, \
"contact\_info":{\
"contact\_phone\_number":\{{contact\_phone\_number\}}, \
"communication\_number":\{{communication\_number\}}, \
"contact\_id": \{{contact\_id\}}, "contact\_full\_name":\{{contact\_full\_name\}} \
}, \
"call\_session\_id":\{{call\_session\_id\}} \
}

Тип события уведомления и название уведомления вы выбираете самостоятельно:

<figure><img src="../../.gitbook/assets/Снимок экрана 2024-10-22 в 16.11.01.png" alt=""><figcaption></figcaption></figure>

При подключении вебхуков после совершения звонка клиенту в диалог приходят вебхуки вида "Uiscom\_event {название\_уведомления}":

![](https://lh4.googleusercontent.com/wZhWT42IpWK4ltttI0UUMTxfYZOiIGBFlxSh67vrDCTnAA7HGY69fzGwNKRCOgw4d1uBbXmrOA1fpBnMjuTXnMFQ_WUbkhTuld_qnzUCZj70tMviqqrGJe82QqkFVQ_XBR3XVgES-JzamV16UQ)

Где название вы задали самостоятельно в настройках Uiscom.&#x20;

## Прочий функционал UISCOM

### 1.Функция для загрузки офлайн-заявок в UISCOM

Для включения функциональности загрузки заявок в личном кабинете UIS / CoMagic, в разделе Тарифы и опции требуется подключить опцию "Загрузка коммуникаций из внешних систем".&#x20;

{% hint style="info" %}
Если такой опции в личном кабинете нет, скорее всего у Вас тариф, на котором данная опция не поддерживается. В таком случае пользователю нужно будет обратиться к своему менеджеру UIS / CoMagic.
{% endhint %}

<figure><img src="../../.gitbook/assets/photo_2023-03-08_22-31-53.jpg" alt=""><figcaption></figcaption></figure>

**uiscom\_offline\_messages(message, site\_id, campaign\_id, visitor\_session\_id, phone, name)**&#x20;

Параметры:\
**message** - текст заявки из параметров site\_id, campaign\_id, visitor\_session\_id должен быть передан только один

**site\_id** - уникальный идентификатор сайта, с которого будет передана заявка ([подробнее  ниже](uiscom.md#2.funkciya-dlya-polucheniya-saitov-i-ikh-identifikatorov))&#x20;

**campaign\_id** - уникальный идентификатор рекламной кампании в CoMagic ([подробнее ниже](uiscom.md#3.funkciya-dlya-polucheniya-reklamnykh-kampanii-i-ikh-identifikatorov))

&#x20;<mark style="color:red;">**Внимание!!!**</mark> Если в campaign\_id выберете id -1, то указывать надо site\_id&#x20;

**visitor\_session\_id** - Уникальный идентификатор сессии посетителя, полученный из CoMagic. Для получения ID необходимо использовать[ метод JS API Comagic.getSessionId() ](http://www.comagic.ru/support/api/javascript-api/)\
<mark style="color:red;">**ВАЖНО!**</mark> эти данные нужно будет получать с использованием JS API на своем сайте, а не через Salebot

**phone** - необязательный параметр, контактный номер телефона.  Будет добавлен автоматически, если номер телефона присваивался какой-либо переменной ранее и не был передан в текущей функции. &#x20;

**name** - имя клиента, если не передать в функции, то будет взято имя клиента из раздела клиенты

### 2.Функция для получения сайтов и их идентификаторов&#x20;

**uiscom\_get\_sites()** - вернет словарь вида: {'test.ru': 80913}. Ключ - доменное имя сайта, значение - его id

### 3.Функция для получения рекламных кампаний и их идентификаторов&#x20;

**uiscom\_get\_campaigns()** - вернет словарь вида: {'Тестовый источник': 401745, 'Посетители без рекламной кампании': -1}, где ключ - имя кампании, значение - его id. <mark style="color:red;">id равный -1 использовать нельзя!</mark>
