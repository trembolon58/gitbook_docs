# Coinpayments

* [Как подключить](coinpayments.md#podklyuchenie)
* [Как сформировать ссылку на оплату](coinpayments.md#kak-sformirovat-ssylku-na-oplatu)
* [Как обработать результат](coinpayments.md#obrabotka-rezultata)
* [Как проверить статус платежа](coinpayments.md#proverka-statusa-platezha)

## Как подключить

Для подключения платежной системы Coinpayments понадобится 4 значения: идентификатор продавца, секрет IPN (для вебхуков), секретный ключ api и публичный ключ api, а также установить url для вебхуков.

Переходим в личный кабинет Coinpayments -> настройки Аккаунта [https://www.coinpayments.net/index.php?cmd=acct\_settings](https://www.coinpayments.net/index.php?cmd=acct_settings)

![](https://lh3.googleusercontent.com/xACTDovKtHxhj7vrWkS0u2TpAy_mK1VU7fR7k2KAD_6lL9OHyKsn4Np54iD4jb7Gjackry858WfaABz37i6tkfn5HZW94n4SKqDq3ooRToxaeXQPRbhvgnKG-KrAssSlHy2lrSSQ)

На первой вкладке копируем идентификатор продавца (**seller ID**)

![](/broken/files/jPDoX1x7g1eqLtS08NUq)

Далее переходим во вкладку Настройки продавца и придумываем и вводим секретный ключ IPN - **IPN secret** (Это используется для подтверждения, что вебхук исходит от нас, используйте надежную сложную строку, которую будет сложно угадать.)

Ссылка IPN - url адрес для вебхуков, добавить следующий: **https://chatter.salebot.pro/coinpayments\_callback/result**

![](https://lh6.googleusercontent.com/K939LTpXmntuJKU1tTN6NTBgl2ziiQTG7okWMRAdOMMQa0K7LbH0X3l7FWmd74FPqY9NOOGl89tbK99fgCpFLva4NJ8VVZVwwGfaE9YYKQ5EOkkb72Qz3FO5jPisxWxrAX8Ac94p)

Далее переходим в раздел Ключи API и генерируем пару ключей для доступа к api.

![](https://lh6.googleusercontent.com/4Y9V4YRgYAvMJNelxlO5bhynVt1er0a5F-QNnOitbBrWFfOLPwJpOM8BHKgMcXxlKzwE9rc32Coxo-iVB_kvGRrgf0XXEjSsop5Uic8CP-8ey8Ll7a_CkvB7D3tcpcEgUo0Dbz7N)

Сохраняем все настройки, копируем данные и переходим к настройкам в Salebot. Открываем раздел "Эквайринг", выбираем Coinpayments.&#x20;

<figure><img src="/broken/files/GdhNFSn5tfDn4WSSv1Ca" alt=""><figcaption></figcaption></figure>

Нужно ввести полученные данные.

<figure><img src="/broken/files/1RmVaSKSGL6nyK8HdNyZ" alt="" width="563"><figcaption></figcaption></figure>

Для генерации ссылки на оплату, вам необходимо установить значение обязательных переменных:

<table><thead><tr><th width="201">Переменные </th><th width="228">Значение переменной</th><th>Примечание</th></tr></thead><tbody><tr><td> <strong>original_currency</strong> </td><td>Исходная валюта транзакции. </td><td></td></tr><tr><td><strong>sending_currency</strong></td><td>Валюта, которую отправит покупатель.</td><td> Например, если ваши продукты оценены в долларах США, но вы получаете BTC, вы должны использовать original_currency = USD и sending_currency = BTC. original_currency и sending_currency могут иметь одно значение, если конвертация валюты не требуется.</td></tr><tr><td><strong>buyer_email</strong> </td><td>Адрес электронной почты покупателя.</td><td>Для отправки уведомлений, если платеж на меньшую сумму и необходимо доплатить или для возвратов. Если эта переменная не задана, почта будет взята автоматически из переменной email, если такая есть у пользователя в Salebot.</td></tr></tbody></table>

После этого нужно установить значение переменной **payment\_sum** (например 10 или 0.0055 (**через точку!**)), сразу после этого появится переменная **coinpayments\_pay\_url**. Эту переменную можно вывести на экран ссылкой или разместить на кнопке с текстом "Оплатить". Ссылка имеет вид: **https://www.coinpayments.net/index.php?cmd=checkout\&id=CPFK5QZ3FKSNWHI75CO8M4BRVD\&key=e7782d2ce24f7d03815606a5c4a882eb**

Также до установки значения переменной payment\_sum, можно задать следующие необязательные переменные, для настройки платежа.

**payment\_description** - название продукта, будет на странице информации о платеже и в IPN для транзакции.&#x20;

**buyer\_name** - имя покупателя

Такой вид имеет страница оплаты.

![](https://lh3.googleusercontent.com/Yn1a6_JOW4wkj2SqNwkkJYMBZoh4JcR1HEinzP67O6WmYBcCV3IdRw_JCEQI0L7OV-8IuH_JdMEdOaduymc0vs5QAmpfcgrU0tFD9ZrT6V_B8vvQqe-sQcUDMsd9PJRa_uUsJAsX)

## Как сформировать ссылку на оплату

Создадим ссылку на оплату в размере 0.0256

<figure><img src="/broken/files/ZNxSBA8QtUzx9jLlSu0y" alt="" width="563"><figcaption></figcaption></figure>

{% hint style="info" %}
**Обратите внимание:** \
\- Сначала указываете email\
\- Далее необязательные параметры  **first\_name, payment\_description** и т.д.\
\- И последней присваиваем значение переменной **payment\_sum**
{% endhint %}

Обратите внимание, вначале задаем переменные для настроек, затем **payment\_sum**. Переменные можно задать и ранее в цепочке, а не в одном блоке, это пример.

Далее в нужном месте выводим переменную **coinpayments\_pay\_url**, в которой содержится ссылка

<figure><img src="/broken/files/0PlRhOhxdCfcWIkb6fwT" alt="" width="563"><figcaption></figcaption></figure>

{% hint style="warning" %}
Для совершения повторного платежа обязательно необходимо обнулить payment\_sum, ранее сформированную ссылку и уже после переназначить переменную payment\_sum для получения свежей ссылки
{% endhint %}

## Как обработать результат

После успешной оплаты в бот придут коллбэки, по которым вы сможете понять, что была успешная оплата. Эти коллбэки в системе вы видите, как сообщения от пользователя. Чтобы их не мог отправить пользователь, они состоят из 10 первых символов секретного ключа и приписки \_success, например: **16831CF4b5\_success**

{% hint style="success" %}
Эти коллбэки НЕ ВИДИТ пользователь, они отображаются только оператору.
{% endhint %}

{% hint style="danger" %}
Тип сравнения должен быть "Полное совпадение"
{% endhint %}

Также после успешной оплаты переменная coinpayments\_payment\_completed устанавливается в True

Например, можно сделать обработку успешной оплаты блоком с условием и вывести соответствующее сообщение пользователю:

<figure><img src="/broken/files/3MA93aQt0H6IW4pg1fTC" alt=""><figcaption></figcaption></figure>

После завершения оплаты клиенту добавится переменная **coinpayments\_payment\_callback**, содержащая данные ответа платежной системы по совершенной операции. Из полученного словаря можно извлечь необходимые данные при помощи метода **get**.

## Как проверить статус платежа

Для проверки статуса платежа, нужно в поле Калькулятор вызвать метод **coinpayments\_get\_payment\_status()**

Пример:

<figure><img src="/broken/files/2YdXOEhG1hPVmHmyMZpb" alt="" width="563"><figcaption></figcaption></figure>

> **Примеры статусов**:
>
> Waiting for buyer funds...
>
> Funds received and confirmed sending to you shortly…
>
> Complete
