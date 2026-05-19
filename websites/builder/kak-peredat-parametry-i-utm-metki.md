# Как передать параметры и UTM-метки

{% hint style="danger" %}
<mark style="color:red;">**\***</mark>**На территории Российской Федерации&#x20;**<mark style="color:red;">**запрещена деятельность**</mark>**&#x20;социальных сетей&#x20;**<mark style="color:red;">**Facebook**</mark>**&#x20;и&#x20;**<mark style="color:red;">**Instagram**</mark>**, принадлежащих компании Meta Platforms Inc**., признанная экстремистской!
{% endhint %}

{% hint style="success" %}
Данный механизм работает в **Telegram**, **Вконтакте**, **Viber,** **Facebook**<mark style="color:red;">**\***</mark>, **Одноклассниках**.

Другие мессенджеры не поддерживают deeplink.
{% endhint %}

Хотя и в Whatsapp также отсутствует deeplink, передача параметров и UTM-меток возможна: вам необходимо вставить специальную переменную в текст автоматически заполненного поля ввода, которое у пользователя появляется сразу после перехода по ссылке.

Подробнее расскажем далее.&#x20;

{% hint style="info" %}
Параметры сохраняются в переменные клиента.
{% endhint %}

Параметр — это пара имя-значение. В зависимости от задаваемого значения параметры могут быть:

* **статические** — передаваемое значение вы задаете сами, например, `utm_term=webinar1` (`utm_term` — имя, `webinar1` — статическое значение);
* **динамические** — рекламная система (РСЯ, ВК ) автоматически подставит необходимые данные, например, `term={keyword}`, где вместо `{keyword}` передается ключевая фраза, по которой произошел показ.

### С использованием сайта

Все параметры, которые придут на сайт, после запуска клиентом бота перейдут в переменные сделки. В частности метки.

Ссылку на сайт можно получить в разделе "Сайты":

<figure><img src="https://lh7-rt.googleusercontent.com/docsz/AD_4nXeZMWRm4rcskjyfbqMKa8d6BLzuiqxD1m4Hm4lj0ASZhrnjBwlsOZ0BaHKe52gXXvuItJbcMaAy1PYjfhFfVDdpuIB2lHAfhYuELUyiAB5gLkP5Ie1iVnAqojRyU116zO6XraWCXQ?key=tFD9Bn9i_ZoiUhJ2SxMfIg" alt=""><figcaption></figcaption></figure>

_<mark style="color:green;">Пример добавления UTM- меток к ссылке на сайт:</mark>_

```

https://salebot.site/st/test_wi_me?utm_source=test_wi_me&utm_medium=cpc&utm_campaign=id_campaign&utm_content=registration
```

Параметры и метки будут переданы в бота и запишутся в Переменные клиента:

<figure><img src="https://lh7-rt.googleusercontent.com/docsz/AD_4nXeKZMgBYa3TyLF5w8OSnwF8XhjiYfKrYPrsrrnAlV_Sx-aZJfgWYkk6wqgo7Af4txoXXfPffs0ao-4Ej4sMVlkPBaYbo9kGnyfdZUkIrZ57BF5uVPXqtF737Trb1eHM0qXFTX8Llg?key=tFD9Bn9i_ZoiUhJ2SxMfIg" alt="" width="375"><figcaption></figcaption></figure>

### Без использования сайта

Вы можете использовать прокси-ссылки, в которые передаете параметры. После запуска бота переданные параметры запишутся в переменные сделки.\
\
Ссылка с параметрами должна иметь вид:\
https://salebot.pro/r/salebot\_1?param1=value\&param2=value2...\
где первая часть ссылки (до знака ?) - это прокси ссылка,\
а вторая часть - ваши параметры

_<mark style="color:green;">Пример как к прямой ссылке с сайта на мессенджер Telegram добавить UTM- метки</mark>_

```
https://salebot.pro/r/salebot_1?utm_medium=cpc&utm_source=yandex&utm_term=kluchevaya_fraza&utm_content=HappyNY#ancor
```

Ссылки на мессенджеры можно получить после создания сайта:

<figure><img src="https://lh7-rt.googleusercontent.com/docsz/AD_4nXe-wIeR32AX1WRFkxHmF8HuRSSZyy3YJ49EvM6z1L3xnEm0xCBOGYEGRiRk_xgoVJVoVdSBXpAIyS5XjrQLVEXq7mruKHc8adV7YBtP4GQbGkDQIrIgr7gBZey7zcMCpuC0EE4X?key=tFD9Bn9i_ZoiUhJ2SxMfIg" alt=""><figcaption></figcaption></figure>

<figure><img src="https://lh7-rt.googleusercontent.com/docsz/AD_4nXfdG_cGpl3eVTnUZWZYpmyhptwzQOGgnjgs2JOqDhMtSnv9mW2Dni7Bkua6QaPigBegH2wJtmdNCtmD_lwTlk3fPYGd2SJz5FjfBZFbz6kQFMFr3Pm0lq__tEGahmH7q2LIcHox0Q?key=tFD9Bn9i_ZoiUhJ2SxMfIg" alt="" width="563"><figcaption><p>Прямые ссылки на мессенджеры в разделе “Сайты”</p></figcaption></figure>

{% hint style="warning" %}
Отображаются ссылки тех мессенджеров, которые подключены к системе.
{% endhint %}

Видео-обзор по работе с метками, если не используете сайт: <br>

{% embed url="https://youtu.be/CstynBBD9mc" %}

## Особенности Whatsapp

Так как в Whatsapp отсутствуют deeplink, необходимо в стартовую фразу Whatsapp добавить переменную, по которой бот определит с какими параметрами был запущен Whatsapp.

Переменная называется. **#{visit\_key}**. При переходе в Whatsapp она заменится на кодовое число.

<figure><img src="https://lh7-rt.googleusercontent.com/docsz/AD_4nXf3flMK_Ff6nE-ZaPTlA60iwh7D2vYuFmr_bxQfcTgImJtQSwjfmbeRdtLDl1zBAxJhDNSYUZABlxCqjdM9LkFmXcvClaMmkbZ36MIEzpgKPjXeLlv_przwf8rMHshaly0MI6JH?key=tFD9Bn9i_ZoiUhJ2SxMfIg" alt=""><figcaption><p>Раздел “Сайты” → Сайт → Настройки страницы сайта → Мессенджеры → Настройки WhatsApp</p></figcaption></figure>

При переходе в Whatsapp с сайта (или по ссылке на мессенджер из настроек сайта) **#{visit\_key} заменится на кодовое число:**

<figure><img src="https://lh7-rt.googleusercontent.com/docsz/AD_4nXea_9axzgi9p-VBCrg3Cg_G2H_fsyxXQ-df2tJTnAtTG5w33JF9swzvnh468Ca7Mlo8hu-q84TPjy_S_2pnIGVqN6uDGJsuooPgdNAH0xQt5ZljBt4upSDOyCKlI1oc4ddP9I46NQ?key=tFD9Bn9i_ZoiUhJ2SxMfIg" alt=""><figcaption></figcaption></figure>

## Как вставить кнопки к Вам на сайт

Чтобы интегрировать на ваш сайт форму бота, нужно создать сайт на Salebot. После создания сайта у вас появится кнопка, как на картинке ниже.

<figure><img src="https://lh7-rt.googleusercontent.com/docsz/AD_4nXcVf9dvWBx7kSG_8vliow7NTKKIXd5SCuXnBKqbGj9e0ZTzGkvmHVrC5tyvcSnAqAOV3QphyLLRIqqqwMXJGNc9EdyrR9kdv5c6ynen6h5gyug-sKG8W3qjjIWJ7RMPIq-ZhGuS0w?key=tFD9Bn9i_ZoiUhJ2SxMfIg" alt=""><figcaption></figcaption></figure>

Данный код нужно вставить в блок на вашем сайте.

{% hint style="danger" %}
Код формы заявки можно поставить один раз на странице.&#x20;

Если есть необходимость на странице в разных местах установить форму сбора данных для заявки, создайте дополнительные сайты и в каждой html-секции вашего сайта используйте коды с разных сайтов.&#x20;
{% endhint %}

<figure><img src="https://lh7-rt.googleusercontent.com/docsz/AD_4nXcTFxOV83Zd9jmun8ClH3m3HptWZ0g30usIiBijUqr-kOGndktqN_3P4n_hiE5apwGhMJbASAJDD46g5ufLmr43DjkSojafRpt01yOiHm8_7DbraauBp8qcwVWlwusqasIGNCVG?key=tFD9Bn9i_ZoiUhJ2SxMfIg" alt=""><figcaption></figcaption></figure>

Пример результата:

<figure><img src="https://lh7-rt.googleusercontent.com/docsz/AD_4nXey6yPzi7xQmOfIZBvf-bocLjSyF7XYdLyteEKVCfSTnTuhBf_28eiOyDXeEjASGLeZndXcvA3RhnRoGPyPgCT5hQoB6IOQqUKXV4EEMg1tDQR6--0pGaHW686ao3xAkX0ZZcI0JQ?key=tFD9Bn9i_ZoiUhJ2SxMfIg" alt=""><figcaption></figcaption></figure>

## UTM-метки в Аналитике

По UTM-меткам вы можете посмотреть статистику в разделе “Аналитика”

Переходим в раздел “Аналитика” выбираем вкладку “Клиенты”

<figure><img src="https://lh7-rt.googleusercontent.com/docsz/AD_4nXfYTvNEQur-_hgRUG6SdMn5gqhzW6ZPSDFDieP1lXePtwS3l6M_SOHH0ZxBQ16NR2TbYz110CQqMc5G7FM15lOV7Tl_L0qCVviKavcmh1n2hqcqkIDGxFg8ai30qWyvHagqXqiY?key=tFD9Bn9i_ZoiUhJ2SxMfIg" alt=""><figcaption></figcaption></figure>

Нажимаем кнопку “Добавить виджет”

<figure><img src="https://lh7-rt.googleusercontent.com/docsz/AD_4nXdVZwd3b17aEwKxu4ftfSyxR6AIN-d1MuWISVbMtwAMYcH6iTJPQBFeWpZhDMjcxyZirpV5dTLKYzBxumaSjFxk6_M9Sg_FMiJlDbVLT_P-2iVeC85gn-08DMoiA_oRHnO0Z9pRog?key=tFD9Bn9i_ZoiUhJ2SxMfIg" alt=""><figcaption></figcaption></figure>

Открывается окно “Конструктор виджета”. Выбираем вкладку UTM-метки. Нажимаем “Добавить значение”

<figure><img src="https://lh7-rt.googleusercontent.com/docsz/AD_4nXfDuDO01fZpqQLfbtZjhTRdU01Iy57USiayd8bh1pdPyTQh-bl0QJbywgdtHuC_HaXPI7fSzkiKMFbTqX1Vtg-bIClkR3-snIb43CbWS8NxQFwlf0YVtT2kI3xy21Ck2qZo1um81Q?key=tFD9Bn9i_ZoiUhJ2SxMfIg" alt=""><figcaption></figcaption></figure>

Появляется дополнительные настройки значений UTM-меток. Нажимаем на поле “Выберите метку”

<figure><img src="https://lh7-rt.googleusercontent.com/docsz/AD_4nXexVgbCxDNpTgnFqpzWG20lstkdRDfxsK8umbryx_Sis7n1JDkeGMDb8GHC9UfeV9Hmpd0Vw7MwvbruSIvOUKlhQ73nX2FUhOwvS4-ZfsKo0bIvnyMdSmp3PaX6P92KgXukWHnqng?key=tFD9Bn9i_ZoiUhJ2SxMfIg" alt=""><figcaption></figcaption></figure>

И выбираем метку по которой вы хотите посмотреть статистику

<figure><img src="https://lh7-rt.googleusercontent.com/docsz/AD_4nXebXmxcrKfkhRlibN_7QbZ3YJqnuGftPQa7kAFgBPtoBr3Bj5ypfznyxQ4chETSsWnofr5Oc9MiB7F_XgZb7tglYOUE90OeNpgno7Q0dlUEG1bua8GPHva2AidfuCIbShbA_HJu-A?key=tFD9Bn9i_ZoiUhJ2SxMfIg" alt=""><figcaption></figcaption></figure>

Если вы хотите добавить несколько меток или все, снова нажмите на “Добавить значение”

<figure><img src="https://lh7-rt.googleusercontent.com/docsz/AD_4nXfzzAw4C1ZQv2It3KybN5UpBMaGYkcrC-sj_eYVjx5EISBI67rGZTnoa1UQWRJO3KfOHL-Vav0iIUuGOpotItUPrGncc6lOx5346PK2gU7gsBsoWbnfJdsGcIzVtrBLE6KJmbBktQ?key=tFD9Bn9i_ZoiUhJ2SxMfIg" alt=""><figcaption></figcaption></figure>

{% hint style="info" %}
Не забудьте указать период и другие настройки и обязательно сохраните.
{% endhint %}

Вот такой виджет с UTM-метками получается в итоге:

<figure><img src="https://lh7-rt.googleusercontent.com/docsz/AD_4nXcZm9ehr6Iz8bRFXajxROUEhl7G5kasdzBl2fEO6SHGwcKvO8O9Gi11Zm36wGD3uI2d4kbKrmAIPc_rGZVuxxzWUUEr3X5r1V3PWKir_eJqjhancKGIAUBohQvDAHHI3vQ8NNV4WA?key=tFD9Bn9i_ZoiUhJ2SxMfIg" alt=""><figcaption></figcaption></figure>

Подробнее о работе с аналитикой читайте в статье “[Аналитика Salebot](../../analitika-dlya-biznesa/analitika-salebot/)”
