---
description: Платежная система для бизнеса
hidden: true
---

# Payselection

## **Как подключить платежную систему к Salebot**

Зайдите в Платежные системы - Payselection и заполните форму в Salebot.pro:

<figure><img src="https://lh6.googleusercontent.com/tn5X99OvHl2A7-t_CO4iEX3Iw-j2Jg3erPJ-L3jH-Q0MSWf5IOBXGqCZ9DOwCGEhFeQdgdO48pN9XrRPPl7xwf326l69bLY1EJ87Za_8OJ5wB8foB6kYchaj85gFb8Nxvz5DrvbhaeM-pAelxcJSLfs" alt=""><figcaption></figcaption></figure>

![](https://lh3.googleusercontent.com/X7JrTCnKmist8ykmE1GNCQhq3x5gS_781FJBZnT8gSzmNmeq1CTvZsMY7cl_tPc-ekaw894bN3VRBLLy66A6jCORVVto4PljQGW3tbrSox7pbnQDMyTY4f2DnkVVk7TvMAsRrNIlBxoOmGCMQcf9Q9Q)

Чтобы найти нужные для работы интеграции данные, зайдите в личный кабинет Payselection в раздел Сервис

![](https://lh4.googleusercontent.com/gEKsnmS0EXiYLF7X0aD4Y1yU0Fv8HtRxHlZKHojeDsp-cyRmij_Mg5e92Ayhf1iFc1FUsID8UIbXtfh42SG-6Htc_kqflJexuhAMbdpjY0j0_gALGZK-wwcX7alvD6xHOot2zmevfHjP_AYf4HZMMfo)

Нужный идентификатор клиента (Client ID) можете увидеть в левой части таблицы

![](https://lh6.googleusercontent.com/_ygPQieeNA2BgZ9kgofycGB9ka2xjwT6puPZNJkkZ8uzEvM6CM-PP8H0vBJt8WrVOa7T3E4U-LQ5yY4b9Q9E5kRCxXaBvw6199x-6YgMImVa_JNPLu25ZsN2LStnma3HaBgFZX75arkSJtCx5lynOQM)

Для получения секретного ключа нажмите на редактирование и откроется окно настроек:

![](https://lh6.googleusercontent.com/RZNiQfbCgA1uUMAPVRJLvwrvb3z8liB2bHke2vPOKQOAIyUGPszQ_5-mrPBousU-KcNNmbiP4xO4KXIgBuTD7PEa52PqbylhanQCKT4iLqwlFKlmh5n9u6UJ__Iga4YrgrfUj0Aq1KlpdEkQX8Nv8BE)

В нем вы найдете секретный ключ, а также можете сразу указать ссылку для отправки уведомлений о действиях клиентов:

![](https://lh4.googleusercontent.com/uUoRCrVkHkATJTbZmEVx8jOYpDINW1z5PxcNFv9hu53iuijtoXNHPkrJo0uUSC0jmjLrAt1NQjExQPhYWRUODqnlzH06fHfIBju2lIrOGHYOCPPQfv1rNowTbN1y77if59xoStTWW6DAdX4oLQIpmNo)

Секретный ключ будет в поле, которое на скриншоте закрашено красным. Тут же поставьте галочку в пункте Оповещения вкл, а в URL оповещения скопируйте ссылку: https://chatter.salebot.pro/payselection\_callback/result \
После того как скопируете необходимые данные в соответствующие поля для активации, можно сразу приступать к использованию платежной системы.

## **Как задать сумму оплаты**

{% hint style="info" %}
Обратите внимание: переменной **payment\_sum** присваивается значение последней, после необязательной переменной **currency**&#x20;
{% endhint %}

Для генерации ссылки на оплату вам необходимо установить значение переменной **payment\_sum**, сразу после этого появится переменная **payselection\_pay\_url.**&#x20;

Эту переменную можно вывести на экран ссылкой или разместить на кнопке с текстом "Оплатить".&#x20;

Ссылка имеет вид: \
https://webform.payselection.com/pay/421092b3-40c5-404e-afe0-1417cf64538b&#x20;

Также до установки значения переменной payment\_sum, можно задать необязательную переменную currency -> для настройки платежа.&#x20;

currency - Валюта по стандарту ISO в буквенном обозначении (USD, EUR и т.д.). По умолчанию будут установлены рубли (RUB)

## **Как обработать результат**

После успешной оплаты в бот придут колбэки, по которым вы сможете понять, что была успешная оплата. Эти колбэки в системе вы видите как сообщения от пользователя. Чтобы их не мог отправить пользователь, они состоят из 7 первых символов секретного ключа и приписки.

Например: \
DLx7yvm\_success - в случае успеха или DLx7yvm\_fail - в случае провала оплаты&#x20;

Эти колбэки НЕ ВИДИТ пользователь - они отображаются только оператору.&#x20;

Тип сравнения должен быть "**Полное совпадение**"&#x20;

Также после успешной оплаты переменная **payselection\_payment\_completed** устанавливается в **True**.&#x20;

Например, можно сделать обработку результата оплаты блоком с условием и вывести соответствующее сообщение пользователю.&#x20;

В случае провала оплаты добавится переменная payselection\_payment\_informations с причиной неоплаты.

После завершения оплаты клиенту добавится переменная **payselection\_callback\_data**, содержащая данные ответа платежной системы по совершенной операции. Из полученного словаря можно извлечь необходимые данные при помощи метода **get**.&#x20;

Для совершения повторного платежа обязательно необходимо обнулить payment\_sum, ранее сформированную ссылку и уже после переназначить переменную payment\_sum для получения свежей ссылки. Можно указать предыдущее значение.

## **Тестовые платежи**

Для проведения тестовых платежей используйте список карт для тестирования:

5500081528083771 3DS SUССESS PAYMENT, SUССESS PAYOUT, SUCCESS REBILL 4021050993225905 3DS FAIL PAYMENT, FAIL PAYOUT 4129436949329530 non3DS SUССESS PAYMENT, SUCCESS PAYOUT, FAIL REBILL 5120196445879588 non3DS FAIL PAYMENT, FAIL PAYOUT

Просто используйте данные карты с любым именем, CVC кодом и сроком, превышающим текущую дату для получения желаемого результат&#x430;**.**&#x20;

Если что-то будет работать не так, как ожидалось, проверьте список карт по ссылке: https://api.payselection.com/#section/Testirovanie

## Функции

1. Для создания ссылки на оплату

payselection\_create\_pay\_url(amount, currency, description)&#x20;

<table><thead><tr><th width="305"></th><th></th></tr></thead><tbody><tr><td>amount</td><td>сумма платежа currency - валюта (необязательный параметр, по умолчанию будут рубли)</td></tr><tr><td>description</td><td>описание (необязательный параметр) вернет ссылку на оплату</td></tr></tbody></table>

2. Для создания ссылки на оплату подписки:&#x20;

payselection\_create\_subscription\_pay(amount, interval, period, max\_periods, start\_date, currency, description)&#x20;

<table><thead><tr><th width="315"></th><th></th></tr></thead><tbody><tr><td>amount</td><td>сумма платежа interval - количество заданных периодов до очередного списания</td></tr><tr><td>period</td><td>периодичность списаний (необязательный параметр, по умолчанию "day"), возможные варианты "day", "week", "month". если в interval передать 3 и в этом параметре указать "week", то списание будет раз в 3 недели</td></tr><tr><td>max_periods</td><td>максимальное количество списаний после которого повторных списаний не последует (по умолчанию ограничения не будет)</td></tr><tr><td>start_date</td><td>Дата и время начала списаний, по умолчанию с текущего момента, необязательный параметр. передавать в формате '11.06.2024' или '11.06.2024 15:40'. Если указать только дату, время начала списаний будет установлено автоматически во время выполнения функции</td></tr><tr><td>currency</td><td>валюта (необязательный параметр, по умолчанию будут рубли)</td></tr><tr><td>description</td><td>описание (необязательный параметр) вернет ссылку на оплату после оплаты будет добавлена переменная payselection_recurring_id в которой содержится id подписки</td></tr></tbody></table>

2. Для отмены подписки

payselection\_cancel\_subscription(payselection\_recurring\_id) в параметр нужно передать id подписки из переменной payselection\_recurring\_id и подписка будет отменена
