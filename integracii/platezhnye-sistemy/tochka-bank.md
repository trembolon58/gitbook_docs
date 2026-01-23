# Точка Банк

В этой статье пошагово рассмотрено подключение **Точка Банк** к **Сейлбот**. Вы узнаете, какие настройки необходимо выполнить, как правильно привязать банк к проекту и обеспечить корректный прием платежей через платформу.

## Настройки в ЛК банка

Для подключения интеграции понадобятся следующие данные:

* JWT токен
* clientID
* customerCode
* merchantId

Шаг 1. Как получить JWT-токен

Чтобы получить JWT-токен перейдите в личный кабинет в Точка Банк, далее во вкладку "Сервисы", затем во вкладку "Интеграции и API".&#x20;

Во вкладке "Интеграции и API" нажмите на JWT-ключи:

<div data-with-frame="true"><figure><img src="../../.gitbook/assets/Снимок экрана 2026-01-23 в 19.46.05.png" alt="" width="563"><figcaption></figcaption></figure></div>

Нажмите на плашку и далее кликните по кнопке «Сгенерировать JWT-ключ». Тогда откроются настройки ключа, где необходимо выбрать доступы:

<div data-with-frame="true"><figure><img src="../../.gitbook/assets/Снимок экрана 2026-01-23 в 19.52.16.png" alt=""><figcaption></figcaption></figure></div>

Выберите следующие доступы:

1. &#x20;"Создание платежей",&#x20;
2. "Создание ссылки на оплату картой и через СБП"
3. "Создание и получение вебхуков"

Далее пропишите название ключа (например, "Salebot"), затем придет sms с кодом для подтверждения.

**Шаг 2. Как получить client\_id**

**client\_id**  находится внутри сгенерированного JWT-ключа (Точка Банка отобразит client\_id после генерации JWT-ключа)

**Шаг 3. Как получить siteUid (merchant\_id) и customerCode**

{% hint style="info" %}
**siteUid (merchant\_id)** - это идентификатор торговой точки в интернет-эквайринге (**ID мерчанта**)

**customerCode** — это ваш уникальный **код клиента**.
{% endhint %}

Для получения siteUid (merchant\_id) необходимо обратиться в чат технической поддержки Точка Банка с запросом "Нужен siteUid (merchant\_id) для интеграции интернет-эквайринга с внешним сервисом". После обращения, техническая поддержка направит уникальный идентификатор торговой точки.

Аналогично можно обратиться с запросом о customerCode.

## Подключение в Salebot

В Salebot в разделе "Эквайринг" найдите Точка Банк и нажмите "Подключить":

<div data-with-frame="true"><figure><img src="../../.gitbook/assets/unknown (2).png" alt=""><figcaption></figcaption></figure></div>

В открывшемся окне укажите свои уникальные данные JWT токен, clientID, customerCode, merchantId в соответствующих полях:

<div data-with-frame="true"><figure><img src="../../.gitbook/assets/Снимок экрана 2026-01-23 в 20.05.24.png" alt="" width="563"><figcaption></figcaption></figure></div>

Затем при необходимости укажите систему налогообложения и ставку НДС.

{% hint style="success" %}
Интеграция готова к работе.
{% endhint %}

## Формирование ссылки на оплату

Для формирования ссылки на оплату используется функция get\_tochka\_bank\_payment\_url

get\_tochka\_bank\_payment\_url(amount, description, recurrent, products\_for\_receipt, customer\_email, customer\_phone, full\_name, expired, twostage)

Описание параметров

<table><thead><tr><th width="279.65234375">Параметр</th><th>Описание параметры</th></tr></thead><tbody><tr><td>amount</td><td>сумма платежа</td></tr><tr><td>description</td><td>описание платежа</td></tr><tr><td>recurrent</td><td>включить рекуррентные платежи. Если параметр включен, после успешной оплаты будет возможность провести повторный платеж. Необязательный параметр</td></tr><tr><td>products_for_receipt</td><td>данные для формирования чека. Необязательный параметр<br>Пример данных, передаваемых в products_for_receipt:<br>[{"name": "Тестовая услуга", "price": "100", "quantity": "1", "method": "full_prepayment", "object": "goods"}]</td></tr><tr><td>name</td><td>Название товара/услуги. Обязательный параметр при формировании чека</td></tr><tr><td>price</td><td>цена за единицу. Обязательный параметр при формировании чека</td></tr><tr><td>quantity </td><td>количество. Обязательный параметр при формировании чека</td></tr><tr><td>method</td><td>тип оплаты. <br>full_payment — полная оплата, <br>full_prepayment — полная предоплата. <br>Необязательный параметр, по умолчанию full_payment</td></tr><tr><td>object</td><td>признак предмета расчёта. goods — товары, service — услуги, work — работа. Необязательный параметр, по умолчанию service</td></tr><tr><td>customer_email</td><td>email клиента. Обязательный параметр при передаче products_for_receipt.</td></tr><tr><td>customer_phone</td><td>телефон клиента. Необязательный параметр, может использоваться при передаче products_for_receipt</td></tr><tr><td>full_name</td><td>имя клиента. Необязательный параметр, может использоваться при передаче products_for_receipt</td></tr><tr><td>expired</td><td>время жизни ссылки в минутах. От 1 до 44 640 минут, по умолчанию 10080. Необязательный параметр</td></tr><tr><td>twostage</td><td>Включить двухэтапную оплату. Не работает при передаче recurrent. Необязательный параметр</td></tr></tbody></table>

Пример формирования ссылки без чека:

<div data-with-frame="true"><figure><img src="../../.gitbook/assets/unknown (4).png" alt="" width="563"><figcaption></figcaption></figure></div>

Пример формирования ссылки с чеком:

<div data-with-frame="true"><figure><img src="../../.gitbook/assets/unknown (5).png" alt="" width="563"><figcaption></figcaption></figure></div>

## Обработка результата

<mark style="background-color:green;">**В диалоге с клиентом при оплате автоматически придет колбек**</mark>, который состоит из 10 символов clientID платежной системы, слова \_success и через пробел сумма платежа.&#x20;

<div data-with-frame="true"><figure><img src="../../.gitbook/assets/Снимок экрана 2026-01-23 в 20.15.52.png" alt="" width="563"><figcaption></figcaption></figure></div>

Например: <mark style="color:blue;">**ovg58keefc**</mark><mark style="color:$success;">**\_success**</mark> <mark style="color:$danger;">**1999**</mark>, где:

* <mark style="color:blue;">**ovg58keefc**</mark> : первые 10 символов секретного ключа платежной системы
* <mark style="color:$success;">**\_success**</mark> : результат обработки запроса (успешный платеж)
* <mark style="color:$danger;">**1999**</mark> : сумма платежа

{% hint style="warning" %}
#### Обращаем внимание!

Колбек о неуспешном платеже от Точка Банка НЕ приходят!
{% endhint %}

Для использования в настройках схемы достаточно скопировать колбек и вставить его в строку "Условие":

1. Можно указать в условии полный текст колбека (тогда укажите выбор соответствия "Полное совпадение):

<div data-with-frame="true"><figure><img src="../../.gitbook/assets/Снимок экрана 2026-01-23 в 20.21.16.png" alt=""><figcaption></figcaption></figure></div>

2. Либо часть колбека (тогда необходимо указать выбор соответствия "По наличию ключевых слов"):

<div data-with-frame="true"><figure><img src="../../.gitbook/assets/Снимок экрана 2026-01-23 в 20.23.34.png" alt=""><figcaption></figcaption></figure></div>

Аналогично можно использовать колбек с блоком "Не состояние с условием", если вы не хотите выбивать клиента из основной воронки:

1. Часть колбека в условии:

<div data-with-frame="true"><figure><img src="../../.gitbook/assets/Снимок экрана 2026-01-23 в 20.24.58.png" alt=""><figcaption></figcaption></figure></div>

2. Весь текст колбека в условии:

<div data-with-frame="true"><figure><img src="../../.gitbook/assets/Снимок экрана 2026-01-23 в 20.25.57.png" alt=""><figcaption></figcaption></figure></div>

Либо продолжить вашу воронку и прописать текст колбека в условиях стрелки:

<div data-with-frame="true"><figure><img src="../../.gitbook/assets/Снимок экрана 2026-01-23 в 20.32.20.png" alt=""><figcaption></figcaption></figure></div>

{% hint style="warning" %}
#### Обращаем внимание

Также после успешного платежа, у клиента появится переменная **tochka\_bank\_operation\_id,** которая может пригодиться для использования в функциях калькулятора.

Например, при возврате платежа.
{% endhint %}

### Возврат платежа

Чтобы вернуть платеж, воспользуйтесь функцией tochka\_bank\_refund\_payment(amount, operation\_id)

<table><thead><tr><th width="275.7578125">Параметры</th><th>Описание</th></tr></thead><tbody><tr><td>amount</td><td>сумма возврата. Не может быть больше суммы платежа.</td></tr><tr><td>operation_id</td><td><p>id платежа из tochka_bank_operation_id. </p><p>Необязательный параметр, если не указать, данные будут взяты из переменной tochka_bank_operation_id</p></td></tr></tbody></table>

<div data-with-frame="true"><figure><img src="../../.gitbook/assets/Снимок экрана 2026-01-23 в 20.38.09.png" alt="" width="563"><figcaption></figcaption></figure></div>

{% hint style="danger" %}
#### Обращаем внимание!

Возврат возможен только по успешный подтвержденным платежам (по которым пришел коллбек "\_success")
{% endhint %}

### Двухстадийная оплата (холдирование)

Чтобы использовать двухстадийную оплату (холдирование), в параметры функции get\_tochka\_bank\_payment\_url нужно передать соответствующий параметр twostage.

{% hint style="info" %}
#### Внимание!

[Описание параметров указано выше в параграфе "Формирование ссылки на оплату".](tochka-bank.md#formirovanie-ssylki-na-oplatu)
{% endhint %}

Если это кнопка для оплаты, то нужно поставить галочку "Двухстадийная оплата".

Теперь после успешной оплаты сначала придет коллбэк вида "eyJhbGciOi\_authorized 10".

<div data-with-frame="true"><figure><img src="../../.gitbook/assets/Снимок экрана 2026-01-23 в 20.41.25.png" alt="" width="456"><figcaption></figcaption></figure></div>

Также у клиента в этот момент появится переменная "tochka\_bank\_operation\_id\_hold" - она пригодится, если нужно будет подтвердить оплату через бота:

* чтобы подтвердить оплату и списать захолдированные средства, нужно использовать функцию "tochka\_bank\_capture\_payment(self, operation\_id)"

В параметр payment\_id передается ранее сохраненный "tochka\_bank\_operation\_id\_hold". Также можно параметр не передавать, тогда он будет взят из переменной клиента tochka\_bank\_operation\_id\_hold

После подтверждения платежа уже придет привычный коллбэк "ovg58keefc\_success 10"

Если платеж не подтвердить, он со подтверждается автоматически со временем со стороны Банка.

## Рекуррентные платежи

После успешного платежа с включенным параметром recurrent или галочкой "Автоплатеж" в настройке кнопки, можно совершить повторный платеж

Для этого нужно воспользоваться функцией tochka\_bank\_recurrent\_payment(amount, operation\_id)

amount - сумма платежа

operation\_id - id платежа из tochka\_bank\_operation\_id. Необязательный параметр, если не указать, данные будут взяты из переменной tochka\_bank\_operation\_id

Если платеж выполнен успешно, в ответе функции вернется "True".
