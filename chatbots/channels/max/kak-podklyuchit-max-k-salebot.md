# Как подключить MAX к Salebot

{% hint style="warning" %}
Обращаем внимание!

В мессенджере запрещены рассылки и сообщения по таймеру. Ограничение «24-часового окна» для отправки сообщений не применяется. При этом соблюдение пункта 1.5 пользовательского соглашения MAX остаётся на вашей стороне.

[См. пункт 1.5 Правил MAX.](https://dev.max.ru/docs/legal/requirements)

Спасибо за понимание!
{% endhint %}

{% hint style="info" %}
При настройке кнопок для чат-бота в одной строке может быть максимум 7 кнопок.
{% endhint %}

## Создание бота

Чат-боты умеют решать типовые задачи прямо в MAX. Создайте бота, который будет делать что-то за вас.

Даже без навыков программирования сделать своего бота в приложении просто — придумайте сценарий и следуйте пошаговой инструкции.&#x20;

## Как получить токен бота

{% hint style="success" %}
Обращаем внимание!

**Создание чат-бота в MAX доступно для ю/л и ИП.**
{% endhint %}

**Шаг 1. Перейдите во вкладку Каналы в Salebot.**

Чтобы перейти на страницу регистрации в мессенджере, войдите в личный кабинет Сейлбот и выберите проект, в котором нужно подключить чат-бота MAX.

Затем в проекте перейдите во вкладку "Каналы" и нажмите на кнопку MAX:

<div data-with-frame="true"><figure><img src="../../../.gitbook/assets/Снимок экрана 2026-02-04 в 14.37.29.png" alt=""><figcaption></figcaption></figure></div>

При клике по кнопке подключения мессенджера откроется форма, где можно найти кнопку для регистрации в мессенджере для компаний (ю/л и ИП):

<div data-with-frame="true"><figure><img src="../../../.gitbook/assets/Снимок экрана 2026-02-04 в 14.40.47.png" alt=""><figcaption></figcaption></figure></div>

**Шаг 2. Создайте бота**

{% hint style="info" %}
Если вы уже создали бота на платформе  и он прошёл проверку, перейдите к разделу "[Подключение мессенджера](kak-podklyuchit-max-k-salebot.md#podklyuchenie-messendzhera)" ниже.
{% endhint %}

<div data-with-frame="true"><figure><img src="../../../.gitbook/assets/Снимок экрана 2025-10-29 в 14.53.01.png" alt=""><figcaption></figcaption></figure></div>

Чтобы подключить инструменты коммуникации с клиентами в MAX, вам нужно:

1. Пройти регистрацию по номеру телефона на платформе MAX для партнеров;
2. Ввести данные своей организации, чтобы создать Личный Кабинет;
3. В ЛК пройти верификацию организации (через Госуслуги или Банки-провайдеры).

**Шаг 3. Скопируйте токен из настроек бота**

Для этого:

1. Перейдите на платформу и авторизуйтесь.
2. Если у вас несколько ботов, в левом верхнем углу выберите нужный.
3. В разделе Чат-бот и мини-приложение нажмите Настроить.

<figure><img src="../../../.gitbook/assets/Снимок экрана 2025-10-29 в 14.40.04.png" alt="" width="375"><figcaption></figcaption></figure>

**Шаг 4. Скопируйте токен:**

<figure><img src="../../../.gitbook/assets/Снимок экрана 2025-10-29 в 14.40.10.png" alt="" width="563"><figcaption></figcaption></figure>

Теперь можно подключать мессенджер к Сейлбот.

## Подключение мессенджера

После того как вы создали бота в мессенджере, необходимо перейти в раздел "Каналы" в Сейлбот:

<div data-with-frame="true"><figure><img src="../../../.gitbook/assets/Снимок экрана 2025-03-26 в 17.43.10.png" alt="" width="327"><figcaption></figcaption></figure></div>

В разделе каналы нажимаем на “MAX” для ввода токена, который вы скопировали ранее при создании бота:

<div data-with-frame="true"><figure><img src="../../../.gitbook/assets/Снимок экрана 2025-10-29 в 14.49.08.png" alt=""><figcaption></figcaption></figure></div>

Вставьте скопированный токен и нажмите на “Готово”:

<div data-with-frame="true"><figure><img src="../../../.gitbook/assets/Снимок экрана 2025-03-26 в 17.39.30.png" alt=""><figcaption></figcaption></figure></div>

{% hint style="success" %}
Готово! Бот подключен
{% endhint %}

При запуске бота, в диалоге с клиентом появится сообщение /start&#x20;

<div data-with-frame="true"><figure><img src="https://lh7-rt.googleusercontent.com/docsz/AD_4nXcSUnHPFsQZwkZ8Es4f4Vr4Y-FPFNp1QvSEm9grsfWdZm7bPOA9Uxa-V0G-VYe-UhMULsB_ryMXzW1BTDqwcQ2IdJIwo-xrU2oG6veJrG8dFxDMrvmlWKjDbg0_yN-nacwGaGPM4Q?key=lOib_VIcXHaMAcJLN34KW0zJ" alt=""><figcaption></figcaption></figure></div>

<div data-with-frame="true"><figure><img src="https://lh7-rt.googleusercontent.com/docsz/AD_4nXc5lbrI_Obv31boqxI_3Uy8rFPSQ1dGzp6z6sK_YyvaVV6DoHuL4J5efIInLkFDUEQuf6i3Z-epXgO_bHUihWseodF6nw3br5Tw2j_rIUPDHlEbmPVS7yUGduhfG52NJT6dhuO5bg?key=lOib_VIcXHaMAcJLN34KW0zJ" alt=""><figcaption></figcaption></figure></div>
