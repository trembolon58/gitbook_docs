---
description: Прием платежей через Сбербанк
---

# Сбербанк Эквайринг

## Как подключить Сбербанк Эквайринг

Для подключения платежей через Сбербанк нужно обратиться в поддержку сбербанка и запросить:

1. **Открытый ключ (API-токен):**

![Рис. 1. Токен](https://lh6.googleusercontent.com/8_Noxv1DRE_wrfo54t8b6BKUo1bACEJ4p4RFKvWNrDrU_xbbWXZgaPoY6tLCGop-W6O4QnmQBuSjnxQ7AtF9ynS9wyO-VvFxuMlpERzedA0IhhT3bYV7aELDFXI8MMU-si3l8Z7b)

2\.  **Установить вебхук и получить Callback токен для уведомлений.**&#x20;

Для этого нужно обратиться в службу технической поддержки Сбербанка. \
В качестве url адреса для callback-уведомлений указываем: \
HTTP-метод: **GET https://chatter.salebot.pro/sberbank\_callback/result** \
и просим включить <mark style="color:red;">симметричную криптографию</mark>

После рассмотрения вашей заявки вам выдадут токен и секретный ключ для проверки callback-уведомлений, которые указываем в настройке формы подключения Сбербанк в проекте Salebot:&#x20;

<figure><img src="/broken/files/nlAgIgQUZTFLBssPilBf" alt=""><figcaption><p>Рис. 2. Подключение Сбербанк эквайринга</p></figcaption></figure>

{% hint style="info" %}
В личном кабинете сбербанка настоятельно рекомендуем включить сумму платежа в уведомления об оплате.
{% endhint %}

<figure><img src="/broken/files/UYizX7AsQnj4yt142Beo" alt=""><figcaption><p>Рис. 3.</p></figcaption></figure>

Для генерации ссылки на оплату, вам необходимо установить значение переменной **payment\_sum** (например 150 или 100.55 (<mark style="color:red;">через точку!</mark>)), сразу после этого появится переменная **sberbank\_pay\_url**. Эту переменную можно вывести на экран ссылкой или разместить на кнопке с текстом "Оплатить".&#x20;

**ПРИМЕР ссылки на оплату:**\
https://3dsec.sberbank.ru/payment/merchants/test/payment\_ru.html?mdOrder=70906e55-7114-41d6-8332-4609dc6590f4

Также, **до установки значения переменной** **payment\_sum**, можно задать следующие необязательные переменные для настройки платежа.

{% hint style="info" %}
**Обратите внимание:** переменной **payment\_sum** присваивается значение **последней**, после необязательных переменных **payment\_description, session\_timeout** и т.д.
{% endhint %}

**payment\_description** – описание заказа <mark style="color:red;">(не более 24 символов, запрещены к использованию %, +, конец строки \r и перенос строки \n)</mark>.

![Рис. 4. ](https://lh4.googleusercontent.com/PiH_ZwrwWLm_BrOjiqUMykhYHFGwLRVdBnxKmBbIL3YHMd4O4zTnb1MNd_KWxBp144G7MqA8KBAu-Gnt1XXLLgr4fDrrFank2mScbhh9Qnr9LWsC189JV9fz9ejMLMI1lzMJP63C)

**session\_timeout** - продолжительность жизни заказа в секундах. по умолчанию (1200 секунд = 20 минут).

**expiration\_date** - дата и время окончания жизни заказа. Формат: дд.мм.гггг чч:мм (например: 25.01.2021 12:23) Если указан этот параметр, то session\_timeout не учитывается.&#x20;

Также можно использовать стандартные переменные, например зададим время действия ссылки 2 дня от текущей даты до 12:00:\
`date = current_date + 2`\
`expiration_date = "#{date} 12:00"`

Еще пример время действия ссылки 30 минут:\
`time = current_time + 30`\
`expiration_date = "#{current_date} #{time}"`

<figure><img src="/broken/files/wOBFOSFGUZ3wUjRYSkhv" alt="" width="563"><figcaption><p>Рис. 5. Пример в калькуляторе</p></figcaption></figure>

**language** - Язык страницы оплаты в кодировке ISO 639-1 (например: en, ru, de). Если не указан, будет использован язык, указанный в настройках магазина как язык по умолчанию.

**currency** - Код валюты платежа ISO 4217. Если не указано, то используется значение по умолчанию. (643 - рубль, 840 - доллар и тд)<br>

![Рис. 6. Платежная форма](https://lh3.googleusercontent.com/wabMAwn20pglIK-XxDX1ORkK8OoQfhdOnJsx14OdVKN6aaRyzEsbXo593o611pgBj4gSSK49DY3aOjm4bpphHXue4_RiXvhisgkPkMP-GgAJ8E2fCEefXdpBDcLaAutXMrqmV22K)

{% hint style="info" %}
**Обратите внимание:** переменной **payment\_sum** присваивается значение **последней**, после необязательных переменных **payment\_description, session\_timeout** и т.д.
{% endhint %}

## Как сформировать ссылку на оплату

Создадим ссылку на оплату в размере 100р (в магазине по умолчанию рубль), для этого заполняем переменную **payment\_sum**

<figure><img src="/broken/files/xf6vQJyHcYrKsoyIYrAL" alt=""><figcaption><p>Рис. 7. Пример настройки блока "Стартовое условие"</p></figcaption></figure>

Далее в нужном месте выведем переменную _**#{**_**sberbank\_pay\_url}**, в которой содержится ссылка.

<figure><img src="/broken/files/A5uDCPS0ZIkJO4HkgtVO" alt=""><figcaption><p>Рис. 8. Настройки ссылки с оплатой</p></figcaption></figure>

На примере выше видно, что для формирования ссылки на оплату необходимо нажать на "Вложения", выбрать тип вложения "Ссылка" и вставить переменную в поле для URL.&#x20;

## **Как обработать результат**

После успешной оплаты в бот придут колбеки, по которым вы сможете понят&#x44C;**,** что была успешная оплата. \
Эти колбеки в системе вы видите как сообщения от пользователя, чтобы их не мог отправить пользователь, они состоят из **10 первых символов секретного ключа и приписки success**, например: omc79l97u4\_success

В случае неудачной оплаты, придет колбек с припиской omc79l97u4\_fail

{% hint style="success" %}
Эти колбеки НЕ ВИДИТ пользователь, они отображаются только оператору.
{% endhint %}

Тип сравнения должен быть "**Полное совпадение**"

Также после успешной оплаты переменная **sberbank\_payment\_completed** устанавливается в **True**.

Например, можно сделать обработку успешной оплаты блоком с условием и вывести соответствующее сообщение пользователю:

<figure><img src="/broken/files/N0SXxyjv51J8qs5iQg1z" alt=""><figcaption></figcaption></figure>

После завершения оплаты клиенту добавится переменная **sberbank\_callback\_data**, содержащая данные ответа платежной системы по совершенной операции. Из полученного словаря можно извлечь необходимые данные при помощи метода **get**.

## Как настроить Callback-уведомления

Бывает, техподдержка открывает доступ:

<figure><img src="/broken/files/4HJXzAmhoo7mF9Zm5H9k" alt=""><figcaption></figcaption></figure>
