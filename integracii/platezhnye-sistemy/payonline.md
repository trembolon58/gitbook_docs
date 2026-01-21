---
description: Платежи из любой точки мира!
hidden: true
---

# Payonline

## Регистрация

После регистрации на странице сервиса https://www.payonline.ru Ваш менеджер выдаст Вам доступы к личному кабинету. В разделе Сайты - Настройки - Параметры интеграции Вы найдете необходимые для связи с Salebot данными - MerchantId и Private security key.

![Личный кабинет Payonline (параметры интеграции)](https://lh6.googleusercontent.com/Itb3S_I5pdpWqUYaaRPBs5MJjd92WDnQOVf80XsMA5SssA0uRBGF4y9EeC8z1u7c3cgV2Myeonmm0BPbB-_xizrR9AsQTpcTRhbfs4SX2Pm5rHabrmLkCdGu3Lry2CQMNsf1izUOVJfd_lvdx3b6IVI)

В примере: \
MerchantId - 82110 \
Private security key - 1830с4а2-.......... \
Настройте Callback Url для успешных транзакций и Callback Url для отклоненных транзакций - https://chatter.salebot.pro/payonline\_callback/result

## **Настройка подключения**

Для подключения платежной системы Payonline Вам потребуется ввести данные выданного вам токена и кода проекта в настройках в Salebot. В Salebot открываем раздел платежные системы, выбираем Payonline и вводим полученные данные:

![](https://lh3.googleusercontent.com/GVL2wUc4aKHRF5NjnsSuF0mMHIAs6eObxjUD0I_lHE5SBg0hpgcvF_ymmgU8BOfCi344wa8WW5GfmygSXLk086bqiRU00USVjMmbdgNsBvqKRE7VMiSRinJ2KsJ4tLlll9Jo0mtWfUsqNNiWrxGJbBU)

## Генерация ссылки на оплату

Для генерации ссылки на оплату Вам необходимо установить значение переменной payment\_sum (например, 10), сразу после этого появится переменная payonline\_pay\_url. Эту переменную можно вывести на экран ссылкой или разместить на кнопке с текстом "Оплатить". Ссылка имеет вид: https://pay.payonline.ru/ru/82110/default/70f8aa020e1d405eaa1b43b30a7edd22

Также, до установки значения переменной payment\_sum, можно задать следующие необязательные переменные для настройки платежа: \
currency - валюта платежа. Если оставить переменную пустой, то валюта по умолчанию будет назначена рубли(‘RUB’). \
language - по умолчанию ‘ru’. Язык платежной формы, которая будет выведена пользователю. Доступные языки: \
Русский — ru \
Английский — en \
Немецкий — de \
Испанский — es \
Французский — fr \
Китайский — zh-cn

![](https://lh4.googleusercontent.com/GQ6g0YZViWcMHKIJDiC18foUO-6rAF7KCJ1lS2KTHiyauZVmpUdFsc_5_zbJy0h0g6iv3Waxks4vR0onDtnxEDmh8AwXXvyO9vBAoyvMToIOUI3tIhJ9STd8empm_d9mfUpgLjZAvQgvGz94AsXRRv8)

## **Пример формирования ссылки на оплату**

Создадим ссылку на оплату в размере 10 рублей

![](https://lh4.googleusercontent.com/MglMF9RbDI8bJPhzseTtTw_Ku5NBx9JAI1M5B9gIVIE49XXW9D-1Gzdzhtj8W8Qg1O52KargV09api_gqKZo-zRoIqXHY6jpq08hLMwyDEPk1vhXb6oZaOhUssDc-vwcdkmKWTzRPQ5y2hu6syq_q_A)

{% hint style="warning" %}
**Обратите внимание:** сначала объявляются дополнительные переменные и в конце payment\_sum
{% endhint %}

Далее в любом месте воронки может быть выведена переменная payonline\_pay\_url, в которой содержится ссылка для оплаты:

![](https://lh5.googleusercontent.com/UglBK9XteKkQMdb1a0bdZ-Fi9QOtZgOAZw6OzNQ5tFcZtnPNyC0VvpdQVOF3FPFNMFGJSWX22VTmFpZcNlAGxNoJyNw9KNL2vxYgKXWQR_W31zqEICI0sL561hVQSa1GzIm6s-Nk781GUE7ZrcdlLNc)

## Обработка результата оплаты (callback об оплате)

После успешной оплаты в бот придет соответствующий callback. Callback в Salebot Вы видите как сообщения от пользователя, чтобы их не мог отправить пользователь, они состоят из MerchantId и приписки success, например: 82110\_success:

![](https://lh5.googleusercontent.com/aWtcAuVet1FYGn0DHxq_-F7QZyiDjlz41-DPGzHRjheeUcRKT6_Dnbob_VDLOWstg6CFcpmy7kw1eQ7pdJ_NPwfZ0WblAU1iUkNckxM7HXs3VcYj6afcHJVlJU8s0uVJEAOKPA72pOR3h2saaK0Cs_8)

{% hint style="warning" %}
Не забывайте, клиент не видит callback, они доступны оператору в карточке клиента
{% endhint %}

{% hint style="info" %}
При обработке callback используйте обязательно тип сравнения "Полное совпадение"
{% endhint %}

После успешной оплаты переменная **payonline\_payment\_completed** получает значение  **True**.

![](https://lh6.googleusercontent.com/Z8MsYevHMQtfsHPM7Cj8ikpKTz4k1M61zTD0oxNgAI9PzsrZixUMT6IKguYEaQrxzl5eMYcnHmgEJnGg5rmZKJXjKgqpGVvbT3AnsBmzagxX4ezwwQ0SFa0B0PkfjBZwyBCJ-pRMkPfu9RZU1sb-ZUQ)

Пример  обработки успешной оплаты с использованием блока с условием и уведомлением пользователя:

![](https://lh5.googleusercontent.com/SPVtPlPrKShtOQf5KLFhVprPs1vOFkUwwiLXPhRZwEMqVs2A0C4Dj3UGCeCfgOYrnx43kaL1v9GXpje4Ea4OuOCMnqxsd3XXOBQlcCixd12QuvcqHmIUjuwD-CBfHRR6C5BET9nW1-PWChl-8MSg900)
