# \*\*cebook Pixel\*

{% hint style="danger" %}
<mark style="color:red;">\*</mark>На территории Российской Федерации запрещена деятельность социальных сетей Facebook и Instagram, принадлежащих компании Meta Platforms Inc., признанная экстремистской!
{% endhint %}

* [Как установить пиксель Facebook на минилендинг ](cebook-pixel.md#ustanovka-pikselya-facebook-na-minilending)
* [Как отправить события в пиксель из бота ](cebook-pixel.md#otpravka-sobytii-v-piksel-iz-bota)
* [Как добавить рекламный аккаунт](cebook-pixel.md#dopolnitelnye-nastroiki)

## Как установить пиксель Facebook<mark style="color:red;">\*</mark> на минилендинг

{% embed url="https://docs.salebot.pro/minilendingi-v-socialnykh-setyakh/kak-sozdat-sait" %}

## **Как отправить события в пиксель из бота**

Для передачи событий из воронки бота, нужно иметь бизнес аккаунт. Зарегистрировать можно по ссылке - [https://business.facebook.com](https://business.facebook.com)

### Как создать новый пиксель

![](https://lh4.googleusercontent.com/lD00d_Yd31buyVUtc7ZgPjj-NT2oeFOQS4XjBX2xyGVESzweGAzIb5yfPsdRk90I3XQZNO9U_No5vLIRjItyEzA9CaqNGV2heh-NMvJCUuPN6XHyHi15z6St6X7siadzY9lpfmmt)

Выбираем API Conversions

![](https://lh3.googleusercontent.com/a1OQ0peFICKvw3LFgOtVjtOh9cBakTZu7gXmB9-UcUn_0WqCBRxOiyC1qszWD0xDsPWr7I5nR0TO_AJEJbKJX6SGiCcFElcySdsaqz3YmYS9MZTRagDk8tNlB14E6IF8fEWEEhm1)

{% hint style="danger" %}
**Внимание!** Если на этапе создания настройки conversion api у вас появится следующее окно, следует выйти из настройки и начать занов&#x43E;**.**
{% endhint %}

![Если у вас появится следующее окно, следует выйти из настройки и начать заново.](https://lh6.googleusercontent.com/8wrVR4FZR2yJSKxmYJmR9uJ3vPcUkgGvuuScEa93kDmaTZWuqWmCV0x2xdtrFZmyVCqjShqrXgNud9U8B5UpI5G-aEIiWzo8hAaBWVSWNFu9oeYiMIWD1Uqi5-XzPe4ZaQA1Kmhn)

![](<../../.gitbook/assets/image (182).png>)

Выбираем нужный пиксель

![](https://lh3.googleusercontent.com/QIjmsqi4ZjGXuqRV9_UhZCL7uf1y6XFvvOHn9ru9zNlYs73tMW3svCWYjG6l0tlvSG9aFFMFo8wZOilDJAvO5UvpmXgPU9qBY65W5c1nMThsdnS3qfzBTfX1PR0PdLCB9gX3h7aZ)

Генерируем маркер доступа (токен) и сохраняем в надежном месте.

![](https://lh4.googleusercontent.com/Qt2ChkjK9A8j4LAhpZ-N42TpRoyZl20GI9g_6H2uBzRzLp1CsXySZiovveiHZHBIQGMM9wS54G6zJg5T5v4mz8OuNf4ZkZCcfhJcsqUZQk6NOu9ieyOhS-vA0BBegVucNs2t2759)

### Как передать события в фейсбук<mark style="color:red;">\*</mark>

{% hint style="danger" %}
<mark style="color:red;">\*</mark>**На территории Российской Федерации&#x20;**<mark style="color:red;">**запрещена деятельность**</mark>**&#x20;социальных сетей&#x20;**<mark style="color:red;">**Facebook**</mark>**&#x20;и&#x20;**<mark style="color:red;">**Instagram**</mark>**, принадлежащих компании Meta Platforms Inc**., признанные экстремистскими!
{% endhint %}

Для передачи события в фейсбук у вас на минилендинг должен быть установлен свой домен, подтвержденный в фейсбук и в настройках минилендинга включено сохранение значений из куки для фейсбук:<br>

![](<../../.gitbook/assets/image (183).png>)

Теперь клиенту, который перешел с минилендинга автоматически запишется переменная: \_fbp, которую нужно передать в пиксель вместе с событием.<br>

![](https://lh3.googleusercontent.com/dfduauw9O5LuwAURGcJ2Ax5I-L9eztzMcyOQp4QB2ZKQzy3SHi-ThwJcwSrgqOzFWOIH4coMcmsyrQh4Dog0Vu_mnwfgOGs3uGJ-js1D8_ZkDgaXw8TBtkjzIfBUNzAWyl8NCG1z)

В воронке в блоке, где необходимо передать событие ставим следующие настройки:<br>

**URL функции:** _https://store.salebot.pro/function/fb\_pixel_&#x20;

**Пример параметров:**\
&#xNAN;_{_\
_"pixel\_id": "#{pixel\_id}",_\
_"access\_token": "#{access\_token}",_\
_"event\_name": "Вошли в бот",_\
_"event\_source\_url": "https://my\_best\_site.ru",_\
_"action\_source": "chat",_\
_"fbp": "#{\_fbp}",_\
_"fbc": "#{\_fbc}"_\
_}_\
**Обязательные параметры:**\
&#xNAN;_&#x70;ixel\_id_ - id пикселя\
&#xNAN;_&#x61;ccess\_token_ - маркер доступа к апи (токен)

_event\_name_ - название события. Можно использовать как стандартные события (например Lead, PageView, Purchase и тд [https://developers.facebook.com/docs/facebook-pixel/implementation/conversion-tracking/#standard-events](https://developers.facebook.com/docs/facebook-pixel/implementation/conversion-tracking/#standard-events)), так и свои (например Вошли в бот).

_event\_source\_url_ - домен, который подтвержден в аккаунте фейсбук\
&#xNAN;_&#x66;bp_ - идентификатор браузера клиента

<figure><img src="../../.gitbook/assets/facebook json.png" alt=""><figcaption></figcaption></figure>

#### Необязательные параметры

_action\_source_ - (по умолчанию other) Это поле позволяет указать, где произошли конверсии. Информация о том, где произошли события, позволяет убедиться, что ваши объявления отображаются целевой аудитории. В поле `action_source` можно отправить следующие значения:

| Значение           | Описание                                                                                 |
| ------------------ | ---------------------------------------------------------------------------------------- |
| `email`            | Конверсия произошла через электронное письмо.                                            |
| `website`          | Конверсия произошла на сайте.                                                            |
| `phone_call`       | Конверсия произошла по телефону.                                                         |
| `chat`             | Конверсия произошла через приложение для обмена сообщениями, SMS или онлайн-переписку.   |
| `physical_store`   | Конверсия произошла в физическом магазине.                                               |
| `system_generated` | Конверсия произошла автоматически, например в результате продления ежемесячной подписки. |
| `other`            | Конверсия произошла другим способом.                                                     |

### Как тестировать события

Для тестирования в тело запроса вам нужно добавить параметр **test\_event\_code** с текстом, который находится во вкладке **Тестирование событий**<br>

![](https://lh6.googleusercontent.com/f1UwHwSkVHNACFuTB6xa74kmNfzoqGF0ZpfkCXpNsTCygu4YA8nxfG6sVDak7428ODrVK9C8p1z4uYeA5zahx6n1Q24H9zpwUSxAl0b5_0bi9nJkagDeqFJTMPHEZisX-h0_r3vP)

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
&#xNAN;_&#x63;lient\_user\_agent_ - user agent браузера клиента<br>

Вы также можете передать собственные параметры в пиксель (не обязательно), для этого дополнительно нужно добавить параметр:<br>

_my\_params_ и в нем перечислить свои поля. Например:

_“my\_params”: {“value1”: “Hello”, “val2”: “Hi”}_

![](https://lh4.googleusercontent.com/yF8Oaa5WEiEcy7NmsH-W0C71PaSzbWieyfpc5vSNiYtKy-PTg1YX3Ua09u9ODk7xlFJRxxZwDewIztJ5_vYvj65FJJWQAW0L0DFmTx3nJCfBkqu0efJUjLgI6Kug7lpQMI7Gks3D)

{% hint style="info" %}
Внимание! Не забудьте удалить этот параметр из запроса, при запуске рабочей версии!
{% endhint %}

![](https://lh6.googleusercontent.com/gVP76G8HiGcvnWh6rG_XHmjohoNVcUNrCN4wD8MbyXVXqZldrOU73EIXobzogw54rJ1Vk-puAALGDNloNnvE2NPRZEcjtbsuLLlH4Nt3eIdDsT0hk8cG6FVpK5cvcXVdT4yHrY2G)

## Как добавить рекламный аккаунт

В настройках нужно открыть доступ своему аккаунту

![](https://lh6.googleusercontent.com/mqZ4ye1I-92QXWoZ8ZZc6BEjCFZbIyI5K16GnXebO_UlCgBRqoJDczvP6DAwwTp-9zW15afzxeK26s6RRpGvj7SqkyWBOavj1wH5umg2sletOippfL_5iCqBBPljK7snq4pTk8Cf)

![](https://lh6.googleusercontent.com/_u0dQq0lyrfo4fXX7_YAxH1CKeoYDLkXvNMmWt-qPs2qN3qKXTYpesoIASZ_CfdzpcMDYhnJSRlblxdxp5e44ElxlY5xE3qcMYWA4bDwlFfnV6fpR9nbTIXzaOIfG8wSr_qBr9us)

Сохраняем и переходим тут же во вкладку Связанные объекты -> Добавить объекты:

![](https://lh6.googleusercontent.com/j8kUsh94LudawBPSIRZhZx5EmJHkWLcy_CLwRhd3kdlfIvuH9xAcPZZOfFjzZnhnZdUB6HC0K02AvvyRuGu48bcbne0lN4VAEMp2wRQofiXDoieSDZlo0ZVRw5ZdahKN3Bfwwt5j)

И добавляем ваш рекламный аккаунт.
