# Facebook\* Pixel

{% hint style="danger" %}
<mark style="color:red;">\*</mark>На территории Российской Федерации запрещена деятельность социальных сетей Facebook и Instagram, принадлежащих компании Meta Platforms Inc., признанная экстремистской!
{% endhint %}

## Как установить пиксель Facebook<mark style="color:red;">\*</mark>

## **Как отправить события в пиксель из бота**

Для передачи событий из воронки бота, нужно иметь бизнес аккаунт. Зарегистрировать можно [по ссылке](https://business.facebook.com/).

### Как создать новый пиксель

<div data-with-frame="true"><img src="https://lh4.googleusercontent.com/lD00d_Yd31buyVUtc7ZgPjj-NT2oeFOQS4XjBX2xyGVESzweGAzIb5yfPsdRk90I3XQZNO9U_No5vLIRjItyEzA9CaqNGV2heh-NMvJCUuPN6XHyHi15z6St6X7siadzY9lpfmmt" alt=""></div>

Выбираем API Conversions

<div data-with-frame="true"><img src="https://lh3.googleusercontent.com/a1OQ0peFICKvw3LFgOtVjtOh9cBakTZu7gXmB9-UcUn_0WqCBRxOiyC1qszWD0xDsPWr7I5nR0TO_AJEJbKJX6SGiCcFElcySdsaqz3YmYS9MZTRagDk8tNlB14E6IF8fEWEEhm1" alt=""></div>

{% hint style="danger" %}
**Внимание!** Если на этапе создания настройки conversion api у вас появится следующее окно, следует выйти из настройки и начать занов&#x43E;**.**
{% endhint %}

<div data-with-frame="true"><img src="https://lh6.googleusercontent.com/8wrVR4FZR2yJSKxmYJmR9uJ3vPcUkgGvuuScEa93kDmaTZWuqWmCV0x2xdtrFZmyVCqjShqrXgNud9U8B5UpI5G-aEIiWzo8hAaBWVSWNFu9oeYiMIWD1Uqi5-XzPe4ZaQA1Kmhn" alt="Если у вас появится следующее окно, следует выйти из настройки и начать заново."></div>

Выбираем нужный пиксель

<div data-with-frame="true"><img src="https://lh3.googleusercontent.com/QIjmsqi4ZjGXuqRV9_UhZCL7uf1y6XFvvOHn9ru9zNlYs73tMW3svCWYjG6l0tlvSG9aFFMFo8wZOilDJAvO5UvpmXgPU9qBY65W5c1nMThsdnS3qfzBTfX1PR0PdLCB9gX3h7aZ" alt=""></div>

Генерируем маркер доступа (токен) и сохраняем в надежном месте.

<div data-with-frame="true"><img src="https://lh4.googleusercontent.com/Qt2ChkjK9A8j4LAhpZ-N42TpRoyZl20GI9g_6H2uBzRzLp1CsXySZiovveiHZHBIQGMM9wS54G6zJg5T5v4mz8OuNf4ZkZCcfhJcsqUZQk6NOu9ieyOhS-vA0BBegVucNs2t2759" alt=""></div>

## Как передать события

{% hint style="danger" %}
<mark style="color:red;">\*</mark>**На территории Российской Федерации&#x20;**<mark style="color:red;">**запрещена деятельность**</mark>**&#x20;социальных сетей&#x20;**<mark style="color:red;">**Facebook**</mark>**&#x20;и&#x20;**<mark style="color:red;">**Instagram**</mark>**, принадлежащих компании Meta Platforms Inc**., признанные экстремистскими!
{% endhint %}

Для передачи события в фейсбук у вас на сайте должен быть установлен свой домен, подтвержденный в фейсбук и в настройках сайта включено сохранение значений из куки для фейсбук.

Теперь клиенту, который перешел с сайта автоматически запишется переменная: \_fbp, которую нужно передать в пиксель вместе с событием.

<div data-with-frame="true"><img src="https://lh3.googleusercontent.com/dfduauw9O5LuwAURGcJ2Ax5I-L9eztzMcyOQp4QB2ZKQzy3SHi-ThwJcwSrgqOzFWOIH4coMcmsyrQh4Dog0Vu_mnwfgOGs3uGJ-js1D8_ZkDgaXw8TBtkjzIfBUNzAWyl8NCG1z" alt=""></div>

### Функция и параметры

fb\_pixel\_event(event\_name, pixel\_id, access\_token, event\_source\_url, action\_source, fbc, test\_event\_code, data) - передает событие в фейсбук пиксель из бота

<table><thead><tr><th width="331.55078125">Параметры</th><th>Описание</th></tr></thead><tbody><tr><td>event_name</td><td>название события. Можно использовать как стандартные события (например Lead, PageView, Purchase и тд https://developers.facebook.com/docs/facebook-pixel/implementation/conversion-tracking/#standard-events), так и свои (например Вошли в бот).</td></tr><tr><td>pixel_id</td><td>id пикселя. Если в настройках проекта создать переменную fb_pixel_id, а в функцию передать пустое значение, то данные будут взяты из переменной fb_pixel_id</td></tr><tr><td>access_token</td><td>маркер доступа к апи (токен). Если в настройках проекта создать переменную fb_access_token, а в функцию передать пустое значение, то данные будут взяты из переменной fb_access_token</td></tr><tr><td>event_source_url</td><td>домен, который подтвержден в аккаунте Фейсбук</td></tr><tr><td>action_source</td><td><p>(по умолчанию other) Это поле позволяет указать, где произошли конверсии. Информация о том, где произошли события, позволяет убедиться, что ваши объявления отображаются целевой аудитории. В поле action_source можно отправить следующие значения:<br>1) email - Конверсия произошла через электронное письмо.</p><p>2) website - Конверсия произошла на сайте.</p><p>3) phone_call - Конверсия произошла по телефону.</p><p>chat - Конверсия произошла через приложение для обмена сообщениями, SMS или онлайн-переписку.</p><p>4) physical_store - Конверсия произошла в физическом магазине.</p><p>5) system_generated - Конверсия произошла автоматически, например в результате продления ежемесячной подписки.</p><p>6) other - Конверсия произошла другим способом.</p></td></tr><tr><td>fbc</td><td>идентификатор клика. Необязательный параметр</td></tr><tr><td>test_event_code</td><td>Код для теста отправки событий. Необязательный параметр (информация где взять в разделе "как тестировать события")</td></tr><tr><td>data</td><td><p>дополнительные необязательные параметры. Представляет из себя словарь с данными. Возможные значения:<br>1) <em>fn</em> - имя </p><p><em>2) ln</em> - фамилия </p><p><em>3) email</em> - емейл пользователя </p><p>4) phone - телефон пользователя </p><p><em>5) fbc</em> - идентификатор клика </p><p><em>6) gender</em> - пол ( f - женский m - мужской)</p><p><em>7) country</em> - страна </p><p><em>8) state</em> - область </p><p><em>9) city</em> - город </p><p><em>10) index</em> - почтовый индекс </p><p><em>11) external_id</em> - Любой уникальный ID клиента, например членский ID, ID пользователя или ID внешних файлов cookie. </p><p><em>12) client_ip_address</em> - IP адрес клиента 13) <em>client_user_agent</em> - user agent браузера клиента</p><p></p><p>Вы также можете передать собственные параметры в пиксель (не обязательно), для этого дополнительно нужно добавить параметр:</p><p><em>my_params</em> и в нем перечислить свои поля. Например:</p><p><em>“my_params”: {“value1”: “Hello”, “val2”: “Hi”}</em></p></td></tr></tbody></table>

Пример:

{"fn": "Ivan", "ln": "Ivanov", "client\_ip\_address":"127.0.0.1", "my\_params": {“value1”: “Hello”, “val2”: “Hi”\}}

Пример сохранения токена в настройках проекта:

<div data-with-frame="true"><figure><img src="../../.gitbook/assets/IMAGE 2026-03-26 100151.jpg" alt=""><figcaption></figcaption></figure></div>

Причем передачи параметров:

<div data-with-frame="true"><figure><img src="../../.gitbook/assets/IMAGE 2026-03-26 100154.jpg" alt=""><figcaption></figcaption></figure></div>

### Как тестировать события

Для тестирования в тело запроса вам нужно добавить параметр **test\_event\_code** с текстом, который находится во вкладке **Тестирование событий**

<div data-with-frame="true"><img src="https://lh6.googleusercontent.com/f1UwHwSkVHNACFuTB6xa74kmNfzoqGF0ZpfkCXpNsTCygu4YA8nxfG6sVDak7428ODrVK9C8p1z4uYeA5zahx6n1Q24H9zpwUSxAl0b5_0bi9nJkagDeqFJTMPHEZisX-h0_r3vP" alt=""></div>

_{_\
_"pixel\_id": "#{pixel\_id}",_\
_"access\_token": "#{access\_token}",_\
_"event\_name": "Вошли в бот",_\
_"event\_source\_url": "https://my\_best\_site.ru",_\
_"fbp": "#{\_fbp}",_\
_"fbс": "#{\_fbс}",_\
_"test\_event\_code": "TEST99986"_\
_}_

{% hint style="warning" %}
Внимание! Не забудьте удалить этот параметр из запроса, при запуске рабочей версии!
{% endhint %}

#### Дополнительные необязательные параметры

_fn_ - имя\
_ln_ - фамилия\
&#xNAN;_&#x65;mail_ - емейл пользователя\
phone - телефон пользователя\
&#xNAN;_&#x66;bc_ - идентификатор клика\
&#xNAN;_&#x67;ender_  - пол ( f - женский  m - мужской)\
&#xNAN;_&#x63;ountry_ - страна\
&#xNAN;_&#x73;tate_ - область\
&#xNAN;_&#x63;ity_ - город\
&#xNAN;_&#x69;ndex_ - почтовый индекс \
&#xNAN;_&#x65;xternal\_id_ - Любой уникальный ID клиента, например членский ID, ID пользователя или ID внешних файлов cookie.\
&#xNAN;_&#x63;lient\_ip\_address_ - IP адрес клиента\
&#xNAN;_&#x63;lient\_user\_agent_ - user agent браузера клиента

Вы также можете передать собственные параметры в пиксель (не обязательно), для этого дополнительно нужно добавить параметр:

_my\_params_ и в нем перечислить свои поля. Например:

_“my\_params”: {“value1”: “Hello”, “val2”: “Hi”}_

<div data-with-frame="true"><img src="https://lh4.googleusercontent.com/yF8Oaa5WEiEcy7NmsH-W0C71PaSzbWieyfpc5vSNiYtKy-PTg1YX3Ua09u9ODk7xlFJRxxZwDewIztJ5_vYvj65FJJWQAW0L0DFmTx3nJCfBkqu0efJUjLgI6Kug7lpQMI7Gks3D" alt=""></div>

{% hint style="info" %}
Внимание! Не забудьте удалить этот параметр из запроса, при запуске рабочей версии!
{% endhint %}

<div data-with-frame="true"><img src="https://lh6.googleusercontent.com/gVP76G8HiGcvnWh6rG_XHmjohoNVcUNrCN4wD8MbyXVXqZldrOU73EIXobzogw54rJ1Vk-puAALGDNloNnvE2NPRZEcjtbsuLLlH4Nt3eIdDsT0hk8cG6FVpK5cvcXVdT4yHrY2G" alt=""></div>

## Как добавить рекламный аккаунт

В настройках нужно открыть доступ своему аккаунту

<div data-with-frame="true"><img src="https://lh6.googleusercontent.com/mqZ4ye1I-92QXWoZ8ZZc6BEjCFZbIyI5K16GnXebO_UlCgBRqoJDczvP6DAwwTp-9zW15afzxeK26s6RRpGvj7SqkyWBOavj1wH5umg2sletOippfL_5iCqBBPljK7snq4pTk8Cf" alt=""></div>

<div data-with-frame="true"><img src="https://lh6.googleusercontent.com/_u0dQq0lyrfo4fXX7_YAxH1CKeoYDLkXvNMmWt-qPs2qN3qKXTYpesoIASZ_CfdzpcMDYhnJSRlblxdxp5e44ElxlY5xE3qcMYWA4bDwlFfnV6fpR9nbTIXzaOIfG8wSr_qBr9us" alt=""></div>

Сохраняем и переходим тут же во вкладку Связанные объекты -> Добавить объекты:

<div data-with-frame="true"><img src="https://lh6.googleusercontent.com/j8kUsh94LudawBPSIRZhZx5EmJHkWLcy_CLwRhd3kdlfIvuH9xAcPZZOfFjzZnhnZdUB6HC0K02AvvyRuGu48bcbne0lN4VAEMp2wRQofiXDoieSDZlo0ZVRw5ZdahKN3Bfwwt5j" alt=""></div>

И добавляем ваш рекламный аккаунт.
