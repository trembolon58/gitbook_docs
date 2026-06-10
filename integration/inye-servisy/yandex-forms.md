# Yandex Forms

Создайте форму в Yandex Forms с вашими вопросами [https://forms.yandex.ru/](https://forms.yandex.ru/) и далее следуйте инструкции ниже.

{% hint style="warning" %}
Обращаем внимание!

Инструкция устарела.

[Для создания опросов и сбора заявок используйте лендинг "Квиз".](../../websites/builder/kviz.md)
{% endhint %}

## Настройка Yandex

{% hint style="danger" %}
**Обязательно!** Необходимо настроить предзаполнение скрытого поля с идентификатором клиента.
{% endhint %}

Скрытые поля формы можно использовать для автоматической передачи в форму служебных или вспомогательных параметров. Это позволяет добавить к ответам пользователей дополнительную информацию для анализа и сбора статистики.

В нашем случае нужно обязательно добавить поле sb\_id - в нем будет записан идентификатор пользователя в Salebot, чтобы после отправки формы данные отправлялись клиенту.

Чтобы настроить скрытый параметр, добавьте на форму вопрос типа _Короткий текст_ с названием sb\_id.

<figure><img src="../../.gitbook/assets/image (250).png" alt=""><figcaption></figcaption></figure>

Для этого вопроса включите опцию Скрытый вопрос.

В поле Идентификатор вопроса укажите sb\_id — это будет название GET-параметра.<br>

<figure><img src="../../.gitbook/assets/image (251).png" alt=""><figcaption></figcaption></figure>

Получите ссылку на форму и добавьте в конец URL-адреса GET-параметр ?sb\_id=#{client\_id}

> Пример ссылки на форму с GET-параметром:
>
> https://forms.yandex.ru/u/6191b18d99e21b1b45b9c82?sb\_id=#{client\_id}

Далее отправьте эту ссылку клиенту из бота.&#x20;

При переходе по ссылке в скрытое поле sb\_id автоматически будет подставляться значение из переменной #{client\_id}.

<mark style="color:red;">**sb\_id - это обязательное поле,**</mark> но вы таким же образом можете передавать и свои данные, например, utm\_source (предварительно добавив это поле в форму, как и sb\_id).

> _Пример ссылки с передачей данных с помощью поля в форме:_ https://forms.yandex.ru/u/6191b18d99e21b1b45b9c82?sb\_id=#{client\_id}\&utm\_source=telegram

## Отправить свой колбек после заполнения формы

По умолчанию после отправки формы клиенту придет колбэк **yandex\_form\_received**.&#x20;

<figure><img src="../../.gitbook/assets/image (68) (1).png" alt=""><figcaption></figcaption></figure>

Как настроить колбек со своим текстом, читайте далее.\
Для этого нужно создать еще одно скрытое поле с названием **callback\_text**, все делаете аналогично как и sb\_id.

<figure><img src="../../.gitbook/assets/image (252).png" alt=""><figcaption></figcaption></figure>

Есть 2 варианта использования этого поля\
\
Замените **стандартный колбек yandex\_form\_received для формы на ваш**, для этого нужно указать _Значение по умолчанию_ и не передавать параметр в ссылке (галочка _Скрытый вопрос_ - установлена ), иначе он будет взят из ссылки.

<figure><img src="../../.gitbook/assets/image (253).png" alt=""><figcaption></figcaption></figure>

**Для отправки уникального колбека** передавайте **callback\_text** в ссылке со своим значением так же, как и sb\_id, пример:\
https://forms.yandex.ru/u/6191b18d99e21b1b45b9c82?sb\_id=#{client\_id}\&callback\_text=test

## Настройка вебхука

{% hint style="warning" %}
<mark style="color:red;">**Обязательно!**</mark> Настройка вебхука должна производиться только после заполнения формы.
{% endhint %}

На странице нужной формы, перейдите во вкладку **Интеграции**

<figure><img src="../../.gitbook/assets/image (254).png" alt=""><figcaption></figcaption></figure>

Далее внизу выбираем API -> Запрос JSON-RPC POST

<figure><img src="../../.gitbook/assets/image (255).png" alt=""><figcaption></figcaption></figure>

<mark style="color:red;">**В поле URL**</mark> <mark style="color:red;">**указываем**</mark> ссылку **https://chatter.salebot.pro/yandex\_form/API\_KEY**\
где **API\_KEY** - апи-ключ из настроек проекта в SaleBot&#x20;

> Пример ссылки: https://chatter.salebot.pro/yandex\_form/43ad8d427073ea93377544cc4a408f89

В параметрах указываем **sb\_id** и значение выбираем _Ответ на вопрос_, указываем **sb\_id**

<figure><img src="../../.gitbook/assets/image (256).png" alt=""><figcaption></figcaption></figure>

<figure><img src="../../.gitbook/assets/image (257).png" alt=""><figcaption></figcaption></figure>

Для **callback\_text** делаем тоже самое.

Так же можно добавить другие параметры, которые будут записаны **в отдельные переменные клиента** в SaleBot с указанными названиями. Например:

<figure><img src="../../.gitbook/assets/image (258).png" alt=""><figcaption></figcaption></figure>

{% hint style="warning" %}
Будьте внимательны с названиями, чтобы не перетереть уже существующие переменные у клиента!
{% endhint %}

Чтоб сохранить все ответы в одну переменную, можно выбрать пункт _Ответы на вопросы_ и выбрать все или, те, которые нужны, а также указать формат JSON, чтоб с ними легче было работать:

<figure><img src="../../.gitbook/assets/image (259).png" alt=""><figcaption></figcaption></figure>

В итоге должна получиться такая настройка (параметры могут отличаться, если добавлены дополнительные):

<figure><img src="../../.gitbook/assets/image (260).png" alt=""><figcaption></figcaption></figure>

{% hint style="warning" %}
Все переменные из формы будут записаны в переменные клиента Salebot.&#x20;
{% endhint %}

Сохраняем изменения. На этом настройка завершена.

_Пример значения переменной answers в диалоге клиента Salebot._&#x20;

В настройках  формы в эту переменную мы объединили ответы на все вопросы формы в формате Json&#x20;

<figure><img src="../../.gitbook/assets/image (69) (1).png" alt=""><figcaption></figcaption></figure>

{% hint style="info" %}
Для каждого вопроса формы можно указать отдельную переменную в настройках вебхука формы.
{% endhint %}

### Выдать ссылку на форму в боте:

Пример 1

<figure><img src="../../.gitbook/assets/image (261).png" alt=""><figcaption></figcaption></figure>

Пример 2

<figure><img src="../../.gitbook/assets/image (262).png" alt=""><figcaption></figcaption></figure>
