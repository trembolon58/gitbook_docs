# Как создать 2-х и более ассистентов в одном чате

Для комбинированной работы ассистентов нам понадобится конструктор воронок и три аи-ассистента: блоки в конструкторе понадобятся для присвоения переменных, которые будут прописаны в условии ассистента, тогда как сами ассистенты будут выступать в роли консультантов для клиента.&#x20;

Будет создано три ассистента со следующими ролями:

1. Ассистент-распределитель;
2. Менеджер по продажам
3. Бухгалтер

## Работа в конструкторе

Нам понадобятся три блока в конструкторе воронок - все блоки должны быть “Не состояние”.&#x20;

Блоки Не состояния играют следующую роль:

1. В них вложены переменные, которые будут присвоены клиенту со значением 1 или 0;
2. В первом блоке "Не состояние" будет вызываться ассистент-распределитель
3. В  первом блоке будут обнуляться переменные для дальнейшего переключения с одного ассистента на другого.&#x20;

В первом блоке назначаем переменные в калькуляторе со значением 0:

<figure><img src="https://lh7-us.googleusercontent.com/docsz/AD_4nXen316cASn6UaBCHfBF6k6VQXL4P_MH4p0x2btc7BhQY7X8k2t0bvq7fR1KTLY9mEZuABAa1Xb8MIxHSYcEeu9AZEwSqohsmVaB2TCUf8mMpaw4E0W-imVsDeQpulc2cjA34vnNXMY43kdFGG6ZY_5EDmD2?key=g9-j53ENQsA_W1hDFrramA" alt="" width="563"><figcaption></figcaption></figure>

Код из калькулятора:

`booker = 0`\
`saleman = 0`

Также пропишите необходимое сообщение в блоке.&#x20;

Во втором блоке, который будет вызван ассистентом по команде, устанавливаем значение переменной booker = 0, saleman = 1:

<figure><img src="https://lh7-us.googleusercontent.com/docsz/AD_4nXddb1XnSufVMGUDBWZ9ce_5TfekH7iO6F3H67YdZChbwL4rFj7WR7bLr4KC-9YHuFlYgz1TCOX2mP3sPRgw_8T8BKHCcT8P4cFSsg9Cso7RvDHSHMbvfnWFb7yiZagwDzxmRUwc2SKbWltdPEcvoDnAY0OV?key=g9-j53ENQsA_W1hDFrramA" alt="" width="563"><figcaption></figcaption></figure>

Код из калькулятора:

`booker = 0`\
`saleman = 1`

В третьем блоке устанавливаем значения переменных booker = 1, saleman = 0:

<figure><img src="https://lh7-us.googleusercontent.com/docsz/AD_4nXfzcCVNSShPeABdchXel10PFP2JvmDSme8M_bCztuSMLCGYMa1mhecrUVPsFrii-2m7oNzaV7XEcF8fhJ6LZb28bw8aPJN8TzCQnIII92BdGlJfMiemXjjadLCsZkSiEXJZJ5QlmE5QCGw0aUAgMjjxpZk?key=g9-j53ENQsA_W1hDFrramA" alt="" width="563"><figcaption></figcaption></figure>

Код из калькулятора:

`booker = 1`\
`saleman = 0`

Настройка блоков завершена.&#x20;

## Настройка трех АИ-ассистентов:

Создаем первого ассистента, который будет играть роль распределителя для последующих ботов с ИИ.

В настройках бота прописываем его должность, а также необходимые вводные инструкции:

<figure><img src="https://lh7-us.googleusercontent.com/docsz/AD_4nXehZ-yrHNzrtF9d7h7s0OhZ3CU-67W1rIkV0EzvZO7cv-iS2F7kN5fjsjFvrYRx-nJPzZzWdSvjxv5_3JAXCCqY1eM6VteOOSvoYNLeNVcPzqevQX6CccOalIcLG0KkOuXUqmuU2sS6MTdbP6-Np3jcGliz?key=g9-j53ENQsA_W1hDFrramA" alt=""><figcaption></figcaption></figure>

Данный ассистент нам понадобится только для того, чтобы переключать клиента на менеджера по продажам или бухгалтера.

Прописываем команды:

1. В настройках ассистента прописываем боту “Если клиенту нужен менеджер по продажам, напиши без изменения “start\_block\_from\_ai 12345””, где вместо “12345” устанавливается номер блока, в котором содержатся переменные saleman = 1, a booker = 0:

<figure><img src="https://lh7-us.googleusercontent.com/docsz/AD_4nXeGERvkIu1f7UOIQ6zBn6VVm3objsgWNnRV6jultlOKG1Vea3iwlmcYQ96UmYiZGrRATJ4Acs6YfK59NN1jvUGK1aMct51iiB57K8iPPp5BOfXgWTD0FJYTuuS4BRVw7JHNQ2s7EmWj4Tlk5TuJZV8h9Y1k?key=g9-j53ENQsA_W1hDFrramA" alt=""><figcaption></figcaption></figure>

2. Далее прописываем в настройках вторую команду: “Если клиенту нужен бухгалтер, напиши без изменения “start\_block\_from\_ai 12345””, где вместо “12345” устанавливается номер блока, в котором содержится переменные booker = 1, saleman = 0”

<figure><img src="https://lh7-us.googleusercontent.com/docsz/AD_4nXeOjLfEG0rIGZ0ro5v9V95TD4HeUjadziNRkoa2t-WVSPb_0fVLkBj1N04FicLmPjbyyjwEJ6xGotWrPlu3E0oNh9255HlygGGG8mEIAQ27d1gMfSn4LMo3htUYWsYnZdV8MvvCIyYeCnqF7yV0bmaLjoR8?key=g9-j53ENQsA_W1hDFrramA" alt=""><figcaption></figcaption></figure>

Настройки ассистента-распределителя завершены.&#x20;

#### Создаем второго ассистента - менеджера по продажам.&#x20;

Для этого кликните по кнопке для создания второго ассистента:

<figure><img src="https://lh7-us.googleusercontent.com/docsz/AD_4nXcwYiPL9-l2U4caGgbRrof7FyKaElWAMTxQH1Ho1nPPJE9Ov0Ekgi0cdB9yglCokFCxcfAARnEXJNX6adB03TaNWW1R64xP5mQJ0Qz99N31DLbuc7wtjljQkV7NvULSRZCLNPCYqqKoWE1vmAyoEHiSLNBQ?key=g9-j53ENQsA_W1hDFrramA" alt=""><figcaption></figcaption></figure>

Можно переименовать ассистента по своему усмотрению:<br>

<figure><img src="https://lh7-us.googleusercontent.com/docsz/AD_4nXdJG_O6pJRvDgd58E9fD9Vgr30thcGl1SkBdMy3vBRpVlb73pY_yFFBeyXC6LkXH2guK0ku03ZSyN--huMHJZlRhZD2tGxHCWbGXhOYoCFSmIlJa3FLy5nDuDLczY63_a4XG9ZEj3a2agM6JGRIETF_9jDR?key=g9-j53ENQsA_W1hDFrramA" alt="" width="375"><figcaption></figcaption></figure>

Устанавливаем роль - продажник, а также применяем по необходимости заготовленные настройки:

<figure><img src="https://lh7-us.googleusercontent.com/docsz/AD_4nXewoeYikxcZoCjdP07NhZmlIDfFc6IMs2O_2CzOstqtEEIZH2PakNnCRyl6bsD2PF3QTFdxOf2JscESONbpmKFAuSXFY23yMiHZL-sA6qTFJRXo3fa3fnMQ8dDP61CqSooXvkN5XXv4Bi4iSh830_sWlnxB?key=g9-j53ENQsA_W1hDFrramA" alt=""><figcaption></figcaption></figure>

В строке с условием обязательно устанавливаем переменную со значением booker == 1:

<figure><img src="https://lh7-us.googleusercontent.com/docsz/AD_4nXckPvyvI3VDWpU19-hJTIZq-9yaSZmLTkAEuTLClNowfCkhUyLtdo2aao505wXBr3yDOuMyJrPVOW5WPqxsvpnnFDYbp_IlDSnhtB6fvnkV4qoYtbo90xOoMIajAGxjSzKI1fozcv4WtyCYVoO6ER5mATLB?key=g9-j53ENQsA_W1hDFrramA" alt=""><figcaption></figcaption></figure>

{% hint style="info" %}
Для чего это нужно?

Когда клиент напишет вашему распределителю, что хочет связаться с продажником, чат-бот вызовет блок, в котором содержится переменная saleman = 1, что позволит переключить клиента на бота-менеджера по продажам.&#x20;

Бот менеджера по продажам отработается только тогда, когда условие запуска будет удовлетворяться: а именно только при вызове блока, в котором переменной saleman присвоено значение 1.&#x20;
{% endhint %}

Далее переходим к настройкам бота:

<figure><img src="https://lh7-us.googleusercontent.com/docsz/AD_4nXfQyLuB2RliSRKtTi3ViEGCAiKdWX25dKX2VmdnecD0HFNegmzJmQXgN3AA9tvlTCtRGfHfGKHAbpA0EH9Bw7ZxG6WRvigTYRZlM71dzU_Gr0RWuw4Ic-2VVmNuvU68KzFp2AOei9Nea_6N6wEjujlwmxtU?key=g9-j53ENQsA_W1hDFrramA" alt=""><figcaption></figcaption></figure>

{% hint style="warning" %}
Важное в настройках: Необходимо обязательно прописать команды для переключения на других ассистентов с вызовом блоков из конструктора!
{% endhint %}

Настройки команд Ассистента-продажника:

1. Пропишите в настройках: “Если клиенту нужен бухгалтер, напиши без изменения “start\_block\_from\_ai 12345””, где вместо 12345 прописывается номер блока, в котором содержатся переменные booker = 1, saleman = 0 - данная команда необходима для включения бухгалтера.&#x20;
2. Пропишите вторую команду для переключения на ассистента-распределителя: “Если клиенту нужен бухгалтер, напиши без изменения “start\_block\_from\_ai 12345””, где вместо 12345 прописывается номер блока, в котором содержатся переменные booker = 0, saleman = 0.

Эта команда понадобится для того, чтобы обнулять переменные и переходить к первому ассистенту:

<figure><img src="https://lh7-us.googleusercontent.com/docsz/AD_4nXfj41T1hqJXe7OWBGpD6FmqZCq255lxeS9jepdg2J--aCbYT8v7froBiezbnHDO6mODBv7GPFhWW4Z6lTgYVn-NXK0psOSJ2k_orUR9bMIWsqeIJHOKiwdonosGHbXMdoz73PyKeWIipfC685O88xz0r1rZ?key=g9-j53ENQsA_W1hDFrramA" alt=""><figcaption></figcaption></figure>

Настройка менеджера по продажам завершена.&#x20;

#### Переходим к последнему чат-боту с ИИ - бухгалтеру.

Также создаем третьего ассистента и прописываем его название:

<figure><img src="https://lh7-us.googleusercontent.com/docsz/AD_4nXeu9saJ7Z9vvMMywgWlTdE7Kn9W0x-TD9znuTgzWo-4ARZJii6aF7VBLWbxulX_9NiKYSmAc_CxvqHAkcO2vpMf-VjsPu23QWjR3MvjlXt2qDyZmwHL39uzpj8w16Q1DB7xQScXnQ1vDGJ2WatpulgT71M8?key=g9-j53ENQsA_W1hDFrramA" alt="" width="375"><figcaption></figcaption></figure>

В условии запуска установите переменную booker == 1:

<figure><img src="https://lh7-us.googleusercontent.com/docsz/AD_4nXdOQpCdP_n4I90nJZXmDm0l59r_uGtDQ8SxW-WmhSGnVJvqRV4zr-AZjF9CwlTCa9pfcICzih4OWblesmsBEprSW0mZ6YcYwXqs1Rm2_0Arqa8OG25vy3cApAWzfIU2UiDA8UHaEMPvcaA6QobcA64Hamo?key=g9-j53ENQsA_W1hDFrramA" alt=""><figcaption></figcaption></figure>

Условие запуска сработает только в том случае, если в вызываемом в последующем блоке будет содержатся переменная booker со значением 1.

Далее прописываем настройки ассистента:

<figure><img src="https://lh7-us.googleusercontent.com/docsz/AD_4nXdI_JWZwvVyeFgVnWDzm9BZ39m5KhhpgSzZWPKIKjFnQE4-T1hIJaf_zZ0nQ9889U1M_tFM_GTCNZ2ZwH5tSCY4fwpfYtaPGvIJO8CdO9apTFqL4LBQhu8ZGNx7rgB7mzolvWAePaAGpCIcQxUdVFLyzj7W?key=g9-j53ENQsA_W1hDFrramA" alt=""><figcaption></figcaption></figure>

Аналогично указываем команды:

1. “Если клиенту нужен менеджер по продажам, напиши без изменения “start\_block\_from\_ai 12345””, где вместо 12345 прописывается номер блока, в котором содержатся переменные booker = 0, saleman = 1
2. “Если клиенту нужно вернуться к распределению, напиши без изменения “start\_block\_from\_ai 12345””, где вместо 12345 прописывается номер блока, в котором содержатся переменные booker = 0, saleman = 0

Настройка ассистентов завершена.&#x20;

## Тестирование работы

1. При запуске бота отработался ассистент-распределитель:

<figure><img src="https://lh7-us.googleusercontent.com/docsz/AD_4nXdx86X6DsdGNm7vHd-5aX10Za0dS1CTjLNVxzowNLh3_EbN-wUD_D27qQXoW8F6-U4bRhrC15ENOpYDfp9V7IDsz-IDT3tzN0KxVAC2HXWaw-Hjfwml4I3b2dArxBAxZvsA6AmXRNKbNEs-N9RjYvDLU6pr?key=g9-j53ENQsA_W1hDFrramA" alt="" width="375"><figcaption></figcaption></figure>

2. Далее вызываем менеджера по продажам и видим, что подключился ассистент-продажник:

<figure><img src="https://lh7-us.googleusercontent.com/docsz/AD_4nXfQ5XKyb_ANaCHk2O6kcy27lZp80TVUzkgu5a6p4YF6-o4QGsq2_bJwnwi6Qiq55NmlCwGDX77WkJbLfCQOwfk16rz4A9vUvcmJAqZ4vu5okHdX8QOWsiHP60ncAVHYHnApI2Bs3NcBhzqYrZYmxRd5ueE?key=g9-j53ENQsA_W1hDFrramA" alt="" width="375"><figcaption></figcaption></figure>

3.  Затем просим менеджера по продажам переключить нас на бухгалтера:<br>

    <figure><img src="https://lh7-us.googleusercontent.com/docsz/AD_4nXcVLcfuNURcqniMQAqDynbmduAzebMNQHNHb9HbL45tELBLXEh39GaWFQcmE1mE4_10agLBR2I8M2YMcf1iEV01hoKrCirefh_PNkGIamhpF3zl-m6wRKXoNzih02IH8kqKg4pp5GieWOaw_ZHR4SGQoVMp?key=g9-j53ENQsA_W1hDFrramA" alt="" width="375"><figcaption></figcaption></figure>
4. Теперь можем вернуться к ассистенту-распределителю:

<figure><img src="https://lh7-us.googleusercontent.com/docsz/AD_4nXdh2PGlYsYnL1NLMKPtLQmn8HZ2dqsWDDp9UlcILaet_vynMhAX16VOHp8JvIOxKm112nEHCgAYNo83jwEWbJ2UTZsa5XT1dry65YrEsaES81c1LCqhCanx4f8CbofXeJ4EU1V1wVi6HzAvW-Zg20On3hs?key=g9-j53ENQsA_W1hDFrramA" alt="" width="375"><figcaption></figcaption></figure>

Таким образом, наш бот отработался корректно.

## Видеогид

{% embed url="https://youtu.be/KEV4_--ETuo" %}
