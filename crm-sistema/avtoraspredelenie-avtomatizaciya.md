---
description: Позволяет автоматически распределять обращения клиентов между операторами
---

# Автораспределение (автоматизация)

Автоматически распределяет клиентов между операторами, которые находятся в активном статусе. Активным считается статус "На смене".

У каждого оператора есть меню настройки активности.

<div data-with-frame="true"><figure><img src="https://lh7-rt.googleusercontent.com/docsz/AD_4nXdPgdR_ZbmWUBMkQneImaTaUmZaK6T8MxjGyVJTbgupQKJXVEjScnwc-WKSJj9-peC-zb6Yd-_S_yI848J4rO9txbYQkbte2Z5HA5goPWEkgFI6NLjAOjMb4HbA0tn3uujHl1y_dg?key=xhY-tTHpzMIIBvXVOxnYCQ" alt="" width="563"><figcaption><p>Статусы доступные операторам</p></figcaption></figure></div>

#### Обзор статусов:&#x20;

<mark style="color:green;">**На смене**</mark> – активный статус. При работе с автоматическим распределением клиентов оператор должен установить этот статус в личном кабинете. Вкладка со статусами доступна на любой странице проекта Salebot.

&#x20;<mark style="color:orange;">**Перерыв**</mark> - устанавливается при перерыве, для временной остановки распределения клиентов на сотрудника.&#x20;

<mark style="color:red;">**Отсутствую**</mark> - статус, распределение при данном статусе не работает. Как правило, устанавливается в случае, если сотрудник не на смене или завершил рабочий день.

При работе с автораспределением обращайте внимание, на статусы сотрудников для корректной работы распределения клиентов.&#x20;

Если статусы сотрудников не "На смене", то распределение не сработает.

## Включение

Перейдите в раздел "Сотрудники" →"Автоматизация" → Активируйте переключатель автоматического распределения клиентов<br>

<div data-with-frame="true"><figure><img src="https://lh7-rt.googleusercontent.com/docsz/AD_4nXcoWcoX4Qcl3xNnqsALE7eH9ewQlNyOikQeD3ZPlkN2fMzlbMipVFuwUN2eZWlysFIT8wAsZnbbdcH7-gl7MWt87SDQgFdhDQSZ-RPIS2XHRx9s-jWyTxaP53U97CjTyc5uiPwUlw?key=xhY-tTHpzMIIBvXVOxnYCQ" alt=""><figcaption><p>Настройки системы автораспределения системы</p></figcaption></figure></div>

Режим работы

Вы можете указать режим работы распределения круглосуточный или задать режим работы вашей компании.

<div data-with-frame="true"><figure><img src="https://lh7-rt.googleusercontent.com/docsz/AD_4nXf0KHuIVYeXUocRAnJ9NdYf4lBaAvDAGoLk0GWbRB8LTDWfn7DzGLfiY2LvlslK_XQJyEhTgnyjahKi5dtY16KCFb03x1qCML0IkUVTA6ym1j1eE08tidR2viegJ43A-yoZLB64dg?key=xhY-tTHpzMIIBvXVOxnYCQ" alt="" width="563"><figcaption><p>В примере активен режим круглосуточной работы</p></figcaption></figure></div>

Если вы выберите режим  “Период” вам необходимо установить рабочее время

<div data-with-frame="true"><figure><img src="https://lh7-rt.googleusercontent.com/docsz/AD_4nXc9zNS7k2k4PjZAMIbYCnfJ88gKaLNMBojKCIaPhilWXob1ibIXvbIiYNmAMI9w7aDOl6caQ1ttiUTLXlMq6o9oyKHs5KORB5CZfvvfStPdFEO3BxnnryjpL5px7M9QEjdfKMegeg?key=xhY-tTHpzMIIBvXVOxnYCQ" alt="" width="563"><figcaption></figcaption></figure></div>

Выходные — выбор дней в которые система автораспределения работать не будет. В примере, как выходные выбраны суббота и воскресенье.<br>

<div data-with-frame="true"><figure><img src="https://lh7-rt.googleusercontent.com/docsz/AD_4nXcu7e7EGRHZlmVyKIXChVjXOvR10VCiI4W2KOtMz9uqGBjwyOzA7OWHCx6hZo11L7AswxmMIX5eUYEN2nEyBg3v26DDFyrrpctfScl9U-jvU1nJxg3opaFTxHX-_Ffpxxj7u3hgLQ?key=xhY-tTHpzMIIBvXVOxnYCQ" alt="" width="563"><figcaption><p>Указаны выходные: Суббота и Воскресенье</p></figcaption></figure></div>

### Как это работает

Когда система включена, клиенты, которые пишут в вашего бота, будут автоматически прикрепляться к операторам, которые находятся НА СМЕНЕ.

Система распределяет клиентов <mark style="color:green;">**равномерно между всеми операторами**</mark>, то есть, если на смене 5 операторов и пришло 55 клиентов, каждому оператору достанется 11 клиентов.

В конце рабочего дня, клиенты, которые пишут, перестают прикрепляться за операторами и уже считаются НОЧНЫМИ КЛИЕНТАМИ. Ночные клиенты распределяются в начале следующего рабочего дня равномерно между операторами, которые зашли на смену ДО рабочего дня.

{% hint style="info" %}
Например: За ночь пришло 30 клиентов, рабочий день должен начаться в 6:00. В 5:55 на смену зашел оператор Богдан, в 5:57 на смену зашел оператор Руслан, на них пока не распределило клиентов. В 6:00 начался рабочий день, в 6:00 на Богдана и Руслана упало по 15 клиентов. После этого в 6:05 на смену зашел оператор Филип, но на него уже просто начинают падать новые клиенты.
{% endhint %}

Если оператор сам напишет СВОБОДНОМУ клиенту, то клиент автоматически будет присвоен ему.

Оператор, который находится на перерыве, не получает новых клиентов, однако клиенты, которые уже присоединены к оператору, будут попадать именно к нему.

Также существуют выходные дни, в которые автораспределение не работает.

## Настройки для операторов

<div data-with-frame="true"><figure><img src="https://lh7-rt.googleusercontent.com/docsz/AD_4nXfMPDllwEKZ4besWFjwH2YfHsV-_lYxSKRH9MjfmRYGfR9IEn7lrY8xR446WxUBqwz1q4l7qcFxWEwVhXRUigyBKot5VEeA3X1w8ozZrlHiRQIzu0NX2ptpFLATQh-tL-LmjkbPNg?key=xhY-tTHpzMIIBvXVOxnYCQ" alt="" width="563"><figcaption><p>Настройки операторов раздел Сотрудники → Автоматизация</p></figcaption></figure></div>

1. **Отображать у операторов кнопки распределения клиентов** — Настройка позволяет оператору закрепить клиента за собой, передать его или отказаться от клиента.
2. **Отображать у операторов разделы "Ожидают ответа" и "Свободные клиенты"** — выбор, нужно ли отображать иконки "Ожидают ответа" и "Свободные клиенты" в левом баре в диалоге с клиентами. Если функция включена, то отображение разделов будет таким, как в скриншоте ниже:&#x20;

<div data-with-frame="true"><figure><img src="https://lh7-rt.googleusercontent.com/docsz/AD_4nXdQtDGOwqtGuOmbw6nUltndTrU07lPFm0GHw8tDxZiFmDT3wX-TVKij8dZ_6rSgyJfo6ksP-IzmN-ylrH-Ae28fvXetCKDF7A6peYULWnIs6UfYWmpgXmSBP9juGJkTVhc7F4yr?key=xhY-tTHpzMIIBvXVOxnYCQ" alt="" width="375"><figcaption><p>Отображение при активной функции</p></figcaption></figure></div>

3. **Снимать операторов со смены** - автоматически убирать операторов со смены по окончании рабочего дня. Конец рабочего дня - это время указанное в режиме работы.
4. **Равномерно распределять клиентов за определенный интервал времени** - при активации, система распределяет клиентов равномерно за весь рабочий день. Например, если за весь день пришло 300 клиентов, а на смене было 6 операторов, то в этот день каждому досталось по 50 клиентов.\
   \
   Также вы можете указать временной интервал (например, 10 минут), система будет равномерно распределять клиентов, которые пришли за этот период (последние 10 минут) Пример: На смене 2 оператора, выставлен интервал в 10 минут. За период 10:40 - 10:50 пришло 50 клиентов, каждому оператору досталось по 25 клиентов. Затем в 11:00 на смену выходит третий оператор. С 11:00 до 11:10 придут еще 60 клиентов. Они равномерно распределятся между тремя операторами — по 20 человек на каждого. Это позволит избежать перегрузки одного сотрудника.\
   \
   Если выставить интервал в 1 минуту, а клиенты будут приходить с интервалом 1 или больше минут, то они будут распределяться между разными операторами, а не доставаться первому.
5. **Не распределять клиентов если бот ответил** - если клиент написал сообщение и ответ получил от бота, то такой клиент не будет распределен на оператора по заданным настройкам автораспределения. \
   \
   Все сотрудники могут быть операторами в чате с клиентами - это значит, что если у сотрудника не стандартная роль оператор, то он так же будет видеть клиентов и сможет отвечать им.
6. **Разрешать удалять клиентов оператору** - по умолчанию, удаление клиентов операторами запрещено. Если вам необходимо, то вы можете выдать данное разрешение вашим операторам. Тогда они смогут удалять клиентов.

{% hint style="warning" %}
Важно!&#x20;

После установки всех настроек не забудьте сохранить изменения.&#x20;
{% endhint %}

Кнопка “Очистить привязку к сотрудникам” - снимает привязку клиентов к операторам. Не распространяется на тех клиентов, которые пришли менее суток назад.

<div data-with-frame="true"><figure><img src="https://lh7-rt.googleusercontent.com/docsz/AD_4nXero4wxBxAzbp9DDNvIZPnBSsYngkXlJtzdrrJA1GgGMY6Tt0bqIU55KwD134Iea_DvLLYSKwBPotnPCXgpR7ZjduQSgZPe-brWqyseFhSH26eO8sPdwW_4CiyqTyADHh2jAOwohQ?key=xhY-tTHpzMIIBvXVOxnYCQ" alt="" width="563"><figcaption></figcaption></figure></div>

Все сотрудники, которые имеют доступ к вашему проекту располагаются на вкладке "Сотрудники".

<div data-with-frame="true"><figure><img src="https://lh7-rt.googleusercontent.com/docsz/AD_4nXfJio6cl8fiMumqMp3fp-TjfCQ3FfwfjMveD2Ua_eNCUaUvq31-yC4l9bJIUHExUscRw__oWs8VAF0_z8XToxq0jKCWg66VYPa6V-KYsOqNKpoOFyspcg6Zo45a_vB1TEHR6EVXww?key=xhY-tTHpzMIIBvXVOxnYCQ" alt="" width="563"><figcaption><p>Список сотрудников проекта.</p></figcaption></figure></div>

Если навести на три точки справа от сотрудника, то будет доступно контекстное меню с командами Редактировать и Удалить.

При редактировании карточки сотрудника с ролью Оператор дополнительно открывается поле выбора статуса. Можно указать любой из обозначенных статусов: На смене, Перерыв или Отсутствую.

<div data-with-frame="true"><figure><img src="https://lh7-rt.googleusercontent.com/docsz/AD_4nXcHEyqhb2IM6RO69cjCjS-JhxJLO8rbJEACF5kWScBtm8sOozJ30gFs1Y_1skVR-VWvAlqq_8ZCqDaaszAqDto7Nruamcc9aRirxVZkexymH2vRnYxTiglN2sbo6T97R7VeInOHqQ?key=xhY-tTHpzMIIBvXVOxnYCQ" alt="" width="375"><figcaption></figcaption></figure></div>

Редактирование карточки сотрудника с ролью Оператор

Вы можете работать, как со стандартными ролями сотрудников, так и созданными кастомными ролями. В таких ролях можно настроить доступы с гибкими настройками.&#x20;

{% hint style="info" %}
[Подробно о том как создать свою роль рассказали тут.](../o-nas/administrirovanie/sotrudniki.md#kak-sozdat-novuyu-rol)
{% endhint %}
