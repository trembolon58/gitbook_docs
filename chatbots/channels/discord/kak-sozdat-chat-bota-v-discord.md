# Как создать чат-бота в Discord

## Подготовка к подключению

### Cоздание бота

Шаг 1. Создайте приложение ([перейдите по ссылке](https://discord.com/developers/applications))

Шаг 2. Добавьте бота (Add Bot)

<div data-with-frame="true"><figure><img src="../../../.gitbook/assets/Снимок экрана 2026-03-10 в 13.30.29.png" alt=""><figcaption></figcaption></figure></div>

Шаг 2.1. В разделе Installation выберите Install Link -> None

<div data-with-frame="true"><figure><img src="../../../.gitbook/assets/Снимок экрана 2026-03-10 в 13.31.30.png" alt=""><figcaption></figcaption></figure></div>

Шаг 2.2. В разделе Bot выключите Public Bot, далее включите Intents:

* Message Content Intent;
* Server memebrs intent;
* но можно и Presence Intent на будущее.

<div data-with-frame="true"><figure><img src="../../../.gitbook/assets/Снимок экрана 2026-03-10 в 13.36.19.png" alt=""><figcaption></figcaption></figure></div>

<div data-with-frame="true"><figure><img src="../../../.gitbook/assets/Снимок экрана 2026-03-10 в 13.37.50.png" alt=""><figcaption></figcaption></figure></div>

&#x20;3\. Получите токен (Reset Token)

&#x20;4\. Добавьте бота на сервер (OAuth2 → URL Generator, в Scopes отметить bot, в Bot Permissions выбрать Send Messages, Read Message History и другие нужные привилегии, перейти по полученной ссылке, выбрать сервер для добавления и согласиться)

<div data-with-frame="true"><figure><img src="../../../.gitbook/assets/Снимок экрана 2026-03-10 в 13.39.07.png" alt=""><figcaption></figcaption></figure></div>

<div data-with-frame="true"><figure><img src="../../../.gitbook/assets/Снимок экрана 2026-03-10 в 13.40.18.png" alt=""><figcaption></figcaption></figure></div>

Для получения полного вебхука от Дискорд достаточно присвоить любое значение переменной  save\_webhook

Если переменная задана, вебхук будет в сохранен в discord\_webhook

## Подключение к Salebot

Теперь перейдите в раздел "Каналы" в своем проекте и нажмите кнопку Discord:

<div data-with-frame="true"><figure><img src="../../../.gitbook/assets/Снимок экрана 2026-03-10 в 14.22.17.png" alt=""><figcaption></figcaption></figure></div>

Откроется окно, куда нужно вставить сгенерирированный токен:

<div data-with-frame="true"><figure><img src="../../../.gitbook/assets/Снимок экрана 2026-03-10 в 14.23.30.png" alt=""><figcaption></figcaption></figure></div>

## Цепочка сообщений и AI-ассистент

Чат-бот в Discord поддерживает стандартные функции для ботов:

* умеет писать в каналы/треды/личные сообщения.&#x20;
* ставить реакции.
* прикреплять/получать вложения.&#x20;
* изменение/удаление сообщений.

Также можно включить AI-ассистента, тогда умный ИИ будет общаться с вашими клиентами в дискорде.

{% hint style="success" %}
Подробнее о том, как создать чат-бота, рассказали в разделе "[Как создать чат-бот для бизнеса](../../builder/)".
{% endhint %}

{% hint style="success" %}
Подробнее о том, как создать включить AI-ассистента, рассказали в разделе "[AI-ассистент](../../ai_assistant/)".
{% endhint %}
