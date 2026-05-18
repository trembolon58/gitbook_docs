---
description: Оплата на вашем сайте по картам со всего мира
hidden: true
---

# Paybox.money

## **Регистрация**

Для получения необходимых данных для интеграции сервиса Paybox с Salebot необходимо зайти в “личный кабинет” - “разработчикам” и забрать со страницы следующие данные:\
**Paybox merchant\_id** - Идентификатор магазина - в примере 545273\
**Paybox secret\_key** - Секретный ключ для приема платежей - в примере t2JM\*\*\*\*\*\*\*\*\*\*\
**Paybox payout\_secret\_key** - Секретный ключ для выплат клиентам - в примере

![](https://lh4.googleusercontent.com/VNVDnLQ3QaZUr1GI0d04d3BZVDO7VCGWjPuURlagxIHqZeec7ZrGWSHxDSvt2KqnQ7Dss-Rg2fmzrpwKaJSGMghgMjxGAkzihLe0ghtzQKJ0gTKZk6wUYPKc6SoS2y0e9URbOQ6XQFHCIbouLRLV_sc)

Так же для получения уведомлений об успешных платежах, следует пройти в “личный кабинет” - “настройки” - “магазины” и заполнить соответствующие поля. В подразделе “Системные настройки” следует вставить следующие данные:\
[https://chatter.salebot.pro/paybox\_callback/result](https://chatter.salebot.pro/paybox_callback/result) - check url\
[https://chatter.salebot.pro/paybox\_callback/result](https://chatter.salebot.pro/paybox_callback/result) - result url\
[https://chatter.salebot.pro/paybox\_callback/success](https://chatter.salebot.pro/paybox_callback/success) - success url\
**GET** - request method\
**Все платежи** - дефолтный фильтр

В поле site url можно ввести URL сайта магазина для показа покупателю ссылки, по которой он может вернуться на сайт магазина после создания счета(необязательно).

![](https://lh4.googleusercontent.com/FeFS9xFxqdiPDIIkQMdN-N0e11aryjUs6-OohHNkpUhcWWPxhbP63J2azNiYppWUClfW1YpehvnMy3rWKttHn0by18fjD8fU8eY1MiNXzJ_Pqw7S1jisPDH391NUS7CsujD5p-ug88CEEk4ePpc4HVI)

Для подключения платежной системы Paybox вам потребуется ввести полученные данные в настройках в Salebot. В salebot открываем раздел платежные системы, выбираем Paybox и вводим их.

![](https://lh3.googleusercontent.com/vrOizNC-17ApX9c-PMTnN08HL0ve3yEB5LA1u2WJkcoebVN-ToVk7tDH3fYHoARIwzHsVzzR0kpOj5r5g93Chi-KICFHJXLF9jt-qTJexsgAF9EK_eTCfNCXd8bVelZL9u5IO2i0BKEHRyYYnY6CmKk)

## **Генерация ссылки на оплату**

Для генерации ссылки на оплату Вам необходимо установить значение переменной payment\_sum (например, 20), сразу после этого появится переменная paybox\_pay\_url. Эту переменную можно вывести на экран ссылкой или разместить на кнопке с текстом "Оплатить".

Ссылка имеет вид: \
https://customer.paybox.money/pay.html?customer=8235a19a9333cd08deb960f64e0250d3&#x20;

Также до установки значения переменной payment\_sum, можно задать следующие необязательные переменные для настройки платежа:&#x20;

* currency - валюта платежа. Если оставить переменную пустой, платеж будет произведен в рублях (‘RUB’).&#x20;
* paybox\_description – описание платежа. Если его не указать, будет добавлено стандартное описание “Оплата онлайн счета {номер счета}”&#x20;
* paybox\_bill\_lifetime - продолжительность жизни платежки в минутах. Если его не указать, ссылка на платежку будет действительна в течение 5 минут с ее создания&#x20;
* paybox\_test - Вы можете установить значение переменной равное 1, тогда следующий платеж пройдет в тестовом режиме. Не забудьте очистить переменную, когда потребуется совершать боевые платежи!&#x20;

{% hint style="info" %}
Подробнее о том, какие карты можно указать для тестовых транзакций, Вы можете узнать в личном кабинете Paybox в разделе для разработчиков
{% endhint %}

![](https://lh5.googleusercontent.com/c4dAVCgnqzPp4q_y9RBFdUQB7VEjzb7VF68lCmtgR6uaITv7j19Lcx71mI2qDXqGwYQBeBH7c9Bux2Mnc5qSUFxd7lqMxX2D1MA8tTHmukgObduVWMjuu2wXfg2qfdKAppBIBzVChK45XVP478YaFZk)

### **Пример формирования ссылки на оплату**

Создадим ссылку на оплату в размере 20 рублей (внимание: в случае, если сумма окажется меньше минимальной, придет соответствующее сообщение. Минимальные суммы зависят от вида валют в Paybox).

![](https://lh3.googleusercontent.com/RvfJ0y69PohbuW3t5pPzynxjxmdKfCA9xioSJ92ag2piLnCjx_t5OxA1uhD1O0PAajgXG2k2aWFt0ovx6i3xFahXSQ7Vsev6zbUnLk8TITBBqcdS3LyILOU2qTrRTKh2BeSpv82vC2Epg_-j09wDKkc)

{% hint style="warning" %}
Обратите внимание: сначала задаются дополнительные переменные для настроек, затем payment\_sum.
{% endhint %}

Переменные можно задать и ранее в цепочке, а не в одном блоке, это пример. Далее в нужном месте выводим переменную paybox\_pay\_url, в которой содержится ссылка для оплаты

![](https://lh4.googleusercontent.com/PPLYBtRG0x8UtakrVwkOxP0KtGvCfIZtUcaJoAakkVnC2FcGdnGTTqhpgdSLS6nYujxy-EhWp5nRcOQJkQ8_bApJeKu3kfprONYL1pPW2keimzBQDYa55IM0oJsltHyenEz8QYr-d1UxdYqej2ZS0Qk)

## **Обработка результата оплаты (callback об оплате)**

После успешной оплаты в бот придут callback , по которым вы сможете понять, что была успешная оплата.

Эти callback в системе Вы видите как сообщения от пользователя. Чтобы их не мог отправить пользователь, они состоят из идентификатора merchant и приписки success, например: 545273\_success

![](https://lh6.googleusercontent.com/CWgSbzBB5yyLdwJDJlKYy1wICwh7U3_JIX7jZYvDOMMoASRLBBjdMQBA8sDjtkvJOPLoBsnRboo0lt3jjoOp-7F1mW7jEqKp7BsnBIH1aho8fkLx5k8dQFNSmPYqnC3yznuz93hFEh7c0rx_MJQkCro)

Эти callback НЕ ВИДИТ пользователь - они отображаются только оператору. **Тип сравнения должен быть "Полное совпадение"** \
Также после успешной оплаты переменная paybox\_payment\_completed устанавливается в True. Например, можно сделать обработку успешной оплаты блоком с условием и вывести соответствующее сообщение пользователю:

![](https://lh5.googleusercontent.com/dwlBzak3kZD2lwzXycLaANHXRAo0aVYp0-kO717oHyY2pm2bTJYl9ouZpFChA4xnXaNep-OvEnDkojzZ4o_1iAB89EAFm9SWSMQ0sp2Iz8ISxUQrXDWww89F8KCcFQosxNyYbpHqifMEln9VKMBk-Mc)

После завершения оплаты клиенту добавится переменная paybox\_payment\_callback, содержащая данные ответа платежной системы по совершенной операции. Из полученного словаря можно извлечь необходимые данные при помощи метода get.

Также в систему Salebot может прийти **callback о неуспешной оплате** вида 545273\_fail, однако, следует иметь ввиду, что в связи с особенностями формирования платежных страниц в Paybox - а именно возможностью повторно оплатить счет по той же платежной ссылке в случае неудачи - система засчитывает неудачу по оплате только в том случае, если клиент прошел по уже просроченной ссылке. В случае, если он совершает попытки оплаты с действующей ссылки, callback о проваленной оплате не придет.
