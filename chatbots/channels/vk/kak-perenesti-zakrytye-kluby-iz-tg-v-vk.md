---
description: В статье подробно расскажем, как перенести закрытые клубы из Telegram в VK
---

# Как перенести закрытые клубы из Tg в VK

## Подготовка закрытой группы Вк

Для начала необходимо подготовить закрытую группу Вконтакте:

Создайте группу/сообщество Вконтакте (если у вас еще нет сообщества):

<div data-with-frame="true"><figure><img src="../../../.gitbook/assets/Снимок экрана 2026-02-24 в 11.11.32.png" alt="" width="563"><figcaption></figcaption></figure></div>

Затем перейдите в настройки и найдите поле "Тип сообщества":

<div data-with-frame="true"><figure><img src="../../../.gitbook/assets/Снимок экрана 2026-02-24 в 11.12.15.png" alt="" width="563"><figcaption></figcaption></figure></div>

Измените тип на "Закрытое":

<div data-with-frame="true"><figure><img src="../../../.gitbook/assets/Снимок экрана 2026-02-24 в 11.14.38.png" alt="" width="563"><figcaption></figcaption></figure></div>

Далее перейдите во вкладку настройки для бота и включите возможности ботов:

<div data-with-frame="true"><figure><img src="../../../.gitbook/assets/Снимок экрана 2026-02-24 в 11.15.53.png" alt="" width="563"><figcaption></figcaption></figure></div>

<div data-with-frame="true"><figure><img src="../../../.gitbook/assets/Снимок экрана 2026-02-24 в 11.17.17.png" alt="" width="563"><figcaption></figcaption></figure></div>

## Подключение группы в Salebot

Далее переходим в Salebot. В разделе каналы выбираем ВК и подключаем сообщество.

<div data-with-frame="true"><figure><img src="../../../.gitbook/assets/Снимок экрана 2026-02-24 в 11.18.32.png" alt="" width="563"><figcaption></figcaption></figure></div>

<div data-with-frame="true"><figure><img src="../../../.gitbook/assets/Снимок экрана 2026-02-24 в 11.20.01.png" alt="" width="563"><figcaption></figcaption></figure></div>

{% hint style="info" %}
[Подробнее о подключении чат-бота для группы VK рассказали в одноименной статье.](chat-bot-dlya-gruppy-vk.md)
{% endhint %}

Активируем переключатели:

<div data-with-frame="true"><figure><img src="../../../.gitbook/assets/Снимок экрана 2026-02-24 в 11.20.40.png" alt="" width="563"><figcaption></figcaption></figure></div>

Переходим по ссылке [https://vkhost.github.io/](https://vkhost.github.io/) для получения токена:

<div data-with-frame="true"><figure><img src="../../../.gitbook/assets/Снимок экрана 2026-02-24 в 11.21.24.png" alt="" width="563"><figcaption></figcaption></figure></div>

И нажмите "Получить":

<div data-with-frame="true"><figure><img src="../../../.gitbook/assets/Снимок экрана 2026-02-24 в 11.22.10.png" alt="" width="563"><figcaption></figcaption></figure></div>

Необходимо подтвердить:

<div data-with-frame="true"><figure><img src="../../../.gitbook/assets/Снимок экрана 2026-02-24 в 11.28.09.png" alt="" width="563"><figcaption></figcaption></figure></div>

А после скопировать в браузерной строке токен:

Вы увидите ссылку следующего вида:

https://oauth.vk.com/blank.html#access\_token=<mark style="color:$danger;">**vk1.a.VFkjZgOWXiNF0c\_q4OxuA7dx72ygOLbjZagmFrQeJYE55v32GvJSVtRckjlU\_yE7Ierh3PZFsdfsdgsgsfbdbddOBuvUYaOWcuhxDntp0MZxYF3K8kKtDeQ7p8oDOjSCM7EKSkl0CvJpw91DWUhMQNARTnoLtzA**</mark>\&expires\_in=0\&user\_id=1234\&email=tets@mail.ru

Вам нужно скопировать часть ПОСЛЕ <mark style="color:$success;">**access\_token=**</mark> и ДО <mark style="color:blue;">**\&expires\_in**</mark> (то, что выделено красным в примере выше!).

Далее перейдите в настройки проекта в Salebot и сгенерируйте API-ключ:

<div data-with-frame="true"><figure><img src="../../../.gitbook/assets/Снимок экрана 2026-02-24 в 11.31.48.png" alt=""><figcaption></figcaption></figure></div>

Далее в разделе "Переменные" в настройках проекта создайте переменные:

1. save\_webhook=1
2. access\_token=vk1.a.VFkjZgOWXiNF0c\_q4OxuA7dx72ygOLbjZagmFrQeJYE55v32GvJSVtRckjlU\_asdfsdfsfsdfsdfuvUYaOWcuhxDntp0MZxYF3K8kKtDeQ7p8oDOjSCM7EKSkl0CvJpw91DWUhMQNARTnoLtzA

<div data-with-frame="true"><figure><img src="../../../.gitbook/assets/Снимок экрана 2026-02-24 в 11.33.22.png" alt=""><figcaption></figcaption></figure></div>

{% hint style="warning" %}
**ВАЖНО!**

**В переменной access\_token УКАЖИТЕ СВОЙ ПОЛУЧЕННЫЙ ТОКЕН!**
{% endhint %}

## Настройки чат-бота

В блоке после успешной оплаты добавляем клиента в Список и выдаем ссылку на группу.

{% hint style="info" %}
Внимание!

Список заранее нужно создать в соответствующем разделе.
{% endhint %}

<div data-with-frame="true"><figure><img src="../../../.gitbook/assets/Снимок экрана 2026-02-24 в 11.37.54.png" alt=""><figcaption></figcaption></figure></div>

\
Когда пользователь подает заявку приходит колбек <mark style="color:$warning;">**client\_group\_join request**</mark>

Настраиваем блок с проверкой на это условие.

После блока делаем переходы с проверкой наличия клиента в списке\
inlist(id списка)==True\
и\
inlist(id списка)==False

<div data-with-frame="true"><figure><img src="../../../.gitbook/assets/Снимок экрана 2026-02-24 в 11.38.47.png" alt=""><figcaption></figcaption></figure></div>

Если клиент есть в списке переводим в блок с одобрением заявки, ф-ция vk\_approve\_request(ID группы ВК, platform\_id, ТОКЕН администратора из ВК)

<div data-with-frame="true"><figure><img src="../../../.gitbook/assets/Снимок экрана 2026-02-24 в 11.46.07.png" alt=""><figcaption></figcaption></figure></div>

Если клиента нет в списке, удаляем его:

<div data-with-frame="true"><figure><img src="../../../.gitbook/assets/Снимок экрана 2026-02-24 в 11.46.53.png" alt=""><figcaption></figcaption></figure></div>
