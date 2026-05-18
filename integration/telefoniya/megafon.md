# Мегафон

## Как подключить сервис

Настройка интеграции производится через личный кабинет администратора. В левом нижнем углу нажмите “Настройки”, чтобы перейти к настройкам АТС.

В окне настроек нажмите на кнопку “Интеграция с CRM”

<figure><img src="https://lh7-rt.googleusercontent.com/docsz/AD_4nXcR_nWHq1cp3uNy_J5_TfiZwK16WDJxHiigQzL36rwZbfKFEyu5xSBZW73as35f0kPEPAtjp0p-n_nPTCQWMF1GJclf7f6afRxhwz8SeNJ6WE4SY5mGbg7ln_BAXcnRu9iWnf90u3OOhAXtB-5AsAbwZGw?key=r63-y2MlsPtZsDlYa6SWBA" alt=""><figcaption></figcaption></figure>

В конце списка найдите “Ваша CRM” и нажмите “Подключить”.

<figure><img src="https://lh7-rt.googleusercontent.com/docsz/AD_4nXcpDJehvNgsHmx-yKT14QOQ0xVBFtLeCcDsDefKenS5GyIt06yGiQDAhGRxYXvIslyz_yNQ3okzVl8MFmjNHXd7eH5IzqWIyK-6AFsB9qoxnAfD9ZCOgL4WXw2xsOXXvf3TLrWvNS5_Aq1ISd2OR0caSmjJ?key=r63-y2MlsPtZsDlYa6SWBA" alt=""><figcaption></figcaption></figure>

В открывшейся странице заполняем все пустые поля.

Имя вашей CRM - можно указать любое (например, Salebot).

Адрес вашей CRM - [https://chatter.salebot.pro/megafon\_webhook](https://chatter.salebot.pro/megafon_webhook) (для получения уведомлений о звонках).

Ключ для авторизации в вашей CRM - в настройках вашего проекта в Salebot скопируйте “Ключ доступа к API” и вставьте его в это поле. (Если ключа в настройках нет, нажмите на кнопку “Сгенерировать”).

Обращаем внимание, что после перегенерации ключей придется заменять их на новые во всех местах, где они использовались.

Также здесь есть уже заполненное поле “Ключ для авторизации в АТС”. Этот ключ пригодится для подключения интеграции в Salebot, сохраните его.

После заполнения полей, нажмите на кнопку “Сохранить”. Настройка интеграции на стороне Мегафон завершена.

<figure><img src="https://lh7-rt.googleusercontent.com/docsz/AD_4nXe1QU23z6nVsNAtM7Ayvt8xutNKU5SaC0jTJNSFphGhsZ2h_kw4aGO0U1htAC2uyiEbZ3nUx_fDiCKm6GfnTNoMPuOJOXZL2PqTmY64OG-aO6DkwUldBRj8e3jR6rNw5T08RpPyj7l6cH0w8Va2s50xpMfU?key=r63-y2MlsPtZsDlYa6SWBA" alt=""><figcaption></figcaption></figure>

## Подключение интеграции в Salebot

В Salebot перейдите в раздел “Телефония” и заполните данные для подключения Мегафон.

<figure><img src="https://lh7-rt.googleusercontent.com/docsz/AD_4nXf2unwb1wA1iilLOor7vejeVmtC-g-SvzhJXcWxoaHxOPplGmnrTBIhDdQxtcm2hFgyOoXkinoZ3ZKvzCkgP566tCSXgX6b5rsY8v8XZwULVDyD7oe4LJz_xHzHMzsGaM3HaF5jVK07LsVVui3_BFn6EsI?key=r63-y2MlsPtZsDlYa6SWBA" alt=""><figcaption></figcaption></figure>

<figure><img src="https://lh7-rt.googleusercontent.com/docsz/AD_4nXcEDykJ6PXukAnyMcdrpn78WOnRp4YZqxfdUKdSQ_ktXCHo_nCH6ZCB4p0trZpTj4YrJ8CQuZePBkZIISQas92XpqthFCIgKRy5zkfHcu62hnZbpN62rbUNPNkcStJ0_E_mmpCdsVxSAFUfwEMmkox-oBo?key=r63-y2MlsPtZsDlYa6SWBA" alt=""><figcaption></figcaption></figure>

API token мы скопировали ранее в личном кабинете Мегафон, в настройках интеграции.

Megafon domain - это адрес вашей виртуальной АТС, по которому вы входите в личный кабинет.&#x20;

Нажмите “Сохранить настройки”.

Сервис Мегафон подключен.

## Настройка звонков из карточки клиента

Для успешной работы с телефонией нам также понадобится информация о сотрудниках.

Для настройки возможности осуществлять звонки непосредственно из карточки клиента введите сотрудников в систему Salebot. После регистрации сотрудника зайдите в редактирование его данных.

<figure><img src="https://lh7-rt.googleusercontent.com/docsz/AD_4nXf1AF0fTJzlEjIBq30oh47sO7MQcGX_7IEvZf3HhhwkWqBpAZp3mKv99Y2K22KTyUgX-i7KbNIOJcToZ3NelDaBMpXZhn0hUI8AQETEWG4stPDzHFoUT4DHX9u4HJgRf8QwQbEsFCS3XYnnx296U8bu5AQF?key=r63-y2MlsPtZsDlYa6SWBA" alt=""><figcaption></figcaption></figure>

В позиции “Способ совершения телефонных звонков” выберите звонки по API Мегафон.

* Если выбрать пункт Отключить звонки, то этот сотрудник не сможет совершать звонки и иконка телефона возле номеров телефона у него не будет отображаться.
* Звонки через приложение - при нажатии на иконку телефона звонок будет перенаправлен в приложение, установленное для звонков на Вашем устройстве (Zopier и тд).
* Звонки по API Megafon - при клике на иконку телефона АТС звонок поступит менеджеру, чей логин или телефон вы указали в карточке, а затем клиенту.

После выбора способа совершения телефонных звонков в “Звонки по API Megafon” появится дополнительное поле, в котором может быть указан логин, внутренний номер или прямой телефонный номер вашего сотрудника.

<figure><img src="https://lh7-rt.googleusercontent.com/docsz/AD_4nXfnrUjZe7reKsEN8PghpNXfJitjnl_ql46XAWHUcsKa_VkSzS0ktB3nvcOHpar_-xztjjasuzjgT4Da_jpGbbVrBImLzmPo2XCfJZWR8vIGg1hDKIGrw64apukLgNzxE8SW5nHB4x5bmd6W8VJz88QsmFl-?key=r63-y2MlsPtZsDlYa6SWBA" alt=""><figcaption></figcaption></figure>

Информацию о номере или логине сотрудника можно найти в личном кабинете виртуальной АТС Мегафон

Для осуществления звонка выбранным методом достаточно в карточке клиента нажать на иконку голубой телефонной трубки рядом с его номером телефона:

<figure><img src="https://lh7-rt.googleusercontent.com/docsz/AD_4nXfLLPEnwWAfNlRXU7h3_VT5O0gFeexnxDkv95J9UW99u2ESZZJ3Auz9ba-nx7fAX5L0DV1cTjaqqx7uT_3Re0xgk-3IBluuJH5m-23HI9oHXRquF8HbG_vD7xeesavUAMlMFPWMhd3UP-B02qC_wnTcP8Rt?key=r63-y2MlsPtZsDlYa6SWBA" alt=""><figcaption></figcaption></figure>

## Как происходит сопоставление клиента

Для работы с телефонией используются номера в формате 71234567890 (должен начинаться с 7( или с иного кода другой страны, например, 375), состоять из 11 и более цифр и не иметь лишних знаков и отступов).

Последовательность сопоставления данных о клиенте: 1. Осуществляется поиск клиента Телефонии. Если клиент не найден, то происходит поиск по значениям всех переменных по всему списку клиентов проекта. Первая найденная запись о клиенте считается тем самым "искомым" клиентом. 2.Если клиент не найден среди клиентов Телефонии и:

* если к проекту подключен любой мессенджер, например, Whatsapp, то будет создан клиент Whatsapp с данным номером телефона;
* если к проекту не подключены иные виды мессенджеров (Whatsapp, Viber, Instagram и т.д.), то будет создан клиент Телефонии. Такому клиенту Вы сможете совершать только звонки с получением информации о них. Написать такому клиенту возможности нет.

## Функция Salebot обратный звонок

Для того чтобы совершить звонок из бота, необходимо использовать функцию megafon\_call(client\_phone, user), которая принимает на вход следующие параметры:

* client\_phone - номер клиента, которому должен быть совершен звонок, строка, пример - '79004443322'.
* user - логин, внутренний номер или прямой телефонный номер вашего сотрудника,  строка, пример - “admin@vats123456.megapbx.ru”.&#x20;

<figure><img src="https://lh7-rt.googleusercontent.com/docsz/AD_4nXfMLWhxd-YWksbUZPymX7fDhliR6zeTWxEgMENSM4eifY357o6DRjoariR5viTcWgYzAy_-4KCrQRdgAhX0iZcX-ZbAmZLk5tn7i0EeQ3LyBHeVvSLn9VZQ6xPHi4MvAG6is29DNqJa9Udg9L8fW1AEius?key=r63-y2MlsPtZsDlYa6SWBA" alt=""><figcaption></figcaption></figure>

## Виды уведомлений

При совершении звонков, в диалог с клиентом будут поступать следующие уведомления:

megafon\_call\_event \<event>, возможные \<event>:

* ACCEPTED - Звонок успешно принят (менеджер снял трубку).&#x20;
* COMPLETED - Звонок успешно завершен (менеджер или клиент положили трубку после разговора)&#x20;
* OUTGOING - Менеджер совершает исходящий звонок (ВАТС пытается дозвониться до клиента)&#x20;
* TRANSFERRED - Входящий звонок переведен на другого сотрудника

После завершения звонка, в диалог приходит колбек со статусом звонка.

megafon\_call\_status \<status>, возможные \<status> звонка:

* Success ‑ Успешный входящий (исходящий) звонок;&#x20;
* Missed ‑ пропущенный входящий (исходящий) звонок;
* Cancel – входящий (исходящий) звонок отменен;&#x20;
* Busy – получен ответ «Занято» (только исходящий);&#x20;
* NotAvailable – получен ответ «Абонент недоступен» (только исходящий);&#x20;
* NotAllowed – получен ответ «Звонки на это направление запрещены» (только исходящий);&#x20;
* NotFound – получен ответ «Вызываемый абонент не найден, нет такого SIP номера» (только исходящий).

<figure><img src="https://lh7-rt.googleusercontent.com/docsz/AD_4nXdX1DlRnQhXcEtSyOUVa0m4BKYsFJajKwUzKTRnze3o3vVaUIW5gjUeGi9f46O3hLJXp_cSrrn-PACm79VvP4zAHtLgKpxKtjjINfCQaHXLIMqtPkssA_7SyRaO2qIZyJGxiKBQJ-ZQarpvbGglDmVDVtxY?key=r63-y2MlsPtZsDlYa6SWBA" alt=""><figcaption></figcaption></figure>

Также после звонка у клиента создаются переменные с информацией о звонке.

<figure><img src="https://lh7-rt.googleusercontent.com/docsz/AD_4nXf44Hj4a1D5LyvY4syKN-CTveGHm8d2n-ZmSEat5z2wpjLukccMpKsifWUtmKGk_D2lpccMFqbH0sX0hdEdf_xGd2E9sh2CBihaALUBaXGp0fXpGmapUoZHBsJYeXFOkdHy8ebOf1JJRHfhHi5WEQpwa1yw?key=r63-y2MlsPtZsDlYa6SWBA" alt=""><figcaption></figcaption></figure>

* megafon\_call\_direction  - входящий или исходящий звонок (in/out)
* megafon\_call\_ext - короткий номер сотрудника
* megafon\_call\_id - ID звонка
* megafon\_call\_user - сотрудник, который разговаривал с клиентом
* megafon\_record\_link - ссылка на запись разговора. Чтобы запись сохранялась, нужно подключить соответствующую услугу в Мегафон
