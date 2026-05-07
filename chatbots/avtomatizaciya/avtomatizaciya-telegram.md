# Автоматизация Telegram

Теперь в Salebot можно полностью автоматизировать работу закрытых каналов/чатов (клубов) в Telegram.

<div data-with-frame="true"><figure><img src="../../.gitbook/assets/Снимок экрана 2026-02-23 в 10.26.11.png" alt="" width="563"><figcaption></figcaption></figure></div>

Выдача доступа после оплаты, добавление и удаление участников, контроль сроков подписки — всё настраивается автоматически.

## Подготовка группы/канала

Чтобы успешно автоматизировать подписки в закрытые каналы или группы, Вам необходимо создать Telegram-бота, затем добавить его в канал/группу с правами администратора.

{% hint style="success" %}
#### Создать Telegram-бота

Как создать Telegram-бота и подключить его к Salebot, [рассказали в этой статье.](../channels/telegram/chatbot.md)
{% endhint %}

### Как добавить бота в группу/канал Telegram

Эта возможность для бота включается  в BotFather:

Шаг 1. Переходим в настройки бота:

<div data-with-frame="true"><figure><img src="../../.gitbook/assets/Снимок экрана 2025-04-24 в 13.45.09.png" alt="" width="358"><figcaption><p>Кликаем на Bot Settings</p></figcaption></figure></div>

Шаг 2. Кликните по "Allow Groups?'

<div data-with-frame="true"><figure><img src="../../.gitbook/assets/Снимок экрана 2025-04-24 в 13.49.11.png" alt="" width="328"><figcaption><p>Allow Groups?</p></figcaption></figure></div>

Шаг 3. Должен быть статус enabled

<div data-with-frame="true"><figure><img src="../../.gitbook/assets/Снимок экрана 2025-04-24 в 13.53.40.png" alt="" width="375"><figcaption></figcaption></figure></div>

### Видео-инструкция

{% embed url="https://www.youtube.com/watch?v=yDVp-rCCHtA" %}
Как включить возможность добавлять бота в группы и каналы
{% endembed %}

### Добавить бота как администратора в группе/канале

Шаг 1.  Перейдите в Управление группой/каналом и выберите вкладку “Администраторы”

<div data-with-frame="true"><figure><img src="../../.gitbook/assets/Снимок экрана 2025-04-24 в 14.11.27.png" alt="" width="375"><figcaption></figcaption></figure></div>

Шаг 2. Нажмите кнопку “Добавить Администратора”

<div data-with-frame="true"><figure><img src="../../.gitbook/assets/Снимок экрана 2025-04-24 в 14.11.42.png" alt="" width="563"><figcaption></figcaption></figure></div>

Шаг 3.  В поисковой строке введите логин Вашего бота.&#x20;

<div data-with-frame="true"><figure><img src="../../.gitbook/assets/Снимок экрана 2025-04-24 в 14.12.24.png" alt="" width="563"><figcaption></figcaption></figure></div>

Шаг 4. Для успешной работы бота предоставьте права на работу/удаление сообщений:

<div data-with-frame="true"><figure><img src="../../.gitbook/assets/Снимок экрана 2025-04-24 в 14.12.38.png" alt="" width="347"><figcaption></figcaption></figure></div>

## Настройки автоматизации

Чтобы автоматизировать работу в закрытых клубах по подписке, наведите курсором на "Конструктор". Тогда откроется меню, где вы увидите вкладку с автоматизацией Telegram:

<div data-with-frame="true"><figure><img src="../../.gitbook/assets/Снимок экрана 2026-02-23 в 09.42.51.png" alt=""><figcaption></figcaption></figure></div>

Далее нажмите на "Добавить автоматизацию". Тогда откроются настройки автоматизации с двумя вкладками: Основные настройки и Настройки сообщений.

### Основные настройки

В основных настройках выберите бота, который подключен к закрытому каналу/группе:

<div data-with-frame="true"><figure><img src="../../.gitbook/assets/Снимок экрана 2026-02-23 в 10.52.33.png" alt="" width="375"><figcaption></figcaption></figure></div>

{% hint style="info" %}
Важно!

Если бот не подключен к каналу или группе, то в плашке выбора группы и канала будет указано "Нет доступных групп":

<img src="../../.gitbook/assets/Снимок экрана 2026-02-23 в 11.02.05.png" alt="" data-size="original">
{% endhint %}

Далее выберите группу/канал, к которому подключен бот с ролью администратора:

<div data-with-frame="true"><figure><img src="../../.gitbook/assets/Снимок экрана 2026-02-23 в 11.10.43.png" alt="" width="563"><figcaption></figcaption></figure></div>

Создайте в настройках Telegram-канала пригласительную ссылку с одобрением заявки (вкл. Заявка на вступление).

<div data-with-frame="true"><figure><img src="../../.gitbook/assets/Снимок экрана 2026-02-23 в 11.12.45.png" alt="" width="375"><figcaption></figcaption></figure></div>

После создания скопируйте ссылку и вставьте ее в указанном поле:

<div data-with-frame="true"><figure><img src="../../.gitbook/assets/Снимок экрана 2026-02-23 в 11.19.42.png" alt="" width="563"><figcaption></figcaption></figure></div>

<div data-with-frame="true"><figure><img src="../../.gitbook/assets/Снимок экрана 2026-02-23 в 11.20.54.png" alt="" width="563"><figcaption></figcaption></figure></div>

В условии запуска бота можно оставить одно условие "/start" и добавить доп. условия через точку с запятой (;).

<div data-with-frame="true"><figure><img src="../../.gitbook/assets/Снимок экрана 2026-02-23 в 11.24.13.png" alt="" width="492"><figcaption></figcaption></figure></div>

{% hint style="info" %}
Внимание!

Условие можно прописать только на латинице.
{% endhint %}

Далее выберите сервис для приема платежей по подписке:

<div data-with-frame="true"><figure><img src="../../.gitbook/assets/Снимок экрана 2026-02-23 в 11.25.55.png" alt="" width="563"><figcaption></figcaption></figure></div>

Затем настройте тарифы для подписки:

<div data-with-frame="true"><figure><img src="../../.gitbook/assets/Снимок экрана 2026-02-23 в 11.26.25.png" alt="" width="563"><figcaption></figcaption></figure></div>

Нужно прописать:

1. Название тарифа;
2. Стоимость тарифа;
3. Количество дней доступа к каналу/группе (период).

Можно создать несколько тарифов для канала:

<div data-with-frame="true"><figure><img src="../../.gitbook/assets/Снимок экрана 2026-02-23 в 11.28.36.png" alt="" width="563"><figcaption></figcaption></figure></div>

Теперь нажмите "Сохранить" и перейдите к настройкам сообщений.

### Настройки сообщений

Во вкладке "Настройки сообщений" необходимо настроить следующие типы сообщений:

<div data-with-frame="true"><figure><img src="../../.gitbook/assets/Снимок экрана 2026-02-23 в 11.32.57.png" alt="" width="563"><figcaption></figcaption></figure></div>

{% hint style="info" %}
Приветственное сообщение — это сообщение является входом в воронку для покупки клиентом подписки в клуб (НЕ является первым сообщением в канале).
{% endhint %}

Можно прописать свой текст для каждого сообщения или оставить текст по умолчанию. После чего нажмите "Сохранить".

{% hint style="success" %}
Готово! Ваша автоматизация подписки в клубы завершена с помощью простых и понятных шагов.
{% endhint %}

Как работает автоматизация с минимальными настройками:

<div data-with-frame="true"><figure><img src="../../.gitbook/assets/Запись экрана 2026-02-23 в 11.41.42.gif" alt="" width="324"><figcaption></figcaption></figure></div>

Больше не нужно вручную проверять оплаты и управлять участниками. Salebot сам следит за доступом и помогает поддерживать порядок в группе.
