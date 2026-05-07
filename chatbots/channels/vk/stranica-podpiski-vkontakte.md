# Страница подписки ВКонтакте

Подписная страница ВКонтакте состоит из баннера, продающего описания и кнопки подписки (призыв к действию). Простой пример:

<figure><img src="../../../.gitbook/assets/image (173) (1).png" alt=""><figcaption></figcaption></figure>

{% hint style="danger" %}
Если **указан** **тег**, то кнопка вк с обычного сайта **будет вести на вк сайт**, чтобы тег не потерялся.
{% endhint %}

{% hint style="danger" %}
Если не указать ТЕГ (сохраняется в переменной клиента **tag)** в настройках сайта, при запуске бота придет слово **Начать** и следом уведомление о подписке на группу. Поэтому бот может запуститься дважды, если добавить блок без условия.
{% endhint %}

### Как сделать страницу с автоподпиской на сообщения бота

Установите приложение Salebot в группе ВКонтакте, чтобы в ней работал сайт.&#x20;

{% hint style="info" %}
Ссылку на приложение можно получить на платформе Salebot в разделе Сайты- создать сайт - Страница сайта - Настройки - Мессенджеры - нажать на ссылку для установки приложения:
{% endhint %}

<figure><img src="https://lh7-rt.googleusercontent.com/docsz/AD_4nXdKyuG-dLJQdn21WxSrV3bxN0BfI3D4OSh2sjllK4C14wHLbu00xychEw6ifwcrAou7k8wT6iiE6RN1VODYfYTzfLMjnAoXJnq-WFxRA5CAB4jZ_w2Yd3_h-bZDx8A71Gq_soFhsA?key=Ua_-5UR8GCA2xCCBsX8L4w" alt=""><figcaption></figcaption></figure>

<figure><img src="https://lh7-rt.googleusercontent.com/docsz/AD_4nXd-0VgVONN_mVtB-clsuj3AYJT7_ylTXjHluYHIEewqywW3L9BLcVbwhoylMu5t2EHpMiNtSRiMGlbtf4wg6tuLrt6i5HyjRSPlXED11WJl7vev0YIKdcjGHJmqvJG1WzU0R-RY?key=Ua_-5UR8GCA2xCCBsX8L4w" alt=""><figcaption></figcaption></figure>

Далее выберите сообщество, в которое необходимо добавить приложение Salebot:

<figure><img src="https://lh7-rt.googleusercontent.com/docsz/AD_4nXcXWsZCjyp6HTB_ytTFDTv4J1Cu7Ds8zdGclluFmZtOl7ISh0p782IFa5Ng2R4Y9S0QI0pTeo_0eoS8Qg1ypIFdj_fLp7znpdsfXLCxJ2xJLI7x2OlfEbFjqz2rgwguRXr4jVr1?key=Ua_-5UR8GCA2xCCBsX8L4w" alt=""><figcaption></figcaption></figure>

При клике по ссылке откроется окно с возможностью увидеть все сообщества под вашим управлением, чтобы проверить и при необходимости выбрать сообщество для добавления приложения:

<figure><img src="https://lh7-rt.googleusercontent.com/docsz/AD_4nXfdg9u3tBa233t6ZB53XsWsTukIWndNTyY-vjFMKyRRrsMn_H-9K6mv5WwKGdRzn2SCiVTSW9O1hFq1hA8ylrkd3NgTQ1ItUqRQ4RvmRwnUMrsngU8HnIORZU5_gn3TbNyMk7t0kA?key=Ua_-5UR8GCA2xCCBsX8L4w" alt=""><figcaption><p>Пример, как выглядит сообщество, в котором установлено приложение</p></figcaption></figure>



В разделе **Основная информация ОБЯЗАТЕЛЬНО** укажите **тег**. Так вы сможете настроить запуск бота на разные сценарии воронки.&#x20;

Тег укажите в поле Условие стартового блока, чтобы запустилась нужная воронка.

{% hint style="success" %}
В поле Тег можно указать любое значение на латинице или кириллице. &#x20;

Именно этот текст придет как сообщение от пользователя при переходе с подписной ВКонтакте в диалог с сообществом. А значение будет записано в переменные клиента - Тег (встроенная переменная **tag**).
{% endhint %}

<figure><img src="https://lh7-rt.googleusercontent.com/docsz/AD_4nXfqKWGMAsbUgdk7Gv8btOuwJITtuYHytrhEGQ5q9apLnxriIwHVWWmE0r8HUwUsJCg-XO2A6i4uOv5IRN14Fitxc4yYGJl153esPpLdOCCWpqPz7nP4cWQ5rzwiliarxoVaQai7OQ?key=Ua_-5UR8GCA2xCCBsX8L4w" alt=""><figcaption><p>Пример заполнения поля Тег.  Используйте удобные и понятные для вас значения в поле Тег</p></figcaption></figure>



Включите чекбокс "**Кнопка ВКонтакте  ведет на подписную с автоподпиской"**:

<figure><img src="https://lh7-rt.googleusercontent.com/docsz/AD_4nXfxlMb67Ue3d8kHM_xKlngdn-SHzI9UR59ecdS5vj4YlILpl0cPyRZSTuwc90kkHLuSqyJDfiN8M6aTnmAyG_g6vvgBmkujYpbjm-3OFjIHzQqtYVy9sEiYDF16_cB-UF_YCNJ8BQ?key=Ua_-5UR8GCA2xCCBsX8L4w" alt=""><figcaption></figcaption></figure>

Чтобы изменить текст на кнопке Подписной для запуска бота заполните поле Текст кнопки сайта ВК .&#x20;

Если вы хотите, чтобы на сайте отображалось количество подписчиков включите   чекбокс "**В ВК отображать количество подписчиков**" и указать подпись к ВК подписчикам:

<figure><img src="https://lh7-rt.googleusercontent.com/docsz/AD_4nXdXjM956bo5yjDyGpaXv-7PPhCnmcD1beRhWSdKArssxbTIua4EKy9UqOeKr0HGesQwqbNozrcaU6-hxnbW7iIQm77r8JKKCjWkgykbn9a9BxMZOhTJ1Htq1Kga_ElTU5ATdTMYiQ?key=Ua_-5UR8GCA2xCCBsX8L4w" alt=""><figcaption><p>Пример настроек</p></figcaption></figure>

В этом случае на подписной будет отображаться количество подписчиков с указанным текстом.



{% hint style="info" %}
Подробнее настройки для кнопок ВКонтакте [описаны в этой статье.](https://docs.salebot.pro/minilendingi-v-socialnykh-setyakh/kak-sozdat-sait#nastroika-knopok-vkontakte)
{% endhint %}

Заполните оформление лендинга и нажмите кнопку **Сохранить и закрыть**.

<figure><img src="https://lh7-rt.googleusercontent.com/docsz/AD_4nXcVRU6GoSPkSxRktTmEvDegzFPVndXs_ERDePD7W34JMwL7XXtPifBZb-1URc0nZpmsoHORckMfzX4PMSmiOm7rf34HnoxLD1jZSf3TACJKjmYN6rbVzVuky1ELiGl0pfITVf-Ogg?key=Ua_-5UR8GCA2xCCBsX8L4w" alt=""><figcaption></figcaption></figure>

После сохранения настроек лендинга в выпадающем списке **Ссылки на мессенджеры** будет доступна Прокси-ссылка на ВКонтакте с функцией автоподписки :thumbsup:

<figure><img src="https://lh7-rt.googleusercontent.com/docsz/AD_4nXfKYTh5-InNjI6Ziw8dC0SxJRs9hR7Bv_OyvXvFPLIFOtP6cU2YY7Fk94VNQFRbDF35nXVedyTMTLtAbLHbevNLlwGdaf--h8g5_MKwAmREAvasTBF1Uo_1H9bM4eLn4As7lyOHkg?key=Ua_-5UR8GCA2xCCBsX8L4w" alt=""><figcaption></figcaption></figure>

<figure><img src="https://lh7-rt.googleusercontent.com/docsz/AD_4nXcA4tvJ4GDvkgEvvOJaAyzA_cyAO1rvmYqA11jzbuvXIWVeqmV6Mhw7fOU_RiXwmdViJIlwfZGJjczd7FuKADOvJvr4_EgPlKCEHyuB1GY6qHd1p2P36HlhTj8gwNe5xK4GaugE?key=Ua_-5UR8GCA2xCCBsX8L4w" alt=""><figcaption></figcaption></figure>

При клике по кнопке посадочной страницы в бота приходит значение указанное в поле Тег настроек лендинга и записывается в переменные клиента:

<figure><img src="https://lh7-rt.googleusercontent.com/docsz/AD_4nXf8wDc0HchgFFsqfgpgNusWGeh50vd7IXH0nWwGk2FHwjz5kjWj3QVm5ukpA57EZlvZ7HQML5AzWCvjTN0EcraDkCR0kjeVViaLxJ2ERlUpvuiLPEsuWYSR4aNM-OwXnT3CAyTe5Q?key=Ua_-5UR8GCA2xCCBsX8L4w" alt=""><figcaption></figcaption></figure>

### Как создать ссылку для рекламы ВК и прикрепить метки (параметры)

{% embed url="https://youtu.be/45Q57HMs5o0" %}

ВКонтакте довольно требователен к ссылкам для рекламы. В статье расскажем как к ссылке на страницу подписки ВКонтакте  добавить метки, чтобы они корректно передавались в бота.

\
Вам потребуется **Ссылка на ВКонтакте с функцией автоподписки**. Выше описали как правильно создать лендинг для ВКонтакте.

Откройте **Ссылки на мессенджеры** и скопируйте её:

<figure><img src="https://lh7-rt.googleusercontent.com/docsz/AD_4nXe8z73vsxMxqrJnFH_Mm_k56nDEXZQObubG9O78j54K3siZPi0B-LJoZ4E2VAVVC68gw7FoRKE1ldYdSgjlOcI7aqnBmEnKdfr34klUdqvllY1u_oflblQeLtU7ZOUHCapltRtg?key=Ua_-5UR8GCA2xCCBsX8L4w" alt=""><figcaption></figcaption></figure>

{% hint style="warning" %}
Важно! Не удаляйте из данной ссылки никакие значения и все параметры (utm  метки) допишите через **& .**&#x20;

**Каждую пару метка=ключ также разделяйте с помощью &!**
{% endhint %}

Например нам нужно передать с ссылкой следующие параметры:

`utm_source=vk`\
`utm_medium=cpc`\
`utm_campaign=bh`\
`utm_content=zakrep`\
\
Копируем ссылку на ВКонтакте из настроек лендинга (раздел Сайты) и через & добавляем все пары меток со значениями:

[https://vk.com/app7062840#9c9ecd13955b76cbfed07d02d80d23be\&force=1\&utm\_source=vk\&utm\_medium=cpc\&utm\_campaign=bh\&utm\_content=zakrep](https://vk.com/app7062840#9c9ecd13955b76cbfed07d02d80d23be\&force=1\&utm_source=vk\&utm_medium=cpc\&utm_campaign=bh\&utm_content=zakrep)&#x20;

Данную ссылку можно использовать в рекламе и все метки будут переданы в бота.

{% hint style="danger" %}
**ОБЯЗАТЕЛЬНО** укажите **тег** в настройках лендинга. Без него параметры не будут переданы в бота и аналитику.
{% endhint %}

### Как сделать отдельную подписную для ВК

Вы можете выбрать для ВК отдельную подписную — так у вас не будет дублироваться информация с основного сайта. Плюс вы сможете вести несколько разных сайтов на одну подписную в ВК.

Для этого создайте отдельный сайт, который будете использовать в качестве подписной ВКонтакте.&#x20;

{% hint style="warning" %}
В настройках указываете нужный тег для запуска бота.&#x20;
{% endhint %}

В отображении кнопок включаете только кнопку ВК.&#x20;

&#x20;Затем в настройках вашего основного сайта находите поле "Подписная, на которую ведет кнопка ВКонтакте"

<figure><img src="https://lh7-rt.googleusercontent.com/docsz/AD_4nXdxCm5nTnFFLn3n2lptjyoy24I2cQAYfBwmMKaySmPjxsckW3xTxo4CNJq4mPYz5BmHWigstv781_KAQJSOFsmtriqvR-BL3hbAn3KN36aDELweuYptBEujPJyO4dHnV2UtfRo0BQ?key=Ua_-5UR8GCA2xCCBsX8L4w" alt=""><figcaption></figcaption></figure>

Выбираете нужную подписную из выпадающего списка.

И сохраните настройки.

Теперь у вас получится как в примере. Основной сайт:

<figure><img src="https://lh7-rt.googleusercontent.com/docsz/AD_4nXdjGAdzmfnsG1x3JJIxAfWFWLFqzHGWxU2IJAp3bFNyG4OVS-9xLXZlrkJ0NkwiK5tR1FvVu0Y7y20wEwHwEGxCYM1t3MlKfpJqx_t1vMPOH8Ltr5iu_rdGtX2e2-rBDR1NKvyrdw?key=Ua_-5UR8GCA2xCCBsX8L4w" alt=""><figcaption></figcaption></figure>

А при клике на кнопку ВК открывается другой:

<figure><img src="https://lh7-rt.googleusercontent.com/docsz/AD_4nXdcIBsKDXBi4xch4wdlxDde2_saRn0B6IGqYKoA_AcCtSW1XCyhNRTYDaB_ES4Fp6fJQtIf7jnfvLCVoXhkspRdXqiKR5dDIAwf-2jEKRn9OPXcSWQyeZVuWtD_w2MAhb-jRJLa_w?key=Ua_-5UR8GCA2xCCBsX8L4w" alt=""><figcaption></figcaption></figure>

### Запрос номера телефона

Чтобы запрашивать номер телефона клиента, необходимо перейти в настройки кнопок лендинга Вконтакте.&#x20;

<figure><img src="https://lh7-rt.googleusercontent.com/docsz/AD_4nXfvfxFWIjQBU4aIERyiY5x2YnLijd5_i5FPtvtSnppizo8ykmuufh4kXEpJYibmfxlvFuOCf_XFJlj5lCSlLo7Pq1uILwXIeVLmpdXJY_wZlwVH5pgoZnuHOyzBYh59-qa8XskSOg?key=Ua_-5UR8GCA2xCCBsX8L4w" alt=""><figcaption></figcaption></figure>

Далее поставьте галочку напротив настройки "Запрашивать на подписной номер телефона".&#x20;

В последующем на подписной странице Вконтакте будет всплывать уведомление следующего вида для пользователей:

<figure><img src="https://lh7-rt.googleusercontent.com/docsz/AD_4nXdF-_Cz_CnzUyplbSr47SmeoEwZ4vL65iE5QDOrq0LoOQKjvL-SybzeRK7GXqKBXS46sOTHSUkZZHUOG0L3V2L5ziWuTwt3Mp-7gDKxZonpmAaRx4uYxlCJ8qJaguvqdSzd8e0YAw?key=Ua_-5UR8GCA2xCCBsX8L4w" alt=""><figcaption></figcaption></figure>

Номер телефона пользователя будет записан в систему: его можно просмотреть в переменных клиента:

<figure><img src="https://lh7-rt.googleusercontent.com/docsz/AD_4nXe5byNhxmZbi8esJt_zRQP8IJc-b5pJZTZv9jM3LJ-NTPvemAatyEVeCgR-RHz8-CdNpeWx9ah9pIjZiVKX9rPCdp2CluyhaLjkhMVmFT_V-K0yy-BTBhfQa4RJbaJoINbEr9dvSg?key=Ua_-5UR8GCA2xCCBsX8L4w" alt=""><figcaption></figcaption></figure>

### Видео-инструкция

{% embed url="https://youtu.be/WrOFTWjLUWk" %}
