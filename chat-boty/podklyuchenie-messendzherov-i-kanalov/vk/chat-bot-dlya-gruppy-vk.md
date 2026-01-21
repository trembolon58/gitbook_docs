# Чат-бот для группы VK

{% hint style="warning" %}
ВАЖНО! При подключении группы Вконтакте необходимо учесть следующее:

1. **Максимальная длина текстового сообщения 4096 символов**
2. В сутки вы можете отправить сообщение не более 20 людям, которые не являются вашими друзьями и не состояли с вами в переписке до этого.
3. К сообщению можно прикрепить максимум 10 вложений
4. Сообщение можно редактировать в течение 24ч
5. Ограничения при использовании кнопок:
6. Клавиатура может отображаться внутри сообщения — это inline-отображение. Чтобы включить его, передайте параметр inline в объект клавиатуры.&#x20;

&#x20;       Её максимальный размер составит 5 × 6.&#x20;

&#x20;       Максимальное количество клавиш: 10.

5. По умолчанию, если не передан параметр inline, клавиатура показывается под полем ввода в диалоге с пользователем (reply).&#x20;

&#x20;       Максимальный размер стандартной клавиатуры — 5 × 10.&#x20;

&#x20;       Максимальное количество клавиш: 40.

[Подробнее в первоисточнике](https://dev.vk.com/api/bots/overview)
{% endhint %}

## Подключение группы ВКонтакте

Для подключения сообщества Вконтакте, Вам необходимо перейти  в раздел "Каналы" и выбрать Вконтакте.

<figure><img src="https://lh7-rt.googleusercontent.com/docsz/AD_4nXecWNZ3aumMwS5UoYJGZLTaFCfzDv-9DBVLVa3vftXe9-R-On0MxoGOuhUioKyIHx8fpBMH44Bsuo2mzhj7L60Z9cx6FSmrOvz_4cCiHpzm8Tu_Afggj3wNT4KPcFDT5iBSSyDpMw?key=HrfPDBYux3Rnmgtyn6-Vww" alt=""><figcaption><p>Подключение бота ВКонтакте</p></figcaption></figure>

Если ранее Вы не авторизовывались через Вконтакте на Salebot, то увидите кнопку "Подключить Вконтакте", на которую необходимо кликнуть:

![Авторизация Вконтакте для получения списка групп, в которых Вы являетесь Администратором](<../../../.gitbook/assets/image (166).png>)

Далее будет выведен список со всеми группами, в которых Вы являетесь администратором, а следовательно, у Вас есть права для подключения к ним бота.&#x20;

В списке будут также отображены группы, у которых отключены сообщения. (Для включения сообщений необходимо перейти в настройки группы, в разделе "сообщения" поставить галочку "разрешить сообщения").&#x20;

Если какая-то из ваших групп уже подключена к другому проекту, будет указан номер этого проекта.&#x20;

В качестве примера подключим группу “Тест”.

<figure><img src="https://lh7-rt.googleusercontent.com/docsz/AD_4nXcIhV1F6iYyxp2tZrODbOm-4r1DK3lMKgDQj2oVa5bXS971SSXh1P-93Bn7wCKJfd6SHS8BCKDrdQCBncDu4EJ611YpTRWoOBT0ZxZ1512BLFQj_E0yPGtxuV3RLXW5LuYV5U0z4w?key=HrfPDBYux3Rnmgtyn6-Vww" alt="" width="563"><figcaption></figcaption></figure>

После нажатия "Подключить" необходимо разрешить системе доступ к основным разделам группы ВКонтакте (здесь также жмем Разрешить).&#x20;

<figure><img src="https://lh7-rt.googleusercontent.com/docsz/AD_4nXdf9WPBPoYLz90mjruPKIFdFi-2ZKiwlkvyhBiyouqLS3Lxc0b0Vt1h79McFOgOKlsiFTzhdZdS7Yus-CRhES28siHJOFqxQAXhSin9rawjr9vrwRQWfgWsDms7HA_RINE8Yv5Q?key=HrfPDBYux3Rnmgtyn6-Vww" alt="" width="563"><figcaption><p>Выдача разрешения доступа к основным разделам группы</p></figcaption></figure>

{% hint style="warning" %}
<mark style="color:red;">**ОБРАТИТЕ ВНИМАНИЕ!**</mark> При подключении дважды запрашивается доступ к группе, так как создаются два ключа доступа к Вашей группе с разным уровнем доступа.

<mark style="color:red;">**ДАТЬ РАЗРЕШЕНИЕ НАДО 2 РАЗА!**</mark>

Также с ключом доступа сообщества можно совершать до 20 запросов в секунду.
{% endhint %}

> Обратите внимание, что с ключом доступа сообщества можно совершать до 20 запросов в секунду.

После успешного подключения группы она появится в списке ботов Вконтакте.

<figure><img src="https://lh7-rt.googleusercontent.com/docsz/AD_4nXfTS2pwmkmY9QrY97b_gxxpJa9ddbMuYsg4b4ME6oKES3POy06vvtAtasIejM_C2CdSRKRW2LxQkGZeEjNlXcxK2uW1s3gQ0tpJW5Pv72dxJPfDZtoAKEE4P_rqSBt5GNmCh6Lj2Q?key=HrfPDBYux3Rnmgtyn6-Vww" alt=""><figcaption><p>Список ботов ВКонтакте</p></figcaption></figure>

На этом подключение бота к группе ВКонтакте завершено.

### Видео-инструкция

{% embed url="https://www.youtube.com/watch?v=VLT5QSXIyKo&feature=youtu.be" %}

## Установка приложения Salebot в сообщество ВКонтакте

Для работы с Подписной страницей Вконтакте, необходимо установить в сообщество ВКонтакте приложение Salebot .

Ссылку на приложение можно получить на платформе Salebot в разделе Сайты- создать сайт - Страница сайта - Настройки - Мессенджеры - нажать на ссылку для установки приложения:

<figure><img src="https://lh7-rt.googleusercontent.com/docsz/AD_4nXfv5pJzs4L6zQnuIB-dK90nBerjM9_7-lysZR0a5aHNDlO9k5FJOqxtmsy_zfWt5-5kE6f7wQ2vP8iFpTxPASeItutF-NSd3CZraD6AvJNCQV_Dpdaq8ZrSGh19biMCwB_Y-lWdnw?key=HrfPDBYux3Rnmgtyn6-Vww" alt=""><figcaption></figcaption></figure>

<figure><img src="https://lh7-rt.googleusercontent.com/docsz/AD_4nXe6gYsL6rYxA4cFgjv1_G0qPBqyeUL5AJwN7COwc4t9009PXAqKyFhBNUM8NUuznPHrcTiUL_0pfcUoE8njrPBAViYV9OWsWJKj--Yv9G-zl6zhuG50GGYjmgkXElSDFuRCbaDS?key=HrfPDBYux3Rnmgtyn6-Vww" alt="" width="563"><figcaption></figcaption></figure>

Далее выберите сообщество, в которое необходимо добавить приложение Salebot:

<figure><img src="https://lh7-rt.googleusercontent.com/docsz/AD_4nXd1tDmNN-Yx0HrFrrDKrkxwuuVdmBL5L_w4U-BXK98V5FABIhC3DdbACQG8StZABd7pXxoMx_Mq0CalymSRx3JYXCrgO8_D5MNyjOWcZlazOaFHBzuo8MVNgn2vUATwDe9zVESLVg?key=HrfPDBYux3Rnmgtyn6-Vww" alt="" width="563"><figcaption></figcaption></figure>

## Уведомления о прочтении сообщений

Для клиентов ВК есть возможность включить функцию прочитанности сообщений.

Для этого в разделе Каналы для группы ВК необходимо переключить бегунок Прочитанность сообщений.

<figure><img src="https://lh7-rt.googleusercontent.com/docsz/AD_4nXcPhXXkP5yscW8G2X0lSEtM05pXSMXAQ55xEhnH5A7MvaiuQvunspc32qIFhi2-IZRxyarIlDlazZ8-OZGyOUf6xOkRIp5dyb87xdsJcZtk_yhh4k-ieJj06cEU-U_Av9WOvjzXGQ?key=HrfPDBYux3Rnmgtyn6-Vww" alt=""><figcaption></figcaption></figure>

После включения уведомления в диалогах можно увидеть сообщения, помеченные галочками. Одна галочка - не прочитано. Две галочки - прочитано.

<figure><img src="https://lh7-rt.googleusercontent.com/docsz/AD_4nXcfW9-mj3Cz3Y-LolM-TUY8XH2ngbBXW5uR7TTJlOBeuCv-mK3MP3pyVIBuMBZWZnTOW8NTVxD0aefX606rldgim3LuxcKBNbhfX9u8sRLD7QoJii-ymLHOlnCRAdO4o-pkQRqnfw?key=HrfPDBYux3Rnmgtyn6-Vww" alt="" width="563"><figcaption></figcaption></figure>

В рассылках при включенной Прочитанности сообщений появляется статистика. На примере ниже в рассылке 24 сообщений ВК, из них просмотрено 12

{% hint style="warning" %}
Рассылка должна быть создана в конструкторе воронок из блоков состояния диалога.

Из **раздела Рассылки и из блоков Не состояния** - статистика о прочтении <mark style="color:red;">**НЕ БУДЕТ СЧИТАТЬСЯ.**</mark>  Потому что клиент <mark style="color:red;">**не находится в данных блоках.**</mark>&#x20;
{% endhint %}



<figure><img src="../../../.gitbook/assets/image (167).png" alt=""><figcaption></figcaption></figure>

На прочитанные сообщения можно установить уведомления.&#x20;

Для этого в блоке с сообщением необходимо включить значок с двумя галочками.

<figure><img src="https://lh7-rt.googleusercontent.com/docsz/AD_4nXfwupgflSnM34X9U1amqzbKzv3ktRJQrNbR3zSuOYPsveqjxn9bFQvrb6HFkBpdKBPEtBsWp6w9wkO6zqDUj_X1D6CJmmLrvp2-YqkZqVis5bW5MPmTBPoNdC2EGqZGCplj8syVqg?key=HrfPDBYux3Rnmgtyn6-Vww" alt=""><figcaption></figcaption></figure>

{% hint style="info" %}
В работе с Вконтакте учитывайте следующее:

1. Максимальная длина текстового сообщения 4096 символов
2. В сутки вы можете отправить сообщение не более 20 людям, которые не являются вашими друзьями и не состояли с вами в переписке до этого.
3. К сообщению можно прикрепить максимум 10 вложений
4. Сообщение можно редактировать в течение 24ч
{% endhint %}

### Параметр уведомление о прочтении: message\_read

{% hint style="warning" %}
Помните: **Callback о просмотре работает в ВК и email!**
{% endhint %}

<figure><img src="https://lh7-rt.googleusercontent.com/docsz/AD_4nXczsjUPFxXkqOvoZT7GoYiw90SgYqX7QBF4YM94iHc7gtLsiLHd4uerHWwo4bMi4qQ-vGrHq2GTuwB5CGwwI4COXuh-kSPo1iQTDgHTY5RNW458v5JshUit8fShcbQc_er12ek_8A?key=HrfPDBYux3Rnmgtyn6-Vww" alt="" width="563"><figcaption><p>Пример Уведомления о прочтении для запуска блока с условием</p></figcaption></figure>

{% hint style="danger" %}
Важно

**Callback придет**, <mark style="color:orange;">**только если клиент находится в данном блоке**</mark>, если он его покинул, то коллбэка не будет.
{% endhint %}

## Как прописать метку в прямой ссылке на сообщения группы ВКонтакте

С помощью данной настройки Вы можете отслеживать с какого именно места/источника перешел пользователь который пишет в сообщения группы.

**Для чего это можно использовать:**

1\. Оценивать эффективность контента, в котором даёте помеченную ссылку на сообщения группы и призываете написать вам.\
2\. Для запуска в боте определенной ветки воронки, проверяя наличие переменной/метки. Давать разный контент в зависимости от того, откуда пришел пользователь.

**Как пользоваться:**

* Ссылка на бота Вашей группы отображена рядом именем группы в списке ботов Вконтакте, скопируйте ее

<figure><img src="https://lh7-rt.googleusercontent.com/docsz/AD_4nXd0uVPvjy3217oWXjr7xCBL89eTf5I75n_SeTqb-Ub4Cfew0sH4ySdUlmXC4mxfelagA2XNGNbgMnQTb59q44qnOdpRP8xJ_16QM2ghbzZEGfDEFZz6rhxnxd-PHgc5nTU5HQG69g?key=HrfPDBYux3Rnmgtyn6-Vww" alt=""><figcaption></figcaption></figure>

* Дописываем к полученной ссылке метки\
  Передать можно два параметра:\
  **ref** и **ref\_source**

Получаем ссылку следующего вида:\
https://vk.com/im?sel=-198248940&**ref=параметр1**&**ref\_source=параметр2**\
вместо “параметр1” и “параметр2” вписываете значения своих меток

**Есть еще 2 варианта ссылок:**\
vk.me/**group\_name**?ref=параметр1\&ref\_source=параметр2\
где **group\_name** - идентификатор вашего сообщества

**или**

vk.com/write-**group\_id**?ref=параметр1\&ref\_source=параметр2 \
где **group\_id** - уникальный числовой идентификатор сообщества

#### Пример использования

Отследим, сколько пользователей пришло в **https://vk.com/public202836320** с телеграм канала Test.\
Для начала соберем ссылку, например, такую:\
vk.me/public202836320?ref=telegram\&ref\_source=test

или вот такую:&#x20;

vk.com/write-202836320?ref=telegram\&ref\_source=test

{% hint style="info" %}
Обратите внимание, что в ссылке должен быть только один знак вопроса **?**, далее мы присоединяем параметры через знак апмерсанта **&**
{% endhint %}

И разместим в канале, при переходе по данным ссылкам откроется диалог и на любое сообщение пользователя ему запишется две переменные в Salebot:

<figure><img src="https://lh7-rt.googleusercontent.com/docsz/AD_4nXetWijeMeXDIi4Kij2Fnw_zvsYEpM1zDDt-eYkPyPxK545oGGthTFp4ftb9w74PHsbMD6C-wPfysicAZvOxedxmWJe6VOAzvIvnw8v6jHQAgoPJkG2u8KeZnFJvDu8X7ifKUVJ45A?key=HrfPDBYux3Rnmgtyn6-Vww" alt="" width="375"><figcaption><p>Получение меток из прямых ссылок ВКонтакте</p></figcaption></figure>

## Автоматизация группы с помощью Salebot

Заходим в Каналы, включаем все события для бота, как на скрине:

<figure><img src="https://lh7-rt.googleusercontent.com/docsz/AD_4nXcEMoWjit4oxsmqWaR0hYLiuj8JOrYCNJ-YUjKM4JTUOIuQslCN16a_TGKNKF6o_ud7SSkIwqY3eGB09zumbxdLq5-hAa8ikZBSkgFICzwpORm6KmefWjU4-AkWPBm2W0zT8SkA?key=HrfPDBYux3Rnmgtyn6-Vww" alt=""><figcaption><p>Подключение событий, на которые должен реагировать наш бот</p></figcaption></figure>

Когда пользователь будет совершать то или иное действие, вы это сможете отследить с помощью коллбэка события:

### 1. Событие: Пользователь оставил новый комментарий

**client\_wall\_reply\_new**

Колбек приходит в виде:

<figure><img src="../../../.gitbook/assets/Снимок экрана 2025-10-27 в 11.16.43.png" alt="" width="375"><figcaption></figcaption></figure>

где 10 — id поста, под которым был оставлен комментарий\
"круто!" — текст оставленного комментария

**Дополнительные параметры сохраняются в переменные**:

<figure><img src="https://lh7-rt.googleusercontent.com/docsz/AD_4nXdszFdevvEd4WTGV3Oiksue3LFLAaEt2aeqCpLJ7tly2onsL3EMLLa1Sl0jdgpGQYoA8itYsXSigEN1m9vMIKB08RPYxbzlxPaVV6SVbFW5ykOYIUf2zBlpVgudfB4Xq5RX9fUX?key=HrfPDBYux3Rnmgtyn6-Vww" alt="" width="375"><figcaption><p>Дополнительные переменные коллбэка на событие Пользователь оставил комментарий</p></figcaption></figure>

wall\_reply\_text — текст комментария, который оставил пользователь

wall\_reply\_id — id комментария

wall\_reply\_post\_id —id поста, который комментируют

wall\_reply\_to\_user — id пользователя, которому ответили

wall\_reply\_to\_comment — id комментария, который оставили

### 2. Событие: Пользователь сделал репост записи себе на стену

**client\_wall\_repost**

<figure><img src="../../../.gitbook/assets/Снимок экрана 2025-10-27 в 11.17.34.png" alt="" width="361"><figcaption></figcaption></figure>

в данном случае 1 — это id поста, который репостнули

{% hint style="warning" %}
Обращаем внимание!\
Если профиль пользователя Вконтакте <mark style="color:red;">**закрыт**</mark>, то коллбэк о репосте на стену не приходит!
{% endhint %}

**Дополнительные параметры сохраняются в переменные:**

<figure><img src="https://lh7-rt.googleusercontent.com/docsz/AD_4nXdIU--9Np0aBYcXADCHA1bNtEEIU0AI_9nOi_knicspoTUEQhdNJj-TAStM81-pk3JmN4F4VSaXTjBoG8cPT6CFVBlVL2mhsZfXBazng1IFznt8DIS8YgJpOx4p2WaDJJOcUot1LQ?key=HrfPDBYux3Rnmgtyn6-Vww" alt="" width="563"><figcaption><p>Дополнительные переменные к коллбэку на событие Пользователь сделал репост</p></figcaption></figure>

wall\_repost\_text — текст, который пользователь добавляет к репосту

wall\_repost\_post\_id — id поста, который репостнули

### 3. Событие: Вступление в группу

**client\_group\_join**&#x20;

Когда у вас добавится новый подписчик, коллбэк будет отображаться так:

<figure><img src="../../../.gitbook/assets/Снимок экрана 2025-10-27 в 11.18.28.png" alt="" width="356"><figcaption></figcaption></figure>

### 4. Событие: **Выход из группы**

**client\_group\_leave**

<figure><img src="../../../.gitbook/assets/Снимок экрана 2025-10-27 в 11.19.05.png" alt="" width="372"><figcaption></figcaption></figure>

### 5. Событие: **Клиент лайкнул пост**

**client\_liked\_post**

<figure><img src="../../../.gitbook/assets/Снимок экрана 2025-10-27 в 10.53.24.png" alt=""><figcaption></figcaption></figure>

Вы можете настраивать разные реакции на коллбэки. Например, присылать сообщение клиенту в лс:

<figure><img src="../../../.gitbook/assets/Снимок экрана 2025-10-27 в 10.47.38.png" alt=""><figcaption></figcaption></figure>



<figure><img src="https://lh7-rt.googleusercontent.com/docsz/AD_4nXe05rhJ9QOYJm4TjhFy_RCKQLLi3J8A35XWVJvRWFOp6X7Q4jSGdEyw5HC485UIi2EThBG0fOSyMhm9RhRPiHYEtLr4kNMx3oFM4zy-fz4mBokT7T6sH6kLNL-bripwFyeJDAkk5w?key=HrfPDBYux3Rnmgtyn6-Vww" alt="" width="563"><figcaption><p>Пример ответа бота из карточки клиента</p></figcaption></figure>

<figure><img src="https://lh7-rt.googleusercontent.com/docsz/AD_4nXd-3vRm6l5MOoFEHQXzLQmlB-AxxozA9iwQM2wmSqI1zcPNF9CzPCXz43vH1ShYs4CGhjrVtH1VDpbTfLbNnivKY1v43ffbjETCU5cqBfwtQTs2c9vtsBm8vbtbMx4hrnfSXWtrjQ?key=HrfPDBYux3Rnmgtyn6-Vww" alt="" width="563"><figcaption><p>Пример ответа бота Вконтакте</p></figcaption></figure>

В примере в условии стартового блока прописано только тело колбека "client\_liked\_post" без ID поста — в таком бот будет реагировать на лайк под любым постом.

Если в условии указать весь текст колбека (тело колбека + ID поста), а в выборе соответствия установить "Полное совпадение", то бот будет реагировать на лайки только под определенным постом (ID которого передан в условии):

<figure><img src="../../../.gitbook/assets/Снимок экрана 2025-10-27 в 11.07.57.png" alt=""><figcaption></figcaption></figure>

<figure><img src="../../../.gitbook/assets/Снимок экрана 2025-10-27 в 11.15.07.png" alt=""><figcaption></figcaption></figure>

{% hint style="warning" %}
При лайке, репосте, вступлении в группу и выходе из неё **клиент не создаётся**
{% endhint %}

{% hint style="danger" %}
Если клиент не давал разрешения на сообщения или не писал ничего ранее в личные сообщения группы, то вы первым написать ему не сможете (например, приветствовать в личку сразу при вступлении в группу **нельзя)**
{% endhint %}

<figure><img src="https://lh7-rt.googleusercontent.com/docsz/AD_4nXfQXRQ995X5pZr3iDWiF2oWnpxqZ9NHNJSZ0_tLmtm7aOjbKYY3ymd1Jonk0v8LPhyl885mToWkDFlZUoIrt92i91cT4KURl7JfGvODystNU-4STJgwMhmikre0Rhy1t1kjuMou3g?key=HrfPDBYux3Rnmgtyn6-Vww" alt="" width="563"><figcaption></figcaption></figure>

Такое вы увидите, если клиент не дал разрешение на отправку сообщений или не писал ничего ранее в личные сообщения группы

Колбеки:&#x20;

**client\_group\_join request** - подан запрос на вступление в группу  \
**client\_group\_join approved** -  клиент принят в группу

### 6. Событие: Реакция на сообщение

Для включения колбека для реакции на сообщение нужно зайти в управление, пункт в настройках работа с API, выбрать во вкладке callback API наш сервер и зайти в типы событий, там найдете Действие с реакциями на сообщение и поставите галочку напротив этого поля. После этого в чаты будет приходить коллбэк с информацией на сообщение с каким conversation\_id была реакция и какая.

`react 2 on 629` - 2 реакция на cmID 629

`cancel reaction on 629` - отменил ранее поставленную реакцию на cmID 629

## Как работать с комментариями под постами ВКонтакте

Чтобы иметь возможность отвечать под комментариями, необходимо вручную добавить токен.&#x20;

Для этого заходите в Вашу группу ВКонтакте, открываете Управление / Дополнительно / Работа с API:

<figure><img src="../../../.gitbook/assets/Снимок экрана 2025-06-26 в 16.20.29.png" alt=""><figcaption></figcaption></figure>

<figure><img src="../../../.gitbook/assets/Снимок экрана 2025-06-26 в 16.20.53.png" alt=""><figcaption></figcaption></figure>

Нажимаете "Создать ключ" и копируете его.

<figure><img src="../../../.gitbook/assets/Снимок экрана 2025-06-26 в 16.25.19.png" alt=""><figcaption></figcaption></figure>

Дальше переходите в Salebot, раздел Каналы, и для подключенного бота ВКонтакте выбираете "Показать токены".

<figure><img src="https://lh7-rt.googleusercontent.com/docsz/AD_4nXemznvCgt6iJewdKfM68-80NvEuMXmiYjiUOW9EMIdvhGAqoBuNm6MAewkIIMXfa7jrZVoIvni2VbjsXUA7DHeG5kxhytA34uGYCG4CWBqnkvF9VVx141FTN1RBZ1gaoG6p7F7e?key=HrfPDBYux3Rnmgtyn6-Vww" alt=""><figcaption></figcaption></figure>

В открывшейся форме вставляете скопированный токен и нажимаете на кнопку "Добавить".

<figure><img src="https://lh7-rt.googleusercontent.com/docsz/AD_4nXelA7DnrfbMRm4muVDUz_dYBRzb8La1FmpWj_1n82FLoYxFp2A_AHwmhfGdfu3s-DDz_1QYp8lBOQ_ziNc1JVFIXpSyp_MBWb45tCw54wyW4Lf2yP3kmdXwU1r_ixQ1xWEacnBoCw?key=HrfPDBYux3Rnmgtyn6-Vww" alt="" width="563"><figcaption><p>Добавление ключа для комментирования на стене сообщества ВКонтакте</p></figcaption></figure>

После того, как добавили токен для работы с комментариями можно работать с комментариями, используя функции(API) в калькуляторе.&#x20;

Все возможные функции работы с комментариями для ВКонтакте можно увидеть в этой статье:

{% embed url="https://docs.salebot.pro/messendzhery-i-chaty/podklyuchenie-bota-k-vkontakte/api-vkontakte-funkcii-dlya-ispolzovaniya-vsekh-vozmozhnostei-vkontakte#kak-ostavit-kommentarii-na-stene-vo-vkontakte" %}

{% hint style="warning" %}
Все функции API указываем в Калькуляторе блока.
{% endhint %}

### Видеогид

{% embed url="https://youtu.be/mJ-oHT3zmyY" %}

## Настройка Чат-бота для группы

### 1. Подключение Чат-бота в группу

Чтобы можно было добавить бота в чат группы Вконтакте, необходимо в настройках включить это разрешение:

<figure><img src="https://lh7-rt.googleusercontent.com/docsz/AD_4nXfX_ePhEnWIBJXE6MVhuD4b11WUNUmlxKP6zvQGmA-e-h6RN6xlZlqV4UdZH02lRKQ91zm0JkotAdiRfXv3HExT3YW5g6C5h8Mm_um3JTKEL5Y-YZYCLJEiUtW12GdgHSMNuklMvw?key=HrfPDBYux3Rnmgtyn6-Vww" alt=""><figcaption><p>Подключение возможностей бота</p></figcaption></figure>

{% hint style="info" %}
Бот **с правами администратора видит все сообщения в чате**. Если бот не обладает этими правами, **бот видит только те сообщения, где его упомянули** через символ @
{% endhint %}

Общие переменные чата:

<table><thead><tr><th width="241">Переменные для чата</th><th>Описание переменной</th></tr></thead><tbody><tr><td>from_id </td><td>идентификатор того, кто отправил последнее сообщение </td></tr><tr><td>conversation_message_id</td><td>идентификатор последнего сообщения</td></tr></tbody></table>

Если в беседе кто-то перешлет сообщение, то в боте появятся эти переменные. В них будет указано, кто и что процитировал.

<table><thead><tr><th width="232">Переменные для чата</th><th>Описание переменной</th></tr></thead><tbody><tr><td>from_id</td><td>идентификатор того, кто процитировал</td></tr><tr><td>reply_from_id</td><td> идентификатор того, кого процитировали</td></tr><tr><td>reply_text </td><td>текст сообщения, которое было процитировано</td></tr><tr><td>reply_attachments</td><td>вложение, которое было процитировано</td></tr></tbody></table>



{% hint style="info" %}
После входящего сообщения в карточке клиента будет появляться переменная cmid, в ней хранится порядковый номер сообщения в чате.
{% endhint %}

Обратите внимание на требования к файлам: можно использовать публичные объекты, которые уже были загружены ВКонтакте (прислать фотографию со стены своего сообщества или видеозапись из поиска), или загрузить новое вложение.

{% hint style="info" %}
Ограничения при использовании кнопок:

Клавиатура может отображаться внутри сообщения — это **inline**-отображение. Чтобы включить его, передайте параметр inline в объект клавиатуры. \
Её максимальный размер составит 5 × 6. \
Максимальное количество клавиш: 10.



По умолчанию, если не передан параметр `inline`, клавиатура показывается под полем ввода в диалоге с пользователем (**reply**). \
Максимальный размер стандартной клавиатуры — 5 × 10. \
Максимальное количество клавиш: 40.
{% endhint %}

### 2. Исключение пользователя из беседы

**vk\_remove\_chat\_user(member\_id)**

где **member\_id** — id пользователя, которого нужно исключить. Здесь же вы можете использовать значение **from\_id**.&#x20;

Пример: исключение из чата при отправке ключевого слова.

<div><figure><img src="../../../.gitbook/assets/Снимок экрана 2025-10-27 в 11.23.34.png" alt=""><figcaption></figcaption></figure> <figure><img src="../../../.gitbook/assets/Снимок экрана 2025-10-27 в 11.24.05.png" alt=""><figcaption></figcaption></figure></div>

Бот удалит из чата того, кто прислал этот текст&#x20;

<figure><img src="https://lh7-rt.googleusercontent.com/docsz/AD_4nXcJiA9ohtSLDUdCCE4ZGTiIF9l6_FlXWFUGKH2aXnwIZyv79Wsa2ik2WASD9Cvd9-U3Z0hjcYLO9gbXAplmGB3LBYn9y4xisOzOs35FKLxD1SLy4TKK2iJP782DGsuoCEUbzgO39w?key=HrfPDBYux3Rnmgtyn6-Vww" alt="" width="563"><figcaption></figcaption></figure>

### 3. Как получить имя пользователя

**vk\_get\_name(from\_id, full)**

где **full** может принимать значение True (вы получите имя и фамилию) и False (получите только имя)

### 4. Как удалить последнее сообщение в беседе

**vk\_delete\_last\_message()**

в скобках ничего не указывается. Произойдёт удаление последнего сообщения в беседе. На личные сообщения не распространяется

### 5. Как отправить стикер

**vk\_send\_sticker(platform\_id, sticker\_id)**

где **platform\_id** — id клиента в мессенджере, **sticker\_id** — id стикера.&#x20;

Как узнать id стикера? Тот, кто подключал бота ВК, отправляет в бота нужный стикер. Его id при этом записывается в переменную. Значение переменной копируете из раздела Клиенты (см скрин:)

<figure><img src="https://lh7-rt.googleusercontent.com/docsz/AD_4nXdLMZrcU9wD3l2CeQvwRWD0VYxJV7u5S6jy10CO86O_NTx-cwQY8kLYb35DBKHlEFvFQgHtDR0RTwQpXHSWEf3HLD8Pll7xnD5TqYyTS_VoVD6GnQwymiGAAVqzCjiF08DcUtANkw?key=HrfPDBYux3Rnmgtyn6-Vww" alt=""><figcaption></figcaption></figure>

Пример: отправка стикера

<figure><img src="../../../.gitbook/assets/Снимок экрана 2025-10-27 в 11.26.11.png" alt="" width="563"><figcaption></figcaption></figure>

Результат:

<figure><img src="https://lh7-rt.googleusercontent.com/docsz/AD_4nXc5I-X1r4dyFC7L7X3QJ1Y2TnAmZtt64o-5VZxUQtVUt7hYV9_eLhi-JQIFukenav5eyXhY6icgHR5AqxfDEzmswVlI2aZNVI8c4dY5GhIKAmhloiiOzSJBOWh-CYbtA5KvHRut?key=HrfPDBYux3Rnmgtyn6-Vww" alt="" width="563"><figcaption></figcaption></figure>

{% hint style="success" %}
Колбеки для группы:

**client\_group\_join request** - подан запрос на вступление в группу  \
**client\_group\_join approved** -  клиент принят в группу
{% endhint %}

### 6. Как обработать реакцию на сторис ВКонтакте

Если клиент отреагировал на сторис, в диалог автоматически придет уведомление об этом:

<figure><img src="../../../.gitbook/assets/Снимок экрана 2025-10-27 в 11.27.02.png" alt=""><figcaption></figcaption></figure>

Данные о сторис будут в разделе "Информация о клиенте" в переменных:

**story\_id** - идентификатор сторис&#x20;

**story\_owner\_id** - владелец сторис

### Html-разметка для сообщений&#x20;

Для сообщений бота Вконтакте доступна html-разметка.

\<b> **жирный текст**  \</b>

\<strong>  **жирный текст** \</strong>

\<em> _курсив_ \</em>

\<u> подчеркивание \</u>

\<a href="ссылка"> отображаемый текст \</a>

<figure><img src="../../../.gitbook/assets/Снимок экрана 2025-10-27 в 11.27.28.png" alt="" width="375"><figcaption></figcaption></figure>

{% hint style="info" %}
Внимание! \
Не забудьте активировать кнопку html, чтобы функция разметки применилась к тексту.
{% endhint %}

<figure><img src="https://lh7-rt.googleusercontent.com/docsz/AD_4nXeLE7qduHh-hDysDVGhffaTHjJP0qOynl5GyY6buLgWjTNCkZ9zzsT7Z58CTimx_Lejl8UR2rT1cV4HTM5SNeTMxWb_YbVh_TE6a6dwG1NaiHsrjxKr4zOlSdZmK8dEpGlSSBH5?key=HrfPDBYux3Rnmgtyn6-Vww" alt=""><figcaption></figcaption></figure>

## Кармабот для группы

Схему кармабота собирать не нужно, мы сделали это за вас! В разделе Шаблоны уже есть готовая воронка, ее нужно только установить и настроить. По ссылке ниже вы найдете подробное описание.

<figure><img src="../../../.gitbook/assets/Снимок экрана 2025-06-26 в 16.27.46.png" alt=""><figcaption></figcaption></figure>

### 1. Как настроить кармабот внутри ВК

Для работы Кармабота вам необходимо создать отдельную группу в ВК. В разделе "Управление - Сообщения - Работа в боте" вам необходимо поставить галочку "Разрешать добавлять сообщество в чаты"

![](<../../../.gitbook/assets/image (168).png>)

После этого в меню группы Кармабота добавится следующее:

<figure><img src="https://lh7-rt.googleusercontent.com/docsz/AD_4nXdPoFHZ86HR0L1RBu1zydPPUfWodN_NMNWvEy3VE1NEyUBwUQ3HXtFxKGmZX73PI-kQqZ4oQaYbt2pFnIsxJUdJSJiI7OoKz3YUJB--XTK1h0Y0K10JcHeKUeqgzjjUxyFVLJ4vpw?key=HrfPDBYux3Rnmgtyn6-Vww" alt="" width="563"><figcaption></figcaption></figure>

Нажимаете и выбираете, в какой чат добавлять будущего бота:

<figure><img src="https://lh7-rt.googleusercontent.com/docsz/AD_4nXdLBZCtqwMBnDbRW3BHNfDtLX9S7eJ45NUdxqh2t6vmXpGvAXuC6422iPZMkANYwQYmp5VG1nvK8MTvc9j5R9Jkt4faPkkBzWdXXUKfmBpe8otAVOaij05Imusj1BJ7r0oFA1gwCw?key=HrfPDBYux3Rnmgtyn6-Vww" alt="" width="563"><figcaption></figcaption></figure>

Далее заходите в группу, где находится эта беседа. Нажимаете в меню справа Управление → Чаты→ Настроить:

<figure><img src="https://lh7-rt.googleusercontent.com/docsz/AD_4nXcP5J4mj9MdZW6ikZSNcsjGH2ZjyMrJxqe6W2FUktne2Dao2RrRm7BiyGuY4ZwNQ_aWVq_DK4O-jI38LglkZpyp58RWyvLzTLXLfFW_lD5kuiFnuGx_jjCawTIkulsHF3u4diDnJA?key=HrfPDBYux3Rnmgtyn6-Vww" alt=""><figcaption></figcaption></figure>

Выбираете нужный чат. В нем кликаете на количество участников (вверху чата), в выпадающем окне устанавливаете боту права администратора

<figure><img src="https://lh7-rt.googleusercontent.com/docsz/AD_4nXfWe_FCkVdxIDx96CzK-s_NAUTk3wx-SMCPGuT36TulUWzY8zHTqpRprqtqaK_nBnmw_5Ci8-GENf1HKTMRXME_BhaGk8UecdRPnvOU74sKpOFzcN6dad9kfhFxjWhG-VMooYvZYg?key=HrfPDBYux3Rnmgtyn6-Vww" alt="" width="375"><figcaption></figcaption></figure>

{% hint style="warning" %}
Назначать администратором обязательно, иначе бот в беседе работать не будет!
{% endhint %}

### 2. Что умеет делать Кармабот:

* начислять +1 кармы, если один пользователь процитировал другого и поблагодарил
* начислять +5 к карме по команде
* исключать из чата по команде "бан"
* удалять сообщения с нецензурными словами

Если участник чата благодарит сам себя, ему приходит сообщение:

![](<../../../.gitbook/assets/image (169).png>)

Если забывает процитировать другого, то получает напоминание:

![](<../../../.gitbook/assets/image (170).png>)

Если цитируют самого Кармабота, то:

![](<../../../.gitbook/assets/image (171).png>)

Карма начисляется автоматически, если один пользователь цитирует другого и пишет ему "спасибо" и другие слова благодарности

![](<../../../.gitbook/assets/image (172).png>)



{% hint style="warning" %}
Сообщения от админов бот удалять не может, как и исключать их из беседы
{% endhint %}

## Как получить Лидформу Вконтакте (ответы из Форм сбора заявок)

### 1. Как подключить Форму заявок к сообществу

Перейдите в Управление → Приложения вашего сообщества → Показать все:

<figure><img src="https://lh7-rt.googleusercontent.com/docsz/AD_4nXcVNrF-pVcPKnpTjE0l3YmNS29Mxg3n4r8zPAzVVDs-rJOEk7v3x6kN_krTLBXycWh1QY2K4XE82NqTzR266uDDLEG_zBFj1mCBuQPfqqnDBLE_sU_68Y5v_lZkCqp0ax7fK9mM?key=HrfPDBYux3Rnmgtyn6-Vww" alt=""><figcaption></figcaption></figure>

Сбор заявок → выберите приложение “Форма сбора заявок”

<figure><img src="https://lh7-rt.googleusercontent.com/docsz/AD_4nXeXCXLk2w2VN2-N6BhtFS0V7Wddl7VedTBb9nOoQaPbEb_9X1bQw_Kr_8ytNzQeBHoD8T0wJ4LoBIfmyDCBP_LO_1PgQqNq3EWYi_moIeLLyKcdBquL_qLd-YDOdDrQMPnuRACoPw?key=HrfPDBYux3Rnmgtyn6-Vww" alt=""><figcaption></figcaption></figure>

### 2. Как настроить лидформу

Чтобы настроить лидформу, нажмите на "Изменить" в Форме сбора заявок:

<figure><img src="https://lh7-rt.googleusercontent.com/docsz/AD_4nXeYbfQqS2cEuUTnOejeYwNIsiIdSReBqKeYXwkG5lAYPVWEUz3yOMQkqVxYVND3GosFBMFbgsdApeaS5f-Qic1Uxu5pW6rnKzMcpr7e9__eqtUvVunwv8kYJRC49rICAUlpGQ4Hfw?key=HrfPDBYux3Rnmgtyn6-Vww" alt=""><figcaption></figcaption></figure>

Откроется форма, где вы можете настроить доступ пользователей, сниппет и выбрать название:

<figure><img src="https://lh7-rt.googleusercontent.com/docsz/AD_4nXezyEJVBpjtLxYGVsG8hJ3nZWpINEkKxNiwmW_xdXdSF7QDBU9-WsI1QSHaKSYTKkpTNp_K4zUtvaqeoO0RWCAzkMVqb_POmRUgdrwD2fpO8Loebiza0GnWQqUkU22y5FQJ8C-M?key=HrfPDBYux3Rnmgtyn6-Vww" alt=""><figcaption></figcaption></figure>

<figure><img src="https://lh7-rt.googleusercontent.com/docsz/AD_4nXfrfSwlQJt8AkAz0IPak1LpGOG0cIn3j2knVSfuT2S2U80mvxgksyf9WwWM105DO-8upMAbMRFwghVi-FOvm49nttxnhtwlSMIGcpMc2oZ_aBWdhHgfZrt0uPeUonoL-2CxhPJgbA?key=HrfPDBYux3Rnmgtyn6-Vww" alt=""><figcaption></figcaption></figure>

<figure><img src="https://lh7-rt.googleusercontent.com/docsz/AD_4nXdFScOs8KOnRJIDCH_lKO9KIhpRr6ToHA1ZVlQ_JdDzjyNxdKcDz7xZaueRT4cWHS9QL1hoZnAxDaCxVlIbATdLH01wsvAh8b-U5sP3gO8D8fEbVIpe5N5dJsTdvhoNjLJicSwPyA?key=HrfPDBYux3Rnmgtyn6-Vww" alt=""><figcaption></figcaption></figure>

### 3. Как получить данные лидформы в бот

Чтобы в Ваш бот передавались ответы из Форм сбора заявок, включите переключатель "Заполнение лидформы" в настройках подключенного канала

<figure><img src="https://lh7-rt.googleusercontent.com/docsz/AD_4nXdG61tKiqouhHtTMvvZLkMVsL0XehWDsZBpHnW0YNrk-AYT0xT99kqw9QtPRwZ_rDp1fdP_1TthfSj0Y0ykLjfWv_g6Oqk7nJGBss7pChZHEpQSUzc8TZVCBS1eM9dAsZ4tA1aTDg?key=HrfPDBYux3Rnmgtyn6-Vww" alt=""><figcaption></figcaption></figure>

### 4. Как активировать лидформу нашего сообщества

После настройки формы нажимаем “Активировать”, копируем ссылку:

<figure><img src="https://lh7-rt.googleusercontent.com/docsz/AD_4nXc51SmJAR23FZF0tn1Kw6za8ffVkEBQQfcumi0_vFmmNA1pIzdKR8p1CJ_w8xyGEZzTNrJIbrKFOXOBD8ge47hMTpGZSLBHnalW0PRDCAGzZdRLeYA02m_XGDFsO8En8PMU7n2RTw?key=HrfPDBYux3Rnmgtyn6-Vww" alt=""><figcaption></figcaption></figure>

Далее в управлении сообществом идем в раздел “Меню”, добавляем новую ссылку.

<figure><img src="https://lh7-rt.googleusercontent.com/docsz/AD_4nXerE4tYYSDwZQRdS3ky1-2BLpHZWWZvFHTUH1wMJRmqchmcXJKzuEJA_kQh7VN-LYuB6EBTjhD-CcqO3EVBY-fe23H9Zf9RZJhTfhwzxk0jWCZvUqHOfgVGSw0BF-MHImesEJhI?key=HrfPDBYux3Rnmgtyn6-Vww" alt=""><figcaption></figcaption></figure>

Заполните название ссылки и добавьте ссылку на вашу форму:

<figure><img src="https://lh7-rt.googleusercontent.com/docsz/AD_4nXf_CTfQfGnSj9-afzUMGkqa8Hr1xf4jUIp1JxWaGGhGtRJJuXcqfDsYNuaGKua7mUkaRLdLRGf3cWnmkjxc2k-6UbozfANiWw9rxtbzrXHZmDUB9lZLRy9_ggLZ7yYzbdqTND696w?key=HrfPDBYux3Rnmgtyn6-Vww" alt="" width="375"><figcaption></figcaption></figure>

Ваш клиент будет видит форму в соответствии с выполненными Вами настройками

<figure><img src="https://lh7-rt.googleusercontent.com/docsz/AD_4nXfbfiW-064QPHZVlp1DH02iWMQSNjon5RVqSIeSPU6iywm7i0rA3MWVsfkC2fS7-UVipxTabssb2vKjwBygcT_laKj2LJXzL03wMu335xiwaCsJEqXYubH3frfhsqk96l3Vrvb2iA?key=HrfPDBYux3Rnmgtyn6-Vww" alt="" width="375"><figcaption></figcaption></figure>

После заполнения данных клиентом значения будут переданы в карточку клиента с соответствующим коллбэком **lead\_forms\_new**

<figure><img src="https://lh7-rt.googleusercontent.com/docsz/AD_4nXcUWrvIGk1ILgCqiEyyERw1DSZfXGtk9aVubeROsr4X1PO2qCYJbmnSrXsEermtfEi5VC_wKDcWrhD207BHBsx4YWtdjEIz-p24pNXRBMuhmzo3T6FTiOYsWNlcEplajvLVtKQS?key=HrfPDBYux3Rnmgtyn6-Vww" alt="" width="375"><figcaption></figcaption></figure>

## Как получить полный Вебхук Вконтакте

**Вебхук (Webhook)** - это возможность встроить уведомления на платформу о произошедшем событии, содержащее значения измененных переменных.&#x20;

Для получения полного вебхука от ВКонтакте достаточно присвоить любое значение переменной **save\_webhook** (переменная может быть как константой проекта, так и переменной сделки). При этом запрос от ВКонтакте будет записан в переменную **vk\_request**.

**remove\_last\_message()** – для удаления последнего сообщения от бота

{% hint style="danger" %}
Работает <mark style="color:red;">только</mark> в Telegram и Вконтакте.&#x20;
{% endhint %}

Если вы включали переключатель "сохранить в истории переписки", то для ТГ/ВК можно удалить последнее сообщение через рассылку из блока, где в калькуляторе прописать remove\_last\_message(). Функция удаляет последнее отправленное ботом сообщение, но только если оно есть в истории переписки.

Пример:

Создаем блок для рассылки:

<figure><img src="../../../.gitbook/assets/Снимок экрана 2025-06-26 в 18.12.39.png" alt=""><figcaption></figcaption></figure>

{% hint style="success" %}
Настройте рассылку по своему усмотрению и перейдите во вкладку "Отправка"
{% endhint %}

Во вкладке отправка активируйте чекбокс "Сохранять рассылку в истории переписки с клиентом":

<figure><img src="../../../.gitbook/assets/Снимок экрана 2025-06-26 в 18.11.24.png" alt=""><figcaption></figcaption></figure>

Важно! Чтобы чекбокс "Сохранить рассылку в истории переписки клиентом" отображался во вкладке "Отправка", отключите в разделе каналы прочитанность сообщений для групп вконтакте:

<figure><img src="../../../.gitbook/assets/Снимок экрана 2025-06-26 в 18.16.12.png" alt=""><figcaption></figcaption></figure>

Далее смело отправляйте рассылку.&#x20;

Если вдруг вы хотите удалить последнее сообщение (например, сообщение с ошибкой), то удалить последнее сообщение можно одним блоком с функцией remove\_last\_message()

<figure><img src="../../../.gitbook/assets/Снимок экрана 2025-06-26 в 18.03.59.png" alt=""><figcaption></figcaption></figure>

Далее отправляйте рассылку с функцией удаления последнего сообщения.

{% hint style="warning" %}
ВАЖНО!&#x20;

Спустя время последнее сообщение удалить нельзя!
{% endhint %}

## Проверка подписки

{% hint style="success" %}
Подробно о том, как проверить подписку на сообщество с помощью чат-бота, рассказали в статье "[API вконтакте](/broken/pages/P9LUPopuvcq5gBab078o#kak-proverit-podpisku-na-soobshestvo)".
{% endhint %}
