# Яндекс.Метрика для сайта

К сайту, созданному в Salebot, можно подключить Яндекс.Метрику. Для этого создайте счётчик в Яндекс.Метрике, создайте цель и укажите данные в настройках сайта:

<div data-with-frame="true"><figure><img src="../../.gitbook/assets/image (463).png" alt=""><figcaption></figcaption></figure></div>

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

<div align="center" data-with-frame="true"><figure><img src="../../.gitbook/assets/image (464).png" alt=""><figcaption><p>Настройки в Яндекс.Метрике</p></figcaption></figure></div>

## Как подключить Яндекс Метрику

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
click\_button\_10 - по клику на Instagram\*\
click\_button\_20 - по клику на MAX

{% hint style="danger" %}
\*Facebook, WhatsApp, Instagram принадлежат Meta platform Inc., деятельность которой признана в РФ экстремистской и запрещена.
{% endhint %}

Сам идентификатор может быть любой. Главное, чтобы в конце было нижнее подчеркивание. К нему будет добавлен индекс мессенджера.

Пример правильно заполненных полей в настройках  сайта и правильно созданных целей в Яндекс Метрике:

<div data-with-frame="true"><figure><img src="../../.gitbook/assets/Снимок экрана 2026-03-20 в 14.03.15.png" alt=""><figcaption></figcaption></figure></div>

<div data-with-frame="true"><img src="https://lh4.googleusercontent.com/mdyucwGzQQcQvxBhQo2iYZQ431GRGDrecFFllaBu4vZQ-QVe6C8MrJfOKQ2AlrijVBNBn5OhYMM9MFXm67n2rPiFqjfszg2mQYrB-77vejCr2JAJLEzbxFA4vYP32wDvdwR_qRM7" alt=""></div>

<div data-with-frame="true"><img src="https://lh3.googleusercontent.com/KThH5z_I7demPYAwyOug67yG20F12JKDPx_XyWUMDS36xITmniRDzkAdznoX-A49FHKMQTAVKs-OHhKlcJf8ibx-n8ZsLbC5V1HSpD6Brv9-t15Kwggz-IhrXZZ3EbxAoJMaDQrf" alt=""></div>

<div data-with-frame="true"><img src="https://lh6.googleusercontent.com/kcDY5g0BPI4mMeLmQ7MF3Z-0mBdJbI5T6vh0e03Oo7y7ggVdIVm3PIK0hWsxPVbo3A8bdf1AUz2dE5e-QhywYD6BGJKgh5goOxuX4K-dUDiwfSREYNty9Ixd-qgP7po42WyQF6g2" alt=""></div>

## Яндекс Метрика - оффлайн конверсии

### Как создать счетчик Яндекс.Метрики?

Для начала сбора оффлайн конверсий в Яндекс.Метрику с Salebot необходимо зарегистрировать Яндекс.Метрику.

**1.** **Если у Вас нет аккаунта Яндекс.Метрики**, следует войти в ваш аккаунт Яндекс почты (или зарегистрировать новый). Далее перейти в[ Яндекс.Метрику](https://metrika.yandex.ru/list?) и нажать добавить счетчик. В настройках счетчика указать следующие данные:

1. Имя счетчика
2. Адрес сайта - в примере ссылка на сайт Salebot (и далее пример будет построен на нем).
3. Автоматические цели и Вебвизор, карта скроллинга и аналитика форм - рекомендуем включить обе галочки для сбора большего количества информации.

<div data-with-frame="true"><figure><img src="../../.gitbook/assets/image (466).png" alt=""><figcaption></figcaption></figure></div>

После заполнения страницы жмем “Создать счетчик”. На открывшейся странице выбираете html-код и копируете весь код, появившийся внизу. Настройки для “Контентной аналитики” и “Электронной коммерции” устанавливайте на свое усмотрение, если они Вам необходимы. Копируем код и вставляем на сайт (см. чуть ниже). Затем нажимаем кнопку “Начать пользоваться”.

<div data-with-frame="true"><figure><img src="../../.gitbook/assets/image (467).png" alt=""><figcaption></figcaption></figure></div>

В настройках сайта, добавьте код во вкладке “Настройки” - “CSS и JS” - HTML-код head(или HTML-код body) и сохранить.

<div data-with-frame="true"><figure><img src="../../.gitbook/assets/image (468).png" alt=""><figcaption><p>Открыть Настройки</p></figcaption></figure></div>

<div data-with-frame="true"><figure><img src="../../.gitbook/assets/image (469).png" alt=""><figcaption><p>Перейти в раздел CSS и JS</p></figcaption></figure></div>

Далее нажмите "Сохранить".

Перейдите в меню Метрики, где видим список созданных счетчиков. Забираем номер счетчика и записываем его  в переменную проекта ym\_counter\_id (настройки проекта - константы проекта)

<div data-with-frame="true"><figure><img src="../../.gitbook/assets/image (470).png" alt=""><figcaption></figcaption></figure></div>

<div data-with-frame="true"><figure><img src="../../.gitbook/assets/image (471).png" alt=""><figcaption></figcaption></figure></div>

**2. Если у Вас есть аккаунт в Яндекс Метрике**, то следует зайти в счетчик, по которому Вы хотите собирать статистику и записать его номер в переменную проекта ym\_counter\_id (настройки проекта - константы проекта). Настраивать счетчик заново Вам не нужно, просто вносим переменную как показано на скриншоте выше и переходим сразу к следующему пункту.&#x20;

Проверяем в настройках проекта все внесенные данные. Все готово, приступаем к настройке Целей.

### Настройка целей

Итак, вы создали счетчик метрики.

<div data-with-frame="true"><figure><img src="../../.gitbook/assets/image (482).png" alt=""><figcaption></figcaption></figure></div>

<mark style="color:orange;">**1.Ручное создание цели в Яндекс. Метрике**</mark>&#x20;

Нажимаем создать цель - добавить цель.&#x20;

<div data-with-frame="true"><figure><img src="../../.gitbook/assets/image (483).png" alt=""><figcaption></figcaption></figure></div>

В меню настройки целей:

1. задаем название цели - например, старт разговора с ботом.
2. Выбираем тип **JavaScript-событие**.&#x20;

{% hint style="warning" %}
<mark style="color:red;">**ВНИМАНИЕ!!!**</mark> Сбор оффлайн-конверсий Яндекса работает только с этим типом целей. Оффлайн сбор информации по другим целям работать не будет!
{% endhint %}

&#x20;3\. Устанавливаем идентификатор цели - <mark style="color:green;">**любое значение(цифры)**</mark> - и ставим маркер на “совпадает”.&#x20;

В примере идентификатором цели является число 666, этот идентификатор понадобится нам в будущем как переменная ym\_js\_event\_id.

4\. По желанию, Вы можете указать доход с цели&#x20;

<div data-with-frame="true"><figure><img src="../../.gitbook/assets/image (484).png" alt=""><figcaption></figcaption></figure></div>

Нажимаем “добавить цель”.

## Как передать данные в Яндекс.Метрику?

{% hint style="warning" %}
**ВАЖНО!**

Отправка оффлайн-конверсий происходит по идентификатору клиента Яндекс. Если у клиента в переменных есть метка \_ym\_uid ([как включить сбор меток в минилендингах смотрите в соответствующем разделе](../../websites/builder/analitika-saita.md)), он автоматически подставится в этот параметр и передаст статистику по данному клиенту.&#x20;

С момента запуска бота до передачи офлайн-конверсии должно пройти достаточно времени для передачи метки \_ym\_uid в Метрику, например, от 5-10 минут. &#x20;
{% endhint %}

<div data-with-frame="true"><figure><img src="../../.gitbook/assets/Снимок экрана 2025-05-14 в 17.01.56.png" alt="" width="563"><figcaption></figcaption></figure></div>

\_ym\_uid - это clientID посетителя, присваиваемый Яндексом каждому пользователю. Он является уникальным и задается только системой Яндекс. Поэтому, если у клиента нет параметра, статистика по нему передаваться не будет. Однако, если у Вас есть данные о метке посетителя, Вы можете добавить клиенту переменную ya\_client\_id, и, если такой посетитель существует, статистика передастся.&#x20;

{% hint style="info" %}
Если клиента с номером, указанным в ya\_client\_id, не существует, то и статистика собираться не будет&#x20;
{% endhint %}

<div data-with-frame="true"><figure><img src="../../.gitbook/assets/image (492).png" alt=""><figcaption></figcaption></figure></div>

Если посетитель с меткой \_ym\_uid прошел по этапам, статистика соберется и отправится в Яндекс Метрику, где потом будет обработана. Статус обработки до появления информации в статистике можно посмотреть в счетчике - настройки -загрузка данных.

<div data-with-frame="true"><figure><img src="../../.gitbook/assets/image (496).png" alt=""><figcaption></figcaption></figure></div>

{% hint style="warning" %}
**Внимание!**

Обработка может длиться до 24 часов! По итогу, при успешной загрузке появится значок “Выполнено”, при неуспешной - красная надпись. Это означает, что Яндекс Метрика не обнаружила клиента по заданному \_ym\_uid в своей системе.
{% endhint %}

Для работы с  функцией нам понадобится токен: для этого нужно перейти в кабинет Метрики в Яндексе:

<div data-with-frame="true"><figure><img src="../../.gitbook/assets/unknown.png" alt="" width="545"><figcaption></figcaption></figure></div>

<div data-with-frame="true"><figure><img src="../../.gitbook/assets/unknown (1).png" alt="" width="563"><figcaption></figcaption></figure></div>

<div data-with-frame="true"><figure><img src="../../.gitbook/assets/unknown (2).png" alt="" width="563"><figcaption></figcaption></figure></div>

Включаем "Measurement Protocol" и копируем токен. Его нужно сохранить в переменную проекта ym\_measurement\_token.

### Функция для передачи данных в Яндекс.метрику

ym\_event(event, client\_id\_type, page\_url, counter\_id, measurement\_token) - передача данных в Яндекс метрику

параметры:

<table><thead><tr><th width="267.3515625">Параметры</th><th>Описание</th></tr></thead><tbody><tr><td><mark style="color:$danger;"><strong>!</strong></mark> event </td><td>событие, которое нужно отправить в аналитику (идентификатор цели). Обязательный параметр</td></tr><tr><td>client_id_type</td><td>позволяет использовать по выбору yclid или _ym_uid для идентификации пользователя. Для использования yclid в этом параметре передайте 'yclid', во всех иных случаях будет отрабатывать как раньше. Необязательный параметр</td></tr><tr><td>page_url</td><td>адрес сайта. Параметр обязательный, если в настройках счетчика включена функция "Принимать данные только с указанных адресов".</td></tr><tr><td>counter_id</td><td>номер счетчика. Нужно указать, если в проекте ведется работа с несколькими счетчиками. Если не передан, будет взят из переменной проекта ym_counter_id</td></tr><tr><td>measurement_token</td><td>Секретный токен, генерируется при включении опции Measurement Protocol. Нужно указать, если в проекте ведется работа с несколькими счетчиками. Если не передан, будет взят из переменной проекта ym_measurement_token</td></tr></tbody></table>

{% hint style="warning" %}
Важно!

measurement\_token и counter\_id  в параметрах функции  приоритетнее тех, что указаны в настройках проекта.
{% endhint %}

## Как отследить события по заявкам и переходам в бота с сайта?

Теперь вы можете отследить события по заявкам и(или) переходам в бота с сайта.

Для этого вам нужно перейти в настройки сайта, в котором создана форма отправки заявки или с кнопками на мессенджеры:

<div data-with-frame="true"><figure><img src="../../.gitbook/assets/Снимок экрана 2026-04-09 в 16.00.31.png" alt=""><figcaption></figcaption></figure></div>

Далее наведите на блок "Форма" и найдите кнопку "Настройки":

<div data-with-frame="true"><figure><img src="../../.gitbook/assets/Снимок экрана 2026-04-09 в 16.01.49.png" alt=""><figcaption></figcaption></figure></div>

Раскройте настройки кнопок:

<div data-with-frame="true"><figure><img src="../../.gitbook/assets/Снимок экрана 2026-04-09 в 16.02.33.png" alt=""><figcaption></figcaption></figure></div>

Здесь вы увидите поле, где нужно вставить название события, настроенное в Яндекс Метрике:

<div data-with-frame="true"><figure><img src="../../.gitbook/assets/Снимок экрана 2026-04-09 в 16.03.36.png" alt="" width="563"><figcaption></figcaption></figure></div>

Чтобы отправка событий работала, [нужно вставить скрипт счетчика Метрики на сайт](yandeks.metrika-dlya-saita.md#kak-sozdat-schetchik-yandeks.metriki).

Аналогично можно проставить название событий для каждой кнопки мессенджера.

<div data-with-frame="true"><figure><img src="../../.gitbook/assets/Снимок экрана 2026-04-09 в 16.06.55.png" alt=""><figcaption></figcaption></figure></div>

<div data-with-frame="true"><figure><img src="../../.gitbook/assets/Снимок экрана 2026-04-09 в 16.07.28.png" alt=""><figcaption></figcaption></figure></div>

<div data-with-frame="true"><figure><img src="../../.gitbook/assets/Снимок экрана 2026-04-09 в 16.07.47.png" alt="" width="375"><figcaption></figcaption></figure></div>
