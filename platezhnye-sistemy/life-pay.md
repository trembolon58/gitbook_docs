---
description: >-
  Прием платежей через платежную систему Life Pay, описание настроек интеграции.
  ​​
---

# Life Pay

* [Как подключить](life-pay.md#kak-podklyuchit)
* [Функция для формирования ссылки](life-pay.md#kak-sformirovat-ssylku-na-oplatu)
* [Как обработать результат](life-pay.md#kak-obrabotat-rezultat-platezha.)

## Как подключить

Для подключения платежей через Life Pay нужно перейти на сайте [home.life-pay.ru](https://home.life-pay.ru/) в личный кабинет, во вкладку "Интеграция" → "Сервисы" и нажать на иконку ключа подключаемого сервиса

<figure><img src="/broken/files/ONdwXgWtuQxjR9gItsFz" alt=""><figcaption><p>"Интеграция" → "Сервисы" → получение ключа</p></figcaption></figure>

Далее необходимо получить ключ магазина и серверный ключ для подключения к Salebot и заполнения формы.

<figure><img src="/broken/files/DAAhIRNPP7QLu5sjSdkR" alt=""><figcaption><p>Ключи для подключения Life Pay к Salebot</p></figcaption></figure>

Далее возвращаемся во вкладку Сервисы → Интеграция на Life Pay и копируем идентификатор сервиса, его также нужно вставить в форму подключения платежной системы в Salebot.

<figure><img src="/broken/files/640BnxcyigyWmpc80Hi7" alt=""><figcaption></figcaption></figure>

Открываем нужный Сервис и вставляем в поле **“URL скрипта для получения веб-хуков”**, адрес:

**`https://chatter.salebot.pro/life_pay_callback/result`**

\
Также указываем ключ API, который получили на первом шаге и выбрать Версия подписи: <mark style="color:orange;">2.0</mark>

<figure><img src="/broken/files/evcdN6OymEBV08eA1nEi" alt=""><figcaption><p>Пример правильного заполнения формы редактирования на стороне Life Pay</p></figcaption></figure>

<figure><img src="/broken/files/RIFxOJVBjDt6HbUCUp22" alt=""><figcaption><p>Указываем версию 2.0, как в примере</p></figcaption></figure>

{% hint style="info" %}
Не забудьте сохранить изменения!
{% endhint %}

Переходим в проект на Salebot, в разделе "Эквайринг" выбираем Life Pay.&#x20;

<figure><img src="/broken/files/ap8yDXGM4m4xrmQB49y3" alt=""><figcaption><p>Раздел "Эквайринг" Salebot</p></figcaption></figure>

Заполняем поля данными, полученными ранее в личном кабинете Life Pay .&#x20;

<figure><img src="/broken/files/R8M6mJzWYuF2oqY4nQw6" alt=""><figcaption><p>Настройка Life Pay в разделе "Эквайринг" Salebot</p></figcaption></figure>

## Как сформировать ссылку на оплату

{% hint style="info" %}
Сформировать ссылку на оплату в блоке можно **ОДНИМ ИЗ** из доступных способов:

* При помощи функции `get_life_pay_payment_url` в поле Калькулятор или
* _При помощи переменной payment\_sum (устаревшая работающая версия, рекомендуется использовать метод через работу с функцией)_
{% endhint %}

## Функция get\_life\_pay\_payment\_url в Калькуляторе

Для формирования ссылки на оплату можно воспользоваться функцией `get_life_pay_payment_url` в Калькуляторе блоке.

В поле Калькулятор  переменной присвоим значение функции `get_life_pay_payment_url`&#x20;

{% hint style="info" %}
Название переменной задаете самостоятельно.  На скринах примеры названия переменных. \
\
В эту переменную запишется ссылка на оплату. Переменную можно вывести на экран ссылкой в сообщении или разместить в кнопке с текстом, например, "Оплатить".&#x20;
{% endhint %}

{% tabs %}
{% tab title="Калькулятор" %}
Пример верно заполненной функции:&#x20;

<figure><img src="/broken/files/MZ1GI4TRsccEef8svsfZ" alt="" width="563"><figcaption><p>Функция указана в калькуляторе, ссылка для оплаты будет выведена в тексте сообщения клиенту</p></figcaption></figure>

<figure><img src="/broken/files/aT5EtCXKlyVjZwSNU4fv" alt=""><figcaption><p>Переменная, в которой будет записана ссылка на оплату, указана в кнопке</p></figcaption></figure>
{% endtab %}

{% tab title="Описание параметров" %}
**`link_lifepay = get_life_pay_payment_url(amount, description, customer_phone, customer_email, expired, recurrent, extra_params)`**

#### Параметры функции:

<table><thead><tr><th width="213">Параметр</th><th>Описание параметра</th></tr></thead><tbody><tr><td><strong><code>amount</code></strong></td><td>Cумма  к оплате. Может быть как целым числом, так и числом с точкой. Пример указания параметров с точкой и без нее:  '120' или '120.25' - <mark style="color:orange;"><strong>параметр обязательный</strong></mark></td></tr><tr><td><strong><code>description</code></strong></td><td><mark style="background-color:blue;">Описание заказа.</mark>  В этом поле можно использовать только символы английского или русского алфавита, цифры и знаки препинания -  <mark style="color:orange;"><strong>параметр обязательный</strong></mark></td></tr><tr><td><strong><code>customer_phone</code></strong></td><td>Телефонный номер плательщика, необходимость обязательного ввода регулируется в настройках сервиса и параметрами платежного канала.<br><br><em>*Параметр необязательный. Чтобы пропустить данный параметр передайте вместо него пару одинарных или двойных кавычек или значение</em> <em><code>None</code></em></td></tr><tr><td><strong><code>customer_email</code></strong></td><td><p><mark style="background-color:blue;">емейл покупателя</mark>, необязательно, если передан параметр <code>customer_phone</code> </p><p></p><p>Чтобы пропустить данный параметр,  передайте вместо него одинарные или двойные кавычки.</p></td></tr><tr><td><strong><code>expired</code></strong></td><td>Время жизни ссылки для оплаты. <br><br><em>*Параметр необязательный. Чтобы пропустить данный параметр передайте вместо него пару одинарных или двойных кавычек или значение</em> <em><code>None</code></em></td></tr><tr><td><strong><code>recurrent</code></strong></td><td>Признак рекуррентного платежа, для передачи параметра укажите в функции '1'<br></td></tr><tr><td><strong><code>extra_params</code></strong></td><td>Дополнительные параметры, которых нет в данной функции. Возможные дополнительные параметры можно посмотреть по ссылке в <a href="https://docs.life-pay.ru/docs/ipsp/interaction/request_format">документации работы с API платежной системы</a></td></tr></tbody></table>
{% endtab %}

{% tab title="Пример кода для копирования" %}
`Пример, для копирования:` \
\
`link_lifepay = get_life_pay_payment_url('100', 'Testov pyyment', '', email, '03.08.2025 16:50', '{"comment": "Testov comment!"}')`
{% endtab %}
{% endtabs %}

Если ссылка на оплату не сформируется или каким-либо образом не получится ее создать, то причина будет отображена в переменной в карточке клиента:

<figure><img src="/broken/files/s46n5QdzVQteK6OpXaW4" alt="" width="371"><figcaption></figcaption></figure>

### Как обработать результат платежа.

После успешной оплаты в диалог клиента поступит уведомление, при помощи которого вы сможете настроить дальнейшую логику схемы. &#x20;

<figure><img src="/broken/files/KNb2cbSqWXTfrU5yaRMt" alt="" width="460"><figcaption><p>Пример уведомления</p></figcaption></figure>

Текст уведомления будет сформирован автоматически, первая его часть - 10 первых символов секретного ключа, далее  \
\
Если в уведомлении окончание `_success` то оплата прошла успешно. Также в уведомлении будет указана сумма платежа. Если у вас несколько продуктов с разной стоимостью, то вы сможете настроить обработку ответа по каждому продукту.&#x20;

\
Пример блока, который реагирует на успешную оплату от клиента

&#x20;`032d2f2e60_success 100.0`

<figure><img src="/broken/files/5z5sNS9NhhSKhS8p6UBO" alt=""><figcaption><p>Пример обработки платежа, блок настроен на успешный коллбэк от платежной системы</p></figcaption></figure>

### Рекуррентные платежи

Пример функции с заполненными параметрами и передачей признака рекуррентного платежа в скриншоте.&#x20;

<figure><img src="/broken/files/D2t9trLKrNy0OlAQrIKp" alt=""><figcaption><p>Функция для формирования ссылки с признаком рекуррентного платежа.</p></figcaption></figure>

После успешной оплаты у клиента появится переменная **life\_pay\_recurrent\_order\_id**, которая автоматически передается при вызове функции **life\_pay\_recurrent\_payment**, при последующих списаниях.

#### Повтор рекуррентного платежа

**`life_pay_recurrent_payment(amount, description, customer_email, additional_params)`**

{% hint style="danger" %}
До вызова функции нужно, чтобы клиент провел установочный платеж, сделав оплату по ссылке, полученной функцией **`get_life_pay_payment_url`**, с включенным параметром установочного платежа.&#x20;
{% endhint %}

Параметры функции: \
&#xNAN;**`amount`** - сумма платежа \
&#xNAN;**`description`** - наименование счета \
&#xNAN;**`customer_email`** - email покупателя \
&#xNAN;**`additional_params`** - дополнительные параметры не описанные в функции

#### Возврат оплаты по счету.

**`life_pay_refund_payment(invoice_id, amount, reason)`**

Параметры функции:\
&#xNAN;**`invoice_id`** - идентификатор счета \
&#xNAN;**`amount -`** сумма к возврату в валюте счета  \
&#xNAN;**`reason -`** причина возврата, параметр необязательный.&#x20;

#### Остановить рекуррентные платежи.

**`life_pay_stop_recurrent_payments()`** \
Остановка рекуррентного платежа. Функция не принимает параметры и удаляет связку  life\_pay\_recurrent\_order\_id

#### Получить параметры счета на оплату.

**`life_pay_get_payment_info(invoice_id)`** Получение параметров счета на оплату возможно реализовать функцией. \
Параметры функции: \
&#xNAN;**`invoice_id`** - внутренний номер инвойса

\
**Получение токена.**

**`life_pay_get_token()`** - получить jwt токен, для api запросов к LIFE PAY API ECOM (токен активен 3 часа (на момент публикации документации))<br>

### Оплата в курсах Salebot

Если планируется использовать платежную систему для оплаты в курсах, то нужно включить пункт в настройках магазина  "Обязательно заполнять поле Email для оплаты". Пример включенного окна в скриншоте ниже.&#x20;

<figure><img src="/broken/files/FKdReGMDZRiOiJB3IgXw" alt=""><figcaption><p>При включении чекбокса вы сможете принимать оплату за курсы на странице курса</p></figcaption></figure>

## Для фискализации чеков

{% hint style="danger" %}
Обращаем внимание! \
Salebot не предоставляет услуги фискализации и не взимает дополнительные платежи за проведение операций и формирование чеков.

Услуги фискализации, начиная от проведения рассчетно-кассовых операций и заканчивая формированием и отправкой чеков, предоставляются платежным сервисом Life Pay, в связи с чем все дополнительные платежи, подключение фискализации и иные необходимые Вам услуги оплачиваются и покупаются только на стороне [Life Pay](https://life-pay.ru/kassa/cloud/?utm_source=docslifepay).&#x20;
{% endhint %}

{% hint style="danger" %}
Обращаем внимание!

Если вы не приобрели подписку на фискализацию на стороне Life Pay, услуга работать не будет.
{% endhint %}

{% hint style="success" %}
Обращаем внимание!&#x20;

Поля для заполнения логина и API ключа в окне подключения на стороне Salebot для использования услуг фискализации являются необязательными.&#x20;

Вы можете подключить интеграцию без услуг для формирования чеков, что описано в разделе '[Как подключить'](life-pay.md#kak-podklyuchit).

[Данный раздел](life-pay.md#formirovanie-chekov-fiskalizaciya) является лишь одной из возможностей на стороне Salebot и не является обязательным.&#x20;
{% endhint %}

{% hint style="info" %}
Подробнее об услуге на стороне Life Pay можно прочитать в [документации сервиса.](https://docs.life-pos.ru/docs/CF/cloud-print/fiscalChequeFfd1_2)
{% endhint %}

Для функции фискализации в Life.pay необходимо перейти [по ссылке](https://my.life-pay.ru/site/login):&#x20;

<figure><img src="/broken/files/oBsxJhiezWZQH4oNn1nQ" alt=""><figcaption></figcaption></figure>

Далее необходимо ввести данные собственного аккаунта и перейти к странице на стороне интеграции:

<figure><img src="/broken/files/C2YYGCS70YZTa2MXfiem" alt=""><figcaption></figcaption></figure>

Далее перейдите в Настройки → раздел "Разработчикам", где вам необходимо найти ключ API для интеграции:

<figure><img src="/broken/files/TylI6WC4rXQ9D3jHjRCL" alt=""><figcaption></figcaption></figure>

Теперь перейдите в настройки проекта Salebot → раздел "Эквайринг":

<figure><img src="/broken/files/YSLnaFITX5JsPGdQCzn9" alt=""><figcaption></figcaption></figure>

Далее найдите необходимый платежный сервис и кликните на "подключить" (если у вас уже подключена интеграция, то будет кнопка "подключено"), после чего откроется окно с полями для заполнения:

<figure><img src="/broken/files/SRJY21U9HQ5syDcAPJnZ" alt="" width="563"><figcaption></figcaption></figure>

Для функции фискализации заполните следующие поля (если у вас еще не подключена интеграция, то необходимо заполнить ВСЕ поля при необходимости фискализации):

<figure><img src="/broken/files/L1txk0xvWdC80nzYXJ0t" alt="" width="563"><figcaption></figcaption></figure>

{% hint style="danger" %}
Логин от LifePay должен начинаться с 7: например, "7937 300 30 30", без плюсов и восьмерок.&#x20;
{% endhint %}

{% hint style="info" %}
Чеки формируются по стандартизированному формату ФФД 1.2.&#x20;
{% endhint %}
