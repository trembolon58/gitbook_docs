---
description: Настройка приема платежей в чат-боте через Paypal
---

# Paypal

* [Как настроить Paypal ](paypal.md#kak-nastroit-paypal)
* [Как создать ссылку на оплату ](paypal.md#sozdanie-ssylki-na-oplatu)
* [Как создать реккурентный платеж](paypal.md#kak-sozdat-rekkurentnyi-platezh)
* [Как обработать результат](paypal.md#obrabotka-rezultata)

## Как настроить Paypal

Для работы с paypal, нужно получить два ключа: **client\_id** и **secret**

Переходим на страницу [https://developer.paypal.com/developer/applications/](https://developer.paypal.com/developer/applications/)

И выбираем из списка или создаем новое приложение:

![](https://lh4.googleusercontent.com/i7wtKw-RzPSHarXCkIVIqPvAvn_39t1r4CPL9lSmxzFc1mNiz24zHj4PJIUUhCzL-YXaNrQbK5edCP9bYHGXkIij59shZ6XPj3YZiVp4uRlDllvWRetnF1Y3GSbQXRZt03OOiGxs)

Вверху меняем переключатель в Live режим и выбираем нужное приложение. Открывается страница с настройками, где находятся нужные нам данные:<br>

![](https://lh4.googleusercontent.com/DEKr4nWXl27UVUoT4Ycl_nOx0Aj-M7KrLcgxWR-uTaUFV82416Wwd2ib4ghxQ3jiW5P53KfMwkqvB_ZS3KjLxNNdn8bzbpvVgfeV5HKsL_iFcv6bc1y_0yntseRKzwPUGz37bpnn)

Копируем данные и вставляем в соответствующие поля в настройках Salebot: перейдите в раздел "Эквайринг" и найдите сервис Paypal:

<figure><img src="/broken/files/d6r7pG9qAWrnKCWWm1eR" alt=""><figcaption></figcaption></figure>

Далее нажмите "Подключить" и заполните поля ранее полученными секретным ключом и Client ID:

<figure><img src="/broken/files/sLuHYpmmNw7vRwHVIaah" alt=""><figcaption></figcaption></figure>

Далее нажмите "Сохранить настройки". На этом подключение окончено.

## **Как создать ссылку на оплату**

### С помощью переменной payment\_sum

Для генерации ссылки на оплату, вам необходимо установить значение переменной **payment\_sum** и сразу после этого появится переменная **paypal\_pay\_url**.&#x20;

| Параметры функции        | Описание параметр                                                                              | Примечание                                                                                                     |
| ------------------------ | ---------------------------------------------------------------------------------------------- | -------------------------------------------------------------------------------------------------------------- |
| **payment\_title**       | <p>(необязательная переменная) </p><p>это название товара.</p>                                 | Если не указать заполняется текстом: **“Оплата счета order\_id”** (order\_id - идентификатор заказа в сейлбот) |
| **payment\_description** | описание товара, необязательное поле                                                           |                                                                                                                |
| **company\_name**        | название вашей компании, отображается в самом верху платежной страницы (пример ниже, компания) |                                                                                                                |

![](https://lh4.googleusercontent.com/sVxsMZdMlVcetXrFFXEWC9lV6dNB3dzDTBWv05Cl5GiilrRWDHlAy69a_ntlX2jY3esyzOPv8TGDm-YHQwnkz1nVMlMtWL6M7rOqeJMNRs0KY22g_d50EksFL8U7y7pF2BZH6FqJ)

Кроме этого, до указания payment\_sum можно задать на каком языке будет платежная страница.&#x20;

Для этого нужно задать переменную **locale. П**о умолчанию стоит русский язык (ru-RU). Возможные варианты: **da-DK, he-IL, id-ID, ja-JP, no-NO, pt-BR, ru-RU, sv-SE, th-TH, zh-CN, zh-HK, zh-TW** и др.(набор доступных языков меняется, ориентируйтесь на [первоисточник](https://developer.paypal.com/api/rest/reference/locale-codes/))

Также можно указать валюту в которой производится прием оплаты, для этого указываем переменную **currency**, по умолчанию установлен рубль (RUB), для доллара задайте ее значение USD (currency = USD). Возможные варианты валют, можно узнать по [ссылке](https://developer.paypal.com/docs/api/reference/currency-codes/).&#x20;

И третий дополнительный параметр это **company\_name** - название вашей компании, отображается в самом верху платежной страницы (пример ниже, компания )

Переменную **paypal\_pay\_url** можно вывести на экран ссылкой или разместить на кнопке с текстом "Оплатить".&#x20;

Ссылка имеет вид: [https://www.paypal.com/checkoutnow?token=07N53571YM296381N](https://www.sandbox.paypal.com/checkoutnow?token=07N53571YM296381N)

Пример реализации.

Задаем сумму платеж и название компании

<figure><img src="/broken/files/6tc5s6qTrR7CBF5hspWo" alt=""><figcaption></figcaption></figure>

{% hint style="info" %}
**Обратите внимание:** переменной **payment\_sum** присваивается значение последней, после необязательных переменных **payment\_title, company\_name** и т.д.
{% endhint %}

Далее указываем переменную #{**paypal\_pay\_url}** во втором блоке "Состояние"**:**

1. **Переменную можно указать в поле сообщения:**

<figure><img src="/broken/files/JCZE1bnK3TAg13yIuWKT" alt=""><figcaption></figcaption></figure>

2. Переменную можно указать в поле url в настройках влоежния:

<figure><img src="/broken/files/4ZA5RTkvDM6sYTdko7et" alt=""><figcaption></figcaption></figure>

3. Переменную можно указать в поле url в настройках кнопки:

<figure><img src="/broken/files/OftDAnUaVQkXdNstujr3" alt=""><figcaption></figcaption></figure>

При открытии ссылки на оплату

![](https://lh3.googleusercontent.com/GvWy17AiTcE0apTWzoPjoADq9h9bXWMRjS61DC00iwnVfSojYKvGS6Puhr6Eg0KfBtBnUza1rY_Mlh0351ka2ikbmNkC6-9zjc2CP-LdUYOQjX4fMaB3V-AT9IRTrMbqRxD-KzW2)

### С помощью функции калькулятора paypal\_payment\_url

Создайте блок конструктора воронок и в калькуляторе вызовите функцию **paypal\_payment\_url**, передав в неё необходимые параметры:

<table><thead><tr><th width="264">Параметры функции</th><th>Описание параметра</th></tr></thead><tbody><tr><td><mark style="color:red;"><strong>!</strong></mark> <strong>payment_sum</strong></td><td> обязательный параметр - сумма платежа</td></tr><tr><td><strong>currency</strong></td><td> валюта платежа, по умолчанию ‘RUB’. Полный список доступен по ссылке <a href="https://developer.paypal.com/docs/api/reference/currency-codes/">https://developer.paypal.com/docs/api/reference/currency-codes/</a></td></tr><tr><td><strong>payment_title</strong></td><td>заголовок платежа (до 127 символов). (Если не указать, заполняется текстом: “Оплата счета payment_id”, где <strong>payment_id</strong> - идентификатор заказа в Salebot)</td></tr><tr><td><strong>payment_description</strong></td><td><p>краткое описание платежа </p><p>(<em>до 127 символов</em>)</p></td></tr><tr><td>company_name</td><td>необязательный параметр, название организации/компании и т.п. </td></tr><tr><td><strong>locale</strong></td><td><p>язык страницы оплаты, указывается в виде en-US, fr-XC и т. д. </p><p>По умолчанию - ‘ru-Ru’. </p><p>Полный список доступен по ссылке https://developer.paypal.com/api/rest/reference/locale-codes/</p></td></tr></tbody></table>

При выполнении условия  блока клиент получит ссылку для оплаты, а также будет создана переменная клиента **paypal\_payment\_completed** со значением <mark style="color:red;">**False**</mark>.

<figure><img src="/broken/files/68GIWaB01xnBUsbTeROA" alt="" width="563"><figcaption></figcaption></figure>

`url = paypal_payment_url(2500, 'RUB', 'Оплата счета payment_id', 'описание платежа', 'название организации', 'ru-Ru')`

## Как создать реккурентный платеж

Для создания и получения ссылки на оплату реккурентными платежами требуется создание  **плана подписки** в личном кабинете.&#x20;

<figure><img src="/broken/files/YcMbGKH6gzIV7zWVIOn1" alt="" width="548"><figcaption></figcaption></figure>

<figure><img src="/broken/files/Q02K7rNAcZC2a5R5j5dK" alt="" width="563"><figcaption></figcaption></figure>

Выбираем уже созданное предложение:

<figure><img src="/broken/files/LMrvW0QY9CpXMXZItmbZ" alt="" width="563"><figcaption></figcaption></figure>

Либо в поисковой строке вводим название предложения и нажимаем Создать

<figure><img src="/broken/files/FgdAOG2y35CoTmjPjzrN" alt="" width="563"><figcaption></figcaption></figure>

<figure><img src="/broken/files/1cuFRDUdlqYCDB9kyEcx" alt="" width="563"><figcaption><p>Создание предложения для подписки в пейпал</p></figcaption></figure>

Выбираем тип автосписания фиксированный:

<figure><img src="/broken/files/QDEXGnqHiniMoZjmurDH" alt="" width="563"><figcaption></figcaption></figure>

Создаём подписку

<figure><img src="/broken/files/Y4FbiNKfgVabNeIxUk7R" alt="" width="563"><figcaption></figcaption></figure>

Выбираем валюту подписки и условия списания:

{% hint style="danger" %}
<mark style="color:red;">**Важно!!**</mark>&#x20;

В Salebot по умолчанию валюта в евро,если списание в долларах или в другой валюте,то при создании подписки указываем другую валюту и в Salebot аналогичную валюту из подписки Paypal
{% endhint %}

<figure><img src="/broken/files/EoKAZoPwEj1EVGjEkTSL" alt="" width="563"><figcaption></figcaption></figure>

Далее активируем подписку:

<figure><img src="/broken/files/kNwFWoPSE0F3DcIYnq2A" alt="" width="563"><figcaption></figcaption></figure>

<figure><img src="/broken/files/S8gz8KSviWn1fhmybn6e" alt="" width="563"><figcaption></figcaption></figure>

После создания будет доступен его идентификатор, который в дальнейшем будем использовать для создания подписки и получения ссылки на оплату.&#x20;

<figure><img src="/broken/files/k9n29aIAeWaePluHu7W5" alt="" width="563"><figcaption></figcaption></figure>

Ссылка на оплату генерируется и возвращается функцией:\
**paypal\_subscription\_url(plan\_id, shipping\_currency, shipping\_payment\_sum, start\_time)**&#x20;

| Параметры функции                                            | Описание параметра                                                                                                                                                                                                                   |
| ------------------------------------------------------------ | ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------ |
| <mark style="color:red;">**!**</mark> **plan\_id**           | идентификатор плана подписки                                                                                                                                                                                                         |
| <mark style="color:red;">**!**</mark> **shipping\_currency** | если оплата указанного плана в долларах, то можно ничего не передавать, иначе передаем код валюты, который указали в плане. Здесь передается валюта, в которой оплачивается доставка (даже для нулевой стоимости). По умолчанию, USD |
| **shipping\_payment\_sum**                                   | необязательный параметр, стоимость доставки. По умолчанию, нулевая стоимость                                                                                                                                                         |
| **start\_time**                                              | <p>необязательный параметр, дата и время начала действия подписки. Если не передать ничего, то дата начала подписки = дате оплаты.<br> Форматы: %d.%m.%Y или %d.%m.%Y %H:%M. </p>                                                    |

<figure><img src="/broken/files/t2iypsMTvAIlVBwKfwSx" alt="" width="563"><figcaption></figcaption></figure>

При создании ссылки также появится переменная **paypal\_subscription\_id**, в которой будет идентификатор подписки.&#x20;

При оплате придет коллбэк, который аналогичен оплате обычного платежа.

**paypal\_subscription\_data(paypal\_subscription\_id)** - получение информации о подписке&#x20;

| Параметры функции            | Описание параметра       |
| ---------------------------- | ------------------------ |
| **paypal\_subscription\_id** | идентификатор подписки.  |

_Результат_ исполнения функции - массив со всей информацией о подписке, включая число оплат, число неудачных попыток списания, статус и прочее

### Как отменить подписку

Функция paypal\_remove\_subscription(paypal\_subscription\_id) поможет отменить подписку на ваши услуги клиентами.&#x20;

Параметры:

| Параметры функции         | Описание                                                                      |
| ------------------------- | ----------------------------------------------------------------------------- |
| paypal\_subscription\_id  | id подписки, который сохраняется в переменную клиента при оформлении подписки |

<figure><img src="/broken/files/2CF5AWUDQMlMAD98rbUG" alt=""><figcaption></figcaption></figure>

## Как обработать результат

{% hint style="info" %}
После успешной оплаты в бот придут колбеки, по которым вы сможете понять, что была успешная оплата.
{% endhint %}

{% hint style="success" %}
В системе вы видите колбеки как сообщения от пользователя, но сам пользователь их НЕ ВИДИТ: они отображаются только оператору.
{% endhint %}

{% hint style="danger" %}
Чтобы обработать колбек в блоке и отправить пользователю сообщения о статусе оплаты, используйте тип сравнения “Полное совпадение”.
{% endhint %}

{% hint style="warning" %}
Колбеки приходят с задержкой, поэтому после вывода ссылки на оплату пользователю рекомендуется отправить сообщение, например: “После оплаты дождитесь сообщения об успешном завершении оплаты”
{% endhint %}

### Для прямой оплаты

Колбек об успешной оплате состоит из 10 первых символов секрета и подписи со статусом. Например: EHsWHYOoWV\_success

Пример 1: реакция на успешный платеж с помощью блока "Стартовое условие":

<figure><img src="/broken/files/OQQWZSyj8myZIHAqLA0M" alt=""><figcaption></figcaption></figure>

Пример 2: реакция на успешный платеж с помощью блока "Стартовое условие":

<figure><img src="/broken/files/Uhfb0qXskYQ35H3geFyE" alt=""><figcaption></figcaption></figure>

{% hint style="info" %}
Если вы не хотите выбивать клиента из основной схемы чат-бота, воспользуйтесь блоком "Не состояние с условием" — в этот блок нельзя перейти, поэтому клиента после оплаты не выбьет из основной воронки и при этом он получит уведомление об успешной оплате.

А если вам нужно продолжить воронку с реакции на успешную оплату, то используйте блок "Стартовое условие", тогда клиент из блока оплаты перейдет в блок "Стартовое условие", с которого вы можете продолжить воронку.
{% endhint %}

{% hint style="info" %}
Подробнее о [блоках с условием рассказали](/broken/pages/VktePfPMzzJlbjBSqE93) в одноименной статье.
{% endhint %}

При успешной оплате переменная paypal\_payment\_completed устанавливается в значение True.

После завершения оплаты клиенту добавится переменная paypal\_callback\_data, содержащая актуальные данные платежной системы о статусе операции. Извлечь необходимые данные из полученного словаря можно при помощи метода get.

{% hint style="danger" %}
Для совершения повторного платежа обязательно необходимо обнулить переменную payment\_sum, переменную с ранее сформированной ссылкой и уже после этого переназначить переменную payment\_sum или вызвать функцию для получения свежей ссылки.
{% endhint %}

### Для оплат по подписке

{% hint style="danger" %}
Функция настройки колбеков для операций, связанных с подписками добавлена 09.01.2024. Для корректной работы колбеков данной категории вам необходимо отключить и снова подключить интеграцию платежной системы Paypal в вашем проекте.
{% endhint %}

При совершении платежа по подписке в бот придет одно из следующих сообщений:

* об активации подписки. Например, subscription\_I-PTV5H4MRC1H3\_activated;
* об успешном последующем платеже по подписке. Например, subscription\_I-PTV5H4MRC1H3\_paid;
* или об ошибке оплаты подписки. Например,  subscription\_I-PTV5H4MRC1H3\_not\_paid;

В указанных примерах “I-PTV5H4MRC1H3” - это id подписки клиента, доступ к которому можно получить с помощью переменной paypal\_subscription\_id.

Колбек добавит клиенту переменную paypal\_subscription\_callback\_data, содержащую актуальные данные платежной системы о статусе операции. Извлечь необходимые данные из полученного словаря можно при помощи метода get.

Пример 1: реакция на активацию подписки с помощью блока "Стартовое условие":

<figure><img src="/broken/files/Jlqi8tEJjMgkQHASQMjr" alt=""><figcaption></figcaption></figure>

Пример 1: реакция на активацию подписки с помощью блока "Не состояние с условием":

<figure><img src="/broken/files/znQg8NLZIQFlkFCcEtU4" alt=""><figcaption></figcaption></figure>
