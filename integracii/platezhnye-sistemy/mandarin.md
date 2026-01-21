---
description: >-
  В статье расскажем, как получать оплаты через платежную систему для бизнеса
  Mandarin
---

# Mandarin

Интеграция с платежной системой Mandarin доступна только на тарифе "Инфобиз".

## Как подключить платежную систему к Salebot

Зайдите в раздел "Эквайринг" - Mandarin и заполните форму в Salebot.pro:

<figure><img src="/broken/files/xm6yCNRjXw51R1OjZWAD" alt=""><figcaption><p>Рис. 1. Раздел "Эквайринг" ("Платежи" - в сокр. виде меню) для подключения платежной системы</p></figcaption></figure>

API-ключ вы должны запросить у менеджера, контакты которого указаны в личном кабинете на сайте Mandarin.&#x20;

<figure><img src="/broken/files/sqnttui43DYvMIyklErH" alt=""><figcaption><p>Рис. 2. Форма с полями ввода для подключения платежной системы</p></figcaption></figure>

Для регистрации используйте [ссылку](https://admin.mandarin.io/user/register?pref_id=111964).&#x20;

После ввода API-ключа можете приступать к работе.

### Формирование ссылки на рассрочку

Для формирования ссылки на оформление рассрочки используйте функцию mandarin\_generate\_payment\_url. Для ее работы потребуются следующий параметры:

<table><thead><tr><th width="240">Параметры</th><th>Значения</th></tr></thead><tbody><tr><td>amount</td><td>стоимость за единицу товара, </td></tr><tr><td>category</td><td>категория товара (любое условное обозначение в виде строки), </td></tr><tr><td>product_id</td><td>идентификатор товара (в виде строки, главное чтобы потом Вам было удобно его найти по этому обозначению), </td></tr><tr><td>amount_with_discount</td><td>необязательный параметр, стоимость товара с учетом скидки (по умолчанию берется значение amount, но если будет нужен следующий параметр, но не нужна скидка, то укажите сумму сделки повторно), </td></tr><tr><td>quantity</td><td>необязательный параметр, количество единиц товара (по умолчанию 1).</td></tr></tbody></table>

Итоговая сумма будет рассчитана автоматически на основании стоимости и количества товара.&#x20;

Если все будет сделано верно, то функция вернет ссылку, а если что-то будет указано неправильно, вернет текст ошибки от сервера.

Ссылка приведет клиента на сайт, на котором нужно будет выполнить ряд действий (подтвердить номер телефона, заполнить анкеты и т.д.). при формировании ссылки в сделке будет сохранена переменная mandarin\_application\_id которая потребуется при одном из способов обработки результатов по заявке

## Как обработать результат

Есть 2 способа обработать результат:

1. Вы можете запросить статус заявки через функцию mandarin\_get\_order\_info. У этой функции лишь один параметр application\_id - в нее вы можете передать содержимое переменной mandarin\_application\_id. В ответ придет идентификатор статуса заявки.Например: PhoneConfirmed
2. Для этого варианта обратитесь к менеджеру и попросите добавить сервер для коллбэков. Передайте ему эту ссылку: https://chatter.salebot.pro/mandarin\_callback/result

При таком способе будут приходить коллбэки, которые состоят из первых 8 символов API-ключа и идентификатора статуса заявки, разделенные символом нижнего подчеркивания

При выборе второго способа Вы можете указать менеджеру какие варианты идентификаторов хотите получать. Вот [полный список](https://docs.google.com/spreadsheets/d/12Ff7Xa4qdXNj21SjVCSBMGnO5-ezp_7zfISLZT4TzCI/edit?usp=sharing) с подробным описанием

## Формирование ссылки на оплату

Теперь в мандарине можно создавать ссылки на оплату. Для подключения нужны merchant\_id и secret\_key:

1. MerchantID - это числовой идентификатор вашего проекта (магазина) в системе Mandarin, используемый для идентификации вас, как пользователя API.
2. Secret - секретный ключ, необходимый для аутентификации запросов.

Найти номер проекта с помощью фильтров можно в Личном кабинете в разделе Проекты или посмотреть весь список. Здесь также можно отследить статус проекта, одобрен он или ожидает еще одобрения и в каком режиме находится ваш проект (тестовый или боевой).

<figure><img src="https://lh7-rt.googleusercontent.com/docsz/AD_4nXc-hbJikNj7p6yH-xB--j3hwxGXTRtP0IbkJC1FX9jC66oHRaQcW09mMPzviUNT80ZFWWeSJpUmxVc12p_wAVddRxJCbVorC8-StbqK5R611Mi1CtL8lOJwIi-PfbpQGaedD8O7sw?key=W9baWfnSGu1UrrssPCGrj9tM" alt=""><figcaption><p>Рис. 3. Раздел "Проекты" в платежной системе</p></figcaption></figure>

Кнопка действия откроет настройки конкретного проекта:

<figure><img src="https://lh7-rt.googleusercontent.com/docsz/AD_4nXfrElwM1GRRrZk9QrM3B2ggMyNiuxsoeuelbE5Y6HWXYWmChtWxzF-B4foHW_50EE6lE1odLZtfDACqvY7BKHYhieZ3avpEepavRjj3aJX7FUm54R3Uq4aYMi2J9JeI8A9COnK8zQ?key=W9baWfnSGu1UrrssPCGrj9tM" alt=""><figcaption><p>Рис. 4. Кнопка "Настроить" для просмотра настроек конкретного проекта</p></figcaption></figure>

<figure><img src="https://lh7-rt.googleusercontent.com/docsz/AD_4nXc0iMCeVHyNXzVG7DDqioN0SmQ0LflHXW-0ok0gcQxDJpqP8NEPmUBlbpvG-Pb45D4LEfK4D_0eltRzsMWbiBGVU2pHKlkBoEjhw45Wtd3L8ZZP3DtBbQcpO_fIoQxm20yMr4Ertg?key=W9baWfnSGu1UrrssPCGrj9tM" alt=""><figcaption><p>Рис. 5. Настройки проекта в платежой системе</p></figcaption></figure>

Здесь необходимо настроить:

1. Адрес для отправки коллбека:[ https://chatter.salebot.pro/mandarin\_callback](https://chatter.salebot.pro/mandarin_callback)
2. Адрес возвращения пользователя: https://[chatter.salebot.pro](https://chatter.salebot.pro/mandarin_callback)/mandarin\_callback/success

Управлять, просматривать Secret-ы может только пользователь с ролью Основной пользователь Личного кабинета.

После успешной авторизации вам будет предоставлен полный список ваших проектов и Secret-ы к ним.

<figure><img src="https://lh7-rt.googleusercontent.com/docsz/AD_4nXdiePLIzxvvHe-bzrWxcjv65jE0LiF9zYzu9-xONp0VhDpQ-Kaw0DDT58lAaPceJx-43DNP6pa9KcOI1kwLvmo0_su2eaARiRs75oaj7wIfA4lulEyEhJydUFWJNOtZAdrF0JYh?key=W9baWfnSGu1UrrssPCGrj9tM" alt=""><figcaption><p>Рис. 6. Список merchant_id</p></figcaption></figure>

Нажмите на нужный Merchant id и откроется окно редактирования/просмотра Secret.

Чтобы обновить Secret проекта, нажмите на кнопку Обновить Secret - значение автоматически будет обновлено и скопируется в буфер обмена.

<figure><img src="https://lh7-rt.googleusercontent.com/docsz/AD_4nXeGMbfF5C-VvpbOhe2PU_pbWXen-xd47hSWg-kDOQFmwb3MCrICIloyChux25lOia0UhnHihp_v1BpiP3qqH5abXkCoEUkr7PJFR8sZcw9lxy7o_WWT0Z0Lvtk1jBDDPO6BptN5dw?key=W9baWfnSGu1UrrssPCGrj9tM" alt=""><figcaption><p>Рис. 7. Обновление secret key</p></figcaption></figure>

Полученный secret нужно внести в настройки интеграции в Salebot

### Как сформировать ссылку на оплату:

get\_mandarin\_payment\_url(amount, email, phone, products\_for\_receipt)

* amount - Сумма к оплате.  В этом поле указываем стоимость товара в рублях;
* email - почта клиента;
* phone - телефон клиента. Параметр необязательный, НО нужно указывать для МСС 4814 и МСС 6050. Уточнить МСС для ваших банковских терминалов можно у вашего менеджера или обратившись в службу технической поддержки
* products\_for\_receipt - Параметры для формирования чеков. Необязательный параметр.

<figure><img src="/broken/files/dq7JyhqlSwqg4Me7IoAD" alt=""><figcaption><p>Рис. 8. Ссылка на оплату</p></figcaption></figure>

После оплаты поступит коллбек вида - ABCDEFGH\_success 110, где&#x20;

\`ABCDEFGH\` - первые 8 символов вашего secret\_key;&#x20;

\`success\` - результат оплаты. success - успешная оплата, fail - неуспешная;

\`110\` - сумма оплаты

Можно указать колбек в условии блока "Стартовое условие":

<figure><img src="/broken/files/NWMstVJwdpailXBsftHh" alt=""><figcaption><p>Рис. 9. Создаем блок "Стартовое условие" для реакции на успешную оплату</p></figcaption></figure>

А также в блоке "Не состояние с условием":

<figure><img src="/broken/files/8N4sxTJXF8Np6rsUIENr" alt=""><figcaption><p>Рис. 9. Создаем блок "Не состояние с условием" для реакции на успешную оплату</p></figcaption></figure>

{% hint style="info" %}
Если вы не хотите выбивать клиента из основной схемы чат-бота, воспользуйтесь блоком "Не состояние с условием" — в этот блок нельзя перейти, поэтому клиента после оплаты не выбьет из основной воронки и при этом он получит уведомление об успешной оплате.



А если вам нужно продолжить воронку с реакции на успешную оплату, то используйте блок "Стартовое условие", тогда клиент из блока оплаты перейдет в блок "Стартовое условие", с которого вы можете продолжить воронку.
{% endhint %}

### Как проводить автоматические платежи:&#x20;

После успешной оплаты по ссылке из get\_mandarin\_payment\_url, у клиента появится переменная \`mandarin\_payment\_id\`.&#x20;

Переменная \`mandarin\_payment\_id\` обязательна для последующих платежей.

Если ее удалить, следующий автоплатеж провести НЕ получится.

Чтобы провести повторную оплату, нужно вызвать функцию mandarin\_recurrent\_payment(amount, email, phone, products\_for\_receipt)

* amount - Сумма списания;
* email - почта клиента;
* phone - телефон клиента. Параметр обязательный, если передаете products\_for\_receipt;&#x20;
* products\_for\_receipt - Параметры для формирования чеков. Необязательный параметр.

**Формирование products\_for\_receipt:**

receipt = \[{"name":"ТОВАР1","quantity":"1","amount":"110""}]&#x20;

* products\_for\_receipt - массив, содержащий товарную номенклатуру.

Каждая единица товара должна быть представлена в виде словаря, содержащего параметры name, quantity, amount

&#x20;! products\_for\_receipt нужно указать в следующем формате:

\[{"name":"Наименование товара","quantity":"Количество товара","amount":"Стоимость товара""}]

где,

1\) name - наименование товара

2\) quantity - количество товара

3\) amount - стоимость одной единицы товара. Полная стоимость, переданная в get\_mandarin\_payment\_url или mandarin\_recurrent\_payment должна быть равна сумме всех товаров
