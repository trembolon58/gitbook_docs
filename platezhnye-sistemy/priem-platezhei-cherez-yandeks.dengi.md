---
description: В статье расскажем, как быстро подключиться к сервису для приема платежей
---

# ЮMoney

Если вам необходимо быстро подключить прием платежей как физическое лицо, то выбор очевиден — ЮMoney

Вам не потребуется ни регистрация магазина, ни его проверка. Настройка занимает 10 минут.

* [Как настроить ЮMoney ](priem-platezhei-cherez-yandeks.dengi.md#nastroika-yumoney)
* [Как настроить Salebot ](priem-platezhei-cherez-yandeks.dengi.md#nastroika-salebot)
* [Как получить уведомление о результате оплаты ](priem-platezhei-cherez-yandeks.dengi.md#uvedomlenie-o-rezultate-oplaty)
* [Пример](priem-platezhei-cherez-yandeks.dengi.md#primer)

## Как настроить ЮMoney

[Перейдите по ссылке](https://yoomoney.ru/transfer/myservices/http-notification), войдите в личный кабинет или зарегистрируйтесь. Вы перейдете на страницу с http-уведомлениями:

<figure><img src="/broken/files/EOZOkGIneWPLcWR4GZ06" alt=""><figcaption><p>Рис. 1. Страница http-уведомлений</p></figcaption></figure>

Здесь необходимо указать url в поле "Куда отправлять" и поставить галочку в поле "Отправлять HTTP-уведомления":

<mark style="color:red;">**URL для уведомлений о платежах: https://chatter.salebot.pro/yandex\_money\_callback/result**</mark>

<figure><img src="/broken/files/4v76V4mPUokphB5iHqOl" alt=""><figcaption><p>Рис. 2. Страница уведомлений с заполненными полями </p></figcaption></figure>

{% hint style="danger" %}
Важно!

Не забудьте установить галочку "**Отправлять HTTP-уведомления**"
{% endhint %}

Далее нажмите "Готово", тогда вы увидите pop-up с информацией, что уведомления будут приходить по указанному вами url Сейлбота:

<figure><img src="/broken/files/fEuS1B0K7eYS2r7Vl85s" alt=""><figcaption><p>Рис. 3. pop-up с url для уведомлений</p></figcaption></figure>

На сервисе Юмани для подключения к Сейлботу понадобится скопировать:

1. Секретный ключ:

Чтобы скопировать секретный ключ, нажмите "Показать секрет":

<figure><img src="/broken/files/lr86ZfxA20PDol8AFZGC" alt=""><figcaption><p>Рис. 4. Копируем секретный ключ</p></figcaption></figure>

<figure><img src="/broken/files/0GbkwY5IYg7XziAv8kZt" alt=""><figcaption><p>Рис. 5. Копируем секретный ключ</p></figcaption></figure>

Сохраните ключ поблизости (или не закрывайте вкладку с http-уведомлениями) — он понадобится нам в дальнейшем.

Шаг 2. Перейдите на главную страницу и скопируйте номер кошелька:

<figure><img src="/broken/files/TekW11yP6qYcca97ARkM" alt=""><figcaption><p>Рис. 6. Копируем номер кошелька</p></figcaption></figure>

{% hint style="success" %}
Готово! Теперь перейдем к подключению в Salebot.
{% endhint %}

## Как подключить Юmoney к Salebot

Для подключения ЮMoney необходимо перейти в раздел  "Эквайринг":

<figure><img src="/broken/files/x3D0OVViqqne8uxWmBhO" alt=""><figcaption><p>Рис. 7. Раздел "Эквайринг" в Сейлботе для подключения сервисов приема платежей</p></figcaption></figure>

Далее необходимо просто указать данные, о которых говорили выше в форму.

<figure><img src="/broken/files/JC5uHPnYTi8qZzAhWEwm" alt=""><figcaption><p>Рис. 8. Заполняем поля номер кошелька и секретный ключ, которые ранее скопировали<br>на стороне Юмани</p></figcaption></figure>

И нажмите "Сохранить настройки".

На этом подключение закончено. Теперь давайте разберемся как использовать данный функционал.

### **Указание суммы**

Для генерации ссылки на оплату вам необходимо установить значение переменной **payment\_sum,**  сразу после этого появится переменная **yandex\_money\_pay\_url.** Эту переменную можно вывести на экран ссылкой или разместить на кнопке с текстом "Оплатить". &#x20;

Ссылка на оплату будет сгенерирована автоматически, вам необходимо вставить&#x20;

**#{yandex\_money\_pay\_url}** в **поле URL вложения либо в кнопку. Как это сделать:**

Шаг 1. В калькуляторе прописываем payment\_sum:

<figure><img src="/broken/files/PEyzF7z6btQkbxeZTUTw" alt=""><figcaption><p>Рис. 9. Указываем переменную payment_sum в калькуляторе в блоке</p></figcaption></figure>

{% hint style="success" %}
Минимальная сумма платежа — 10 рублей.&#x20;
{% endhint %}

Далее протяните стрелку ко второму блоку, в которой будет лежать ссылка в виде **#{yandex\_money\_pay\_url}.**&#x20;

**Шаг 2. В следующем блоке вставляем конструкцию #{yandex\_money\_pay\_url}:**

**а) во вложение в виде ссылки:**

<figure><img src="/broken/files/QmqzAg2b4SgzR4JfA6Un" alt=""><figcaption><p>Рис. 10. Пример № 1, указываем #<strong>{yandex_money_pay_url} в поле url для отправки вложения в виде ссылки</strong></p></figcaption></figure>

б) в кнопке в виде ссылки — для этого нужно создать кнопку во втором блоке:

<figure><img src="/broken/files/dsK55JUV00cj2wxFBoAF" alt=""><figcaption><p>Рис. 11. Пример " 2, указываем <strong>#{yandex_money_pay_url} в поле url настроек кнопки</strong></p></figcaption></figure>

Укажите конструкцию <mark style="color:green;">**#{yandex\_money\_pay\_url}**</mark>**&#x20;в настройках кнопки&#x20;**<mark style="color:green;">**в поле url**</mark>

Шаг 3. Тестируем

а) Тестирование бота с ссылкой на оплату во вложении:

<figure><img src="/broken/files/6yEV3wBuPjuCb0Qoz25f" alt="" width="563"><figcaption><p>Рис. 12. Бот направляет ссылку в сообщении</p></figcaption></figure>

При переходе по ссылке клиент попадает в платежную форму Юмани:

<figure><img src="/broken/files/TUu5oC9bkc8G1zbeW99x" alt=""><figcaption><p>Рис. 13. Платежная форма</p></figcaption></figure>

б) Тестирование бота с ссылкой на оплату в кнопке:

Бот отрабатывается верно и направляет клиенту кнопку с ссылкой на оплату.

<figure><img src="/broken/files/4BbAYNsUs8Gcfv4BkCS8" alt="" width="563"><figcaption><p>Рис. 14. Отработка ботом схемы с кнопкой</p></figcaption></figure>

При клике на кнопку клиент переходит в форму оплаты:

<figure><img src="/broken/files/TUu5oC9bkc8G1zbeW99x" alt=""><figcaption><p>Рис. 15. Платежная форма</p></figcaption></figure>

{% hint style="danger" %}
Обращаем внимание!

1. Ссылка на оплату живет ограниченное количество времени (несколько часов).
2. Ссылка генерируется после назначения переменной **payment\_sum**, поэтому устанавливайте переменную перед отправкой ссылки. Также продумайте возможность повторной генерации ссылки.
3. Для совершения повторного платежа обязательно необходимо обнулить payment\_sum, ранее сформированную ссылку и уже после переназначить переменную payment\_sum для получения свежей ссылки.&#x20;

Чтобы обнулить переменную payment\_sum, в калькуляторе в следующем блоке присвойте ей значение, равное 0, а на следующей строке калькулятора указанть yandex\_money\_pay\_url=""
{% endhint %}

## Уведомление о результате оплаты

После успешной оплаты в бот придет колбек, по которому вы сможете понять, что оплата прошла. Этот колбек в системе вы видите как сообщения от пользователя, _<mark style="color:green;">**но пользователю он не отображается**</mark>_<mark style="color:green;">**.**</mark>&#x20;

<figure><img src="/broken/files/ndIboFHmYexxpd4btU1p" alt="" width="563"><figcaption><p>Рис. 16. Пример колбека</p></figcaption></figure>

Колбек состоит из секрета и приписки со статусом, например: **qxgZ7zkNX4HHnG8UpZ61\_success**. Также после успешной оплаты переменная **yandex\_money\_payment\_completed** устанавливается в **True.**

{% hint style="success" %}
Эти колбеки НЕ ВИДИТ пользователь, они отображаются только оператору.
{% endhint %}

{% hint style="danger" %}
Тип сравнения должен быть "**Полное совпадение**"
{% endhint %}

{% hint style="warning" %}
Для совершения повторного платежа обязательно необходимо обнулить payment\_sum, ранее сформированную ссылку и уже после переназначить переменную payment\_sum для получения свежей ссылки:\
\
Пример обнуления переменных:\
payment\_sum=0\
yandex\_money\_pay\_url=""
{% endhint %}

После завершения оплаты клиенту добавится переменная **yoomoney\_callback\_data**, содержащая данные ответа платежной системы по совершенной операции. Из полученного словаря можно извлечь необходимые данные при помощи метода **get**.

Чтобы отреагировать на колбек, необходимо создать блок с условием. Это может быть блок "Стартовое условие" или "Не состояние с условием":

<figure><img src="/broken/files/1PZp85OVDofX21I35qzs" alt=""><figcaption><p>Рис. 17. Пример настройки реакции в блоке "Стартовое условие"</p></figcaption></figure>

<figure><img src="/broken/files/1ugwz64r1UM9aPl2C6jC" alt=""><figcaption><p>Рис. 18. Пример настройки реакции в блоке "Не состояние с условием"</p></figcaption></figure>

## **Пример**&#x20;

### **Ссылка на оплату для разных тарифов**

Пример схемы, которая позволит протестировать Чат-бота и быстро начать работу с ЮMoney:

<figure><img src="/broken/files/KDLnvT6QBMmKWT9LeyOs" alt="" width="563"><figcaption><p>Рис. 19. Итоговая схема</p></figcaption></figure>

1. Выберите тип блока "Стартовое условие" и пропишите ключевые слова, на которые будет реагировать бот:

<figure><img src="/broken/files/vM7nk8hHGRO1VVzgloVq" alt=""><figcaption><p>Рис. 20. Настройка блока "Стартовое условие"</p></figcaption></figure>

Так бот будет реагировать на приветственное сообщение от пользователя:

<figure><img src="/broken/files/JQzZIJhHhsEKS2IFGonY" alt="" width="563"><figcaption><p>Рис. 21. Отработка ботом в режиме тестирования</p></figcaption></figure>

2. Далее в этом же блоке создадим две кнопки "Базовый" и "Премиум", чтобы клиент переходил по стрелкам:

<figure><img src="/broken/files/GJakpne6hTntKFvXYJqM" alt="" width="563"><figcaption><p>Рис. 22. Кнопки в настройках блока</p></figcaption></figure>

3. Создаем два блока ниже. В настройках стрелки указываем в условие текст из кнопок:

<figure><img src="/broken/files/AoV76aeCp8cnS5wLe526" alt=""><figcaption><p>Рис. 23. Указываем в условии стрелки названия кнопок</p></figcaption></figure>

Теперь схема выглядит следующим образом:

<figure><img src="/broken/files/XQ1HK5zMlLl2q22OXQnX" alt=""><figcaption><p>Рис. 24. Промежуточный вид схемы</p></figcaption></figure>

Теперь в зависимости от того, на какую кнопку нажмет клиент "Премиум" или "Базовый", он перейдет в один из блоков состояние.

3. В настройках блока, стрелка к которому ведет по клику на кнопку "Премиум", укажем payment\_sum = 300, а во втором блоке payment\_sum = 150.

<figure><img src="/broken/files/PDzcnKE9H7bYlcvxAd9I" alt=""><figcaption><p>Рис. 25. Настройки блока, в который ведет стрелка с условием "Премиум"</p></figcaption></figure>

Аналогичные настройки у второго блока "Состояние":

<figure><img src="/broken/files/HMWvrbyL3rHwPVX9p1Qe" alt=""><figcaption><p>Рис. 26. Настройки блока, в который ведет стрелка с условием "Базовый"</p></figcaption></figure>

3. Сформируем ссылку на оплату.

Создадим блок ниже, в котором будет лежать ссылка на оплату. К этому блоку проведем стрелки из двух предыдущих блоков, в которых лежит переменная payment\_sum:

<figure><img src="/broken/files/yFABQ4B8qISo3wGQlssD" alt=""><figcaption><p>Рис. 27. Настройки блока с кнопкой, в которой лежит ссылка на оплату</p></figcaption></figure>

Добавим кнопку с ссылкой на оплату:

<figure><img src="/broken/files/aQZmlbNyFtWI4I0U5WLv" alt=""><figcaption><p>Рис. 28. Настройки кнопки</p></figcaption></figure>

Обратите внимание, что в поле url <mark style="color:red;">**#{yandex\_money\_pay\_url} — это ссылка на оплату.**</mark>&#x20;

Далее протягиваем стрелки из двух блоков к блоку с ссылкой на оплату:

<figure><img src="/broken/files/qp1kJQGtT8x6t4AG89qY" alt=""><figcaption><p>Рис. 29. Настройки стрелки с таймером</p></figcaption></figure>

В настройках стрелки указываем задержку "0 секунд".&#x20;

Теперь наша схема выглядит следующим образом:

<figure><img src="/broken/files/KDLnvT6QBMmKWT9LeyOs" alt="" width="563"><figcaption><p>Рис. 30. Итоговая схема</p></figcaption></figure>

Как работает схема:

1. Клиент пишет боту;
2. Бот отвечает клиенту и направляет кнопки для выбора тарифа.
3. Клиент выбирает тариф и бот формирует ссылку на оплату.
4. Ссылка на оплату формируется с суммой, которая указана в payment\_sum. В зависимости от выбора тарифа сумма будет разная.

Тестирование схемы:&#x20;

Сначала выберем **базовый тариф:**

<figure><img src="/broken/files/hEJAVxPJga0ymnWloxXg" alt="" width="563"><figcaption><p>Рис. 31. Тестирование схемы: выбираем тариф "Базовый"</p></figcaption></figure>

При клике на кнопку оплаты клиент перейдет в форму оплаты Юмани с суммой в 150 рублей:

<figure><img src="/broken/files/ixVnxHz8PvOOlA8KDlOJ" alt=""><figcaption><p>Рис. 32. Форма оплаты</p></figcaption></figure>

Теперь выберем тариф "Премиум":

<figure><img src="/broken/files/PeDbQtOiNBGOkvVV0kp5" alt="" width="563"><figcaption><p>Рис. 33. Тестирование бота: выбираем тариф "Премиум"</p></figcaption></figure>

Теперь перейдем по ссылке:

<figure><img src="/broken/files/yr1ikXZulGLkaln83Ox6" alt="" width="563"><figcaption><p>Рис. 34. Форма оплаты</p></figcaption></figure>

Бот снова отработал верно, при этом мы даже не обнуляли данные клиента при тестировании.&#x20;

### Ссылка на оплату, когда клиент сам выбирает сумму

Теперь давайте сделаем чат-бота для благотворительности: в данном случае клиент сам будет выбирать, какую сумму отправлять вам на благотворительность.

1. Создаем блок "Стартовое условие" и прописываем основные настройки:

<figure><img src="/broken/files/4Sygw3XGgfYLhxcI2SQM" alt=""><figcaption><p>Рис. 35. Настройки блока "Стартовое условие"</p></figcaption></figure>

2. Создаем блок ниже и в настройках стрелки указываем в поле "Условие" текст кнопки:

<figure><img src="/broken/files/gORvu0gMaLMpyLNzfZmQ" alt=""><figcaption><p>Рис. 36. Настройки стрелки</p></figcaption></figure>

{% hint style="success" %}
Кнопка в блоке "Стартовое условие" простая: функция "По умолчанию" без ссылки.&#x20;
{% endhint %}

3. Далее во втором блоке спрашиваем у клиента, какую сумму он готов пожертвовать:

<figure><img src="/broken/files/PH0C1vIfRcVybMCnqtZw" alt=""><figcaption><p>Рис. 37. Настройки блока "Состояние".</p></figcaption></figure>

4. Создаем третий блок ниже и в настройках стрелки активируем чекбокс "Пользователь вводит данные" и указываем переменную payment\_sum:

<figure><img src="/broken/files/PCktuRtZfc8YM1ziE5je" alt=""><figcaption><p>Рис. 38. Указываем переменную payment_sum в настройках стрелки</p></figcaption></figure>

5. В третьем блоке создаем кнопку и прописываем любое сообщение:

<figure><img src="/broken/files/fTdqPo5yAQh0Af9QcEOa" alt=""><figcaption><p>Рис. 39. Настройки кнопки, в которой лежит ссылка на оплату</p></figcaption></figure>

В поле url в настройках кнопки указываем <mark style="color:red;">**#{yandex\_money\_pay\_url} — это ссылка на оплату.**</mark>&#x20;

<figure><img src="/broken/files/zyMkLGbMohBvTaBhQUh2" alt=""><figcaption><p>Рис. 40. Настройки третьего блока "Состояние", который будет отправлять клиенту кнопку с ссылкой на оплату</p></figcaption></figure>

Как работает схема?

1. Пользователь пишет боту.&#x20;
2. Бот отправляет пользователю блок с кнопкой и сообщением.&#x20;
3. Если пользователь нажимает на кнопку "Я хочу пожертвовать приюту", то переходит в следующий блок. Если не нажимает, то остается в блоке "Стартовое условие".
4. Далее Бот спрашивает у пользователя, какую сумму пользователь хочет пожертвовать.
5. Пользователь пишет сумму цифрами, сумма записывается в переменную payment\_sum.
6. Далее бот отправляет кнопку с ссылкой на оплату на сумму, которую написал клиент.&#x20;

Тестирование схемы

В режиме тестирования бот отработался верно.&#x20;

<figure><img src="/broken/files/ElNvCcAXtHEJI2krXRJs" alt="" width="563"><figcaption><p>Рис. 41. Тестирование схемы чат-бота</p></figcaption></figure>

При клике на кнопку с ссылкой на оплату, открывается форма оплаты с введенной суммой в боте:

<figure><img src="/broken/files/fWmL43x9HB5shLxGRpnX" alt=""><figcaption><p>Рис. 42. Форма оплаты</p></figcaption></figure>

{% hint style="success" %}
Готово!&#x20;

Теперь вы знаете, как собрать чат-бот для благотворительности!
{% endhint %}

### Видео-инструкция

{% embed url="https://youtu.be/dDV0aeiw7mw" %}
