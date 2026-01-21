# SMS-сервисы

Вы можете интегрироваться с любым сервисом отправки SMS-сообщений, у которого есть API. Данные сервисы представлены для примера интеграции.

## Как работать с SMS.RU

Пример работы с [sms.ru](https://vk.com/away.php?to=http%3A%2F%2Fsms.ru\&cc_key=)\
\
Запрос: **GET**\
url:\
**https://sms.ru/sms/send?api\_id=#{sms\_api\_key}\&to=#{phone}\&msg=#{msg}\&json=1**\
\
где \
&#xNAN;**#{sms\_api\_key}** - api ключ сервиса\
&#xNAN;**#{phone}** - телефон пользователя, кому уходит смс\
**msg** - сообщение

<figure><img src="../../.gitbook/assets/image (125).png" alt=""><figcaption></figcaption></figure>

Ссылка для регистрации: [https://evlanalytics.sms.ru ](https://evlanalytics.sms.ru)
