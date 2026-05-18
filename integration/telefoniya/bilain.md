# Билайн

## Как подключить сервис

Настройка интеграции производится через личный кабинет, <mark style="color:yellow;">**причем личный кабинет должен быть только НОВОГО типа**</mark>. В левом меню нажмите “Услуги”, чтобы перейти к дополнительным услугам для АТС.

<figure><img src="https://lh7-rt.googleusercontent.com/docsz/AD_4nXd69Ran0l2teLfYgrJmbAFowvsBIqf8L87ooXwdUvVaYYWEFYVMLTToEkBtqfXloWqrGR6_cedkPgnhpg9gAFCtdkP5L7rAqkakHF4x4WQkRdxyzac4nWAIDu8mRSsuyWc6ndWO?key=8odw0PcwhL9OffjwDEdRe6vU" alt=""><figcaption></figcaption></figure>

В конце списка найдите “Интеграция по API” и нажмите “Подключить”. Создайте токен для аутентификации API и скопируйте его.

<figure><img src="https://lh7-rt.googleusercontent.com/docsz/AD_4nXc3ggH8Hj3IbrUsst-w_jbxdmPwsdL_G8rxWQyNiFswVBTfTVAkI-sbHfqdMogjEhbR2I6cWMR_Dqd-TwXRSKs9MSnYM7zA7aKrP2Z1PPMjTOuYh76WujSv0obBmuMlv_wZH7Af_Q?key=8odw0PcwhL9OffjwDEdRe6vU" alt=""><figcaption></figcaption></figure>

## Подключение интеграции в Salebot

В Salebot перейдите в раздел “Телефония” и заполните данные для подключения Билайн:

<figure><img src="https://lh7-rt.googleusercontent.com/docsz/AD_4nXcdhSbrQF_rLW6k1_9J68M6zy4GSKdUGy4eaN0pVEocMxZCMsluJBXizh6C5fQ3B3q-XWr8K3kvee5MpLYy2Kwh736jVlhHoQs0wNXXndW_R7pqI_qDoGsA5X8TNmRrxYt2oQ_y?key=8odw0PcwhL9OffjwDEdRe6vU" alt=""><figcaption></figcaption></figure>

<figure><img src="https://lh7-rt.googleusercontent.com/docsz/AD_4nXdLHYRFHgCAiPFVPMoSKsLxXFAJb3SC6htnTEEEyeq2uMr_GXQHhbsh1pjaqa65wTbtP0ewuhWOap1Wpni6pWkkE6pbKbecmM_zVZLmwfDn-DUZ6i8K9C5gupqQ_lVjIeWv27Wi7w?key=8odw0PcwhL9OffjwDEdRe6vU" alt=""><figcaption></figcaption></figure>

API key (токен для аутентификации API) мы скопировали ранее в личном кабинете Билайн, в настройках интеграции.

<figure><img src="https://lh7-rt.googleusercontent.com/docsz/AD_4nXc3ggH8Hj3IbrUsst-w_jbxdmPwsdL_G8rxWQyNiFswVBTfTVAkI-sbHfqdMogjEhbR2I6cWMR_Dqd-TwXRSKs9MSnYM7zA7aKrP2Z1PPMjTOuYh76WujSv0obBmuMlv_wZH7Af_Q?key=8odw0PcwhL9OffjwDEdRe6vU" alt=""><figcaption></figcaption></figure>

Нажмите “Сохранить настройки”. Теперь Вы сможете выбирать для своих сотрудников способ совершения телефонных звонков “Звонки по API Beeline”.

## Настройка вебхуков

Вебхук - поможет отслеживать звонки на облачную АТС Beeline и передавать их в систему Salebot.

{% hint style="success" %}
Вебхуки привязываются не ко всей облачной АТС «Beeline», а к каждому абоненту АТС по отдельности
{% endhint %}

Привязка вебхуков происходит на стороне Salebot, в разделе Сотрудники.&#x20;

Выберите сотрудника, нажмите … (Редактировать), далее выберите способ совершения телефонных звонков “Звонки по API Beeline” и укажите номер сотрудника.

<figure><img src="https://lh7-rt.googleusercontent.com/docsz/AD_4nXc3PVbf_icqYOwaGs0LN-eAVLkI4_6xpB4OR7nrnYv6XuNWhgU5BVnZLOHqzZew-8iph2r6qhxwF0xsXlc7U2CKhKEZ_7Cyn7SpcZE1WRPeDXlEj9DNsrU959_fjG9AZzU8Vqcp1Q?key=8odw0PcwhL9OffjwDEdRe6vU" alt=""><figcaption></figcaption></figure>

Номер необходимо взять из личного кабинета Beeline и ввести только цифры: без скобок, пробелов или дефисов.

<figure><img src="https://lh7-rt.googleusercontent.com/docsz/AD_4nXc7oNqNFNGVdiw4CdNuhmcZ_6iSRllQfwtEQktSu1qMI0ZSJot1U_LvfKA2p54eq24VA2s-0F0KHlRC25vzfUOxAfq1WUsqVFrMeYwEfn3TNvdsDCQRfZMLNPgdKGJKW95X0tHd-Q?key=8odw0PcwhL9OffjwDEdRe6vU" alt=""><figcaption></figcaption></figure>

После нажатия кнопки Готово получение вебхуков от облачной АСТ Beeline будет настроено.&#x20;

<figure><img src="https://lh7-rt.googleusercontent.com/docsz/AD_4nXc3PVbf_icqYOwaGs0LN-eAVLkI4_6xpB4OR7nrnYv6XuNWhgU5BVnZLOHqzZew-8iph2r6qhxwF0xsXlc7U2CKhKEZ_7Cyn7SpcZE1WRPeDXlEj9DNsrU959_fjG9AZzU8Vqcp1Q?key=8odw0PcwhL9OffjwDEdRe6vU" alt=""><figcaption></figcaption></figure>

{% hint style="info" %}
Если Вы заметили, что от АТС Beeline перестали поступать оповещения о звонках, повторите это действие: откройте редактирование сотрудника и нажмите Готово
{% endhint %}

## Как происходит сопоставление клиента

Для работы с телефонией используются номера в формате **71234567890: номер** должен начинаться с <mark style="color:yellow;">**цифры 7**</mark> или с иного кода другой страны (например, 375), <mark style="color:yellow;">**состоять из 11**</mark> и более цифр и не иметь лишних знаков и отступов.

Последовательность сопоставления данных о клиенте:&#x20;

1. **Осуществляется поиск клиента Телефонии.**&#x20;

Если клиент не найден, то происходит поиск по значениям всех переменных по всему списку клиентов проекта. Первая найденная запись о клиенте считается тем самым "искомым" клиентом.&#x20;

2. **Если клиент не найден среди клиентов Телефонии и:**

* если к проекту подключен любой мессенджер, например, Whatsapp, то будет создан клиент Whatsapp с данным номером телефона;
* если к проекту не подключены иные виды мессенджеров (Whatsapp, Viber и т.д.), то будет создан клиент Телефонии. Такому клиенту Вы сможете совершать только звонки с получением информации о них. Написать такому клиенту возможности нет.

## Виды уведомлений

В диалог с клиентом будут поступать следующие уведомления:

beeline\_call\_event \<call\_type>, где < call\_type >:

* Incoming – Входящий звонок.&#x20;
* Outgoing – Исходящий звонок.&#x20;

<figure><img src="https://lh7-rt.googleusercontent.com/docsz/AD_4nXfq1dMkGcFSCKd-cXqP7EQ9fPmsSDJFljWLM1xWdwzT6ghLi711qcdplKPq_2UMj4qGDqhTrtLpNFAGBB9fPMv_gwYoiHW2VeffRuDQdHrxYRXDSM-ek0zXbLXWDpQ97SSBu4oz-w?key=8odw0PcwhL9OffjwDEdRe6vU" alt=""><figcaption></figcaption></figure>

Также после звонка у клиента создаются переменные сделки с информацией о звонке.

<figure><img src="https://lh7-rt.googleusercontent.com/docsz/AD_4nXeQZg7B7jcpbP3E7yvIT0m2BsNLoxlO6MJQk9rrtLjuVqgCYNynZW4rwIXP7ftTRFMWZMmGa7dDuD_h2TapLO7iUw2MZUFcDbDCFhLZl6i6eWsfulLZcviApYioT8PSom0XhhtoQw?key=8odw0PcwhL9OffjwDEdRe6vU" alt=""><figcaption></figcaption></figure>

* beeline\_call\_type – Incoming (входящий) или Outgoing (исходящий)
* beeline\_client\_phone - номер клиента.
* beeline\_operator\_phone – номер сотрудника (АТС Билайн)
* beeline\_start\_time – дата и время начала звонка
* beeline\_release\_time - дата и время завершения звонка
* beeline\_record\_link - ссылка на запись разговора. Не гарантируется что все звонки будут иметь ссылку на запись разговора, по независящим от Salebot причинам.
* beeline\_call\_description – Описание звонка: <Дата, время> принят (пропущен) входящий (исходящий). Абонент: <номер сотрудника> Клиент: <номер клиента>

## Функция Salebot обратный звонок

Для того чтобы совершить звонок из бота, необходимо использовать функцию beeline\_call(client\_phone, user), которая принимает на вход следующие параметры:

* client\_phone - номер клиента, которому должен быть совершен звонок, строка, пример - '79220001122'.
* user - телефонный номер вашего сотрудника, строка, номер должен начинаться с 9, пример - “9333221100”.&#x20;

<figure><img src="https://lh7-rt.googleusercontent.com/docsz/AD_4nXdNEuFqIa8m5kJvEDDwYwxN34JtE_PQhavo79LXG9enhoG0LGRQfaqY4WAj28Em3opm5jSxpMxiInb-6fWqV-2jg1QNSZ8YUyEXBE0WUOiPPmDGci9Vf3UjwvnxoFWjq-lNZp2xfA?key=8odw0PcwhL9OffjwDEdRe6vU" alt=""><figcaption></figcaption></figure>

<figure><img src="https://lh7-rt.googleusercontent.com/docsz/AD_4nXe-Dixv_nN3ayNp7nsop1okEMPlHlHt3r7jhXpAotHDLLvszdLCkcKj3_G8lIysKELl4WQL5PDX5QAp2cVMbdKj4pUQW3zXIyKbIBWKCtIH7NwnIt1p5i9-4oJ177krefFqtrHX?key=8odw0PcwhL9OffjwDEdRe6vU" alt=""><figcaption></figcaption></figure>

Если удалось установить созвон между client\_phone и user, то функция возвращает результат {"status":"1","result":"Call ID: <идентификатор вызова>"}

Если созвон установить не удалось, то вернется {'status': '0', 'error': "<Описание ошибки>"}
