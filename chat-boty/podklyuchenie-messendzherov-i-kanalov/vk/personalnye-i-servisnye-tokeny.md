# Персональные и сервисные токены

## Персональный токен доступа

Для некоторых методов калькулятора для ВК может потребоваться токен пользователя. Для его получения перейдите по ссылке:[ https://vkhost.github.io](https://vkhost.github.io). \
Далее прочтите инструкцию и выберите пункт настройки:

<figure><img src="https://lh7-rt.googleusercontent.com/docsz/AD_4nXdltYVIhZQYMWwy8QgtlX0JNPPf40wemk4H9vtjuA9dh603x01O7rush0oY5wdFToWjmuH8lJN7Zc2k8pb_4YoFVh9_X7ObzV_ChjNKT5GAIGa7lk7TeuE0pjN_xf87dKqre1Gjcg?key=7gBYiIsUQfHzAEcQPztY1g" alt=""><figcaption></figcaption></figure>

Далее удостоверьтесь, что активированы пункты, как на скриншоте ниже.&#x20;

<figure><img src="https://lh7-rt.googleusercontent.com/docsz/AD_4nXdqvXIAZBidVQk8L_X9ERwevmAdQrGJGiO-TgotY-LMjHhwu415uRs5uMi091t3iiI9o7Mso54SlSUAq9wsHcS9G-53uai6kyWx7O83UqTsr8Z8NDvVZl6N6UH8N10v8JbQXkT5YQ?key=7gBYiIsUQfHzAEcQPztY1g" alt=""><figcaption></figcaption></figure>

Нажмите Получить, далее в открывшемся окне нажмите Разрешить.

<figure><img src="https://lh7-rt.googleusercontent.com/docsz/AD_4nXcFXXTH2bH5fx8vk92gB8IJlQKIIe433Vpyoa8-sB6gpoxT_jUhtR_qA8aC084PxoBhIlLb1nmd2BA97s31k3Eqn9b3P25JcKNMcUW2ioe1DD6LpsXrxkFL5MaGF9NDHDgwhxm4?key=7gBYiIsUQfHzAEcQPztY1g" alt=""><figcaption></figcaption></figure>

После этого для удобства скопируйте все из адресной строки в любой текстовый редактор, она будет иметь такой вид: https://oauth.vk.com/blank.html#access\_token=xxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxx\&expires\_in=0\&user\_id=xxxxxxx\&email=xxxxxxxxxxxxxxxx \
Для извлечения токена найдите в ссылке ‘access\_token=’ и удалите все, что идет до знака равенства, затем найдите ‘\&expires\_in’ и оставьте только то, что идет до знака &. В итоге останется только токен.

{% hint style="warning" %}
Внимание! Персональный токен ни в коем случае нельзя передавать кому-либо, так как он может быть использован для получения полного доступа к странице, для которой он был получен.
{% endhint %}

Полученный токен можете сохранить в любую удобную переменную и передавать ее в качестве параметра. Все действия, совершенные с помощью этого токена, будут отмечены как совершенные Вами (отправка в бан, принятие в группу).

### Функция для проверки пользователя онлайн (VK) vk\_check\_user\_online(token)

<table><thead><tr><th width="217">Параметры функции</th><th>Значение параметра</th><th>Ответы</th></tr></thead><tbody><tr><td><strong>token</strong></td><td>индивидуальный <strong>access_token</strong> пользователя</td><td><p><strong>True</strong> — в сети</p><p><strong>False</strong> — не в сети</p></td></tr></tbody></table>

## Сервисный токен VK Vision

Vision | Технологии компьютерного зрения от VK Cloud. Воспользуйтесь готовыми решениями для автоматизации анализа фото и видео

{% hint style="warning" %}
<mark style="color:red;">**Внимание!**</mark> Услуга платная.
{% endhint %}

1. Зарегистрироваться на сайте [https://mcs.mail.ru/app/auth](https://mcs.mail.ru/app/auth)
2. Войдите в раздел AI API (Машинное обучение) ->Vision Компьютерное зрение&#x20;

<figure><img src="https://lh7-rt.googleusercontent.com/docsz/AD_4nXeUuttW1240Cn_ZgSgzXIwljfmwCndacVwEWOuCKgDojDwfPCb_D2WKfVcy5Vh7iH2bA6kYpLXVpIfi0DJgvQCG_06w7DP9WvAztRJw-W5Gt-nNV1Debucgyh0f7eCGRdZ_IWjV4w?key=7gBYiIsUQfHzAEcQPztY1g" alt=""><figcaption></figcaption></figure>

3\. Добавьте доступ через Сервисные токены

<figure><img src="https://lh7-rt.googleusercontent.com/docsz/AD_4nXfVq8HPTCz0tAMQVQ9Fahc2qOgSkn6H5N0EO_j60kTLU0ZjoLto3vtzIFXElZZKdl8OQB9U-NqRx5hyULXmrbQiTnNroQguOHnpnRXE_l2WC0SL2hlSBsw_6Q3LNWjd9BWDHeWo?key=7gBYiIsUQfHzAEcQPztY1g" alt=""><figcaption></figcaption></figure>

4\. Скопируйте полученный сервисный токен. Можете работать.
