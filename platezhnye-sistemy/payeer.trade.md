---
description: >-
  Payeer.tradeБиржа Payeer – торговая площадка, запущенная одноименной платежной
  системой. PAYEER Exchange позволяет обменивать ряд популярных криптовалют одну
  на другую или покупать/продавать за фиат.
---

# Payeer.trade

### Настройка подключения

Для работы с сервисом payeer.trade необходимо найти слева в меню вкладку API, далее перейти на вкладку **БИРЖА** и нажать **ДОБАВИТЬ**. На странице откроется окно, в котором вы должны заполнить название.

Секретный ключ (в примере 9yblcxjEZ4Vi666y) выдается системой: необходимо скопировать его к себе в надежное место.

{% hint style="warning" %}
ВАЖНО! В случае потери восстановить его нельзя, можно только сменить на новый
{% endhint %}

В строке IP-адрес потребуется ввести IP Salebot 134.209.254.246.&#x20;

{% hint style="info" %}
Если Вы хотите получать ответы на еще один IP., просто добавьте его через символ “;”. Например, 2.2.2.2;3.3.3.3
{% endhint %}

![](https://lh6.googleusercontent.com/SoHPw3QRlEMm_Sq_JxJL0ajiPfGegjtlPzlZYxrChdRfc-I3UzVkGNCYesie5VTeUlkeQP2YvdmCZuD5a-o3X3Ry0OrRlsKbgrAAa2nwzVz_kL8WYyFIfsBiou6-LY9j8kBmg99m)

После успешного заполнения данных у Вас появится следующее окно:

![](https://lh5.googleusercontent.com/nGEKbfbl-xeTqmbzglIdy8eOMKvB2iz6P1GCfPMYKipF_RWj2h9q4WYPkoU4bitAjRrQnKzEHoX2sGsg5Vog87quepz0tFP7rsTxuA-fA6fT2__mezAhNMAfFQhTj4O3vwdCWyzG)

Перейдите в настройки и скопируйте значение id( в примере d95c634e-b17d-4a75-9aa8-b59fecbdb402), оно нам понадобится.

![](https://lh5.googleusercontent.com/4Tw5UCdZkkCAmzy_YxIjhIa5DCnzmjxgIKjZoKfrVuUVblfyAiM86HrIAbA1cMXWV8kpv1sZPGI3xA_4iH5rnwkBxlpXAAGkZbCT4Rl1QqkDVqYBGm2-6Kv_WlHg4sJzSfCuwosT)

### Получение данных в Salebot

Для получения данных нужно воспользоваться функцией payeer\_function(api\_id, secret\_key, method, data), где:

1. api\_id = ‘d95c634e-b17d-4a75-9aa8-b59fecbdb402’ - строка, Ваш ID в системе Payeer. Обязательный параметр.
2. secret\_key = ‘9yblcxjEZ4Vi666y’ - строка, Ваш секретный ключ. Обязательный параметр \
   method = ‘account’ - строка, обозначающая тип запрашиваемой информации. Обязательный параметр Доступны следующие **методы:** \
   \- Баланс пользователя - ‘account’ \
   \- Создание ордера - ‘order\_create’ \
   \- Статус ордера - ‘order\_status’ \
   \- Отмена ордера - ‘order\_cancel’ \
   \- Отмена ордеров - ‘orders\_cancel’ \
   \- Мои ордера - ‘my\_orders’ \
   \- Моя история - ‘my\_history’ \
   \- Мои сделки - ‘my\_trades’&#x20;
3. data - список необходимых для выполнения метода данных. Необязательный параметр. \
   Для методов ‘account’, ‘my\_orders’, ‘my\_history’ и ‘my\_trades’ параметр data можно не передавать. \
   -‘order\_create’ - список должен включать в себя следующие параметры: \
   **Для создания ордера-лимит:** \
   pair-пара-TRX\_USD \
   type-тип ордера-limit \
   action-действие-buy, \
   sell amount-количество-10 \
   price-цена-0.08 \
   **Для создания ордера-маркет**(\*возможно указание одного из двух параметров для создания маркет-ордера (amount или value)): \
   pair-пара-TRX\_USD \
   type-тип ордера-market \
   action-действие-buy, \
   sell amount-количество-10\
   value-сумма-10000 \
   **Для создания ордера стоп-лимит:** \
   pair-пара-TRX\_USD \
   type-тип ордера-stop\_limit \
   action-действие-buy, \
   sell amount-количество-10 \
   price-цена-0.08 \
   stop\_price-стоп-цена-0.078 \
   -'order\_status’ - список должен включать в себя следующие параметры: \
   order\_id-id ордера-37054293 \
   -‘order\_cancel’ - список должен включать в себя следующие параметры: \
   order\_id-id ордера-37054293 \
   -‘orders\_cancel’ - в данном случае эти параметры необязательные, без них запрос просто удалит все ордера \
   pair-список пар для отмены ордеров-TRX\_RUB,DOGE\_RUB action-действие-buy, sell

Функция возвращает словарь вида:&#x20;

* в случае успеха: {"status":"1","result":{"success":true,"balances":{"USD":{"total":0,"available":0,"hold":0},"RUB":{"total":0,"available":0,"hold":0},"EUR":{"total":0,"available":0,"hold":0},"BTC":{"total":0,"available":0,"hold":0},"ETH":{"total":0,"available":0,"hold":0},"BCH":{"total":0,"available":0,"hold":0},"LTC":{"total":0,"available":0,"hold":0},"DASH":{"total":0,"available":0,"hold":0},"USDT":{"total":0,"available":0,"hold":0},"XRP":{"total":0,"available":0,"hold":0},"DOGE":{"total":0,"available":0,"hold":0},"TRX":{"total":0,"available":0,"hold":0\}}\}}&#x20;
* в случае ошибки, например: {"status":"0","error":{"code":"INVALID\_PARAMETER","parameter":"pair"\}}

### Пример использования

Создаем блок “Стартовое условие”.&#x20;

В калькуляторе указываем значения необходимых нам переменных:&#x20;

1. **метод:** \
   msg = 'account',&#x20;
2. **API ID:**\
   api = '‘d95c634e-b17d-4a75-9aa8-b59fecbdb402'
3. **секретный ключ:**\
   key = '9yblcxjEZ4Vi666y'&#x20;
4. **переменная с функцией:**\
   r = payeer\_function(api,key,msg,' '),&#x20;
5. **переменная, которая выводит результат:**\
   s = get(r,'result')&#x20;

<figure><img src="../.gitbook/assets/Снимок экрана 2025-07-01 в 18.04.08.png" alt=""><figcaption></figcaption></figure>

В тексте сообщения прописываем #{s}, и после запуска бота получаем список сведений о счете аккаунта.

<figure><img src="../.gitbook/assets/Снимок экрана 2025-07-01 в 18.05.50.png" alt=""><figcaption></figcaption></figure>
