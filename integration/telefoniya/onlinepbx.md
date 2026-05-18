# OnlinePBX

## Ключ API и домен

Чтобы подключить сервис к Salebot, перейдите в свой аккаунт на платформе OnlinePBX:

<figure><img src="../../.gitbook/assets/Снимок экрана 2024-07-04 в 16.57.36.png" alt="" width="563"><figcaption></figcaption></figure>

Далее перейдите в раздел "Интеграция":

<figure><img src="../../.gitbook/assets/Снимок экрана 2024-07-04 в 16.59.06.png" alt=""><figcaption></figcaption></figure>

Затем в раздел API:

<figure><img src="../../.gitbook/assets/Снимок экрана 2024-07-04 в 17.02.28.png" alt=""><figcaption></figcaption></figure>

В данном разделе вам понадобится скопировать API-ключ:

<figure><img src="../../.gitbook/assets/Снимок экрана 2024-07-04 в 17.03.37.png" alt=""><figcaption></figcaption></figure>

А также домен onlinePBX:

<figure><img src="../../.gitbook/assets/Снимок экрана 2024-07-04 в 17.05.42.png" alt=""><figcaption></figcaption></figure>

На данном этапе настройки подключения нами были получены необходимые данные для подключения. Переходим в настройки Salebot.

## Подключение к Salebot

Для подключения интеграции перейдите в раздел "Телефония" в настройках проекта:

<figure><img src="../../.gitbook/assets/Снимок экрана 2024-07-04 в 17.07.54.png" alt="" width="375"><figcaption></figcaption></figure>

Далее найдите onlinePBX среди доступных сервисов для интеграции:

<figure><img src="../../.gitbook/assets/Снимок экрана 2024-07-04 в 17.08.57.png" alt="" width="563"><figcaption></figcaption></figure>

Далее кликните на "Подключить", после чего откроется окно модальной формы с пустыми полями для ввода значений:

<figure><img src="../../.gitbook/assets/Снимок экрана 2024-07-04 в 17.09.59.png" alt=""><figcaption></figcaption></figure>

В поле API-key вставьте ключ-API:

<figure><img src="../../.gitbook/assets/Снимок экрана 2024-07-04 в 17.11.31.png" alt=""><figcaption><p>Поле с ключом АПИ в окне подключения</p></figcaption></figure>

<figure><img src="../../.gitbook/assets/Снимок экрана 2024-07-04 в 17.12.19.png" alt=""><figcaption><p>Ключи АПИ из сервиса OnlinePBX</p></figcaption></figure>

Затем вставьте в следующее поле домен от сервиса:

<figure><img src="../../.gitbook/assets/Снимок экрана 2024-07-04 в 17.14.58.png" alt=""><figcaption><p>Домен в поле формы подключения сервиса</p></figcaption></figure>

<figure><img src="../../.gitbook/assets/Снимок экрана 2024-07-04 в 17.05.42 (1).png" alt=""><figcaption><p>Домен в разделе API сервиса OnlinePBX</p></figcaption></figure>

Затем нажмите "Сохранить настройки":

<figure><img src="../../.gitbook/assets/Снимок экрана 2024-07-04 в 17.17.05.png" alt="" width="563"><figcaption></figcaption></figure>

Если вы сделали все верно, то в разделе "Телефония" в настройках проекта вы увидите, что сервис был подключен:

<figure><img src="../../.gitbook/assets/Снимок экрана 2024-07-04 в 17.18.09.png" alt=""><figcaption></figcaption></figure>

## Настройка Webhook

Вебхук - поможет отслеживать события на сервисе OnlinePBX и передавать их в систему Salebot при помощи функций.&#x20;

Чтобы добавить вебхук перейдите в раздел "Webhooks" на стороне сервиса OnlinePBX:

<figure><img src="../../.gitbook/assets/Снимок экрана 2024-07-04 в 16.59.51.png" alt=""><figcaption></figcaption></figure>

Кликните на кнопку "Добавить":

<figure><img src="../../.gitbook/assets/Снимок экрана 2024-07-04 в 17.20.43.png" alt="" width="524"><figcaption></figcaption></figure>

Откроется поле для ввода URL:

<figure><img src="../../.gitbook/assets/Снимок экрана 2024-07-04 в 17.21.23.png" alt=""><figcaption></figcaption></figure>

В поле URL необходимо указать:

**https://chatter.salebot.pro/onlinepbx\_webhook/\<domain>**

где \<domain> - это ваш домен onlinePBX.&#x20;

<figure><img src="../../.gitbook/assets/Снимок экрана 2024-07-04 в 17.24.01.png" alt=""><figcaption></figcaption></figure>

### Функции в калькуляторе

1. onlinepbx\_employee\_call(short\_number, client\_number) - для инициации звонков между сотрудниками и клиентами.

<table><thead><tr><th width="317">Параметры</th><th>Описание</th></tr></thead><tbody><tr><td>short_number</td><td>внутренний короткий номер сотрудника</td></tr><tr><td>client_number</td><td>номер клиента</td></tr></tbody></table>

2. onlinepbx\_group\_call(group\_number, client\_number) - для групповых звонков.

<table><thead><tr><th width="317">Параметры</th><th>Описание</th></tr></thead><tbody><tr><td>group_number,</td><td>внутренний номер группы сотрудников</td></tr><tr><td>client_number</td><td>номер клиента</td></tr></tbody></table>

Эта функция инициирует звонок сразу же группе сотрудников, после того как один из сотрудников возьмет трубку - он начнет звонить клиенту.
