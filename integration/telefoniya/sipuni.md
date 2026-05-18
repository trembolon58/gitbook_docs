# Sipuni

## Как подключить сервис

Для подключения Sipuni к Salebot необходимо получить ключ интеграции. Для этого следует зайти в настройки - API, и сгенерировать себе API ключ доступа. Также в правом верхнем углу будет номер Вашего кабинета Sipuni - на примере 038226 - этот номер будет Вашим User ID.

![](https://lh6.googleusercontent.com/2ueLP8Ikf9bGY9_o2jTm5JvDpmYF4AS70HoBzzJEpkOMXEUq6qqJzpVUT0tH8EP2fikXI8VAtw3CbfBPNb4-GIglBfss5Bn4RrD4vf_crRm2IRkzcRUQy2QkRY3prOlArsuxJOfWchUvUWyM8A)

Далее следует перейти в Salebot во вкладку телефония и ввести полученные данные в окно Sipuni.

![](https://lh4.googleusercontent.com/38G5t8-S-q78tGAzLpbIGVYbpgHvbowFRN27o81XMwGAP8ovpGfhy4N2qWahcZcYCxgzsZZ1cY1DimVEx3sWrwbQJYUzprHnt1mWuuMKdMZe7rGFzCLh4S7F8TEgQ2365z4De1IS-np9d9mSRA)

![](https://lh3.googleusercontent.com/pAkzsMajHRjJ4jSNOu8k2YD327OOhV6V9M8gvio5f35q4kIpLe7oEcfBpnRWCdYJifh3bQeBMc04sZbuUozdWp1AxZAlHR-oarfOFUf3iii3sCGLJrK7reSXqv3l9knUB7ExXzUEjma9p8X_GA)

Sipuni подключен! Однако для успешной работы с телефонией нам также понадобится информация о сотрудниках и схемах работы. В меню “Конструктор”, подменю “Сотрудники” добавляем необходимое количество работников, уделяя особое внимание короткому номеру(в примере 201 и 202).

![](https://lh5.googleusercontent.com/KUXIOCu4n7RftonUQhe46oB0dH4F29xHsekQ159xLqpcar_udgWIavh4pI8RNkK1BwJUjn4wOO-WM9TnaNKQjpVqIJ4EsIJkTj5CMtgcHtGAxJzkSR6d7sofXprrkZRNAYeTyUKihonaIXFwVw)

![](https://lh6.googleusercontent.com/agbgPLxLhgvthvSZWF5KgEnR5wcaNOpVh4sHHp0W5FT1o1vbihh_6R8uVmS_elToPjJ_btFFibzhDH2QpG6lN4HdBdTNXFKC7_Qc8iEPWHzXceW3iRy19W44EwBFHiAj4YQdpwxhWZNYD06jJQ)

Если Вам понадобится работа со сценариями звонков в телефонии, то в том же “Конструкторе” Вам следует настроить исходящие и входящие схемы. Для успешных звонков в Salebot по сценариям необходимо запомнить номер требуемой схемы. Для этого следует зайти в настройки(или создание) схемы. В примере - номер схемы “000-430122”.

![](https://lh5.googleusercontent.com/2oRiYDq-XoM0D1hmL5rBM_qwAKMmdwWZXrp-QwsMvk5gg6Zrc5yDpH15Egp_LlW7lPbywE0Nw8pEYkWHL6ueKErcMdYxqgjs9H-deh5IwnWNSJwU6qhXd27jo58Tb8eEDrIJmbrwZ74ulNCLBQ)

![](https://lh5.googleusercontent.com/BoJXh-GRNNMatk0BuwyuF1I6hlF4mBgwUHj-K7Xi4pBREssRTDMV5jYTga_7dd7_fUmFetMLQHNskscihaaOc1TQQpv5CVK2gqXoGjsI1ahuplfUuHWAD2QyHvk2twrot1AIeMtwcFF2n7URgw)

{% hint style="warning" %}
Для звонков по Аpi Sipuni из карточки клиента и при помощи функций необходимо дополнительно подключить Услугу совершение звонков по API Sipuni для сотрудников.
{% endhint %}

## **Как происходит сопоставление клиента**

Для работы с телефонией используются номера в формате 71234567890 (должен начинаться с 7( или с иного кода другой страны, например, 375), состоять из 11 и более цифр и не иметь лишних знаков и отступов).&#x20;

Последовательность сопоставления данных о клиенте:\
1\. Осуществляется поиск клиента Телефонии. Если клиент не найден, то происходит поиск по значениям всех переменных по всему списку клиентов проекта. Первая найденная запись о клиенте считается тем самым "искомым" клиентом.\
2.Если клиент не найден среди клиентов Телефонии и:

* к проекту подключен любой мессенджер, например, Whatsapp, то будет создан клиент Whatsapp с данным номером телефона.
* к проекту не подключены иные виды мессенджеров (Whatsapp, Viber, Instagram и т.д.), то будет создан клиент Телефонии. Такому клиенту Вы сможете совершать только звонки с получением информации о них. Написать такому клиенту возможности нет.

## **Функция Salebot звонок с внутреннего номера на внешний**

Для того чтобы совершить звонок сотруднику из бота, необходимо использовать функцию sipuni\_internal\_to\_external\_call(client\_phone, short\_employee\_phone) , которая принимает на вход следующие параметры: \
client\_phone - номер клиента, которому должен быть совершен звонок, строка, пример - '79004443322'. \
short\_employee\_phone - короткий номер сотрудника в системе Sipuni, строка, пример - ‘201’&#x20;

{% hint style="warning" %}
Для звонков по Аpi Sipuni  при помощи Функции звонок с внутреннего номера на внешний необходимо дополнительно подключить Услугу совершение звонков по API Sipuni для сотрудников
{% endhint %}

Пример реализации функции в боте:

<figure><img src="../../.gitbook/assets/2023-12-01_18-46-32.png" alt="" width="563"><figcaption></figcaption></figure>

## Функция звонок по сценарию в Salebot

Для того чтобы совершить звонок сотруднику из бота, необходимо использовать функцию sipuni\_scheme\_call(client\_phone, short\_employee\_phone, tree\_code), которая принимает на вход следующие параметры: \
client\_phone - номер клиента, которому должен быть совершен звонок, строка, пример - '79004443322'. \
short\_employee\_phone - короткий номер сотрудника в системе Sipuni, строка, пример - '201'

tree\_code - номер схемы, по которой будет распределен звонок от клиента, строка, пример - ‘000-430122’.&#x20;

{% hint style="warning" %}
Для звонков по Аpi Sipuni  при помощи Функции звонок по сценарию необходимо дополнительно подключить Услугу совершение звонков по API Sipuni для сотрудников
{% endhint %}

Пример реализации функции в боте:

<figure><img src="../../.gitbook/assets/2023-12-01_18-50-50.png" alt="" width="563"><figcaption></figcaption></figure>

## **Настройка звонков из карточки клиента**

Для настройки возможности осуществлять звонки непосредственно из карточки клиента введите сотрудников в систему Salebot. После регистрации сотрудника зайдите в редактирование его данных.

![](https://lh6.googleusercontent.com/CC4pUzO3LDXnWhF83fsgdhHwJbJ6a6iwRsiOoMnj0J07f0-GOWsi8CDnkbTyo6lzOHva8L4lHGq8xxDedr0uAUGEjsuathU3C5RSdngeN6cLoBP4zBxsvz_JucK9F116MRr4qU_Poe-8RJjQsQ)

{% hint style="warning" %}
Для звонков по Аpi Sipuni из карточки клиента необходимо дополнительно подключить Услугу совершение звонков по API Sipuni для сотрудников
{% endhint %}

В позиции “Способ совершения телефонных звонков” выберите звонки по API Sipuni.&#x20;

* Если выбрать пункт **Отключить звонки**, то этот сотрудник не сможет совершать звонки и иконка телефона возле номеров телефона у него не будет отображаться.&#x20;
* **Звонки через приложение** - при нажатии на иконку телефона звонок будет перенаправлен в приложение, установленное для звонков на Вашем устройстве (Zopier и тд).&#x20;
* **Звонки по API Sipuni** - при клике на иконку телефона АТС звонок поступит сначала сотруднику, чей id вы указали в карточке, а затем перенаправляет звонок клиенту.&#x20;

После выбора способа совершения телефонных звонков в “Звонки по API Sipuni” появится дополнительное поле, в которое следует вписать короткий номер Вашего сотрудника в системе Sipuni.

![](https://lh6.googleusercontent.com/wtTV8tdoxEczh7jLoeTSp24qihVgy6beXmqn3eBSS_SbweisEK42ao69JR4rNDNLkogn7YbAb1EW4U95NNFXTStdysedkFM5HFSXEsvI0dz3fDEFfLqUhEQNRNBLT8BM89gtS0SZ6CvA0QRQNA)

Для осуществления звонка выбранным методом достаточно в карточке клиента нажать на иконку голубой телефонной трубки рядом с его номером телефона:

![](https://lh3.googleusercontent.com/tl19l4QtCfgAKQ95a76pHE3tGKWJ_icGHsPKYMiUiLFm5W304QfRRmwnk7X4sG8V91FyncavQrDtWpNd_9WpTNzyBM-Fe1_t7YUPGcqXMjM3X386BIAdVYPRVmQAEMAwwJTRkZHrJuS8HjBmKA)

## **Настройка вебхуков**

Для того чтобы настроить получение колбеков о завершении звонка, необходимо в системе Sipuni перейти в “Настройки”-”Api” - “События на АТС” и подключить данную услугу и в поле “URL принимающего скрипта”, прописать адрес вида: https://chatter.salebot.pro/sipuni\_webhook/<апи-ключ>, например, https://chatter.salebot.pro/sipuni\_webhook/0.a3skqw8js8d

![](https://lh4.googleusercontent.com/grS9KG9NPmjFY5qquF93dqtCyPdsL2vp-d5mmQzhlO0GAOB5jaJ6jN1RMpiArLiWkxvucynHmmwTJXwGpMqjZPYLDXd6Ykn3cSJFVclojQKlGIT3xLMBpoUgoPG9b1UPw1I6PSXCILf88smzyA)

В результате при завершении звонков в Salebot будет приходить уведомление следующего вида:

![](https://lh5.googleusercontent.com/xQmT5AeUsq-FNXA86uEAq1ICsKK2PQDNFQXcVvdArhQPqsrA2F40fpVoExGl3QEGNgQh9lIWSXs0A4OWhG5NwooJg62Pcbkh4QcmebpPwoRpif9ywvTh2840rFb2Qe1OfDwHN1NUGiwxsf2pWw)

В системе используются следующие статусы: \
ANSWER - вызов отвечен \
BUSY - абонент занят \
NOANSWER - абонент не ответил после определённого таймаута \
CANCEL - вызов сброшен \
CONGESTION - перегрузка сети \
CHANUNAVAIL – абонент недоступен (например, sip абонент не зарегистрирован в сети)

Также если у звонка будет иметься запись разговора, то у клиента будет создана соответствующая переменная, содержащая ссылку на запись.

![](https://lh4.googleusercontent.com/avi2Y2qLc_Vwbwi6G2jaS0SbFeYzuIybnzaMeSeJ0w53InMBZ063sTBb7-B8us5CHCQlDhZW2IR1C5Zpj7dLJQLY9JNBFWT3HSG5T5IO9m12xUWN-BEqAHFkwL5xPKz_pJ8bTWDG9QHl0rbVAA)
