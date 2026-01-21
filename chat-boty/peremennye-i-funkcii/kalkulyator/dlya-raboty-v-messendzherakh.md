# Для работы в мессенджерах

{% hint style="danger" %}
**\*Facebook, Instagram, Whatsapp принадлежат Meta, деятельность котороый признана экстремистской и запрещена в РФ!**
{% endhint %}

## Для проверки подписки в Инстаграм\*&#x20;

**check\_insta\_subscription()**

{% tabs %}
{% tab title="Описание" %}
<mark style="background-color:blue;">**Для проверки подписки на**</mark> [<mark style="background-color:blue;">**Instagram**</mark>](#user-content-fn-1)[^1]<mark style="color:red;background-color:blue;">**\***</mark><mark style="background-color:blue;">**-аккаунт**</mark>

**check\_insta\_subscription()**

Параметры: Без параметров

Функция возвращает логическое True, если пользователь подписан на аккаунт, False - . не подписан.
{% endtab %}

{% tab title="Примеры" %}
<figure><img src="../../../.gitbook/assets/image (218).png" alt=""><figcaption></figcaption></figure>
{% endtab %}

{% tab title="Пример кода для копирования" %}
```
r=check_insta_subscription()
```
{% endtab %}
{% endtabs %}

## Для работы с Whatsapp\*&#x20;

**check\_whatsapp() | get\_whatsapp\_bot\_id\_by\_phone()**

{% tabs %}
{% tab title="Описание" %}
{% hint style="warning" %}
Функции работают, если к проекту подключен Whatsapp-бот
{% endhint %}

<mark style="background-color:blue;">**Для проверки, есть ли Whatsapp на номере телефона**</mark>

**check\_whatsapp(phone\_number) -** метод для проверки, подключен ли на данный номер Whatsapp

Параметры:

**phone\_number** - номер телефона в формате 79999999999 или 89999999999

Функция возвращает логическое True - номер зарегистрирован в Whatsapp, False - номер не зарегистрирован

<mark style="background-color:blue;">**Для получения Whatsapp bot\_id по номеру телефона**</mark>

**get\_whatsapp\_bot\_id\_by\_phone(bot\_phone)** - функция для поиска whatsapp bot\_id по номеру телефона
{% endtab %}

{% tab title="Примеры" %}
Проверим есть подключенный Whatsapp к номеру телефона:

<figure><img src="../../../.gitbook/assets/image (219).png" alt=""><figcaption><p>Пример применения функции check_whatsapp()</p></figcaption></figure>
{% endtab %}

{% tab title="Пример кода для копирования" %}
```
rs=check_whatsapp(79999999999)
```
{% endtab %}
{% endtabs %}

## Для удаления последнего сообщения

**last\_message\_id() | remove\_last\_message()**&#x20;

{% tabs %}
{% tab title="Описание" %}
**last\_message\_id()**- для получения номера последнего сообщения от бота

{% hint style="info" %}
Если были отправлены картинка и текст, номера сообщений разделены символом подчеркивания
{% endhint %}

{% hint style="warning" %}
Для корректного получения номера последнего сообщения от бота, нужно чтобы сообщение было сохранено в переписке с клиентом.&#x20;

То есть в блоке воронки было должно быть включено сохранение в историю, если отправлено через воронку, или при отправке рассылки было включено "сохранять сообщение в историю переписки"
{% endhint %}

**remove\_last\_message()** – для удаления последнего сообщения от бота

{% hint style="danger" %}
Работает <mark style="color:red;">только</mark> в Telegram и Вконтакте.&#x20;
{% endhint %}

Если вы включали переключатель "сохранить в истории переписки", то для ТГ/ВК можно удалить последнее сообщение через рассылку из блока, где в калькуляторе прописать remove\_last\_message(). Функция удаляет последнее отправленное ботом сообщение, но только если оно есть в истории переписки.

Пример:

Создаем блок для рассылки:

<figure><img src="../../../.gitbook/assets/Снимок экрана 2025-06-26 в 18.12.39.png" alt=""><figcaption></figcaption></figure>

{% hint style="success" %}
Настройте рассылку по своему усмотрению и перейдите во вкладку "Отправка"
{% endhint %}

Во вкладке отправка активируйте чекбокс "Сохранять рассылку в истории переписки с клиентом":

<figure><img src="../../../.gitbook/assets/Снимок экрана 2025-06-26 в 18.11.24.png" alt=""><figcaption></figcaption></figure>

Важно! Чтобы чекбокс "Сохранить рассылку в истории переписки клиентом" отображался во вкладке "Отправка", отключите в разделе каналы прочитанность сообщений для групп вконтакте:

<figure><img src="../../../.gitbook/assets/Снимок экрана 2025-06-26 в 18.16.12.png" alt=""><figcaption></figcaption></figure>

Далее смело отправляйте рассылку.&#x20;

Если вдруг вы хотите удалить последнее сообщение (например, сообщение с ошибкой), то удалить последнее сообщение можно одним блоком с функцией remove\_last\_message()

<figure><img src="../../../.gitbook/assets/Снимок экрана 2025-06-26 в 18.03.59.png" alt=""><figcaption></figcaption></figure>

Далее отправляйте рассылку с функцией удаления последнего сообщения.

{% hint style="warning" %}
ВАЖНО! Спустя время последнее сообщение удалить нельзя!
{% endhint %}
{% endtab %}

{% tab title="Примеры" %}
<figure><img src="../../../.gitbook/assets/image (220).png" alt=""><figcaption></figcaption></figure>
{% endtab %}

{% tab title="Пример кода для копирования" %}
```
soob = last_message_id()
status = remove_last_message()
```
{% endtab %}
{% endtabs %}

## Для приостановки работы бота

pause\_bot(minutes)

{% tabs %}
{% tab title="Описание" %}
pause\_bot(minutes) - приостанавливает действие бота на указанное количество минут.

minutes - число, обязательный параметр. Передавать можно как целое число, так и с точкой

Функция работает аналогично нажатию на кнопку "пауза" в диалоге с клиентом, только мы передаем сами на какое время останавливаем бота. При успешном выполнении возвращает True
{% endtab %}
{% endtabs %}

## Удаление запланированных сообщений

delete\_pended\_messages\_from\_list(message\_id\_list, with\_not\_delete)

{% tabs %}
{% tab title="Описание" %}
delete\_pended\_messages\_from\_list(message\_id\_list, with\_not\_delete)

Функция поможет удалить необходимые сообщения из запланированных.&#x20;

<mark style="color:red;">!</mark> message\_id\_list - обязательный параметр, передается список блоков, сообщения из которых из запланированных необходимо удалить;

with\_not\_delete - необязательный параметр; удалит сообщения с пометкой "Не удалять". В параметре можно передать любое значение

Возвращаемое значение в виде "<mark style="color:red;">**wrong message\_id\_list**</mark>" отображается в том случае, если message\_id\_list не передан или передан не массив

Как передать параметры:

<figure><img src="../../../.gitbook/assets/2024-09-05 18.07.36.jpg" alt=""><figcaption></figcaption></figure>

Где взять обязательный параметр:

<figure><img src="../../../.gitbook/assets/Снимок экрана 2025-08-28 в 17.42.52.png" alt=""><figcaption></figcaption></figure>
{% endtab %}
{% endtabs %}

## Проверка статуса оператора

check\_operator\_status(email, with\_pause)

{% tabs %}
{% tab title="Описание" %}
check\_operator\_status(email, with\_pause) - проверяет, на смене ли оператор. Возвращает True, если оператор на смене, False - если нет.

<mark style="color:red;">**!**</mark> email - обязательный параметр, email сотрудника

with\_pause - необязательный параметр, значения - 1 или 0. Если указать 1, функция вернет положительный ответ, если статус сотрудника  "На смене" или "Перерыв". Если указать 0, то положительный ответ будет, только если статус сотрудника "На смене". По умолчанию 1
{% endtab %}
{% endtabs %}

[^1]: **На территории Российской Федерации&#x20;**<mark style="color:red;">**запрещена деятельность**</mark>**&#x20;социальных сетей&#x20;**<mark style="color:red;">**Facebook**</mark>**&#x20;и&#x20;**<mark style="color:red;">**Instagram**</mark>**, принадлежащих компании Meta Platforms Inc**., признанные экстремистскими!
