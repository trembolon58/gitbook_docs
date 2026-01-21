# FAQ ВКонтакте

## Что делать, если при отправке аудио в ВК не воспроизводится?

Вопрос: При отправке аудио в вк с телефона не воспроизводится. На компьютере воспроизводится.

В вк аудио должно отправляться в формате mp3 моно

## Что делать, если дублируются сообщения в ВК?

Причина: дублирование серверов в настройке группы

Решение: Если у вас дублируются сообщения в ВК, проверьте количество подключенных серверов в настройках группы.

Для этого заходите в группу, подключенную к проекту, там открываете раздел Управление - Работа с API:

<div><figure><img src="../../../.gitbook/assets/unnamed (8).png" alt="" width="339"><figcaption></figcaption></figure> <figure><img src="../../../.gitbook/assets/unnamed (1) (4).png" alt="" width="322"><figcaption></figcaption></figure></div>

Далее нам нужна вкладка Callback API, нажимаем:

<figure><img src="https://lh7-rt.googleusercontent.com/docsz/AD_4nXdK6ZMJCJKSRsvzDLjq-4maPApHKPbDBlkWVspNR-LgORCuN6I3Um9o13Z6kds4IT6pQjwmJe-dxZwC7xTOCmYTSeyxhzdqCL939CHlBumTh55M-LjaadnVTyjpDJtgF_q450TdIg?key=MRCVrH0QkhdVOmRJFhgYWQ" alt="" width="375"><figcaption></figcaption></figure>

Удаляем серверы, которые там есть:

<figure><img src="https://lh7-rt.googleusercontent.com/docsz/AD_4nXcc_JGmp6cs6UlAb7FA_1PCo8XvrykdMJkyITYfq3YTbXi9m-24NbTA3KU01r0Kjgwbow4k7NBP53Ut4y7g7JoJyOWRsdLP_9A-Cx5qDjb575gYg8y8ZMAjRdfRld8DnyZ6-_UOAA?key=MRCVrH0QkhdVOmRJFhgYWQ" alt="" width="375"><figcaption></figcaption></figure>

После этого возвращаемся в Salebot, открываем Каналы, удаляем подключенную группу:

<figure><img src="https://lh7-rt.googleusercontent.com/docsz/AD_4nXdXGjldidniNj3jiEZAgNnXdtY3-Pmd8WOHljWXD4LyP6c0tu6-ntAwHzqgyQO9jQ0pBX7s9PryNBF9LoiqY2NfNpfjbRpaKvxN35ZCz_aFzFxSvm4zkCnpPaeCh_qrFYlmI4WZpg?key=MRCVrH0QkhdVOmRJFhgYWQ" alt="" width="563"><figcaption></figcaption></figure>

и переподключаем заново:

<figure><img src="https://lh7-rt.googleusercontent.com/docsz/AD_4nXff6sM98HGFfVtPeh8gv4M_otyGqKjXIHJH9Ah-qLkn7DX6tYIqsxmrAyNQPvh9v3TvhS7xamXZoU58kkaab9M7wLxCWiJkYaOTRFCYIf_gA_tjCBzuAN3rSDP6_k-i6gY7PtgKkg?key=MRCVrH0QkhdVOmRJFhgYWQ" alt="" width="563"><figcaption></figcaption></figure>

## Что делать, если не отвечает бот?

<figure><img src="https://lh7-rt.googleusercontent.com/docsz/AD_4nXeMujEsy_O9P4SGBmG96oov6qkvPsJwpNyy6gY590oxUz2KnEaVmkad4DYfOkJ1kUx_P59pV55PDqlkKl5lZfJfTJItZ_PNR1tDtMNVnrxKdh3xiqh0M7yNCDn0URI_ZuFIo4Suvg?key=MRCVrH0QkhdVOmRJFhgYWQ" alt="" width="375"><figcaption></figcaption></figure>

Причина: Не дан полноценный доступ для успешной интеграции платформе Salebot

Решение: Проверьте, количество токенов для подключенной группы. Их должно быть не менее двух! Подробнее о подключении ВКонтакте[ тут](https://docs.salebot.pro/messendzhery-i-chaty/podklyuchenie-bota-k-vkontakte/kak-podklyuchit-gruppu-vkontakte)

<figure><img src="https://lh7-rt.googleusercontent.com/docsz/AD_4nXd8ELLN9gWPlisbWZ_gbUccpgawY58KBKqwCW_e1WsoCEk7oElJbaqVpnypuAPmUb7EjaD6W0Xcag3qtunPo-2Rp4RoXiWU3yH_sbMS6AgUFSNWfIUVYC_dZ285rrOyBuk1WjZC?key=MRCVrH0QkhdVOmRJFhgYWQ" alt="" width="563"><figcaption></figcaption></figure>

## Ошибки, возникающие при работе с Вконтакте

### Ошибка доступа на сайте

<figure><img src="https://lh7-rt.googleusercontent.com/docsz/AD_4nXdK26_67yGrqH6bEl3TALk42oU2id_fQP9fKt07rH_Bj0-RVga9fIMUXiFVgW_Od2i00LWGevYUp6U_1kltExXnzHmqwxe4QMa0NCYh4FukJemWzGkXRuYpIcirzGJm3g4L1LZj8Q?key=MRCVrH0QkhdVOmRJFhgYWQ" alt="" width="375"><figcaption><p>Ошибка доступа</p></figcaption></figure>

Причина: В Вашем сообществе не установлено приложение Salebot.

Решение:  Установите приложение в группу[ по ссылке](https://vk.com/add_community_app?aid=7062840)

<figure><img src="https://lh7-rt.googleusercontent.com/docsz/AD_4nXcTWtN8xXpGLcnbKMlmlCRURGiAU2T22feJfjS3WCV-RsKR_NSvl22WBP_8GmXcibP0iTGfmFIV5ksUyy-m2qD-XGjB4Bh8KNai1piGRwJSk2UwPNbmL2L6gfbYrgaFLYu2MghzMA?key=MRCVrH0QkhdVOmRJFhgYWQ" alt="" width="563"><figcaption></figcaption></figure>

Пример установки приложения в группу

### Ошибка 2000

При попытке подключения группы ВК может возникать такая ошибка:

<figure><img src="https://lh7-rt.googleusercontent.com/docsz/AD_4nXceg6QXisLNz86KS2wiBnSHJDaMTDIYVWxdZNTi52Pn6ST8sdul6Pu6d9_fmtmSzj2wp6s1U_wzsZ7qT97_Kh1eZvbwJ4z_CfjpDGlCtHoXZKGje6c7rewDlpZLSMJl88Is5jIbDA?key=MRCVrH0QkhdVOmRJFhgYWQ" alt="" width="563"><figcaption></figcaption></figure>

Причина: Эта ошибка означает, что в сообществе установлено максимальное количество серверов для работы с Callback API.

Решение: Зайдите в Управление группы - Настройки - Работа с API - Callback API. На рисунке ниже стрелочкой выделена кнопка управления серверами. Все лишние и неиспользуемые сервера следует удалить. После этого предпринять еще одну попытку подключения.

<figure><img src="https://lh7-rt.googleusercontent.com/docsz/AD_4nXebHR9i26ZxkCtAhyFp_JGVSZVJptJbky6336uA4Ri1LPkEe-weSVN0Cc_nFjQYNouwuEaRKDa7UysdTpS-IjqRqlxdDfIm62-Km8lZd5NunqUhqFE_ntGTiAHNyQPhjH-EF9Ir4Q?key=MRCVrH0QkhdVOmRJFhgYWQ" alt="" width="563"><figcaption></figcaption></figure>

Управление группы - Настройки - Работа с API - Callback API

### Ошибка 5

<figure><img src="https://lh7-rt.googleusercontent.com/docsz/AD_4nXeyRszQ5uqX6QUItgkyhzV-Qh3nVdSc077nt0tECou4Rr1-d4weKNPjSEuRQ_W-u7zM7lYTLQTGFx_7i_gNMvZG23FakEGMjs0V4HXjO7TBYH5DGJZrBDjlH0gMh3yevfosqvqR?key=MRCVrH0QkhdVOmRJFhgYWQ" alt="" width="375"><figcaption></figcaption></figure>

Причина: Недействительная сессия (или Invalid Session) - данная ошибка может возвращаться при обращении к методам API ВКонтакте с ключом доступа пользователя

Решение: Что-то с ключом доступа. Попробуйте переавторизоваться. Если не помогает, то удалите ключи доступа и создайте заново

### Ошибка 10 (912)

<figure><img src="https://lh7-rt.googleusercontent.com/docsz/AD_4nXcKudGRYkVRhoXpzkeZUa3tJWgEyDKOi0ioQHBgiTpPS2XTEzqqCpE12a91IQqB0oE-qJ-ILd3unIoBuSLCxcPkW404d-V_xTP8Rpy6RaiQwBXBHtc-4W0tP5e3-VOnddOl_HoxfQ?key=MRCVrH0QkhdVOmRJFhgYWQ" alt=""><figcaption></figcaption></figure>

Error 10

Если при подключении группы Вы получаете ошибку как на рисунке выше, то попробуйте подключиться позже. Как правило, через час или два, подключение происходит без проблем.

<figure><img src="https://lh7-rt.googleusercontent.com/docsz/AD_4nXcHaxutIk6fsPrNLsbddPrRwBJr856t3jCAsmkJ4Y44DsXH2wiXVs-MMHzgs2s0nGKhiIBYtaKWODiDJ5ZpIzTNsKsn7ifiQ_w3KNPkviLY_R3bfE7CyZPKl7DSIhwnXNaIT44Etw?key=MRCVrH0QkhdVOmRJFhgYWQ" alt="" width="563"><figcaption></figcaption></figure>

Error 912

Причина: Если не отправляются сообщения, а в разделе клиенты Вы видите ошибку "This is chatbot feature, change this status in settings", Вы не разрешили Возможности ботов.

Решение: Перейдите в настройки для бота ВКонтакте и включите возможности ботов

<figure><img src="https://lh7-rt.googleusercontent.com/docsz/AD_4nXdagFfq0Gxh4gzXukZYDXXaCR2VdRVFI3H5RGqSh7werW6YJgCvB4cnxCIszzAQeqBDsgsO3lwgVU7igxzBz-UNxH2MwDgWRtu2paqjZ5dltGkmRNyFjX7xiPlnk3ffUWLPDAT3dA?key=MRCVrH0QkhdVOmRJFhgYWQ" alt="" width="563"><figcaption></figcaption></figure>

Если у вас не воспроизводится аудио на мобильном телефоне, то его необходимо перекодировать в mp3 mono

### Ошибка 27

<figure><img src="https://lh7-rt.googleusercontent.com/docsz/AD_4nXftUQbR5tDlI_TYD_Jq3tOHyGnXFjGSbcyHumq0e3CJppJnNBDq7KKzrvqBKLllyZ-CtgpzL1UJV9HFJndztRV_y6aBhqii7oPaNva5pNj6OnAGAKcHsD2TG5wCzRNztiBl6BR0lQ?key=MRCVrH0QkhdVOmRJFhgYWQ" alt="" width="563"><figcaption></figcaption></figure>

Причина: Такая ошибка возникает в результате удаление ключа доступа в в Управлении сообществом ВКонтакте

Решение: Ошибка исправляется после добавления нового ключа.

### Ошибка 100

<figure><img src="https://lh7-rt.googleusercontent.com/docsz/AD_4nXcg6FIqlx74OWaXhS4dSAPrYmkn0UeKCzbz3kYlZthTYx4ehKenFDGIf4yfqely06Un9iTOgWNFAHvAu9DYj1zlzoK652P0uisBE3yhH82VFwqrwQllDeZVx7UuFrTv-Qfgy-vqJw?key=MRCVrH0QkhdVOmRJFhgYWQ" alt="" width="563"><figcaption></figcaption></figure>

Причина: Ошибка появляется при подключении сообщества в разделе Каналы. В сообществе достигнуты лимиты по  серверам.

Решение: Удалить лишние неиспользуемые сервера и повторить попытку подключения

### Ошибка 15

<figure><img src="https://lh7-rt.googleusercontent.com/docsz/AD_4nXd_Qfg9sGAIFqf8RRZxLYUes5fd-ofSaH2pwT18dd3tpH956LSlKZaBTrJ4kF-rpmPIxVvqGPV1r-Ll2GNab150PWsf3WLhdv8SnfwfCkSIMCLfGgP_neJQNe_Zd7MlLomHXCGa?key=MRCVrH0QkhdVOmRJFhgYWQ" alt="" width="563"><figcaption></figcaption></figure>

Причина: Ошибка 15 возникает в случае, если вы не выставили необходимые настройки в группе/сообществе Вконтакте:

Решение: Перейдите в Управление сообществом в раздел "Сообщения". Установите настройку Сообщения сообщества на "Включены":

<figure><img src="https://lh7-rt.googleusercontent.com/docsz/AD_4nXcOR8GFwb90kNT55bKZEwOvZVRDl2M6zkf-43Dq4F2_ra2Qda_0JVXjWRQYVHYiy7fqgG8iSqSCQ4M1pUOwXiqtIjEZ9eUetYoFm2GJjtEQoOdn0D6S7OLP6v8cdRJqUe6HBFZXMA?key=MRCVrH0QkhdVOmRJFhgYWQ" alt="" width="563"><figcaption></figcaption></figure>

#### Ошибка: Клиент отказался от получения сообщений

<figure><img src="https://lh7-rt.googleusercontent.com/docsz/AD_4nXd-Hw5IUOavOZ8fu1eluU2WJ9dEsE9zOOX7kb_w8zIFTQrKBkGgmTCiBkNp0PCPa8q3TiswSs9BR6xba59pRU1KtFe1p0U2r6LZu9_Crsgb5AwFfxib7Avo0zE98smifhaog46viw?key=MRCVrH0QkhdVOmRJFhgYWQ" alt="" width="375"><figcaption></figcaption></figure>

Причина: клиент отказался получать сообщения от вашего сообщества:

<figure><img src="https://lh7-rt.googleusercontent.com/docsz/AD_4nXdSZdgb75mC8Fz5D2uKALVFbpB5y6L0NmwOA27_EPmEkCjDwlAnB4IJl2tKFUsG9eZnPLnxuuJZ6R8K7zAZssdrAXPaIcniIL6wEY4_sxXu1ZXS8JIjDfikByzrnFEh61V3tnybWg?key=MRCVrH0QkhdVOmRJFhgYWQ" alt="" width="375"><figcaption></figcaption></figure>

В данном случае, ошибка возникает из-за ограничения отправки сообщений пользователем от сообщества. Поскольку мы не нарушаем политику интеграции с Вконтакте, данная ошибка пропадет лишь в том случае, если клиент разрешит отправку сообщений.
