# Подключение рекламного кабинета ВКонтакте через GTM

Переходим на [сайт](https://tagmanager.google.com/) и нажимаем кнопку "Создать аккаунт"

<figure><img src="../../.gitbook/assets/image (235).png" alt=""><figcaption></figcaption></figure>

Заполняем поля

&#x20;                                                <img src="../../.gitbook/assets/image (236).png" alt="" data-size="original">

Нажимаем кнопку "Создать" и далее соглашаемся с Политикой использования GTM

<figure><img src="../../.gitbook/assets/image (237).png" alt=""><figcaption></figcaption></figure>

<figure><img src="../../.gitbook/assets/image (238).png" alt=""><figcaption></figcaption></figure>

Из основного кода копируем тег GTM

<figure><img src="../../.gitbook/assets/image (239).png" alt=""><figcaption></figcaption></figure>

Переходим в Salebot, и в минилендинге, в разделе аналитика вставляем этот код:

<figure><img src="../../.gitbook/assets/image (240).png" alt=""><figcaption></figcaption></figure>

Далее переходим в рекламный кабинет ВК и создаем код пикселя

<img src="../../.gitbook/assets/image (241).png" alt="" data-size="original"><img src="../../.gitbook/assets/image (242).png" alt="" data-size="original">

<img src="../../.gitbook/assets/image (243).png" alt="" data-size="original">

Копируем код

![](<../../.gitbook/assets/image (244).png>)

Переходим в GTM, создаем новый Тег, в разделе Конфигурация Тегов выбираем Пользовательский HTML и вставляем скопированный код пикселя из Рекламного кабинета ВКонтакте

![](<../../.gitbook/assets/image (245).png>)

<figure><img src="../../.gitbook/assets/image (246).png" alt=""><figcaption></figcaption></figure>

<figure><img src="../../.gitbook/assets/image (247).png" alt=""><figcaption></figcaption></figure>

Настраиваем триггер, допустим для этого тега выбираем "Просмотр страницы"

<figure><img src="../../.gitbook/assets/image (248).png" alt=""><figcaption></figcaption></figure>

<figure><img src="../../.gitbook/assets/image (249).png" alt=""><figcaption></figcaption></figure>

Далее уже можно настраивать события для передачи по связке.&#x20;



Проверить связку GTM-Salebot легко с помощью кнопки Предварительный просмотр в GTM:&#x20;

<br>

<figure><img src="../../.gitbook/assets/image (250).png" alt=""><figcaption></figcaption></figure>

После нажатия вводим адрес Минилендинга:

<figure><img src="../../.gitbook/assets/image (251).png" alt=""><figcaption></figcaption></figure>

После нажатия на **Connect** откроется сам минилендинг и окно отладки с событиями которые сработали. Tags Fired - те что применились.



В рекламном кабинете ВКонтакте спустя некоторое время после срабатывания надпись “Данные не поступают” сменится на график со значениями.

<figure><img src="../../.gitbook/assets/image (252).png" alt=""><figcaption></figcaption></figure>

## Доступные события

### Для Минилендингов

{% hint style="info" %}
На минилендинги нужно прописывать триггеры тех тегов, которые необходимо пробросить дальше
{% endhint %}

событие **page\_view** - просмотр всех привязанных минилендингов

событие **page\_view\_N** где N - номер минилендинга - просмотр конкретного минилендига

нажатия на кнопки перехода мессенджеров:

* button\_vk
* button\_telegram
* button\_viber
* button\_facebook
* button\_whatsapp
* button\_ok
* button\_instagram

кастомное событие вашей личной кнопки (для этого надо добавить CSS класс кнопки, он и будет названием события нажатия)

<figure><img src="../../.gitbook/assets/image (253).png" alt=""><figcaption></figcaption></figure>

### Для подписной ВКонтакте

* событие **page\_view** - просмотр всех привязанных минилендингов
* событие **page\_view\_N,** где N - номер минилендинга - просмотр конкретного минилендинга
* событие **button\_vk** - кнопка “К диалогу”
* событие **buttons-type\_button -** любая кастомная кнопка

