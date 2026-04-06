# Яндекс.Метрика для сайта

## Яндекс Метрика

К сайту, созданному в Salebot, можно подключить Яндекс.Метрику. Для этого создайте счётчик в Яндекс.Метрике, создайте цель и укажите данные в настройках сайта:

<div data-with-frame="true"><figure><img src="../../.gitbook/assets/image (44) (1) (1).png" alt=""><figcaption></figcaption></figure></div>

**ID Яндекс Метрики.** Укажите ID счётчика Я.Метрики&#x20;

**Идентификатор цели в Яндекс Метрике.** Укажите идентификатор цели события.

Если передадите идентификатор цели без нижнего подчеркивания в конце, для всех кнопок на минилендинге будет действовать одинаковая Цель, идентификатор которого передан в поле.

Если передадите идентификатор в виде "button\_" со знаком "\_" в конце, то цель будет отправлена для каждой кнопки мессенджера разная.&#x20;

Например, настройка целей в Метрике: \
"button\_0" - для ВКонтакте \
"button\_1" - для Телеграм.&#x20;

Идентификаторы мессенджеров для настроек на стороне Метрики: \
0 - Вконтакте \
1 - Телеграм \
2 - Viber \
3 - FaceBook\*\
6 - WhatsApp\*\
8 - Одноклассники \
10 - Instagram\*\
20 - MAX

{% hint style="danger" %}
\*Facebook, WhatsApp, Instagram принадлежат Meta platform Inc., деятельность которой признана в РФ экстремистской и запрещена.
{% endhint %}

_<mark style="color:green;">Пример как настроить на клики по кнопкам разных мессенджеров:</mark>_

<div align="left"><figure><img src="../../.gitbook/assets/2023-03-29_13-54-33.png" alt=""><figcaption><p>Настройки на сайте</p></figcaption></figure></div>

_Настройки на стороне Яндекс.Метрика:_

<div align="center" data-with-frame="true"><figure><img src="../../.gitbook/assets/image (45) (1) (1).png" alt=""><figcaption><p>Настройки в Яндекс.Метрике</p></figcaption></figure></div>

### Как подключить Яндекс Метрику

{% hint style="success" %}
Для подключения Метрики необходимо в первое поле вписать ID Яндекс Метрики.&#x20;
{% endhint %}

Первое поле принимает в себя ID счетчика Яндекс Метрики, его вы можете увидеть на странице Яндекс Метрики в разделе “Сводка” вверху возле Имения счетчика и Адреса сайта, на рисунке выделено

<div data-with-frame="true"><img src="https://lh3.googleusercontent.com/9TyuC74q0abBhLa92hj5G8FtqiQ2jYKy7vUQZI6oiz7u-wYCTC65MBsFryO3igeKTJXf2Yy6Fu0nxXXFBpB_CC3t_1GzAnhu_Dg9fVhoM-ulDwdFpSUVsURPcHofTZZuomNTGyj0" alt=""></div>

{% hint style="info" %}
Вставка ID счетчика равносильна добавлению “Код счетчика” на сайт
{% endhint %}

Это значительно сокращает время на интеграцию Яндекс Метрики в Ваш минилендинг.\
Во второе поле, в настройках минилендинга, вы можете вписать идентификатор Цели для отслеживания нажатий по кнопкам мессенджеров. Для этого вам следует создать цель/цели на сайте Яндекс Метрики. Чтобы это сделать, перейдите в раздел “Цели” и нажмите кнопку “Добавить цель”. У вас откроется попап меню для создания новой Цели.

<div data-with-frame="true"><img src="https://lh3.googleusercontent.com/PoJmABnzLB2qvjdd_-VqVPCm5GyWJRksqa89HrGH8hLhy-hn4xG87svBYxva0cLIoBtLID2of5KzHpRiEGpa8OHKH8Z_QC8KIEzmJAueRS0kzIm56MHbXixA75HajuQoqDsuvEKt" alt=""></div>

В поле “Название” вы можете написать что угодно. В графе “Тип условия” нужно выбрать “JavaScript-событие”. После этого ниже появится поле “Идентификатор цели”. В него нужно занести идентификатор, который вы позже укажите в настройках минилендинга.

{% hint style="info" %}
Цель будет срабатывать по нажатию на любую кнопку минилендинга.&#x20;
{% endhint %}

{% hint style="success" %}
Если вы хотите разделить цели по нажитию на разные кнопки минилендинга, название цели должно заканчиваться на знак подчеркивания "\_"
{% endhint %}

Пример:\
Если вы передадите в наше поле “click\_button”, тогда вам в Яндекс Метрику будет передаваться одна Цель по клику на любой из мессенджеров.&#x20;

Цель с идентификатором “click\_button”.\
Однако, если вы передадите в наше поле “click\_button\_” (у которого в конце стоит “\_” знак нижнего подчеркивания), в вашу Яндекс Метрику будет передаваться разная цель для разного мессенджера,

click\_button\_0 - по клику на ВКонтакте\
click\_button\_1 - по клику на Телеграм\
click\_button\_2 - по клику на Viber\
click\_button\_3 - по клику на FaceBook\*\
click\_button\_6 - по клику на WhatsApp\*\
click\_button\_8 - по клику на Одноклассники\
click\_button\_10 - по клику на Instagram\*

{% hint style="danger" %}
\*Facebook, WhatsApp, Instagram принадлежат Meta platform Inc., деятельность которой признана в РФ экстремистской и запрещена.
{% endhint %}

Сам идентификатор может быть любой. Главное, чтобы в конце было нижнее подчеркивание. К нему будет добавлен индекс мессенджера.

Пример правильно заполненных полей в настройках  сайта и правильно созданных целей в Яндекс Метрике:

<div data-with-frame="true"><figure><img src="../../.gitbook/assets/Снимок экрана 2026-03-20 в 14.03.15.png" alt=""><figcaption></figcaption></figure></div>

<div data-with-frame="true"><img src="https://lh4.googleusercontent.com/mdyucwGzQQcQvxBhQo2iYZQ431GRGDrecFFllaBu4vZQ-QVe6C8MrJfOKQ2AlrijVBNBn5OhYMM9MFXm67n2rPiFqjfszg2mQYrB-77vejCr2JAJLEzbxFA4vYP32wDvdwR_qRM7" alt=""></div>

<div data-with-frame="true"><img src="https://lh3.googleusercontent.com/KThH5z_I7demPYAwyOug67yG20F12JKDPx_XyWUMDS36xITmniRDzkAdznoX-A49FHKMQTAVKs-OHhKlcJf8ibx-n8ZsLbC5V1HSpD6Brv9-t15Kwggz-IhrXZZ3EbxAoJMaDQrf" alt=""></div>

<div data-with-frame="true"><img src="https://lh6.googleusercontent.com/kcDY5g0BPI4mMeLmQ7MF3Z-0mBdJbI5T6vh0e03Oo7y7ggVdIVm3PIK0hWsxPVbo3A8bdf1AUz2dE5e-QhywYD6BGJKgh5goOxuX4K-dUDiwfSREYNty9Ixd-qgP7po42WyQF6g2" alt=""></div>

### Яндекс Метрика - оффлайн конверсии

### Как создать счетчик Яндекс.Метрики?

Для начала сбора оффлайн конверсий в Яндекс.Метрику с Salebot необходимо зарегистрировать Яндекс.Метрику.

**1.** **Если у Вас нет аккаунта Яндекс.Метрики**, следует войти в ваш аккаунт Яндекс почты (или зарегистрировать новый). Далее перейти в[ Яндекс.Метрику](https://metrika.yandex.ru/list?) и нажать добавить счетчик. В настройках счетчика указать следующие данные:

1. Имя счетчика
2. Адрес сайта - в примере ссылка на сайт Salebot (и далее пример будет построен на нем).
3. Автоматические цели и Вебвизор, карта скроллинга и аналитика форм - рекомендуем включить обе галочки для сбора большего количества информации.

<div data-with-frame="true"><figure><img src="../../.gitbook/assets/image (47) (1) (1).png" alt=""><figcaption></figcaption></figure></div>

После заполнения страницы жмем “Создать счетчик”. На открывшейся странице выбираете html-код и копируете весь код, появившийся внизу. Настройки для “Контентной аналитики” и “Электронной коммерции” устанавливайте на свое усмотрение, если они Вам необходимы. Копируем код и вставляем на сайт (см. чуть ниже). Затем нажимаем кнопку “Начать пользоваться”.

<div data-with-frame="true"><figure><img src="../../.gitbook/assets/image (48) (2).png" alt=""><figcaption></figcaption></figure></div>

В настройках сайта, добавьте код во вкладке “Настройки” - “CSS и JS” - HTML-код head(или HTML-код body) и сохранить.

<div data-with-frame="true"><figure><img src="../../.gitbook/assets/image (49) (1) (1).png" alt=""><figcaption><p>Открыть Настройки</p></figcaption></figure></div>

<div data-with-frame="true"><figure><img src="../../.gitbook/assets/image (50) (1) (1).png" alt=""><figcaption><p>Перейти в раздел CSS и JS</p></figcaption></figure></div>

Далее нажмите "Сохранить".

Перейдите в меню Метрики, где видим список созданных счетчиков. Забираем номер счетчика и записываем его  в переменную проекта ym\_counter\_id (настройки проекта - константы проекта)

<div data-with-frame="true"><figure><img src="../../.gitbook/assets/image (51) (1) (1).png" alt=""><figcaption></figcaption></figure></div>

<div data-with-frame="true"><figure><img src="../../.gitbook/assets/image (52) (1) (1).png" alt=""><figcaption></figcaption></figure></div>

**2. Если у Вас есть аккаунт в Яндекс Метрике**, то следует зайти в счетчик, по которому Вы хотите собирать статистику и записать его номер в переменную проекта ym\_counter\_id (настройки проекта - константы проекта). Настраивать счетчик заново Вам не нужно, просто вносим переменную как показано на скриншоте выше и переходим сразу к следующему пункту.&#x20;

В созданном счетчике следует перейти в настройки - загрузка данных и включить передачу оффлайн конверсий.

<div data-with-frame="true"><figure><img src="../../.gitbook/assets/image (53) (1) (1).png" alt=""><figcaption></figcaption></figure></div>

Далее выйдет уведомление о том, что учет оффлайн конверсий станет доступен в течение суток. Следует помнить, что на данный момент обработка запросов может занимать до 24 часов и появится в статистике метрики лишь на следующие сутки. Сбор информации по цели доступен в течение 21 дней, далее данные будут затираться.

<div data-with-frame="true"><figure><img src="../../.gitbook/assets/image (54) (1) (1).png" alt=""><figcaption></figcaption></figure></div>

РЕГИСТРИРУЕМ ПРИЛОЖЕНИЕ ЯНДЕКСА И ПОЛУЧАЕМ ТОКЕН АВТОРИЗАЦИИ ДЛЯ ПОДКЛЮЧЕНИЯ API ЯНДЕКС.МЕТРИКИ К SALEBOT

Ссылка на документацию API Яндекс.Метрики, в которой описан Вызов API Яндекс.Метрики из браузера [https://yandex.ru/dev/metrika/doc/api2/intro/browser.html](https://yandex.ru/dev/metrika/doc/api2/intro/browser.html)

Для работы с API из браузера необходимо использовать [авторизационный токен](http://api.yandex.ru/oauth/doc/dg/concepts/authorization-scheme.xml). Чтобы получить токен:

1. [Создайте приложение](https://oauth.yandex.ru/client/new), при этом заполните поля:
   * название — можно указать произвольно;
   * иконка сервиса — необязательно;
   * платформы приложения — выберите веб-сервисы;
   * redirect URI — укажите https://oauth.yandex.ru/verification\_code;
   * доступ к данным — **укажите metrika:read и metrika:write.**
2. Нажмите Создать приложение и скопируйте его ClientID (напротив идентификатора нажмите значок ![](https://yastatic.net/s3/doc-binary/freeze/f5obaUMTmSVBtiqmZn0Jz-ZnL8s.png)).
3.  Добавьте скопированный ClientID в ссылку вида

    ```
    https://oauth.yandex.ru/authorize?response_type=token&client_id=<идентификатор приложения>
    ```
4. Перейдите по ссылке и на открывшейся странице скопируйте ваш авторизационный токен.

<mark style="color:green;background-color:green;">1) Регистрируем приложение Яндекса</mark>&#x20;

Для получения данных для связи Яндекс Метрики с Salebot необходимо зарегистрировать [приложение](https://oauth.yandex.ru/client/new) (по ссылке https://oauth.yandex.ru/client/new)

При переходе по ссылке откроется страница:

<div data-with-frame="true"><figure><img src="../../.gitbook/assets/image (55) (1) (1).png" alt=""><figcaption></figcaption></figure></div>

Далее заполняем данную форму:

<div data-with-frame="true"><figure><img src="../../.gitbook/assets/image (56) (1) (1).png" alt="" width="563"><figcaption></figcaption></figure></div>

1. Введите имя приложения. При желании добавьте иконку.
2. В подпункте “Платформы приложения” выберите веб-сервисы. Укажите `https://oauth.yandex.ru/verification_code`&#x20;

3\. В подпункте “Доступ к данным” выберите поочередно `metrika:read` и `metrika:write`

{% hint style="warning" %}
**ПРИМЕЧАНИЕ**

Вы можете по своему усмотрению подключить и другие сервисы для приложения, если собираетесь использовать его где-то еще, однако стоит иметь ввиду, что часть пунктов сокращают жизнь токена авторизации до полугода, а то и до 7 дней
{% endhint %}

<div data-with-frame="true"><figure><img src="../../.gitbook/assets/image (57) (1) (1).png" alt="" width="561"><figcaption><p>сокращает жизнь токена до 7 дней</p></figcaption></figure></div>

<div data-with-frame="true"><figure><img src="../../.gitbook/assets/image (58) (1) (1).png" alt="" width="562"><figcaption><p>сокращает с года до 180 дней</p></figcaption></figure></div>

После нажатия на кнопку Создать приложение будет переход на следующую страницу:

<div data-with-frame="true"><figure><img src="../../.gitbook/assets/image (59) (1) (1).png" alt=""><figcaption></figcaption></figure></div>

Вы получаете данные для получения авторизационного токена для связи с API Salebot - ClientID. (в примере 04cb02016fa54163a9e14b5bb6e\*\*\*\*\*). Скопируйте его.

<mark style="color:green;">2)</mark> <mark style="background-color:green;">Получение токена авторизации</mark>

Для получения токена авторизации следует перейти по ссылке вида `https://oauth.yandex.ru/authorize?response_type=token&client_id={clientID}`

где {clientID} в ссылке замените на значение ClientID скопированный в шаге выше

В нашем случае, токен будет располагаться по ссылке "https://oauth.yandex.ru/authorize?response\_type=token\&client\_id=04cb02016fa54163a9e14b5bb\*\*\*\*\*\*"\
Перейдя по ней, вы увидите окно авторизации в приложение, и, подтвердив вход, получите окно с токеном. Сохраните его в переменные проекта(настройки проекта - константы проекта).&#x20;

<div data-with-frame="true"><figure><img src="../../.gitbook/assets/image (60) (1) (1).png" alt=""><figcaption></figcaption></figure></div>

<div data-with-frame="true"><figure><img src="../../.gitbook/assets/image (61) (1) (1).png" alt=""><figcaption></figcaption></figure></div>

<div data-with-frame="true"><figure><img src="../../.gitbook/assets/image (62) (1) (1).png" alt=""><figcaption></figcaption></figure></div>

{% hint style="warning" %}
**ВАЖНО!**

Время жизни токена - год или меньше: зависит от настроек приложения. Через год необходимо будет заново перепройти по той же ссылке и сохранить новый токен авторизации на новый год.&#x20;

Если при выполнении функций по связи с метрикой, Вы получите уведомление системы по типу “Expired or wrong token. Please, check or refresh your ym\_oath\_token”, повторите действия из этого пункта и замените токен.&#x20;
{% endhint %}

Проверяем в настройках проекта все внесенные данные. Все готово, приступаем к настройке Целей.

### Настройка целей

Итак, вы создали счетчик метрики.

<div data-with-frame="true"><figure><img src="../../.gitbook/assets/image (63) (1) (1).png" alt=""><figcaption></figcaption></figure></div>

<mark style="color:orange;">**1.Ручное создание цели в Яндекс. Метрике**</mark>&#x20;

Нажимаем создать цель - добавить цель.&#x20;

<div data-with-frame="true"><figure><img src="../../.gitbook/assets/image (64) (1) (1).png" alt=""><figcaption></figcaption></figure></div>

В меню настройки целей:

1. задаем название цели - например, старт разговора с ботом.
2. Выбираем тип **JavaScript-событие**.&#x20;

{% hint style="warning" %}
<mark style="color:red;">**ВНИМАНИЕ!!!**</mark> Сбор оффлайн-конверсий Яндекса работает только с этим типом целей. Оффлайн сбор информации по другим целям работать не будет!
{% endhint %}

&#x20;3\. Устанавливаем идентификатор цели - <mark style="color:green;">**любое значение(цифры)**</mark> - и ставим маркер на “совпадает”.&#x20;

В примере идентификатором цели является число 666, этот идентификатор понадобится нам в будущем как переменная ym\_js\_event\_id.

4\. По желанию, Вы можете указать доход с цели&#x20;

<div data-with-frame="true"><figure><img src="../../.gitbook/assets/image (65) (1) (1).png" alt=""><figcaption></figcaption></figure></div>

Нажимаем “добавить цель”.

<mark style="color:orange;">**2.Создание НОВОЙ цели через функцию в Salebot**</mark>

{% hint style="warning" %}
Функция (API в калькуляторе) для создания новой цели **ym\_create\_js\_event\_goal()** работает только <mark style="color:green;">на тарифе Премиум</mark>!
{% endhint %}

В Salebot есть функция создания цели типа JS-событие, \
**ym\_create\_js\_event\_goal(name,price, oauth\_token,counter\_id)**, где \
\
Обязательный параметр:\
<mark style="color:red;">**!**</mark>**&#x20;name** - это имя цели, обязательный параметр, строка \
\
Необязательные параметры:\
**price** - стоимость цели, необязательный параметр, число&#x20;

_<mark style="color:blue;">**Если у вас 2 и более аккаунта нужно передавать данные в параметрах:**</mark>_

**oauth\_token** - токен авторизации&#x20;

**counter\_id** - номер счетчика

{% hint style="danger" %}
**Обращаем внимание!**

**oauth\_token** и **counter\_id**  в параметрах функции **приоритетнее** тех, что указаны в настройках проекта.&#x20;
{% endhint %}

Пример: \
Создадим две цели, одна(‘Haos goal’) - со стоимостью, другая(‘Free goal’) без нее

<figure><img src="../../.gitbook/assets/image (66) (1) (1).png" alt=""><figcaption></figcaption></figure>

Результатом выполнения будет список, состоящий из номера цели (ym\_goal\_id), ее имени (ym\_goal\_name) и идентификатора отслеживания события (ym\_js\_event\_id). В переменных также можно найти этот список с характеристиками целей. А в Яндекс Метрике появятся заявленные цели:

<div data-with-frame="true"><figure><img src="../../.gitbook/assets/image (67) (1) (1).png" alt=""><figcaption></figcaption></figure></div>

<div data-with-frame="true"><figure><img src="../../.gitbook/assets/image (68) (2).png" alt="" width="336"><figcaption></figcaption></figure></div>

<div data-with-frame="true"><figure><img src="../../.gitbook/assets/image (69) (2).png" alt=""><figcaption></figcaption></figure></div>

**Дополнительно. Вывод информации обо всех целях в Salebot** \
Если Вы запамятовали данные о своих целях в Яндекс Метрике и хотите вывести их все в переменную в Salebot, воспользуйтесь функцией \
**ym\_info\_about\_goals(ym\_goal\_id, oauth\_token, counter\_id)**, где&#x20;

1. **ym\_goal\_id** - необязательный параметр. &#x20;

&#x20;Если параметр указан, то информация подгрузится о конкретной цели с данным идентификатором.

Если вы не хотите указывать данный параметр, то вместо него пропишите <mark style="color:red;">**"None"**</mark> (в кавычках!).

_<mark style="color:blue;">**Если у вас 2 и более аккаунта нужно передавать данные в параметрах:**</mark>_

2. **oauth\_token** - токен авторизации&#x20;
3. **counter\_id** - номер счетчика

{% hint style="danger" %}
Обращаем внимание!

**oauth\_token** и **counter\_id**  в параметрах функции  **приоритетнее** тех, что указаны в настройках проекта.&#x20;
{% endhint %}

Пример:

<figure><img src="../../.gitbook/assets/image (70) (1) (1).png" alt=""><figcaption></figcaption></figure>

Ответом является список, состоящий из словарей с goal\_id, name, js\_event\_id всех целей. Если цель не является JS-событием, то js\_event\_id будет содержать ссылку/указание на соц. сеть/другой идентификатор. Если указать их при выгрузке конверсий, система Яндекс Метрики их просто не зачтет и вернет ошибку.

<div data-with-frame="true"><figure><img src="../../.gitbook/assets/image (71) (1) (1).png" alt=""><figcaption></figcaption></figure></div>

Информация об одной конкретной цели содержит словарь с данными.

<div data-with-frame="true"><figure><img src="../../.gitbook/assets/image (72) (1) (1).png" alt=""><figcaption></figcaption></figure></div>

### Отправка оффлайн конверсий в Яндекс метрику

Функция (API в калькуляторе) для передачи офлайн-конверсий из бота  **ym\_send\_offline\_conversions()**

Для того чтобы отправить данные в Яндекс Метрики, следует использовать функцию **ym\_send\_offline\_conversions(js\_event\_id, client\_id\_type, time\_delta, oauth\_token, counter\_id, comment** **)**, где:&#x20;

<table><thead><tr><th width="328.75390625">Параметр</th><th>Описание</th></tr></thead><tbody><tr><td><mark style="color:red;"><strong>!</strong></mark> <strong>ym_js_event_id</strong></td><td>идентификатор отслеживания события, <strong>обязательный параметр</strong>, число. </td></tr><tr><td><strong>client_id_type</strong></td><td>позволяет использовать по выбору yclid или _ym_uid для идентификации пользователя. Для использования yclid в этом параметре передайте 'yclid', во всех иных случаях будет отрабатывать как раньше</td></tr><tr><td><strong>time_delta</strong></td><td>количество секунд, что необходимо вычесть из времени в которое выполняется функция. Чаще всего не требуется, но в редких случаях может помочь решить вопрос с конверсией, что пришла в "неподходящее" время. Подбирать параметр рекомендуется, начиная с 5.</td></tr><tr><td><em><mark style="color:blue;"><strong>Если у вас 2 и более аккаунта нужно передавать данные в параметрах:</strong></mark></em></td><td></td></tr><tr><td><ol><li><strong>oauth_token</strong></li></ol></td><td>токен авторизации </td></tr><tr><td><ol start="2"><li><strong>counter_id</strong> </li></ol></td><td>номер счетчика</td></tr><tr><td>comment </td><td>необязательный параметр, комментарий. Максимальная длина — 255 символов. Допустимы цифры, латинские и кириллические буквы</td></tr></tbody></table>

{% hint style="warning" %}
**Важно!**

**oauth\_token** и **counter\_id**  в параметрах функции  **приоритетнее** тех, что указаны в настройках проекта.&#x20;
{% endhint %}

{% hint style="warning" %}
**ВАЖНО!**

Отправка оффлайн-конверсий происходит по идентификатору клиента Яндекс. Если у клиента в переменных есть метка \_ym\_uid (как включить сбор меток в минилендингах смотрите в соответствующем разделе), он автоматически подставится в этот параметр и передаст статистику по данному клиенту.&#x20;

С момента запуска бота до передачи офлайн-конверсии должно пройти достаточно времени для передачи метки \_ym\_uid в Метрику, например, от 5-10 минут. &#x20;
{% endhint %}

<div data-with-frame="true"><figure><img src="../../.gitbook/assets/Снимок экрана 2025-05-14 в 17.01.56.png" alt="" width="563"><figcaption></figcaption></figure></div>

\_ym\_uid - это clientID посетителя, присваиваемый Яндексом каждому пользователю. Он является уникальным и задается только системой Яндекс. Поэтому, если у клиента нет параметра, статистика по нему передаваться не будет. Однако, если у Вас есть данные о метке посетителя, Вы можете добавить клиенту переменную ya\_client\_id, и, если такой посетитель существует, статистика передастся.&#x20;

{% hint style="info" %}
Если клиента с номером, указанным в ya\_client\_id, не существует, то и статистика собираться не будет&#x20;
{% endhint %}

<div data-with-frame="true"><figure><img src="../../.gitbook/assets/image (73) (1) (1).png" alt=""><figcaption></figcaption></figure></div>

Пример:\
Представим, у нас есть цели “Старт чата с ботом” и “клик по кнопке хорошо”&#x20;

<div data-with-frame="true"><figure><img src="../../.gitbook/assets/image (74) (1) (1).png" alt=""><figcaption></figcaption></figure></div>

В боте у нас создан стартовый блок с приветствием и предложением нажать на две кнопки, нажатие на одну из которых(“хорошо”) приведет нас во второй блок с поздравлением.

<div data-with-frame="true"><figure><img src="../../.gitbook/assets/image (75) (1) (1).png" alt=""><figcaption></figcaption></figure></div>

Впишем в калькулятор функцию **ym\_send\_offline\_conversions("666")**, где \
666 - идентификатор(ym\_js\_event\_id) цели “Старт чата с ботом”.

В блоке ниже, куда пользователь попадет при нажатии клавиши “Хорошо”, мы поставим ту же функцию с идентификатором второй цели - “клик по кнопке хорошо”.

<div data-with-frame="true"><figure><img src="../../.gitbook/assets/image (76) (1) (1).png" alt=""><figcaption></figcaption></figure></div>

Если посетитель с меткой \_ym\_uid прошел по этим этапам, статистика соберется и отправится в Яндекс Метрику, где потом будет обработана. Статус обработки до появления информации в статистике можно посмотреть в счетчике - настройки -загрузка данных.

<div data-with-frame="true"><figure><img src="../../.gitbook/assets/image (77) (1) (1).png" alt=""><figcaption></figcaption></figure></div>

{% hint style="warning" %}
**Внимание!**

Обработка может длиться до 24 часов! По итогу, при успешной загрузке появится значок “Выполнено”, при неуспешной - красная надпись. Это означает, что Яндекс Метрика не обнаружила клиента по заданному \_ym\_uid в своей системе.
{% endhint %}

<div data-with-frame="true"><figure><img src="../../.gitbook/assets/image (78) (1) (1).png" alt=""><figcaption></figcaption></figure></div>

{% hint style="warning" %}
**Внимание!**

Иногда системы Яндекса сбоят, и засчитывают загрузку на второй день после ее отправки, поэтому ошибочные загрузки могут выполниться через сутки после появления красной надписи, что увеличивает суммарное время обработки загрузок ДО 48 ЧАСОВ. Возможно, в будущем Яндекс починят свои лаги, но пока что следует учитывать их ошибки.
{% endhint %}

Если офлайн конверсии подключены меньше суток, то в ответ на запрос придет ошибка с указанием даты, когда данные могут быть загружены:

<div data-with-frame="true"><figure><img src="../../.gitbook/assets/image (79) (1) (1).png" alt=""><figcaption></figcaption></figure></div>

А в Метрике вы увидите ошибку:

<div data-with-frame="true"><figure><img src="../../.gitbook/assets/image (80) (1) (1).png" alt=""><figcaption></figcaption></figure></div>
