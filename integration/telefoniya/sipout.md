# SipOut

## Как подключить сервис

{% hint style="warning" %}
Для того, чтобы у Вас появилась возможность интеграции c Salebot, обратитесь в техподдержку SipOut
{% endhint %}

**Шаг 1.** Перейдите в  раздел Документация и скопируйте API-ключ:

![Раздел Документация в SipOut](https://lh5.googleusercontent.com/DZTzfrkiq-baNbpHiiwbG60P16eYXNTTchGuEE2-s90ybgdkHWUkSqizybRdaeKmR5hJOtsLSdtcVPJSwmx9M9szHAurjK2Nnr80Gpsm63qX-xFYAObhEtToYe_ejdreq116hma_)

**Шаг 2.** Переходим в настройки подключения в Salebot, раздел Телефония и нажимаем кнопку **Подключить** для сервиса SipOut:

![Раздел Телефония в Salebot](https://lh3.googleusercontent.com/2s0VTYQ-gBmTRYXKTPrPrSZlwqLQWXWaSUrcvbHb_8OH-gN_JfcMjEHlF6B3c4TYNd1q7GruCt0PhCS2y7W7h6HkeJHac_i2_46BuO7-EDTKJcDhi57N2Bl3ALr1FHfZYXToO_Bi)

&#x20;**Шаг 3.** Вводим API-ключ, скопированный в SipOut, и нажимаем кнопку **Сохранить настройки**:

![Форма ввода ключа для подключения Salebot к SipOut](https://lh5.googleusercontent.com/R6D96iCehGFng5f0DiG-50HziyLECNSNztVL4qy6JF2LKjiLff5J9A2wur-i1M5AtghRb5pGn0uVMLGwg7r764yfGU2F-sWUBCKy6Tw99miDLHsZff4Leo0KdoVjYYbSRVsF3NGX)

**Шаг 4.** Возвращаемся в кабинет SipOut и в подключенных интеграциях появится Salebot (возможно нужно будет обновить страницу):

![Раздел интеграции в SipOut](https://lh4.googleusercontent.com/HnVA-8BTZos8ybA4y6ILWMuLHkJUuxjLRQhLJjgLZP9VMlpcz1iVS1iVttdqs7VwmGvMWNIlvq9U8QyOEY_7SpPWTIkW1aT7CmpyUfM-Hy5sxcM5fO-T_KxvMq9S9ROuPOhBWYn-)

Нажимаем иконку **Редактировать:** в SipOut подтянутся все сотрудники из Вашего проекта. Для каждого сотрудника назначаем внутренние номера, которые будут использоваться при звонке по click2call:

![Настройка внутренних номеров для каждого из сотрудников проекта в Salebot](https://lh6.googleusercontent.com/lW_2dadeOYE30jh0XJp7i_fGDe17F2uz4dl7nrHbnnWvyjZqWPnNMyUeDSq3sMwm6YRo1-8cNUTrHKzrSgXJjQDWUEbxWcpKw-e8i5mwOqOPh8GmiRqBy6Gw257i0mapxoz3SqPh)

**Шаг 5.** Возвращаемся в Salebot и переходим в раздел Сотрудники. Для каждого сотрудника необходимо указать способ совершения телефонных звонков, выбрав из трех доступных режимов: Звонки через приложение, Звонки по API SipOut и Отключить звонки:

![Раздел Сотрудники Salebot](https://lh4.googleusercontent.com/sJe8ahyNmsxznQId6OSrQDtmTL5DptXJDxRRoNvxK4InqiH3EjBkqQa7bWWmLAfxXNCbPg4Xzt7fhz4Z-ni92dJ5BDVf5PeZ0tJOKHDkgbPSaNluhfFc7c2DJf0VOIrRIZz8SZmT)

![Настройка способа совершения телефонных звонков](https://lh3.googleusercontent.com/j5WxsvWJzEckQyR2ICSmKMx72SCLeVWne8jGpPtT6fRAfki8cVGseVayTwKzFDOlFtPQeqE-PcVmNTbRbstoXyGei-WNG3aP3t4rYaAx9t5R3KvQOu9fHl_uljW13UehKCXxa9wT)

Если выбрать пункт **Отключить звонки**, то этот сотрудник не сможет совершать звонки и иконка телефона возле номеров телефона у него не будет отображаться.&#x20;

**Звонки через приложение** - при нажатии на иконку телефона звонок будет перенаправлен в приложение, установленное для звонков на Вашем устройстве (Zopier и тд).&#x20;

**Звонки по API SipOut** - при клике на иконку телефона АТС звонит сначала сотруднику на номер, указанный в настройках SipOut для этого сотрудника, а уже после ответа сотрудника  звонок поступит клиенту.

Для осуществления звонка выбранным методом достаточно в карточке клиента нажать на иконку телефонной трубки рядом с его номером телефона:

![Вид карточки клиента Salebot](https://lh5.googleusercontent.com/DIW6A0pU_uZ8Acs_FfGf70CNavzFrsrDMKJMgdM9r00EDjMuCcmfvCM1HKKd_g9EJ9rqJjl6ZCr7w3vTvJpTDlM5KOY8yX4x559UAJiDBkRKdDNxiaKyQgOCrJVXNxKnQ2mfrGez)

## Как работать с уведомлениями

Для телефонии создан специальный тип уведомлений: **Уведомление Телефонии**. На такие уведомления бот не реагирует.

После начала разговора приходит уведомление с типом Телефония, содержащее данные о звонке:

![Уведомление Телефонии](https://lh6.googleusercontent.com/woJAuv1s1f5UpsbXs4WEsIyvi5SLmYywM_gVVhZSSpyqV0OyzsK6j4P9xbZ4wG0xAQyAZ-By2mFgP40QxKdKaZDBhWVNqXKPpn28prpTO3ZGGmlrpNQTKxg7qNtEdwTBT_4dc1Zi)

После окончания разговора и получения вебхука все данные будут сохранены в переменных сделки:

![Переменные сделки в карточке клиента Salebot](https://lh5.googleusercontent.com/0QeVRgrAIOi4AdGIEyb3C-z3_HgR7ZBEI5h28Tyk3JfKJ4ilh368WkskQYxHSy5Z2JizAeIk9XuYJL4gl0fzflxL5te8Ue8HifhkLWxvxcLhvLFWZfIJpOkNpHFH89FbbCBF2ABM)

**call\_action** - dial (начало разговора) или complete (окончание разговора)&#x20;

**call\_status** - статус звонка, примеры: Success, Busy, Missed&#x20;

**call\_total\_duration\_sec** - продолжительность в секундах (учитывая гудки)&#x20;

**call\_talk\_duration\_sec** - продолжительность разговора в секундах&#x20;

**call\_record\_link** - ссылка на запись&#x20;

**call\_did** - при входящем вызове номер, на который поступил вызов.

А также придет уведомление Телефонии со всеми данными звонка и обычное уведомление, на которое можно поставить условие и запускать бот:

![Уведомление о звонке](https://lh4.googleusercontent.com/gut34x7zj-QRTXVFZznifHlrlOG2u_P7QfW6m77v365P3jVksnylFRXHKBieWfokuaBELciBCo1SAF4doPRIUJKVUCPrpn2Q__ylXKUKykaQCW06Tya82F_wdJUDDNEFEPTVaAri)

Уведомления бывают 4 разновидностей: \
**telephony\_call\_success** - успешный звонок \
**telephony\_call\_busy** - занято \
**telephony\_call\_missed** - пропущенный звонок\
**telephony\_call\_text** - приходит с текстом разговора, если используется данная функция (описание ниже)

## Как происходит сопоставление клиента

{% hint style="warning" %}
Для работы с телефонией используются номера в формате 71234567890 (должен начинаться с 7, состоять из 11 цифр и не иметь лишних знаков и отступов).
{% endhint %}

Последовательность сопоставления данных о клиенте:&#x20;

1. Осуществляется поиск клиента Телефонии. \
   Если клиент не найден, то происходит поиск по значениям всех переменных по всему списку клиентов проекта. Первая найденная запись о клиенте считается тем самым "искомым" клиентом.&#x20;
2. Если клиент не найден среди клиентов Телефонии и:\
   \- к проекту подключен любой мессенджер, например, Whatsapp, то будет создан клиент Whatsapp с данным номером телефона. \
   \- к проекту не подключены иные виды мессенджеров (Whatsapp, Viber, Instagram и т.д.), то будет создан клиент Телефонии. Такому клиенту Вы сможете совершать **только** звонки с получением информации о них. Написать такому клиенту возможности нет.

## Как использовать виджет обратного звонка или "звонок из блока"

Еще один из вариантов использования интеграции - это возможность заказа обратного звонка.&#x20;

Для этого в SipOut переходим в раздел **Click2Call** и создаем виджет.&#x20;

Далее нажимаем кнопку **Редактировать**:

![Настройка виджета обратного звонка SipOut](https://lh3.googleusercontent.com/WJpg3hY-2LtKwnI0e9GnSYF6lEiBxJnWZ-_yXYeQcWsKpvynyyOS4MYb8Dg_gymh2fqF4nQVPEEiXPq0mHcTrcEPhAoq06nZuyECOhqb6EPYGVFDWtZiqrZsq7L7i75g58ClXuJX)

Скопируйте строку с адресом API-url:

![Получение адреса API-Url](https://lh6.googleusercontent.com/6-Mr2p6IiSLhqqzYeEZpzCHqe81p3aQ_fCCvVAYj3pU3_wZMpwGonnLhcdH8kYlzmNuDl3q-72KY-ZKKCDuWhQ2--lABsHw4DEBFy645rvjkvcONrIHtjOAkdE7YkQmtdo4kJHPw)

В нужном блоке сделать GET-запрос с использованием полученного API-Url. Вместо <номер телефона> укажите номер клиента, например:&#x20;

![](<../../.gitbook/assets/image (16) (1).png>)

При таком варианте реализации сначала вызов поступит клиенту и только потом менеджеру. Внимательно продумайте схему работы перед использованием.

## **Как получить весь разговор в виде текста**

{% hint style="info" %}
Данная функция платная. С размером тарифа Вы можете ознакомиться на сайте SipOut
{% endhint %}

![Включение режима речевой аналитики (транскрибация текста через Яндекс)](https://lh5.googleusercontent.com/IOcRLPQ3sjMBc_fr0rhiA-oBG3MeuulhyxH9QNgGJL82sQudRcyzTxqUzzzkmQX0L1mloC9FmttLudL-jWfcNoa4LpK7gEwDZ3HDKStIKn7v0Me0A1sm6RlhyVMjL5UsKNLiBpIz)

Если включена функция Речевая аналитика (транскрибация текста через Яндекс), то по окончании звонка, через пару минут придет текст разговора в виде уведомления Телефонии, а также колбек **telephony\_call\_text**, который можно использовать для реакции бота на это событие:

![Уведомление по окончании разговора с включенным режимом речевой аналитики](https://lh6.googleusercontent.com/WqHee-RzRx6s43cEeoo3ugw8bugdmPoXNATGRF36XzpM7EtZ044LimSQ9Cs5G3TvS0iFYzb_38noiSPsfmery8JUyxNTpKSY4t5e3Y_dIfL9_VEhFUwhZk0ZM3jIalToDcyC9bpM)

## Как подключить уведомления Телефонии в AMO CRM и Bitrix24

В Bitrix24 и AMO CRM уведомления Телефонии будут поступать при подключении отправки уведомлений о действиях пользователя:

![Настройки при подключении Bitrix24](<../../.gitbook/assets/image (17) (1).png>)

![Настройки при подключении AMO CRM](<../../.gitbook/assets/image (18) (1).png>)
