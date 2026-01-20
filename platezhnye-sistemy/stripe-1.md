---
hidden: true
---

# Copy of Stripe

* [Как подключить](stripe-1.md#podklyuchenie)
* [Как получить ссылку на оплату](stripe-1.md#kak-poluchit-ssylku-na-oplatu)
* [Как обработать результат](stripe-1.md#kak-obrabotat-rezultat)
* [Как настроить рекурентные платежи](stripe-1.md#kak-nastroit-rekurentnye-platezhi)
* [Как тестировать платежи](stripe-1.md#kak-testirovat-platezhi)

## Как подключить

Для подключения платежной системы Stripe вам потребуется секретный API-ключ и ключ webhook.&#x20;

Секретный API-ключ можно скопировать перейдя в раздел Developers -> API key и копируем Secret key.

Шаг 1. Переходим в раздел Developers -> API key:

<figure><img src="/broken/files/7PXmgc9q9TbSuoIDRwF0" alt=""><figcaption><p>Рис. 1. Как найти раздел api keys</p></figcaption></figure>

Шаг 2. Находим и копируем Secret key:

<figure><img src="/broken/files/29gwrx1CgRYcha1CSVgH" alt=""><figcaption></figcaption></figure>

Дальше нужно установить URL-адрес для колбэков. Это необходимо для того, чтобы бот получал уведомления об оплате.&#x20;

Переходим в раздел Webhooks и добавляем адрес для вебхуков.

<figure><img src="/broken/files/ahMHELMih7Bv6iOHe6QK" alt=""><figcaption></figcaption></figure>

Откроется форма:

<figure><img src="/broken/files/LQxWOXF2ZIkI9o9J8ZjI" alt=""><figcaption></figcaption></figure>

Шаг 1. Нажимаем на "+add destination".

Шаг 2.  Выбираем events:

<figure><img src="/broken/files/iIMCeFK0sJqLhu3cUStt" alt=""><figcaption></figcaption></figure>

Шаг 3. Выбираем тип "Webhook endpoint":

<figure><img src="/broken/files/dF76w2p9vlher1F5GTls" alt=""><figcaption></figcaption></figure>

Шаг 4. Ознакамливаемся с типом запроса и кликаем "Продолжить":

<figure><img src="/broken/files/tsZ810hZF51peu52zWi0" alt=""><figcaption></figcaption></figure>

Шаг 5. Прописываем название и указываем URL endpoint:

<figure><img src="/broken/files/2sGw3pAiUAMURp8EEqAQ" alt=""><figcaption></figcaption></figure>

URL указываем - [https://chatter.salebot.pro/stripe\_callback/result](https://chatter.salebot.pro/stripe_callback/result)

Шаг 6. Будет создано два эндпоинта, можно посмотреть настройки перед добавлением:&#x20;

<figure><img src="/broken/files/CVzE0hN4c1X9sYFZBdKx" alt="" width="563"><figcaption></figcaption></figure>

&#x20;и выбираем событие:

* `checkout.session.completed`

![](https://lh5.googleusercontent.com/gUvTcXFVw9WG-h_xl5BqBVYqTKNqq6pZ1OZ39QyKWBz8Mmn-gHWcmstNPRu0qYTVUR3Tza6OIYXnNK5JN3WzCIhKGQaiohdn2sxwkXeK59q_LafgIlqRlP7XnATuUdyJWiZ737lq)

Сохраняем и попадаем на страницу с установленным вебхуком, копируем ключ (Signing secret) вебхука (в salebot поле - Webhook key):

![](https://lh3.googleusercontent.com/exU2HdcUyAfQ4KwT5PKR0MbZoLD5gLV9inyUBk9xRjx5qGkXWhrief6qgx1BJEqJBeNs5Kf-lvepWSjFgGQxHCdOt6QIneP57Js55zSWls1CfW1YJ2H-j9GxO8qAtOr2K5IyCAAf)

после нажатия **Reveal** откроется ключ Webhook, который будет начинаться с **whsec\_**...

После получения ключей переходим к настройкам в Salebot.

В salebot открываем раздел платежные системы, выбираем Stripe. На странице подключения, нужно ввести полученные данные.

![](/broken/files/wN9Ht3ydUY2MhhuAjOp4)

<figure><img src="/broken/files/LXuOAkprQXIC9wyYYOwD" alt=""><figcaption></figcaption></figure>

## Как подключить колбек о статусе транзакции

Для получения дополнительного колбека нам потребуется подключить вебхук **дополнительно к имеющемуся.**&#x20;

URL указываем - [https://chatter.salebot.pro/stripe\_callback/\<api\_key>/charge\_status](https://chatter.salebot.pro/stripe_callback/%3Capi_key%3E/charge_status)

&#x20;и выбираем события:

* `charge.failed`
* `charge.pending`
* `charge.succeeded`

<figure><img src="/broken/files/Shu6S7ygJqazPFRECc3E" alt=""><figcaption></figcaption></figure>

<mark style="color:blue;">**Подробнее о каждом из типов вебхука:**</mark>\
**charge.succeeded** - содержит информацию об успешном завершении транзакции (аналогичен колбеку об успешной оплате)\
**charge.pending** - "транзакция выполняется", на выполнение может уйти до 7 дней. \
Вебхук будет иметь вид {первые 10 символов }_{тип вебхука}_ \
Например: _sk\_test\_45LDPJLKT95d\_charge.pending_ \
**charge.failed** _- "транзакция провалилась"._ \
_Вебхук будет иметь вид {первые 10 символов }_{тип вебхука} \
Например: _sk\_test\_45LDPJLKT95d\_charge.failed_

Полученный после сохранения вебхук добавляем в Salebot поле - Webhook key2:

<figure><img src="/broken/files/29ZgF198sYBy3qZn723K" alt=""><figcaption></figcaption></figure>

**stripe\_invoice\_id** - идентификатор сделки, по которой не пришел колбек об успешной оплате сразу после платежа

## Как подключить налоги

Для использования налогов в платежах нужно сперва создать их в личном кабинете Stripe. Для этого перейдите в раздел Products, где нужно выбрать пункт Tax rates

<figure><img src="/broken/files/489ozFu9WKxvDWBLKxCI" alt=""><figcaption><p>Настройка налоговых начислений</p></figcaption></figure>

Далее указываем применяемую налоговую ставку

<figure><img src="/broken/files/1TTnrP2pe3y5yugeSQzv" alt=""><figcaption><p>Добавление налоговой ставки</p></figcaption></figure>

В открывшемся меню выберите тип налога, регион, для которого он применяется, процентную ставку и признак - будет этот налог включен в сумму платежа Inclusive или будет добавлен сверх суммы - exclusive

После создания налоговой ставки скопируйте его id в переменную **stripe\_tax\_id** до объявления суммы платежа.

Во избежание ошибок желательно после получения ссылки в переменную stripe\_tax\_id поместить пустую строку (""), так вы сможете применять налог только тогда, когда он нужен

Если все сделать правильно, то в случае с налоговой ставкой с параметром exclusive Вы увидите следующее

<figure><img src="/broken/files/xCVAL1yrIjVtse1G3AHX" alt=""><figcaption><p>Пример платежа с налоговой ставкой типа exclusive</p></figcaption></figure>

## **Как получить ссылку на оплату**

Для генерации ссылки на оплату вам необходимо установить значение переменной **payment\_sum** (например 150 или 100.55 (через точку!)), сразу после этого появится переменная stripe\_pay\_url. Эту переменную можно вывести на экран ссылкой или разместить на кнопке с текстом "Оплатить".&#x20;

Ссылка имеет вид:&#x20;

`https://checkout.stripe.com/pay/cs_test_a17mskKFFRwEuo3WgBSAUjfk7xaZZIrct9B3Ds2AdODVq1I8aRiqYEBdrU#fidkdWxOYHwnPyd1blpxYHZxWjA0TGFsVzFPVmpmMzJAbVYzUkp1Y0lLYDVgfzR2Q0NxcWZBNUNnTnRSVVRJSGFobEB1UExSczRMMTc8PWRLMGBddl8xalxyPDRoUGhnZm9xXXZANDZyaF0wNTVBVExsPHZyfycpJ2N3amhWYHdzYHcnP3F3cGApJ2lkfGpwcVF8dWAnPyd2bGtiaWBabHFgaCcpJ2BrZGdpYFVpZGZgbWppYWB3dic%2FcXdwYHgl`

{% hint style="warning" %}
По умолчанию установлен USD (доллар), если нужна другая валюта нужно установить значение переменной **currency**
{% endhint %}

Также до установки значения переменной **payment\_sum**, можно задать следующие необязательные переменные, для настройки платежа.

<table><thead><tr><th width="255">Параметры функции</th><th>Описание паараметра</th></tr></thead><tbody><tr><td><strong>currency</strong></td><td>валюта заказа. Допустимые значения - <a href="https://stripe.com/docs/currencies">https://stripe.com/docs/currencies</a></td></tr><tr><td><strong>payment_description</strong></td><td>описание заказа</td></tr><tr><td> <strong>stripe_tax_id</strong></td><td>идентификатор налоговой ставки, настроенной в личном кабинете Stripe</td></tr><tr><td><strong>stripe_invoice_enable</strong> </td><td>признак необходимости сохранять инвойсы (счет-фактуры, чеки).  Укажите любое значение, тогда все необходимое Вы найдете в личном кабинете Stripe </td></tr><tr><td><strong>stripe_locale</strong></td><td>установить язык страницы оплаты: en, ru, de.  Все доступные:  <a href="https://stripe.com/docs/api/checkout/sessions/create#create_checkout_session-locale">https://stripe.com/docs/api/checkout/sessions/create#create_checkout_session-locale </a><br>Если не передано значение <strong>stripe_locale,</strong> то будет использован язык браузера клиента.</td></tr><tr><td><strong>stripe_payment_method_type</strong></td><td><p> метод оплаты, по умолчанию стоит оплата картой (card).  Можно заменить на другие доступные для Stripe методы оплаты. Ниже указаны доступные методы.</p><p>Например, <code>stripe_payment_method_type = "customer_balance"</code></p></td></tr><tr><td><strong>stripe_additional_payment_method_type</strong> </td><td>добавить дополнительный метод оплаты. Ниже указаны доступные методыНапример, <code>stripe_additional_payment_method_type  = "sepa_debit"</code></td></tr><tr><td><strong>coupon_id</strong></td><td>идентификатор купона скидки</td></tr><tr><td>stripe_expired </td><td>время жизни ссылки на оплату. Указывается в секундах. Минимальное время 30 минут, максимальное - 24 часа. По умолчанию 24 часа</td></tr><tr><td>stripe_automatic_tax</td><td>включение автоматического расчета и сбора налогов при оплате. Для включения передать "1". Подробная информация об этой настройке <a href="https://docs.stripe.com/tax/set-up">в документации Stripe </a></td></tr></tbody></table>

{% hint style="warning" %}
Важно! Если используете обе переменные _**stripe\_payment\_method\_type** и  **stripe\_additional\_payment\_method\_type, то значения в них ОБЯЗАТЕЛЬНО должны быть РАЗНЫМИ!**_
{% endhint %}

_<mark style="color:green;">**Список значений для**</mark>**&#x20;&#x20;****stripe\_payment\_method\_type** и  **stripe\_additional\_payment\_method\_type:**_

card\
acss\_debit\
affirm \
afterpay\_clearpay \
alipay\
au\_becs\_debit \
bacs\_debit \
bancontact \
blik \
boleto \
cashapp \
customer\_balance \
eps \
fpx \
giropay \
grabpay \
ideal \
klarna \
konbini \
link \
oxxo \
p24 \
paynow \
paypal \
pix \
promptpay \
sepa\_debit \
sofort \
us\_bank\_account \
wechat\_pay zip\
\
Подробнее про каждый из методов и для каких стран они доступны можно узнать в документации Stripe: [посмотреть на сайте ](https://stripe.com/docs/api/payment_methods/object#payment_method_object-type)

### **Пример формирования ссылки на оплату**

Создадим ссылку на оплату в размере 2 евро (по умолчанию доллар)

![](/broken/files/gbflX3ENSpc6OluOn1oK)

{% hint style="warning" %}
Для формирования ссылки рекомендуется использовать блоки Первостепенной проверки условия (светло-зеленые) с переходом в них по условию (без стрелок с таймером).&#x20;
{% endhint %}

{% hint style="info" %}
**Обратите внимание:** \
\- Сначала указываете необязательные параметры  **first\_name, payment\_description** и т.д.\
\- И последней присваиваем значение переменной **payment\_sum**
{% endhint %}

**Обратите внимание,** вначале задаем дополнительные переменные для настроек, затем payment\_sum. Переменные можно задать и ранее в цепочке, а не в одном блоке, это пример.<br>

Далее в нужном месте выводим переменную **stripe\_pay\_url**, в которой содержится ссылка в блоке либо в кнопке:

<figure><img src="/broken/files/14rcWL8BD4hihc0S2If7" alt=""><figcaption></figcaption></figure>

<figure><img src="/broken/files/fr9CFq5XSCHHQf194TIL" alt="" width="480"><figcaption></figcaption></figure>

Допустимо оба варианта вставки ссылки в блок.&#x20;

Пример платежной страницы

![](https://lh3.googleusercontent.com/0246dEgnqPF00mHryviFdzqduBSBnjkcVMawEwLBxQ1nTcbjsBsxDT9klqlJvrTRIl1J8fJ6vdoTiuYfc4KvPwlnZBwOs9E6iGUQht1Nq5M5oNlB_y0wJqQdVXXzu5qt8VfXEgnY=s0)

### Как добавить скидку в заказ

1. При генерации ссылки на оплату (работает как для подписок, так и для разовых платежей).

В калькуляторе блока до объявления переменной **payment\_sum** задайте переменную **coupon\_id**, передав в неё идентификатор скидки из личного кабинета stripe.<br>

<figure><img src="https://lh7-us.googleusercontent.com/h3JIvFePtG2iosF4g67APvVBJwbqwu0OELqgNEYAvcwogYmGUiZqms7BqF5WLNO6COa_i2r0PrFyg0mhpD3ovzpmpgPjkG422YZw7Pdt-KcTDwgID7s6bXIG_99Xd5LV_BaFj8JndyQDFT7pTtTMhNY" alt=""><figcaption></figcaption></figure>

2. В существующую подписку с помощью функции **stripe\_add\_subscription\_discount.**

Задайте условия для срабатывания блока и в калькуляторе вызовите указанную функцию, передав в нее параметры stripe\_subscription\_id (id подписки) и coupon\_id (id купона на скидку). Скидка будет применена для последующих платежей по подписке.

<figure><img src="https://lh7-us.googleusercontent.com/x7PlCq4dNOEJ3CQevnJg6eqoZkMQp0rmLG7JzKLXdTD-VMMdqAayusdGcPHZyPWdo7KgcpDwoqv5z5UCV0TkRAycoGndNb3Dxz39yqMqJH0iHJd5h8v7DRf5KCrjirygtcic4QW1qUdnsVepnYfz__U" alt="" width="563"><figcaption></figcaption></figure>

При успешном добавлении функция вернёт сообщение с указанием id подписки, вида, суммы или процента скидки, а также срока её действия.

<figure><img src="https://lh7-us.googleusercontent.com/b-Ykyl6U-AHe7zGmR3NDImJe_89DfVs1kpd26NmxoEQGIssPmFjufBy8fxnv-1EImgwxU81qxqGi5IK-60FQYz93gKhlQnTihtkvz25VIxjHnIhiehmkb9C_tFWz7AjWWLWUIi2B-pR8Yie0TBekZXU" alt=""><figcaption></figcaption></figure>

### Как создать купон и получить ID скидки

Для получения идентификатора скидки создайте купон в личном кабинете в разделе ”coupons”. ([https://dashboard.stripe.com/coupons](https://dashboard.stripe.com/coupons)).&#x20;

<figure><img src="https://lh7-us.googleusercontent.com/540OxGn1xUgwTaCqJHGZ15-Scf81QaQtw6jdpRvBRG2zf7CGe6i1nxxLZhHJBxY8s4CTCijlcD1u6MUjJ9K5bZBynkVBl8P878y4pP9DDoAmIoMWLWyiFx4XBW5qR5QU3G47-5fs8rQIBLL-1unbqw8" alt=""><figcaption></figcaption></figure>

При нажатии кнопки “New” откроется страница, где нужно указать Name (название скидки), ID (идентификатор, также генерируется автоматически), Type (вид скидки: в процентах или фиксированная сумма), Duration (длительность скидки: разовая или продолжительная, например, для подписок) и другие параметры.

<figure><img src="https://lh7-us.googleusercontent.com/ubyDZRBTtEeyPqovLZVbvgiqOI74nygpr5814QKRuPM3GlO013oqjD4XzD9-W4NIzj7bxrmvASrXi4Tq-WbpY8e8LDFyNdT2pFtdzUa3lsHRmm99otRnpsIpS-oZbytdy2LqKQpdZljLWYSrY753-KU" alt=""><figcaption></figcaption></figure>

Купон со скидкой появится в каталоге “Product catalogue“ в разделе “Coupons”, а ID скидки вы можете посмотреть, зайдя в меню купона.



### Как удалить/изменить скидку для подписки

Прикрепленную к подписке скидку можно удалить или заменить другой скидкой.

Если вы хотите прекратить действие скидки, задайте условие для срабатывания блока и в калькуляторе вызовите функцию  **stripe\_remove\_subscription\_discount**, передав в неё параметр **stripe\_subscrition\_id** (id подписки).&#x20;

<figure><img src="https://lh7-us.googleusercontent.com/jM4gKBJKTz1KWCbiNMpNKzpG0Y-VIS8hrWCWeD5-6XvyjMHZQOXTR00WH_Dp_BBEKvQQLlQttxLVtCQ8aRuXxG5SUcRyERCGtOTfdSxU8rUI1u6xQ0EF3_cfo50U9Si87x7fyf_X4TmvSaliko5E2vc" alt=""><figcaption></figcaption></figure>

При успешном выполнении операции функция вернёт сообщение, содержащее id подписки и дату отмены скидки.

<figure><img src="https://lh7-us.googleusercontent.com/RvJXLIyOeSxWbfiQ9UJ55mFDgj8CZTz83ezN4akReEds5qhRcXwRzvGDBHwKuIUePRxTD9oRRpmazUNkw_YuEvrATAPo4MF4JnLwIh5dYbPiT3hJpZv4Eq-r0MOd1cOi3r9Um4q7QcvyG-Nn1XK1DCE" alt=""><figcaption></figcaption></figure>

Замена скидки, как и добавление новой, производится с помощью функции **stripe\_add\_subscription\_discount.** Не забудьте передать в нее параметры **stripe\_subscription\_id** и **coupon\_id**.\
Успешный запрос обновит прикрепленный к подписке купон и вернет сообщение с актуальными данными.

Например: сообщение в ответ на запрос о добавление скидки

<figure><img src="https://lh7-us.googleusercontent.com/x0gxaca1j9P5RYxSSocowhN5_awJVfmi6QkQkJJ54q269xMR6kt10pEs-1lDiPtYXZkygJm4nuMcU3If7g_CJntl3Qvm0xN-HhHyvQI6_n2-ywDuEllfZ9TTaSiOnRMRuJWFA-7bTSR1rKAgN8-HvBA" alt=""><figcaption></figcaption></figure>

Сообщение в ответ на запрос о замене скидки&#x20;

<figure><img src="https://lh7-us.googleusercontent.com/eqC0DAOYJ75E9tFxjEBx7OihPOsojhAssiT-21Gh8PQSQFfq7IWflEFaaMWcd_Jv7rygrddke_2Ej7GUzbDnXhyN3-fQ7U_xxChAyH1t_55OVUgVieLPzy1LJXQqb73tcwrjjAySl4OZ6ex9ta2qrOw" alt=""><figcaption></figcaption></figure>

Для получения идентификатора скидки создайте купон в личном кабинете в разделе ”coupons”. ([https://dashboard.stripe.com/coupons](https://dashboard.stripe.com/coupons)).&#x20;

## **Как обработать результат**

После успешной оплаты в бот придут колбэки, по которым вы сможете понять, что была успешная оплата. Эти колбеки в системе вы видите как сообщения от пользователя, чтобы их не мог отправить пользователь, они состоят из 20 первых символов секретного ключа и приписки success, например: **sk\_live\_d35gky6d8ers\_success**&#x20;

Эти колбеки НЕ ВИДИТ пользователь, они отображаются только оператору.

Тип сравнения должен быть **"Полное совпадение"**

Также после успешной оплаты переменная **stripe\_payment\_completed** устанавливается в **True**.

Например, можно сделать обработку успешной оплаты блоком с условием и вывести соответствующее сообщение пользователю:

![](/broken/files/wRWiTALe7DS8imS99umg)

После завершения оплаты клиенту добавится переменная **stripe\_callback\_data**, содержащая данные ответа платежной системы по совершенной операции. Из полученного словаря можно извлечь необходимые данные при помощи метода **get**.

{% hint style="warning" %}
Для совершения повторного платежа обязательно необходимо обнулить payment\_sum, ранее сформированную ссылку и уже после переназначить переменную payment\_sum для получения свежей ссылки. Можно указать предыдущее значение.
{% endhint %}

## **Как настроить рекуррентные платежи**

Для рекуррентных платежей (подписки) нужно до объявления переменной **payment\_sum** объявить переменную **stripe\_subscription** и присвоить ей название подписки. \
Также можно добавить следующие переменные: \
**interval** – продолжительность интервала подписки, в эту переменную нужно передать значение **‘day’** - для дней, **‘week’** - недель, **‘month’** - месяцев, **‘year’** - лет. \
Если переменная не объявлена, то _**по умолчанию**_ будет передан параметр **‘month’**;

{% hint style="warning" %}
**Важно!** Продолжительность одного цикла подписки не может быть более 1 года (для параметра ‘year’), более 12 месяцев (для параметра ‘month’), более 52 недель (для параметра ‘week’).
{% endhint %}

**interval\_count** – количество указанных интервалов, сколько дней, недель или месяцев будет в подписке за указанную сумму. _**По умолчанию**_ будет передан параметр, равный единице (**1**);

**stripe\_payment\_method\_type** - метод оплаты, по умолчанию стоит оплата картой (card).  Можно заменить на другие доступные для Stripe методы оплаты. Ниже указаны доступные методы.

Например, `stripe_payment_method_type = "customer_balance"`

**stripe\_additional\_payment\_method\_type** - добавить дополнительный метод оплаты. Ниже указаны доступные методы

Например, `stripe_additional_payment_method_type  = "sepa_debit"`

{% hint style="warning" %}
Важно! Если используете обе переменные _**stripe\_payment\_method\_type** и  **stripe\_additional\_payment\_method\_type, то значения в них ОБЯЗАТЕЛЬНО должны быть РАЗНЫМИ!**_
{% endhint %}

_<mark style="color:green;">**Список значений для**</mark>**&#x20;&#x20;****stripe\_payment\_method\_type** и  **stripe\_additional\_payment\_method\_type:**_

card\
acss\_debit\
affirm \
afterpay\_clearpay \
alipay\
au\_becs\_debit \
bacs\_debit \
bancontact \
blik \
boleto \
cashapp \
customer\_balance \
eps \
fpx \
giropay \
grabpay \
ideal \
klarna \
konbini \
link \
oxxo \
p24 \
paynow \
paypal \
pix \
promptpay \
sepa\_debit \
sofort \
us\_bank\_account \
wechat\_pay zip

{% hint style="info" %}
Подробнее про каждый из методов и для каких стран они доступны можно узнать в документации Stripe: [посмотреть на сайте ](https://stripe.com/docs/api/payment_methods/object#payment_method_object-type)
{% endhint %}

{% hint style="warning" %}
**Важно!** Продолжительность подписки не может быть более 1 года (для параметра ‘year’), более 12 месяцев (для параметра ‘month’), более 52 недель (для параметра ‘week’).
{% endhint %}

В данном примере подписка с названием 'My\_subscription' будет создана с ценой 90 USD за 3 месяца и повторный платеж будет с той же суммой по истечении этих 3 месяцев:

![](https://lh4.googleusercontent.com/aqgoveJt-JY-NBi-k1cD-l6q4D6XcDIurZKTiF_C25aaMUTyGphdewi1nBD3Qb-p3ucsqjns89x2l7iSohBmR9RwimrwTSe0l8rIky0xzd5o7iYQ7bGt2WlLL8TzzkBQOLRzGHXbX2exnD4hCCg)

Пример для копирования:

`stripe_subscription = 'My_subscription'` \
`interval = 'month'` \
`interval_count = 3` \
`payment_sum = 90`&#x20;

После оплаты в переменных сделки у клиента появится переменные **stripe\_subscription\_id,** которая потребуется для настройки отмены подписки, и **stripe\_customer\_id**, которую в дальнейшем можно использовать для проверки статуса подписки.

{% hint style="warning" %}
Уведомление(колбэк) приходит только при первом рекуррентном платеже!

На повторные коллбэка НЕ БУДЕТ. Контроль идет [через функцию](stripe-1.md#proverka-statusa-podpiski) и stripe\_customer\_id.
{% endhint %}

<figure><img src="/broken/files/spCHK42QWAZyfUzhSUs1" alt="" width="371"><figcaption></figcaption></figure>



### Настройки для возврата к обычным платежам

Для возврата к обычным платежам присвойте переменной subscription пустую строку **stripe\_subscription = ''**. В таком случае переменные interval и interval\_count не повлияют на создание ссылки

![](https://lh4.googleusercontent.com/EO4ZmQikzxo6sxOHgAcKMMtMcAF733OcUNDOgi1xX02CPFVvpEXTaA1RQVWOqlKK0kBR0MR5woD02xa1gwO6Ngai-XEtYVvxwsB_e_KbJUk9Zb-ice2njUpdDBYIwf1cC83pCK5bHlMQeS4yY60)

### **Настройки для отмены подписки**

Для отмены подписки в калькуляторе используйте метод **stripe\_remove\_subscription(stripe\_subscription\_id)**, где \
**stripe\_subscription\_id** – идентификатор, который был сохранен в переменных о сделке после оплаты\
Это позволит оставить оплаченную подписку активной до конца текущего оплаченного срока, но дальнейшие списания не произойдут, и по истечении срока подписка будет отменена:<br>

![](https://lh4.googleusercontent.com/drLvBUMIL3gEy5U-M6uahYblrwc37qhKA3li6Rg-uNHm5CDiCIW_OsTn2jQSFkD9_u03Ibn4_vpoyRAxLyZhh5lj-Dts-rhaMlazud3b8ewZxGBMWb9B-h7xfxkKOdkV0oEdDDQcgvtVVGdJJac)

answer = stripe\_remove\_subscription('#{stripe\_subscription\_id}')

stripe\_remove\_subscription -  в случае успеха придет ответ с информацией до какого числа будет действовать отмененная подписка

В данном примере результат выполнения функции будет помещен в переменную answer и можно будет проверить результат выполнения.&#x20;

### Проверка статуса подписки

**stripe\_check\_subscription(subscription\_id, customer\_id)**, где

**stripe\_subscription\_id** - идентификатор подписки \
**stripe\_customer\_id** - идентификатор клиента в Stripe (необязательный параметр)

<figure><img src="/broken/files/13m0BPSf27vg2qG6bxAc" alt=""><figcaption></figcaption></figure>

> Функция проверки подписки добавлена в обновлении от 17 мая 2023

## К**ак тестировать платежи**

Для тестирования интеграции можете использовать секретный ключ из тестовой среды. Для этого в личном кабинете stripe меню справа, нужно переключиться в тестовую среду.&#x20;

![](https://lh5.googleusercontent.com/r-tuJboMES8alkTUpKwA4HKrmL_epNtSXdENrv12EyR9dGCtvRLBK6qw4UGcr59GA3unxc1cV1otCu80nqHEw9VhbEK05ovPQ1Ad8chBv50LAWPO16nEPC2hFhCAsCe3khtBJrob=s0)

Далее провести настройку описанную в начале этой инструкции. Ввести тестовый секретный ключ и добавить адрес для вебхуков в тестовую среду.

Тестовый номер карты

4242 4242 4242 4242\
дата любая в будущем\
CVC - любые три цифры

Если что-то не работает, сравните данные с данными на официальном сайте: [https://stripe.com/docs/testing#regulatory-cards](https://stripe.com/docs/testing#regulatory-cards)
