# MAX

{% hint style="warning" %}
Обращаем внимание!

В мессенджере запрещены рассылки и сообщения по таймеру.

Спасибо за понимание!
{% endhint %}

## Создание бота

Чат-боты умеют решать типовые задачи прямо в MAX. Создайте бота, который будет делать что-то за вас — например, присылать расписание на день или подсказывать упражнения в зале

Даже без навыков программирования сделать своего бота в приложении просто — придумайте сценарий и следуйте пошаговой инструкции.&#x20;

## Как получить токен бота

Чтобы подключить инструменты коммуникации с клиентами в MAX, вам нужно зарегистрироваться на платформе MAX для партнеров, создать чат-бот и пройти модерацию.

После этого у вас появится токен бота — он нужен для дальнейшей интеграции с MAX.

{% hint style="warning" %}
Обращаем внимание!

Подключение к платформе и создание ботов пока доступно для ограниченного круга юридических лиц.

Позднее в мессенджере появится возможность подключения ботов для ИП.
{% endhint %}

Чтобы получить токен:

**Шаг 1. Создайте бота**

Если вы уже создали бота на платформе (https:/ /business.max.ru/self) и он прошёл проверку, перейдите к следующему шагу.

<figure><img src="../../.gitbook/assets/Снимок экрана 2025-10-29 в 14.53.01.png" alt=""><figcaption></figcaption></figure>

Если у вас ещё нет бота, следуйте следующим шагам:

1. Войдите на платформу или зарегистрируйтесь по номеру телефона.
2. Создайте и верифицируйте профиль организации.
3. Создайте бота и пройдите его модерацию.

Готово!

Шаг 2. Скопируйте токен из настроек бота

Для этого:

1. Перейдите на платформу и авторизуйтесь.
2. Если у вас несколько ботов, в левом верхнем углу выберите нужный.
3. В разделе Чат-бот и мини-приложение нажмите Настроить.

<figure><img src="../../.gitbook/assets/Снимок экрана 2025-10-29 в 14.40.04.png" alt="" width="375"><figcaption></figcaption></figure>

4. Скопируйте токен:

<figure><img src="../../.gitbook/assets/Снимок экрана 2025-10-29 в 14.40.10.png" alt="" width="563"><figcaption></figcaption></figure>

Теперь можно подключать мессенджер к Сейлбот.

## Подключение мессенджера

После того как вы создали бота в мессенджере, необходимо перейти в раздел "Каналы" в Сейлбот:

<figure><img src="../../.gitbook/assets/Снимок экрана 2025-03-26 в 17.43.10.png" alt="" width="327"><figcaption></figcaption></figure>

В разделе каналы нажимаем на “MAX” для ввода токена, который вы скопировали ранее при создании бота:

<figure><img src="../../.gitbook/assets/Снимок экрана 2025-10-29 в 14.49.08.png" alt=""><figcaption></figcaption></figure>

Вставьте скопированный токен и нажмите на “Готово”:

<figure><img src="../../.gitbook/assets/Снимок экрана 2025-03-26 в 17.39.30.png" alt=""><figcaption></figcaption></figure>

{% hint style="success" %}
Готово! Бот подключен
{% endhint %}

При запуске бота, в диалоге с клиентом появится сообщение /start&#x20;

<figure><img src="https://lh7-rt.googleusercontent.com/docsz/AD_4nXcSUnHPFsQZwkZ8Es4f4Vr4Y-FPFNp1QvSEm9grsfWdZm7bPOA9Uxa-V0G-VYe-UhMULsB_ryMXzW1BTDqwcQ2IdJIwo-xrU2oG6veJrG8dFxDMrvmlWKjDbg0_yN-nacwGaGPM4Q?key=lOib_VIcXHaMAcJLN34KW0zJ" alt=""><figcaption></figcaption></figure>

<figure><img src="https://lh7-rt.googleusercontent.com/docsz/AD_4nXc5lbrI_Obv31boqxI_3Uy8rFPSQ1dGzp6z6sK_YyvaVV6DoHuL4J5efIInLkFDUEQuf6i3Z-epXgO_bHUihWseodF6nw3br5Tw2j_rIUPDHlEbmPVS7yUGduhfG52NJT6dhuO5bg?key=lOib_VIcXHaMAcJLN34KW0zJ" alt=""><figcaption></figcaption></figure>

## Как получить полный вебхук

Для получения полного вебхука от Max достаточно присвоить любое значение переменной  save\_webhook(переменная может быть как константой проекта, так и переменной сделки).

При этом ответ из мессенджера будет записываться в переменную tt\_request, которую вы найдете в карточке клиента среди переменных сделки

<figure><img src="https://lh7-rt.googleusercontent.com/docsz/AD_4nXfkxBmjNp7B04tzU3usUJQdbLHaUVQb4zgmO9wG67avS7Z3sfVfSIPLt4BW216hNA9TFAF3uCMZL0yaItSClObKS0TE3cXwHw5c-4l87lQOC9bBkYQzO1ZzbQnmRUvQkJ52p7hjhg?key=lOib_VIcXHaMAcJLN34KW0zJ" alt=""><figcaption></figcaption></figure>

Max поддерживает кнопки callback, кнопки с ссылкой, запрос номера телефона, запрос геолокации

Если клиент нажмет на кнопку с запросом номера и даст разрешение, в чат поступит сообщение с его номером телефона и появится переменная phone

<figure><img src="https://lh7-rt.googleusercontent.com/docsz/AD_4nXf8hqPt54QLddtsoPBV_7MMIJ692rZKtitBdtDOYdtS4_zcZAfIF1cUR3dEqAzIu-wz_ylxA5csjPZ0iviryykp6Aehh4QwCh70lAShabaQGsBhiZSVQjzs8FABCI-Ufh4-LNnahA?key=lOib_VIcXHaMAcJLN34KW0zJ" alt=""><figcaption></figcaption></figure>

Если клиент поделится своей геолокацией, данные поступят в виде сообщения, и будут созданы переменные latitude и longitude

<figure><img src="https://lh7-rt.googleusercontent.com/docsz/AD_4nXdqY5OvrFwuivc-KzKohVVqf0W0ZCf4MLCd6iOFnkPwB_eLJ887PK_Kcet6H1CaG3Uh6yDUJLkicvmz5wm35yi5jzSfKnJ6hR9zyrgEk_7WE5_MqYGgj1yppXPnRQG7pVHDMFAK-w?key=lOib_VIcXHaMAcJLN34KW0zJ" alt=""><figcaption></figcaption></figure>

<figure><img src="https://lh7-rt.googleusercontent.com/docsz/AD_4nXcYdlcImfwnNhYKZqHdx3MP0U9RbNZeXPPHbelHTc-AC4rWJBjRmO2TKCZ64oNshE5xHnvqHyjftAYT-mgT7aapd5YD2mrmwzZS765W7DX3uUyu_s1SIqRZTValGbDuifcRpfUE5Q?key=lOib_VIcXHaMAcJLN34KW0zJ" alt=""><figcaption></figcaption></figure>

## Inline-клавиатура

Такая клавиатура может иметь до 210 кнопок, сгруппированных в 30 рядов — до 7 кнопок в каждом. Если ряды кнопок не помещаются в плейсхолдер клавиатуры, автоматически подключается скролл

<figure><img src="https://lh7-rt.googleusercontent.com/docsz/AD_4nXdOvlu3Pf5fE3kBIxON37cXuey0fmeh9X4DW7Elvs44dc3jtroJ-rQjaGtNAScvF4T81KnWGSSapshEoqxZt5WjidQmA1O5_Folelg2-mabcYXPoVULb7c66A9yz8iLMAZbp4Vusw?key=TskrhZ7SwgOwOYQNjojb7VKN" alt=""><figcaption><p>Inline-клавиатура в чат-боте</p></figcaption></figure>

Поддерживаемые типы кнопок

* callback — сервер MAX отправляет событие с типом message\_callback (через Webhook или Long polling)
* link — позволяет пользователю открыть ссылку в новой вкладке
* request\_contact — запрашивает у пользователя разрешение на доступ к контактам — нику или телефону
* request\_geo\_location — запрашивает у пользователя его местоположение

## Доступные коллбеки

bot\_added -  подключенный бот добавлен в групповой чат/канал

bot\_removed - подключенный бот удален из группового чата/канала

user\_added - в групповой чат добавлен новый участник/другой бот

user\_removed  - из группового чата удален участник/другой бот

При срабатывании коллбеков на добавление/удаление участников, создаются переменные клиента

chat\_member\_name - имя пользователя

chat\_member\_username - ник пользователя (если установлен)

chat\_member\_id - id пользователя

Чтобы писать сообщения от имени бота, а также видеть сообщения других участников в групповом чате/канале, бота нужно назначить администратором и дать соответствующие разрешения&#x20;

<figure><img src="https://lh7-rt.googleusercontent.com/docsz/AD_4nXcayIDrqacWVl_jDsnno0J51KkSGhOeI2VidLf1g2mo5SZjCN1raRljOcxcU9Vn4kBZ1CI4q7m70yPylwBTfwOOO_Rcif0D7vrz8EoMHzse2fPFaqCuTBNj6o8ahcq_DVknscWnqQ?key=lOib_VIcXHaMAcJLN34KW0zJ" alt=""><figcaption></figcaption></figure>

### Форматирование сообщений <a href="#formatirovanie-soobshenii" id="formatirovanie-soobshenii"></a>

#### Markdown <a href="#markdown" id="markdown"></a>

\*Курсив\* или \_курсив\_

\*\*Жирный\*\* или \_\_Жирный\_\_

\~\~Зачеркнутый\~\~

++Подчеркнутый++

\`Моноширинный\`

<figure><img src="https://docs.salebot.pro/~gitbook/image?url=https%3A%2F%2F4216716816-files.gitbook.io%2F%7E%2Ffiles%2Fv0%2Fb%2Fgitbook-x-prod.appspot.com%2Fo%2Fspaces%252F-LxKl4rC_EcwBAz40Qn_%252Fuploads%252FE0sQVcLuODi0XSr5k8zb%252F%25D0%25A1%25D0%25BD%25D0%25B8%25D0%25BC%25D0%25BE%25D0%25BA%2520%25D1%258D%25D0%25BA%25D1%2580%25D0%25B0%25D0%25BD%25D0%25B0%25202026-01-05%2520%25D0%25B2%252010.27.57.png%3Falt%3Dmedia%26token%3D31a84f7b-98b9-4d43-9d6c-822ce8c56030&#x26;width=768&#x26;dpr=4&#x26;quality=100&#x26;sign=8670001d&#x26;sv=2" alt="" width="375"><figcaption></figcaption></figure>

<figure><img src="https://docs.salebot.pro/~gitbook/image?url=https%3A%2F%2F4216716816-files.gitbook.io%2F%7E%2Ffiles%2Fv0%2Fb%2Fgitbook-x-prod.appspot.com%2Fo%2Fspaces%252F-LxKl4rC_EcwBAz40Qn_%252Fuploads%252FOP3kBsfJNFP8ATB5WXmC%252F%25D0%25A1%25D0%25BD%25D0%25B8%25D0%25BC%25D0%25BE%25D0%25BA%2520%25D1%258D%25D0%25BA%25D1%2580%25D0%25B0%25D0%25BD%25D0%25B0%25202026-01-05%2520%25D0%25B2%252010.16.22.png%3Falt%3Dmedia%26token%3D3bfad43a-a62e-4369-aae0-309bf2e0b3b1&#x26;width=768&#x26;dpr=4&#x26;quality=100&#x26;sign=160a1748&#x26;sv=2" alt="" width="375"><figcaption></figcaption></figure>

#### HTML <a href="#html" id="html"></a>

\<i>курсив\</i> или \<em>курсив\</em>

\<b>жирный\</b> или \<strong>жирный\</strong>

\<del>зачёркнутый\</del> или \<s>зачёркнутый\</s>

\<ins>подчёркнутый\</ins> или \<u>подчёркнутый\</u>

\<pre>моноширинный\</pre> или \<code>моноширинный\</code>

ссылка \<a href="https://dev.max.ru">Docs\</a>

<div><figure><img src="../../.gitbook/assets/Снимок экрана 2026-01-21 в 14.54.37.png" alt=""><figcaption></figcaption></figure> <figure><img src="../../.gitbook/assets/Снимок экрана 2026-01-21 в 14.54.47.png" alt=""><figcaption></figcaption></figure></div>
