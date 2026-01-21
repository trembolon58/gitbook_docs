# Новофон

## Как подключить сервис

В некоторых случаях Новофон не работает. Обязательно проверьте следующее:&#x20;

\- Новофон просит активацию через e-mail

\- CRM Новофон должна быть активна

Настройка интеграции производится через личный кабинет администратора.

По умолчанию доступ к API запрещен всем. Чтобы можно было делать запросы необходимо открыть доступ. Это можно сделать через личный кабинет администратора в разделе "Настройки -> Правила и настройки безопасности" вкладка "API".

<figure><img src="https://lh7-rt.googleusercontent.com/docsz/AD_4nXdAzDKPvqRVarx9PxQBi8sWfaG9Cyn5jVle11QxfXz5JCmg3WdL786C3dK0Q2ASIOXx8Feof7ApStTKSRCPYltCxSVddYu_dJR6qdcaXmUxRt9RXCbKwgj3qkFZHqyIXg1jZChkqNr2f0ueaS3toQlCBY1P?key=gRO4Wih9euT2ZU7mHveHOA" alt=""><figcaption></figcaption></figure>

В поле IP/Маска введите “0.0.0.0/0”.

<figure><img src="https://lh7-rt.googleusercontent.com/docsz/AD_4nXc2_8MUkPJRVejiAMlRSXgtHLLj0WlbnwBZhS3IAoAzNsdTFFbWg-9ZpQfVAlOIP768zmlK8-t_IWRLf4kmbjlqMpfx9k04rg8uxH2DMw1DU4wuOmGCuQQBaz567jcFv53qaKOp8W8sntdXXNUSEeL_iy5B?key=gRO4Wih9euT2ZU7mHveHOA" alt=""><figcaption></figcaption></figure>

Для подключения Новофон к Salebot в настройках пользователя Администратор нужно включить доступ по ключу. Для этого в разделе Телефония - Пользователи АТС открыть настройки пользователя "Администратор". В настройках пользователя в вкладке API поставьте галку "Использовать ключ API". Также установите  параметр “Время жизни” - вечно. В этом разделе понадобятся данные из полей Key и Secret.

<figure><img src="https://lh7-rt.googleusercontent.com/docsz/AD_4nXdkPTSOqmMoz63XhhhGza3dovI1o8MyZNVCeAk9oVxIysx_vf0ZFC1qvTVkmQcp4iFMawJ0SNacTwUP7BLGqKl0oxoPGeaWX10AkJ8b2E_1hMoeI_AKTYJYWgRQnMxRiiFu90jEn12KqNoiF3yGO51XugWm?key=gRO4Wih9euT2ZU7mHveHOA" alt=""><figcaption></figcaption></figure>

После генерации, сохраните Secret в надежное место. Вы всегда можете использовать ранее полученные ключи или перегенерировать их.

Обращаем внимание, что после перегенерации ключей придется заменять их на новые во всех местах, где они использовались.

Далее следует перейти в Salebot во вкладку телефония и ввести полученные данные в окно Zadarma.

<figure><img src="https://lh7-rt.googleusercontent.com/docsz/AD_4nXe12ZUIjmTQ2gWE8wcfrSf9qhnN0iD71VvSL1eGx_QL8vynn8YtC7IGzbmaLaEyVS1e0fvt7ecjsJ4BzPARgD-AH48BPsYwzi2qyTIKwhOYzLFN2BZTGhqJEMlmyGBYZIlbSaCC2RGhCZMVCBGwULHNXS-g?key=gRO4Wih9euT2ZU7mHveHOA" alt=""><figcaption></figcaption></figure>

<figure><img src="https://lh7-rt.googleusercontent.com/docsz/AD_4nXdh5a-FT1NcFylqzfVOh24oTG3Hk9ryGz5COwn-Bzf667DYfXKfz4EsIm8LUFGbXAs0M5chpN9pglYo9bmPzUkSAnwo02UuioLy07PSscMriBFhwIYUVQGHQKQCDS7rMldubkX7nQjVx6F2Bc5NeVmSsuda?key=gRO4Wih9euT2ZU7mHveHOA" alt=""><figcaption></figcaption></figure>

Сервис Новофон (ex. Zadarma) подключен.

Однако для успешной работы с телефонией нам также понадобится информация о сотрудниках и схемах работы.

Для осуществления звонков следует подключить виртуальные номера. Такая настройка осуществляется в «Телефония» → «Виртуальные номера». Также в разделе “Пользователи АТС” нужно добавить сотрудников и назначить им номер для исходящих звонков. Назначение номера происходит во вкладке “ВАТС” настроек сотрудника.

Без подключенного номера для сотрудника звонки из Salebot работать не будут!

<figure><img src="https://lh7-rt.googleusercontent.com/docsz/AD_4nXeGXRgkWpMcwwLa-8ZhzBtrCtZjwxqP6C9wBO9OlFOuFkwgv03YuO84djKQsfRXCGx6auM35XezaPbMNU5SN7AHt4TNdE91QZ473pVRyL3T9h6iR-fbXeRBsDhTTZ23TxYSp0jnIFUDM12C4rKcBDokDrY?key=gRO4Wih9euT2ZU7mHveHOA" alt=""><figcaption></figcaption></figure>

Кроме виртуального номера, нам также нужен id сотрудника. Найти его можно в адресной строке, находясь на странице сотрудника. В этом примере id это “111111”

<figure><img src="https://lh7-rt.googleusercontent.com/docsz/AD_4nXc4OuFdL-Z7x9s7wZL9xOqCJqf4TGkitniDqkf7dtxc3LLssFIMbIBEbdNIfIn4zqyMtR4Jeaj9DRjNQyAX_wHaoEWeNBulGHFhS9TS5e3P9t9-nDn6HgdVddx3hK4Yt2IneCJZoTgV3h0oBHqf4MzhYPuK?key=gRO4Wih9euT2ZU7mHveHOA" alt=""><figcaption></figcaption></figure>

### Как происходит сопоставление клиента

Для работы с телефонией используются номера в формате 71234567890 (должен начинаться с 7( или с иного кода другой страны, например, 375), состоять из 11 и более цифр и не иметь лишних знаков и отступов).

Последовательность сопоставления данных о клиенте: 1. Осуществляется поиск клиента Телефонии. Если клиент не найден, то происходит поиск по значениям всех переменных по всему списку клиентов проекта. Первая найденная запись о клиенте считается тем самым "искомым" клиентом. 2.Если клиент не найден среди клиентов Телефонии и:

* если к проекту подключен любой мессенджер, например, Whatsapp, то будет создан клиент Whatsapp с данным номером телефона;
* если к проекту не подключены иные виды мессенджеров (Whatsapp, Viber, Instagram и т.д.), то будет создан клиент Телефонии. Такому клиенту Вы сможете совершать только звонки с получением информации о них. Написать такому клиенту возможности нет

### Функция Salebot обратный звонок

Для того чтобы совершить звонок из бота, необходимо использовать функцию zadarma\_call(client\_phone, employee\_phone, employee\_id), которая принимает на вход следующие параметры:

* client\_phone - номер клиента, которому должен быть совершен звонок, строка, пример - '79004443322'.
* employee\_phone - виртуальный номер, с которого будет совершен звонок,  строка, пример - “79500000033”.&#x20;
* employee\_id - id сотрудника, которому поступит звонок в систему в Новофон.
* Пример реализации функции в боте:

<figure><img src="https://lh7-rt.googleusercontent.com/docsz/AD_4nXcFylMoqBuGgZuSAEkEY1a3-CYbu_dYGkIPkJB3plvy5PjO5A09xehxARXjnjyjObA8j9c-wFnWslYDJ_K6c3hB-nET1yB-W6ouWb9stJWZXEzrCMZ2_QT4eWxSIVammgiWt8fCHtuwanl8sbWlXPbNZ51H?key=gRO4Wih9euT2ZU7mHveHOA" alt=""><figcaption></figcaption></figure>

### Настройка звонков из карточки клиента

Для настройки возможности осуществлять звонки непосредственно из карточки клиента введите сотрудников в систему Salebot. После регистрации сотрудника зайдите в редактирование его данных.

<figure><img src="https://lh7-rt.googleusercontent.com/docsz/AD_4nXcfsKj8ZY2aqNDC9KlMfPBP-tMpXiuQ99g81dRQOupI83CGwYm00w7xb1U-tqkZx1yj0ZGp13Kx288dOdNuzw1lC3INfSttUIrOCLzyCD1y2Db_kEVEhKqtKmauurp3wERj7KwMz2BQLjKeF1b5tGefeIEx?key=gRO4Wih9euT2ZU7mHveHOA" alt=""><figcaption></figcaption></figure>

В позиции “Способ совершения телефонных звонков” выберите звонки по API Новофон.

* Если выбрать пункт Отключить звонки, то этот сотрудник не сможет совершать звонки и иконка телефона возле номеров телефона у него не будет отображаться.
* Звонки через приложение - при нажатии на иконку телефона звонок будет перенаправлен в приложение, установленное для звонков на Вашем устройстве (Zopier и тд).
* Звонки по API Zadarma - при клике на иконку телефона АТС звонок поступит сотруднику, чей id вы указали в карточке, а затем клиенту

После выбора способа совершения телефонных звонков в “Звонки по API Zadarma” появятся дополнительные поля, в которые следует вписать виртуальный номер и id вашего сотрудника в системе.

<figure><img src="https://lh7-rt.googleusercontent.com/docsz/AD_4nXd1Qs1Y4UIYBWaBGMqH7-LOMFAcXCimw8wdi5u5mohGA44BxPXvxpLqdSNgTW24e83BxUqA3bv0lDv3Tsbcx86Br7L8be0zmKSM0R1zm-_XZ3LSsBUj0EnmJL6NSQPM2rw28FSbrnXQX_fPO0t1ICo3Ubc?key=gRO4Wih9euT2ZU7mHveHOA" alt=""><figcaption></figcaption></figure>

Для осуществления звонка выбранным методом достаточно в карточке клиента нажать на иконку голубой телефонной трубки рядом с его номером телефона:

<figure><img src="https://lh7-rt.googleusercontent.com/docsz/AD_4nXdjWCXnaAvatRtdcwJ8tprGJOfHLFwfNpBRmIZxCw744nQM99BJSMRFliIvi72qJIXf-OgvjCnnJeMrEcIloKoynmyyuaGXVSBcapjDtRkduRJJ5QCAKtM3Z_s16Lf_5Zjj3Xkka7tKicBslOPYFlA5xaM?key=gRO4Wih9euT2ZU7mHveHOA" alt=""><figcaption></figcaption></figure>

### Настройка вебхуков

Для того чтобы настроить получение колбэков о завершении звонка, необходимо в системе Новофон перейти в раздел “Интеграции” - “Уведомления о событиях v1”. Здесь нажимаем “Подключить интеграцию”.

<figure><img src="https://lh7-rt.googleusercontent.com/docsz/AD_4nXct3WNXZvX7ApKmd3pwgerID1h6WUlXsRk6dobKk8hNJIVZ8vMXs9TIkf6ECAx3tRKaDZ3iBbGVs7kGbORvBYbSIBH5-GR3T4bb0DH-vzqbFYtP-stAVhmYgMs84o28b6ebGw-sbPGqaH4hxsxInnnqZNk?key=gRO4Wih9euT2ZU7mHveHOA" alt=""><figcaption></figcaption></figure>

В поле “URL для уведомлений о звонках АТС” вставьте ссылку на вебхуки вида: https://chatter.salebot.pro/zadarma\_webhook/\<secret-key>, например, https://chatter.salebot.pro/zadarma\_webhook/4aa6\*\*\*\*\*\*\*\*\*\*\*

Обратите внимание! Secret используется тот, который Вы получили в Zadarma.

Также проставляем галочки на события, по которым хотим получать уведомления.

{% hint style="warning" %}
Обращаем внимание!

Обязательно внизу страницы переключаем ползунок “Интеграция активна”
{% endhint %}

<figure><img src="https://lh7-rt.googleusercontent.com/docsz/AD_4nXd_X5TeU-tLngdc9ahbFW3ahcgZyyiwbs4_QOle3d3zIzCzMAcC4Jk__5H-fyOYdnOufihFI6ZSMp42NsaNqXrJamBMUBlF3XvdgVFYWWLW53klFwZ6xr_u1uLaPH963gx3j6mRJaBeqzl8UShj55qGVDs?key=gRO4Wih9euT2ZU7mHveHOA" alt="" width="563"><figcaption></figcaption></figure>

При подтверждении всплывет уведомление вида:

<figure><img src="https://lh7-rt.googleusercontent.com/docsz/AD_4nXcOzz9iF4-4L6y1xWb9802_Sx6WE8_0OoucYQwZTI8B6bJb_7WGmFDyU5nhLG5_8CzFdu3TP366oQRdNrN4Mq-zaShjvLgqXxEKoiAY64hGjLx2j3ECoQpSwFFuvEuY3McQaApVhMhLCs_MaRGqB0rnQ4lr?key=gRO4Wih9euT2ZU7mHveHOA" alt=""><figcaption></figcaption></figure>

В результате при завершении звонков в Salebot будет приходить уведомление следующего вида:

<figure><img src="https://lh7-rt.googleusercontent.com/docsz/AD_4nXexUzvwL_33qGWS9yKWtirT_JICojwO_Hfx5-XhdgQr-GEWyWIXCb8prxnfpkKjHsL5cRSdO19oGTcu9SqXbKLEXVbOFLdTsacHdbzhhkO2SW_Z12fVbqMHxsiNYJEeRuuMWIq7MNh6FSqpqAmTkWIvBUnU?key=gRO4Wih9euT2ZU7mHveHOA" alt=""><figcaption></figcaption></figure>

В системе используются следующие статусы:&#x20;

NOTIFY\_START | NOTIFY\_OUT\_START  -> начало звонка&#x20;

NOTIFY\_END | NOTIFY\_OUT\_END -> конец звонка&#x20;

NOTIFY\_INTERNAL -> начало входящего звонка на внутренний номер АТС&#x20;

NOTIFY\_ANSWER -> ответ при звонке на внутренний или на внешний номер&#x20;

OUT в статусе означает, что звонок исходящий из Новофон.

Также если у звонка будет иметься запись разговора, то у клиента будет создана переменная zadarma\_record\_link, содержащая ссылку на запись.
