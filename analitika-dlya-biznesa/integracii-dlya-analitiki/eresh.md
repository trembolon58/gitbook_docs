# Eresh

### Как р**азмечать трафик**

Чтобы видеть аналитику входящего трафика в чат-бот, нужно разметить его по источникам.\
Делаем это с помощью UTM-меток по инструкции:\
[https://vk.com/@ereshtarget-instrukciya-po-utm-metkam-v-eresh\
<br>](https://vk.com/@ereshtarget-instrukciya-po-utm-metkam-v-eresh)Если всё настроено верно, то при попадании пользователя в бота мы увидим метку, показывающую с какой именно ссылки (с какого объявления или от какого партнера) был переход.

![](https://lh4.googleusercontent.com/A6gM7sR933A6hzKDR4BQmEvApymtgRCPXO1Kmp8TsIXMc1lCPPSL_brwIlL52BMatMut--hOTYGFfTj8DGZkKYzQOUkqqUrm1BWyi7qCMfZFvz94N7LMmPR3ce3-v4veRrvxkxPi)

Видим записанные метки в карточке клиента в Salebot.

## **Как сделать разметку внутри чат-бота**

Выстраиваем метки целевых действий внутри воронки, чтобы увидеть сколько стоит пользователь на каждом этапе.\
\
Создаём для этого в ключевых блоках воронки клиентскую переменную и присваиваем ей значение. На примере показана переменная step.

![](<../../.gitbook/assets/image (212).png>)

Таким образом, пользователи доходя до ключевых этапов воронки помечаются соответствующей переменной.\
Например это могут быть такие этапы как:\
1\) Подписался = вошел в бота\
2\) Был на вебинаре\
3\) Оставил заявку на оплату\
4\) Оплатил

## **Как вывести статистику**

Все данные мы подготовили, можем посмотреть результат в Эриш.\
\
Зарегистрироваться можно по ссылке: [https://eresh.zemedia.ru/?reg=7d22614fa7a966f98234c43c7beecda1\
<br>](https://eresh.zemedia.ru/?reg=7d22614fa7a966f98234c43c7beecda1)Заходим в раздел **внешние данные**, выбираем период за который хотим видеть статистику и нажимаем кнопку **получить данные с Salebot**.

![](https://lh6.googleusercontent.com/-5_9LFP6Vws8wdoXGwg5UfYK643bDwJLXaeXIGVARWTIofB5GL9B2yQX35TZvKrnPzDhnT_cW8PvSQNQkiD0ycDMxqfeel1TiAKZx7D4wBY7H-Jph0AIgxoG0t7AYiMR-xoIozgW)

![](https://lh6.googleusercontent.com/lUmKrm7PJikmZeUWztyrMMxGZ5oCHmyRkM8m5yVmqdEleFaJiVBHKC1k7_QxqBERB6jSATpYzLNdXyXRZUskFLwbXIPYnf7dBc-FGTR9kzXJ368c1INRVoohsuiC5_wph_an735J)

В открывшемся окне заполняем поля:\
1\) ключ API -  берем из настроек проекта в Salebot;\
2\) tag - если вели трафик через минилендинг с тегом\
3\) ID группы вк - открываем любой пост, опубликованный в группе вк, в которую вели трафик и копируем только номер из адресной строки [https://vk.com/topispolniteli?w=wall-198248940\_35](https://vk.com/topispolniteli?w=wall-198248940_35)

![](https://lh5.googleusercontent.com/YZpg8Shlud3TKwvrPKR4yFutl19T-eMGbbxZCTKJcJwz2NrMLWh6S9pDngSqji4Oy7XihV3JrUNiYXRL-spviHO8k-bQzWQwYmciief0fhkM2lPWkarj8Zi6VCWzxnJq8Tnkh1LC)

#### **Что видим в результате**

![](https://lh4.googleusercontent.com/G5iu4Kq9NJOdHNaclpW5XR-7at5pAQClfjhvnW3yg6EeIJXi6fZx6Hnow4uZanCiJzzQA6YOuJH9KnervHCQ7lYFcLCU9rvPTJykatDHGlYZnAQEIILpnEEgfqfb-PjaoB3mpVjg)

Eresh подгрузила данные всех пользователей которых нашла в Salebot с тегом pereezd. Справа в колонках указаны все дополнительные метки.

## **Как вывести аналитику с данными о затратах**

Идём в раздел **команды**, выбираем нужный рекламный кабинет, выделяем все кампании (или только те по которым хотим видеть статистику), и нажимаем кнопку **статистика**:

![](https://lh5.googleusercontent.com/iFqw9-eKQ4GQcSmjwB8DWxFMJKvXmKNuMMjDdPsm2uKz7-G3LT5wvnDWM_H30AGL-EHcWd44qRknhgT09jygqNq84podHvGthugTVlUmpyQjE2kxAqSsttJxIzACDuHJ29Y-iZgT)

В открывшемся окне снова жмём **получить**, и видим данные по каждой кампании:

![](https://lh3.googleusercontent.com/d4m9DQvK4Wt9nKaqBNgPkDV6LiShjIM6mTn-OK3qeAFpT5cU4VlUIGIzJQKiIxrlYECSHHsj9qtyxPUjFZPagAL7mfc8aD_6zXvJttSLmJSHFvkUYmPU225QgilDCWgZOpAAGUHz)

* **Затраты** - сколько денег открутилось; данные учитываются с первого дня открутки самого раннего объявления в рекламном кабинете.
* **Показы** - сколько раз была показана реклама;
* **еСPM** - эффективная стоимость 1000 показов (среднее значение);
* **Клики** - количество кликов;
* **СTR** - кликабельность, (click-through rate) — показатель кликабельности;
* **eCPC** - эффективная стоимость клика (среднее значение);
* **Вступления** - кол-во вступивших в сообщество;
* **СR** - конверсия из кликов во вступления;
* **еСР** - стоимость вступления.

Идём дальше:\
\
Посмотрим стоимость подписчика в воронку и конверсию в подписчика.\
Нажимаем кнопку **получить данные из Salebot**, и снова кнопку **получить**:

![](https://lh3.googleusercontent.com/iDRLuOTscFO4BSr0F4WMpcV1s_5xprFvzotKhTig5_tdXXcSUW8YWo3rGnsgrigIVO0yKCmdTG1nP6lJk-0ZJYC2Wm5exqIPlRph2zCHLZ0WnaKm7eoWhnHCqAoqzwYTAv9THqnZ)

Eresh посчитала нам данные:

![](https://lh6.googleusercontent.com/nAG_hxyK89VgGQ64x_M56qZVcGpiA9G6VhwSPUfm6DCM7T_kMpPg919DIuIGo9g9My0Sv8bqDS-QiX3H042muENgJ2TKMDGmHFLWwVMaPADuBlpYZHl6coZeY1CIGEHdyZnNQ9vs)

ACTION - целевое действие (подписка в воронку или тот шаг, который мы обозначили переменной);\
CRA - конверсия из кликов в целевое действие;\
eCPL - стоимость целевого действия.<br>

Теперь пересчитаем все эти же параметры, но не на момент первого шага воронки (подписка или вступление), а до того шага который отметили себе клиентской меткой/переменной в Salebot.\
\
Для этого снова нажимаем кнопку **получить данные из Salebot** и вставляем название и значение переменной по которой будем смотреть срез статистики.<br>

Например, так:

![](https://lh6.googleusercontent.com/fnPWbL4b8-z5EdKAKKeSgl2bBDKaCHYNwv7bfkfaKiAw9iUkQzgDuijXqorhoXi1zaQ9L_fLYJRdq08mENxzMytiZCDHUQ8Gf5ZH7RXoTa3MWZ-bVjoO3JcXk9g5m51s2bphGwfA)

Eresh пересчитывает показатели по введенным данным:

![](https://lh6.googleusercontent.com/g0tZQnTKxyIunutTkD0r1lt_c7asq4J-1NzJNymEErz7AuRXSGTB2Y4nMAmTU8Y3sFVgGTwFvOgoJmIqS39jviAsuLzV-ERd_S1OjM0hHeE2ub7OSpe4x6BlnIS6FvzBP-cDqFlu)

### Пример

Смотрим данные по тегу минилендинга, пока без дополнительных переменных

![](https://lh4.googleusercontent.com/VhlMW1xMs4aSxDmRAZJkSUryvvX2YxogsA0nvPtScrsI2FVTIqrG5wtSoKFc_zSEkb-GoTSRRz6ciNWe7p_9FLpUBSMFwJwTStMJRggGvJNwXRwLGXsuMxn9f_w5LA3OPo46Y1zu)

![](https://lh6.googleusercontent.com/yT_bfuemnzblpVMJASEgZcxWTJaSXJhMZsO_uEBKYgGW2zELjNB-V_Dow9xPoiVP8qX6Zm_3T_obilrFnGNGUWxOFo_WBDAvS6kZt7zEuPkcMUJnX5fmyWS_RfSdlqXsvxikSBfW)

**28** человек пришло в воронку\
**150,05 руб** - цена подписчика в воронке\
**7,071%** - конверсия из кликов в подписчика воронки.

Смотрим данные по второму шагу воронки (например метка step = 2, это участник вебинара)

![](https://lh4.googleusercontent.com/mv6kLpi65hblBmLBCb57m7r1QBvzVPpRmOEW6ka1Vj0IqOeljEzxj-zTVHaljNsMT2yB91cSgHK3Pz9fpEk4TyyO9SL4ZHAJrINJv-cWMyj3MfdmrobeIkRgsd6stZF-Ov__g1hR)

получаем:

![](https://lh3.googleusercontent.com/kyQUgJNzBCGS6tcyHNgbwoKE1LFWVvPUy4oZp1nJ1afIGDrEOorBzkObb_70a_y-Ab46gCHVHchTme2Makb9PbX7EtrPGr_Dhp2KTkzIhzuNRmxdX2QogFnq7lcXny9TFBcK2fq_)

**24** человека дошли до этого шага воронки\
**175,06 руб** - цена участника вебинара\
**6,061%** - конверсия из кликов в участников веба.

Смотрим данные по третьему шагу (например метка step = 3, это покупатель)

![](https://lh3.googleusercontent.com/XnMLJEfcHRF_XDp5YKbVqoDFzAqyfRGUetAtxnxAldHxCo4PNwK0ExHLsUN4-PWo2pc4cR9vVASG1A-UQd6ipRnmIdTHf5QnAsofRu_FJcTVmJt01nYXoyMa1iWLA9oJQCp3X2vz)

получаем:

![](https://lh5.googleusercontent.com/xv8kO9MRlRwuhiUjJ-qUhCszSAsUuqjl_-hYAV5tGUfplnZuOflWDnlSSBGn-iFhqZmI3KrfGP63f8Bj7a-zNUnnVYvY4yYWzRa2zrs39aEkwe0dfP2grTyI7keoyr5vdjst9X_9)

**4** покупателя,\
**1050,35 руб** - цена покупателя,\
**1,01%** - конверсия из кликов в покупателей.

## **Как поставить ТЗ и KPI таргетологам**

Зная эти конверсии и стоимость участника воронки на каждом шаге мы можем ставить ТЗ и KPI таргетологу.\
\
Например стоимость покупателя мы хотим снизить до 900 руб.\
Вписываем в окошко нужную цифру и нажимаем кнопку **посоветуй maxСРС**.

![](https://lh4.googleusercontent.com/tary-mdMwiB7hiQDw-Nx0tga5iwa7_c_AQBshuxjHiMU-e8aMIEGzGoRiMxjQl4o3CEo51UYfFhlCf9wshmqN_BvV8xZjmYvcL8tilV1GL1OcX5BJIzfmw1MolOP8f0vpzpAROEu)

Получаем данные от Eresh, что таргетологу нужно укладываться в стоимость клика 9 рублей. Данные по предельной стоимости клика рассчитываются исходя из конверсии из клика в текущий шаг.
