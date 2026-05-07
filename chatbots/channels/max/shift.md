# Перенос закрытых клубов из TG в MAX

Сначала необходимо зарегистрироваться в MAX и создать бота.

{% hint style="info" %}
[Подробнее о создании чат-бота для MAX и возможностях мессенджера рассказали в статье MAX.](chatbot_max.md)
{% endhint %}

{% hint style="warning" %}
После прохождения верификации в мессенджере, в настройках бота вы найдете **токен.** Обязательно скопируйте его, он понадобится вам далее.
{% endhint %}

После регистрации и верификации, создайте групповой чат в MAX:

<div data-with-frame="true"><figure><img src="../../../.gitbook/assets/Снимок экрана 2026-02-26 в 10.28.03.png" alt="" width="375"><figcaption></figcaption></figure></div>

Далее добавьте бота в группу и назначьте бота суперадминистратором:

<div data-with-frame="true"><figure><img src="../../../.gitbook/assets/Снимок экрана 2026-02-26 в 10.30.06.png" alt="" width="563"><figcaption></figcaption></figure></div>

Теперь перейдите в Salebot в раздел "Каналы" в проекте и нажмите на кнопку MAX:

<div data-with-frame="true"><figure><img src="../../../.gitbook/assets/Снимок экрана 2026-02-26 в 10.32.46.png" alt=""><figcaption></figcaption></figure></div>

Вставьте токен, скопированный в настройках бота, в одноименное поле "Токен" и нажмите "Готово". Тогда бот будет подключен к вашему проекту в Salebot.

{% hint style="warning" %}
Теперь скопируйте ID группового чата в MAX.
{% endhint %}

Затем перейдите в настройки проекта в раздел "Константы" и пропишите константы:

* save\_webhook=1
* access\_token=ntp0MZxYF3K8kKtDeQ7p8oDOjSCM7EKSkl0CvJpw91DWUhMQNARTnoLtzA\
  <mark style="color:$success;">**(здесь указывается токен вашего бота в MAX)**</mark>
* chatId=-1234567\
  <mark style="color:blue;">**(здесь указывается ID вашего группого чата в MAX. Обращаем внимание, ID группового чата прописан со знаком "-"!)**</mark>

<div data-with-frame="true"><figure><img src="../../../.gitbook/assets/Снимок экрана 2026-02-26 в 10.36.23.png" alt="" width="563"><figcaption></figcaption></figure></div>

{% hint style="warning" %}
Перейдите в раздел списки и создайте Список для подписчиков. ID данного списка вам понадобится далее по настройкам.
{% endhint %}

В блоке после успешной оплаты в Telegram добавляйте клиента в Список, созданный ранее. Далее будем отправлять блок с функцией в калькуляторе на добавление в групповой чат в MAX.

Шаг 1. Создайте блок в конструкторе SaleBot:

<div data-with-frame="true"><figure><img src="../../../.gitbook/assets/Снимок экрана 2026-03-04 в 17.01.48.png" alt=""><figcaption></figcaption></figure></div>

И пропишите в калькуляторе функцию `max_add_chat_member(chat_id, user_id)`

Чтобы удалить клиента после окончания подписки, воспользуйтесь функцией `max_delete_chat_member(chat_id, user_id)`

<div data-with-frame="true"><figure><img src="../../../.gitbook/assets/Снимок экрана 2026-03-04 в 17.01.08.png" alt=""><figcaption></figcaption></figure></div>
