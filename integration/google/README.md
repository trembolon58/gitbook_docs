# Google

## Подготовка сервисного аккаунта

Перейдите по [ссылке](https://console.cloud.google.com/cloud-resource-manager?pli=1) для начала работы.  &#x20;

1. Создаем проект&#x20;

<figure><img src="../../.gitbook/assets/image (19) (1).png" alt=""><figcaption></figcaption></figure>

2\. Придумайте название, но <mark style="color:red;">НЕ указывайте организацию.</mark> Нажмите Create

<figure><img src="../../.gitbook/assets/image (20) (1).png" alt=""><figcaption></figcaption></figure>

3\. Проверьте права доступа: должен быть уровень доступа “owner”

<figure><img src="../../.gitbook/assets/image (21) (1).png" alt=""><figcaption></figcaption></figure>

&#x20;

<figure><img src="../../.gitbook/assets/image (22) (1).png" alt=""><figcaption></figcaption></figure>

4\. Перейдите во вкладку Service Accounts и создайте сервисный аккаунт Create Service Account.&#x20;

<figure><img src="../../.gitbook/assets/image (23) (1).png" alt=""><figcaption></figcaption></figure>

Укажите имя в первом пункте:

<figure><img src="../../.gitbook/assets/image (24) (1).png" alt=""><figcaption></figcaption></figure>

&#x20;Выставьте права Owner во втором пункте и пропустите третий. Нажимаем Done.

<figure><img src="../../.gitbook/assets/image (25) (1).png" alt=""><figcaption></figcaption></figure>

Сохраните имя полученного аккаунта - оно нам понадобится при предоставлении доступа к файлу (документу, таблице, форме... и тд)

5\. После создания аккаунта перейдите в его настройки и подготовьте ключ. Выберите Manage keys.

<figure><img src="../../.gitbook/assets/image (26) (1).png" alt=""><figcaption></figcaption></figure>

Создайте новый ключ. Выберите параметр JSON в качестве сохранения.

<figure><img src="../../.gitbook/assets/image (27) (1).png" alt=""><figcaption></figcaption></figure>

<figure><img src="../../.gitbook/assets/image (28) (1).png" alt=""><figcaption></figcaption></figure>

Сохраните сервисный ключ в любом удобном месте - это “Ключ доступа”, с помощью которого будет предоставлен доступ к Google-документам.&#x20;

{% hint style="info" %}
Храните файл с ключом в надежном месте, потому что этот ключ невозможно восстановить в случае утери.
{% endhint %}

<figure><img src="../../.gitbook/assets/image (29) (1).png" alt=""><figcaption></figcaption></figure>

6\. Далее переходите к подключению API-сервисов.&#x20;



### Подключение API-сервисов. Google Drive API

Для этого перейдите в главное меню:

<figure><img src="../../.gitbook/assets/image (30) (1).png" alt=""><figcaption></figcaption></figure>

Необходимо выбрать “APIs & Services”, далее “Enabled Api’s and services” и нажать "enable Apis and services".

<figure><img src="../../.gitbook/assets/image (31) (1).png" alt=""><figcaption></figcaption></figure>

<figure><img src="../../.gitbook/assets/image (32) (1).png" alt=""><figcaption></figcaption></figure>

Включите нужные нам сервисы APi - Google Drive Api и Google Docs API (не забудьте развернуть список)

<figure><img src="../../.gitbook/assets/image (33) (1).png" alt=""><figcaption></figcaption></figure>

Подключаем. Если на этом этапе картинка будет не такая, как на скрине, то обновляем страницу “F5”. Жмём “Enable”

![](https://lh3.googleusercontent.com/eQoFWdk_n3S2NRziujCOtZx7-zbF8hjcl8sSf4LdeoYALQRY6z1-M6H_6ILMu1lvUOrfx10p45LofCnwftxEam3OI7sS1LGwiWgemFjFylQ_t2_Acq1a128lMGd0zvB3d5wQCo3a)

Подключилось.

![](https://lh3.googleusercontent.com/K4NazlTXfacgpzQ35ZxO9Blar4gy6CWs0oFmWhU07slp3lEkEvd-3pp60izzzLdfuoRvei4gPQuO_Kien_3EaVBATbbZTTgoawVEGEZdoc53JTDIHhoYxZLcMVhUvamAKE5wROe_)

Далее подключите сервис в соответствии со своей надобностью:&#x20;

\- Для работы через сервисный аккаунт с таблицей - Google Sheets API,&#x20;

\- с календарем - Google Calendar API и т.д.



### Подключение API-сервисов. Google Sheets API

![](https://lh6.googleusercontent.com/tBVfJgNGiLBPICwrup4QvL0bJHvlqiCwkyUY8q0PUKFxUmaapZtmSytzP-bA4jAgTGm0Kug1ag6_TivcFHy0sfA0zmoMIx7EFew2zHwjJq6RUQWG97AX59eA8wW2AH-2xWpjGhM3)

Только теперь выбираем Google-Sheets API

![](https://lh3.googleusercontent.com/xWZCb249ov3iPL209TIlMmxdc7S1QkP-ov-icq_ADr_nxfbdt3ikmFjztjGJEXndykxwJZZQ3f6ytfy87MIg9RwBCxonBUPR1qykZoFEbuJGFDoe49XQmVzeGOp0Ut6TLZfhkHgW)

Подключилось.

![](https://lh4.googleusercontent.com/oNKDEPfe6anIXdZFeeNzvIYRXuFio5mfoNTAPYpAfhRmpxNkMws9hEzaBSGlVKYbOHeC0zh0linHITb1_63MVpGqDXTHFLswR0IEkcq0CXOLD0dCk0G2PvU4nD9-TWmTKY5M3Ag_)

На этом настройки аккаунта закончены.



## Предоставление доступа к документу через сервисный аккаунт

1. Перейдите в Настройки доступа

<figure><img src="../../.gitbook/assets/image (34) (1).png" alt=""><figcaption></figcaption></figure>

2\. Откройте доступ к файлу (документу, таблице, форме и тд) с правами редактора. Для этого укажите имя сервисного аккаунта, который вы сохраняли на 4-ом шаге создания сервисного аккаунта. Снимите выбор "Уведомление пользователей" и укажите права "Редактор". Нажмите Отправить

<figure><img src="../../.gitbook/assets/image (35) (1).png" alt=""><figcaption></figcaption></figure>

Проверяем:

<figure><img src="../../.gitbook/assets/image (36) (1).png" alt=""><figcaption></figcaption></figure>

В дальнейшей работе вам потребуется ID файла, который мы копируем из адресной строки

<figure><img src="../../.gitbook/assets/image (37) (1).png" alt=""><figcaption></figcaption></figure>



## Предоставление доступа к таблице через сервисный аккаунт

Аналогично процедуре настройки доступа к документу через сервисный аккаунт:

Перейдите в Google-таблицу и нажмите “Настройки доступа” в правом верхнем углу:

![](https://lh4.googleusercontent.com/i_MSJuv2bHdHQGwzsLadRNGRYQs8oryC0jH8RXZuEJtmVuYcQcAn46vwMJz5Fn1_urbk1YMe3nbEeOyT5HfIubnMEWQuKxBV64ZiVfbalL5tg6sNvE2BrfM604CFQ5WqWAz5eQPM)

Появляется окно для ввода названия сервисного аккаунта, который мы копировали выше.

![](https://lh4.googleusercontent.com/FSvfypdh3wPMcFqiTK6WZ9l3dpjUPNB2WPMd2i3TywxeXEpQESm4-nr0O478RgAsa00LhsSBHSj9mSLT3_KP6TQOXBeCZu_RFxF_9tknJFLi5EFOpw57kg-AHVQ_cPoM0ZijppiQ)

Вставьте название. Уберите “галочку” Уведомления, и проверьте, чтобы было выбрано “Редактор”

![](https://lh5.googleusercontent.com/SuvE3mstbzFCVaOoPX2Q5LkcWWSwJ1xnJnGp7itL6Kkbvourgq51kqbddo9C8pcMeWahxADcAdKh1PSlov4VOIgT8AimBy2QREVuWhn61_D1Wopl7g_KVJNy6YySbRwzPjJkHvmc)

Нажмите “Открыть доступ” и проверьте на всякий случай

![](https://lh4.googleusercontent.com/9DOXwAcZ-T9v7tXKLWjRR1hjCg5dFafYL-PYpJZlA-qCWBQYKhAD3gKe8QdrmTJwdxHfmRjS1OMHPWx86ZXGac844zgZhDw9FufBTIeKkqwshdNyXXpO3whRf2KiZtQ8nEl6YdNn)

Теперь скопируйте ID таблицы. Оно вам пригодится сейчас.

## Предоставление доступа к файлу (документу, таблице, форме и тд) для бота из проекта Salebot (подключение сервисного аккаунта для работы бота)

1. Перейдите  в свой проект и создайте серый блок - "Не состояние"
2. В настройках вложений прикрепите файл сервисного ключа, полученный при создании сервисного аккаунта. Сохраните блок.

<figure><img src="../../.gitbook/assets/image (38) (1).png" alt=""><figcaption></figcaption></figure>

Откройте вложенный документ: для этого щелкните на иконке документа. В открывшемся окне заберите ссылку из адресной строки:

<figure><img src="../../.gitbook/assets/image (39) (1).png" alt=""><figcaption></figcaption></figure>

3\. Перейдите в настройки проекта и добавьте переменную docs\_json\_keys в константы. В качестве значения укажите скопированную из адресной строки ссылку в формате \[“ссылка”] - в нашем случае значение будет следующим: \["https://files.zmservice.ru/uploads/message/file/48/dynamic-mystery-367310-0377023 d3e26.json"]&#x20;

<figure><img src="../../.gitbook/assets/image (40) (1).png" alt=""><figcaption></figcaption></figure>

Нажимаем “Готово”



## Как работать через свой аккаунт

По умолчанию конструктор работает с собственными сервисными аккаунтами для доступа к вашим таблицам, поэтому вам необходимо выдавать доступ на редактирование по ссылке. Чтобы обеспечить достаточный уровень безопасности, вы можете передавать json с аутентификационными данными.&#x20;

{% hint style="warning" %}
У гугл-таблиц есть лимиты на количество запросов в единицу времени. Чтобы не зависеть от лимитов, вы можете использовать свой аккаунт.
{% endhint %}

Каждая функция по работе с таблицами принимает creds\_path - необязательный параметр: путь или url к вашему файлу, содержащему сервисные данные для авторизации в таблице.

Самый простой путь получения такого url - загрузить файл с данными в конструктор.&#x20;

Для этого нужно создать блок первостепенной проверки условия, в условие которого вписать любой набор знаков, а во вложения - положить файл с сервисными данными (как его получить - читайте ниже), включив вывод ссылкой. После этого вам будет достаточно в тестовом чате вызвать данный блок - он в ответ пришлет вам нужную ссылку.&#x20;

{% hint style="warning" %}
Чтобы файл даже случайно не оказался у посторонних - после получения ссылки измените тип блока на состояние диалога.
{% endhint %}

Останется только скопировать ссылку из тестового чата и указать ее в параметрах запроса, передавая полученный URL в параметре creds\_path (подробнее - читайте ниже).

Например: \
`{"id": "id таблицы", "client_type": "#{client_type}", "show": "количество результатов для вывода", "creds_path": "УРЛ_вашего_json_файла_с_ключом"}`

### Подготовка сервисного аккаунта

Перейдите по [ссылке](https://console.cloud.google.com/cloud-resource-manager?pli=1).

Шаг 1. Создайте проект

![](https://lh3.googleusercontent.com/9He2ARNX_3TVno8HVGVBLlnYaJB6pbMVnQHNDi9eXHUn6zJ9jRsLRWobCCn_S7WLr9xZtByTlWUC1a3Cjt7_yXBpINSVZ5bLkpZj5UB4R_9jGXmxvkT5v096yx6JTiqJ631S1_vg)

Необходимо придумать название для проекта:

![](https://lh6.googleusercontent.com/xCWJa-7Jn5TVBDR39iYwTdqfWy67SA6e0yEuq8TUk5IUyYMDUBBE9rEtwBpvxFNdcElAonAYWRKFB0kYFyK2A9MZGXfddB7iSVEN3cc2GVWCzXPDDowoJapewS7TsuSaQO2g9OYu)

![](https://lh6.googleusercontent.com/P5P5uq5m9w7wfvfyFd7M7n19uJW7vCVuli5pDhv1Y0Lib7v82cDjLTdUzVwqYP0KYu48DSkJQmORqrpBvU6d2olBdPcpHKMyiyTCaRrpVJEnXyfsO7bxa8yM_MCV3fYkAI65M08j)

Перезагрузите страницу, нажав “F5”

![](https://lh4.googleusercontent.com/mBBazgw3WpZtUaLTK5PoB23XyI-KcoKNgj8WYqBtq1uonidT3HmV6kIgnMNPbieRBlbh7vXEPFhQEua2_LoaAYBZGQqV6bQ8ntVlywDCVWtZGHztT6qW2tQ7ZzprTVmkMl7hIxIh)

Шаг 2. Проверьте права доступа. Должно быть Полное -”Owner”

![](https://lh6.googleusercontent.com/T4lzJAl5iKhs2C2tX_qLX5moikjcByZuv85w0Dl2xZ2MlHPyJk557oLLKkdDG68a6JUsY4tbUpD6aY3eitEewprSAWHEBxEZ1yDN1KK8-gKKJVf4kwBPCCHzoGneftybm9LpbzKm)

Шаг 3. Теперь перейдите в “Настройки”

![](https://lh5.googleusercontent.com/4W-_xQYOs2OPmbgpe-B0tYbkAnM7ZXveyMEKiwoel9df90svzx5Aa_7L-ApANlob38yGba_psuk3WQB0eVrFedp6_7ibB-TqfMZ6rgtPGi2yJF7E3mdurKCca90UZ79hz4UMX6zh)

Найдите вкладку “Сервисные аккаунты”:

![](https://lh4.googleusercontent.com/GN4Q6OPwRWD6XAPZx3m1G_L08D5cAkwBJaOY8Vz5XhKAJy7B3GKKtCY1LSm8JNlVlV4UPcWoLE5MzIMpu9ptkezaoKebca0jMB74AROV6DTDBrxrEsmx4cAqj2_Vriw4C216DUcC)

и создайте Сервисный аккаунт:

![](https://lh5.googleusercontent.com/wnQwK9s0nUDFuxrr1s8bAFEKCjfb993gaEETgXRzFRMUMLIDrAMcDsz0DXzU1saP1JdMtTYPXmVKMwXg6MDA-hUXh9i9L686y-b3gPq0w1V33Z_BLqu98jVKo8vq5i_CUghp0tfB)

![](https://lh4.googleusercontent.com/r-8LvBATeOpbI0VyYOs7nEdZdhuwiYnBilSJDOh7d6bOvQ94GtEAgwIDDqADIEEqjb9QlQVLNENbdqPWc17UMNkfTu4dVh3CMX8PkM-jXyax7D4LmS7brZ_0adjT7g7spNtlUD2W)

Придумайте аккаунту любое название и нажмите “продолжить”

![](https://lh5.googleusercontent.com/naT1s3Z2r7cjZiW8ACkDF59SdUVKOXDJWc82jaqIXcW7kSzfy9iFNmrTgmJ4lzV9X_26Lg0Aq_hGETRVsi8wpPB4kEuMoC0RFWlWmETzB2KEoeVvxUGIotbEi-yt3Vy38XCjfZea)

Шаг 4. Далее выберите “Роль”. Она должна быть “Owner”, т.е. “Полная” - Владелец.

![](https://lh5.googleusercontent.com/AiBQwCGU_Qsc2S7E6mKp_n0vHjnnK0PkMkhJj_dPW5dSR7p734BHMFal14Ve29mqkc8X_Z8UrgTsYUFnGT1oN3hkJ3KhNCvdZYOd-MOy4KREHg_Wm_TKC6U1YD1UhkNFkdF7n_Ho)

Нажмите “Продолжить” и далее “DONE”, т.е. “Закончить”

![](https://lh3.googleusercontent.com/POheYX0DaUTqAfi5kRDT9wGCZDIcwdlT8FFCeauKBcq0VZzxW7TrF1T8fpdY7aVQ5XLYRWFmPXkJgi5KKEbtoaHl_rrj3wM1_p0fPP1VgDcY85HrmjqAjuIc1xIljHKLE9So9EPr)

После вы увидите созданный аккаунт

![](https://lh5.googleusercontent.com/XjoW-ihXoiz4_SJrSEC4obeU9bBYer81FSTq2Rs9LNfiX3JR5i6C-IccOu9Vye3tqs8x5N8WpcjmOXAbUkKo6wWYESKMMJNPoAc9G_7EGDRiYUypI7EB3DvGdwtQGChXjzcFh_uC)

Шаг 5. Скопируйте свой адрес сервисного аккаунта.&#x20;

{% hint style="danger" %}
ВНИМАНИЕ! Обязательно сохраните себе его название. Оно понадобится нам в дальнейшем.
{% endhint %}

![](https://lh3.googleusercontent.com/rROGe163yoNO4-kCEm6J2Z_ZyqC9JkkdwVkYiCYAIvNY8RJw7zlzyqKQ168AOI4HS1ehLdTcycWJ7znjbc3m1CEuZTF2D-9qYlYM0FjwGe-Mp98h8NbfDcpmDNlHb8nKfDMyOUvf)

Шаг 6. Теперь необходимо создать ключ безопасности. Жмём на 3 точки и выбираем “Manage keys”

![](https://lh4.googleusercontent.com/Cp_IbTdhF-zdWKMz-C_AP0NI0E70VnHV0Yfn2D2GZeXpR2mz8BumW5g0w5iGYFZd2JrFKuA5hpZOHIXvk5yjznZBieXKCAq8Q5IOmYt5YS6PHgwunrxMPZDUHzOHd6lJtNy2GgCN)

Переходим в “Keys” “Добавить новый ключ”

![](https://lh3.googleusercontent.com/ru9w7kZihQnNNnlH7lgLxrqyZLiWh543A9eZVYaSAx7LyXpawUevB8POq4H3FG_249WUMiOwxoyhyq5avYiopLHEbf45vWnVBQCP15FXPq7lTMGn8vAeSZYuyWY8pGJpqUQcibZw)

Создаётся закрытый ключ для "SaleBot\_1" Скачиваем файл, содержащий закрытый ключ.

![](https://lh4.googleusercontent.com/V2GqfB2eniKJ91PUr9kHtKJS18w_deMcNJrPuMaPeWfiaXe58EubngSRMtkbKxFhmUCXNIhC_6_YR8YMz8zrFf1AvSGGnOOCyv6Fbwx0gZmb7EtLrndQHvzADzsVm8s1k7X98DMp)

Скачайте ключ куда удобно. Главное запомнить куда. Это “Ключ доступа”, с помощью которого в дальнейшем будете давать доступ к вашим Google-таблицам **Храните файл с ключом в надежном месте, потому что этот ключ невозможно восстановить в случае утери.**

![](https://lh4.googleusercontent.com/6eXAUb1M2gONE5BxU1FSttsfqvBa5VS30MAPiVxzUspESkDv21JQcCjDdkD3efcL6pbOfPbz7Jl0gRf6mWcpP6y4GTQbEHNzgD3SL-pq0WZ-OlOeNrHiNxXddzZho_9u4JV4uXMP)

Шаг 7. Теперь необходимо добавить API-интеграции. Для этого заходим сюда.

![](https://lh5.googleusercontent.com/vU023G2LQGSFZNTADW2Zh8qiZ0xnFZmN2vMCmd7VDBHGVCF3A5bzKmY28TRnIWvDRPTtKDXWQs-C5rf9YdJdf6SsP_wvD1qRkiBbekew5qbMZwf0tSZg6zgOFQHwoxevnJtjM1O4)

Выбираем “APIs & Services”, далее “Dashboard”.

![](https://lh4.googleusercontent.com/xn_ak0PnKZtrpiHWfQw_wzaBe70WMJF4AsatS4DR06WYo7Bw0H1Ivmx2EPERytbKXrIgsdz9_uoINv3RPZhPIxY_j_kOexmtlQaKrodNlM5mOq4OdVuC1StbUBXw6ta7XoUJZQOm)

Это “Доска”, на которой можно выбрать подключаемые сервисы: мы подключим два. Это Google-таблицы, и Google-драйв. Нажимаем “Подключить API”

![](https://lh5.googleusercontent.com/96wJDBqC3q6c3iasL0E60EIPL4g9Cn2asNsTLrOicZr-XWLYv6RCk0h57rMdvGvOeK3LS2SySZlWJqfXbQefiGPanyeANhiKfX3v3REucozLuHCQav_FFUJmOEXp2CveSr5O689C)

Можно выбрать в Поиске, а можно найти нужный сервис, прокрутив страницу ниже

![](https://lh4.googleusercontent.com/6WKIwu50XPoUNRWSB7P5bbMnqnRXxunuDbwYC3LNoPSAIsZNIs032ekiRcXAlhoMH3kBbVwwzuINT_4WmnYZ-6-Sn_uNs752TkZ2qfuWOTqg_TvBTZVQBl8FvCC6BfBoV-a7HO9n)

Подключаем. Если на этом этапе картинка будет не такая, как на скрине, то обновляем страницу “F5”. Жмём “Enable”

![](https://lh3.googleusercontent.com/eQoFWdk_n3S2NRziujCOtZx7-zbF8hjcl8sSf4LdeoYALQRY6z1-M6H_6ILMu1lvUOrfx10p45LofCnwftxEam3OI7sS1LGwiWgemFjFylQ_t2_Acq1a128lMGd0zvB3d5wQCo3a)

Подключилось.

![](https://lh3.googleusercontent.com/K4NazlTXfacgpzQ35ZxO9Blar4gy6CWs0oFmWhU07slp3lEkEvd-3pp60izzzLdfuoRvei4gPQuO_Kien_3EaVBATbbZTTgoawVEGEZdoc53JTDIHhoYxZLcMVhUvamAKE5wROe_)

Теперь повторяем тоже самое для Google-таблиц.

![](https://lh6.googleusercontent.com/tBVfJgNGiLBPICwrup4QvL0bJHvlqiCwkyUY8q0PUKFxUmaapZtmSytzP-bA4jAgTGm0Kug1ag6_TivcFHy0sfA0zmoMIx7EFew2zHwjJq6RUQWG97AX59eA8wW2AH-2xWpjGhM3)

Только теперь выбираем Google-Sheets API

![](https://lh3.googleusercontent.com/xWZCb249ov3iPL209TIlMmxdc7S1QkP-ov-icq_ADr_nxfbdt3ikmFjztjGJEXndykxwJZZQ3f6ytfy87MIg9RwBCxonBUPR1qykZoFEbuJGFDoe49XQmVzeGOp0Ut6TLZfhkHgW)

Подключилось.

![](https://lh4.googleusercontent.com/oNKDEPfe6anIXdZFeeNzvIYRXuFio5mfoNTAPYpAfhRmpxNkMws9hEzaBSGlVKYbOHeC0zh0linHITb1_63MVpGqDXTHFLswR0IEkcq0CXOLD0dCk0G2PvU4nD9-TWmTKY5M3Ag_)

На этом настройки аккаунта закончены.

**Шаг 8. Теперь переходим в Google-таблицу.**

Нажимаем “Настройки доступа” в правом верхнем углу

![](https://lh4.googleusercontent.com/i_MSJuv2bHdHQGwzsLadRNGRYQs8oryC0jH8RXZuEJtmVuYcQcAn46vwMJz5Fn1_urbk1YMe3nbEeOyT5HfIubnMEWQuKxBV64ZiVfbalL5tg6sNvE2BrfM604CFQ5WqWAz5eQPM)

Появляется окно для ввода названия сервисного аккаунта, который мы копировали выше.

![](https://lh4.googleusercontent.com/FSvfypdh3wPMcFqiTK6WZ9l3dpjUPNB2WPMd2i3TywxeXEpQESm4-nr0O478RgAsa00LhsSBHSj9mSLT3_KP6TQOXBeCZu_RFxF_9tknJFLi5EFOpw57kg-AHVQ_cPoM0ZijppiQ)

Вставляем название. Убираем “галочку” Уведомления, и проверяем, чтобы было выбрано “Редактор”

![](https://lh5.googleusercontent.com/SuvE3mstbzFCVaOoPX2Q5LkcWWSwJ1xnJnGp7itL6Kkbvourgq51kqbddo9C8pcMeWahxADcAdKh1PSlov4VOIgT8AimBy2QREVuWhn61_D1Wopl7g_KVJNy6YySbRwzPjJkHvmc)

Нажмите “Открыть доступ” и проверьте:

![](https://lh4.googleusercontent.com/9DOXwAcZ-T9v7tXKLWjRR1hjCg5dFafYL-PYpJZlA-qCWBQYKhAD3gKe8QdrmTJwdxHfmRjS1OMHPWx86ZXGac844zgZhDw9FufBTIeKkqwshdNyXXpO3whRf2KiZtQ8nEl6YdNn)

Теперь копируем ID таблицы. Оно нам пригодится сейчас.

![](https://lh4.googleusercontent.com/iMhHw0CsRjwsKzImUGITFRK4pSKhm9jcpau4KVAiaQ_4LpD3Cm8R8nwKczB7D5szHKyWru0DwEqL5S4YYqDu6oxAVT7qXxXj5qvjmeGph20A-UDDa0iidhLCK0hHlGmqCalMxY18)

**Далее необходимо перейти в конструктор SaleBot в свой проект.**

Создайте блок с первостепенной проверкой условия. В условии напишите “ключ”. В настройках вложений выбираем файл ключа, который мы сохраняли выше.

![](https://lh5.googleusercontent.com/o4TFnIEavF7SFFgIUCgMD-5SK3q8ywzEeDDfz3-0Qb8aBWvgCV-nOaNbOcGmodoLPA2AMYznPQgoPkYGuk5omzokTsj6qPWz_r0GpSFJ3XF3Ygm1-uu4X9EDydgUwIY6S3TqT3y4)

Обязательно сохраните. Перейдите в тестирование бота: набираем ключевое слово, которое записывали в Условии (в нашем случае “ключ”) и получите ссылку:

![](https://lh5.googleusercontent.com/kPhZjUwY9Puu_i4HfBrpdE0tXxaJ_p_UCPr6_NcFnmkjVYjEUtyhBQSY2bt2yw37CPWp0zW6XmPhqlPXdaxpecTDHvh2HvOM8q8t3w17oeropDexj2bb53wSrfzyQkaju0e9pX2b)

Скопируйте ссылку.

Теперь необходимо сделать запрос в таблицу. Создайте ещё один блок с первостепенной проверкой условия, который запускается по команде “старт”. В тексте сообщения выводим переменную #{custom\_answer}

![](https://lh4.googleusercontent.com/KEhcoO0xZWPo9ogn4wb9UmcsvZzQFdUsckGzo7CNsYiqUqaA3G464riG5ZBqIeBdcVIhNPrKkB45sVc5rC8V8XkbUHtvzWLfNm9PRWh_BoHzAXCieGLHtYOZe81zkp7Ht92Bb33j)

Сделаем запрос “mapping”, т.е. построчно запишем некий текст.

Формируем запрос

Выбираем Post-json, а в поле "JSON параметры" записываем параметры запроса:&#x20;

&#x20;`{"id": "ид таблицы", "mapping": { "a": "Проверка" }, "list_name": "Лист1", "creds_path": "Путь к вашему файлу с данными для авторизации" }`&#x20;

В “creds\_path” прописываем ссылку, которую вы получили при тестировании, когда набирали стартовую команду “ключ”

![](https://lh3.googleusercontent.com/hI-_VNBM9hkh5W-MS0i_Kui843W9d8tU5rD15MQI2YcxQrhYxHtgJIpTeNXQ_wVCYd7kwUpyCyUTnuGxTP96dnUy4lIlxH4abuwO5-7q8Ub1mClqlcq1RqTHa7GfXeUCmLV_wroh)

И вставляем ID-таблицы

![](https://lh3.googleusercontent.com/BqehTWGiaQo6Eo-ejFPKrDm-2sAlD4VShDnrTnSyPDG1cqTgklNnNibjVESPKKWomjPNVoTGoSa1-iNA6inevXmvckjoQ5obqUKPI3Y2vQcSIpC8MEuJAhCMjjXCUF4VIz2OkWaN)

И вставляем это в JSON параметры. В url запроса прописываем функцию из документации для функции mapping

![](https://lh4.googleusercontent.com/TFsGEhSCxtsJN6WIJ2pHVJm9hxcpyI_X0SDqt6Y6YNq_9XOlivkaBqR5QJ6qDv9Blk8_ZRFi97T6AZVosdsY-RQ0SoiF77wVzNakUjXEWHYI0wgPLbJ7Tu0Oedr_EThYw_k2jGyT)

Обязательно сохраните новый блок с настройками.&#x20;

Теперь протестируйте. Наберите команду “старт”:

![](https://lh3.googleusercontent.com/xhnJ9Y-p6dokcHMuGkz5M0AZNlwszRzQm1_MYaqyV9u-gM2XXjqybaX_HsfY8QWsb7XCh4zTtIyppn5aQC7ipRFkQDAEiREgdW4h2k_mHt4SW7NZy5YAwZbZN8Ruv-n58AkBxhaf)

Вы увидите, что всё работает. Наш тестовый текст “Проверка” записался во вторую строку. Проверяем таблицу.

![](https://lh4.googleusercontent.com/TqB_zmrnJ7B8TJJl_QJeZ_619-Ppwobq_Vqr3Mb3vVkltTcEdQ-pyLi7rx4-bgdC1Zd8hTwAIXkpo-kgUN2kWWRoKZa77OyCO6AiPlvR2mYRev-IT2IR7rOWizYJLIgXLed1s964)

Всё нормально записалось. на этом Настройка аккаунта, и тестирование закончено.

## Видеоинструкция

{% embed url="https://youtu.be/zlTcojOvdvQ" %}
