# QuizGO

QuizGO - это функциональный конструктор квиз-опросов. Позволяет создать квиз, встраиваемый в сайт или доступный по прямой ссылке.

Для регистрации нажмите на -> [ссылку](https://panel.quizgo.ru/).

<div data-with-frame="true"><figure><img src="../../.gitbook/assets/Снимок экрана 2026-03-25 в 15.14.35.png" alt=""><figcaption></figcaption></figure></div>

## **Как передать результаты в чат-бота**

После заполнения квиза все ответы клиента можно передать в чат-бота.

{% hint style="info" %}
Данный механизм работает только в Telegram, Вконтакте, Viber, Facebook\*, Whatsapp\*
{% endhint %}

{% hint style="danger" %}
\*Facebook, Whatsapp принадлежат Meta inc., деятельность которой признана в РФ экстремисткой и запрещена.
{% endhint %}

Создаем в QuizGO новый проект и в нем новый квиз.&#x20;

<div data-with-frame="true"><img src="https://lh3.googleusercontent.com/3pCx8bxf_dZqfP3P695O4HhBpAGG4w-5P9qYRhnY54ALh26Cc9rZ0tGrvj0sn9loSsrniIBdL8ADckjSsvH_cCTdeJw9pu9VjdiUpfNTdTqVE2AWoprTzpPyG66l_0eO32s3aZtp" alt=""></div>

Выбираем готовые шаблоны или создаем свой квиз.

<div data-with-frame="true"><img src="https://lh6.googleusercontent.com/2xHfOUyNvlSOSWbpPasJMwNMCDxHrjNWg0OTtIKPlZfzYp5K2Mnh47zTs52plxni5G0sjaBoRuTwsO1KDsQE3h43Z3wGz1rFnaX8uvOXRpPwjiavVXK_xYOE-f1US41_0tXCFc6w" alt=""></div>

Настраиваем внешний вид стартовой страницы и вопросы квиза

<div data-with-frame="true"><img src="https://lh5.googleusercontent.com/wheck0wpiBAm1UfNCM16cTNqujOP0ofNdTTOuVQYhqXovKTnkHy4JFtPqjI4ToH9EE6Tv-M_r4g39Tm-s922hVNeR7eJINeVCNnZ9cH1xyeayIiMO3AvCZjAc41wT3Kclawg9M7K" alt=""></div>

В Salebot создаем сайт (можно пустой) и активируем в нем нужные мессенджеры.&#x20;

{% hint style="success" %}
Важно! Для Whatsapp\* необходимо задать начальное сообщение и указать в нем переменную #{visit\_key} как на примере ниже.&#x20;
{% endhint %}

<div data-with-frame="true"><img src="https://lh3.googleusercontent.com/iDIWTG0WEroDzS1ifnbcMkvRwY1VMjpMlFyczU1NOWS08ZGCWZKsuVlAwHl0NFrPVkwC3kMEXb3eWZCjP71nbTJ4p1XhcJ-TpHClZpTevjvUX2KF1034z9_lX9g2I091eIgNSH94" alt=""></div>

Сохраняем сайт и забираем прокси-ссылки на мессенджеры.

### Первый вариант передачи данных

В QuizGO переходим в раздел “форма контактов”, включаем опцию “сбор контактов”, указываем, какие контакты нам нужны (если контакты не нужно собирать - выключаем опции). Также указываем в какие мессенджеры необходимо перенаправление.&#x20;

<div data-with-frame="true"><img src="https://lh3.googleusercontent.com/DwouCMpB0-padVLB6Vvxvc1CMFkcwM_zVCqTCG-GEQMdeWZ3gagt7nsJ-xRto_BYQruvpln69Bc4f4ahl-vv-l7ZOj-Is_f_0eTOdrJh8cu9ChnfK1AGvtq0TS9Gj9dIFc42MPfc" alt=""></div>

Ниже активируем опцию “перенаправление в чат-бот” и вставляем прокси-ссылки с сайта Salebot в нужных мессенджерах. Обязательно сохраняем квиз.&#x20;

<div data-with-frame="true"><img src="https://lh6.googleusercontent.com/Abq9FStkcRJH3bTc23z4x-4A6N1WgJSxHXHkL31liLIfomfrFEhZklirxnf3TxbaSO5OSZz5nEy6bVW81ET5wc08eubfKm9FmM0D-qAvqQ5gz9n0p4LloZoWy8S2NT9W2-AhX_Lq" alt=""></div>

Дальше получаем прямую ссылку на квиз или встраиваем его на сайт (подробнее в документации - [https://quizgo.ru/docs/](https://quizgo.ru/docs/) ). После прохождения квиза клиенту будет предложено выбрать нужный мессенджер.&#x20;

### **Второй вариант передачи данных**

В разделе “форма контактов” выключаем сбор контактов

<div data-with-frame="true"><img src="https://lh3.googleusercontent.com/TOzQxgxFLda8yUNL3Hf_zsI6hNUrtrJ95Eg_UqngCzBRxJpEM33UUh0rQkVWHZXvudF5ibrfexfm6o-xqjJXDdlpuabTJF8Xuy9_YzemV5W1PcXCl2MiA67_wivm06nHS-qFWOdP" alt=""></div>

Затем переходим в раздел “Результаты” и здесь возможны следующие варианты:<br>

**Автоматический редирект** - после прохождения квиза клиент будет автоматически перенаправлен по заданной ссылке (можно указать там как общую ссылку на минилендинг, так и прокси-ссылку на нужный мессенджер).&#x20;

<div data-with-frame="true"><img src="https://lh6.googleusercontent.com/MD5HawPj7NXRvqZKJOncetCtxHJ-mMNtilxhQW2Jpkl_T5us-LRthhbByuakIqg6OrKypIv_ParnW-XhtFmzap0OAbc0KteAzoLlEGLf2LSO2FiynSJ8mubQH7TfvX-e5KS7uccV" alt=""></div>

**Список результатов** - ниже добавляем результат, оформляем его и в поле url указываем ссылку (здесь так же можно указать как общую ссылку на минилендинг, так и прокси-ссылку на нужный мессенджер).

<div data-with-frame="true"><img src="https://lh6.googleusercontent.com/aFWgz-4fmQZU5Z2XzqANkJUgOrFfUtsFU_hqoTB5cPrmCitaO-Kw1zQmy3xtksWAx7ShmVfJNEs6o_h7Lf_abZpw26v7XzW4Pbc_dgu1gnQqa7aRm6xMJm06QeQT9gYKvzr0_3sQ" alt=""></div>

После прохождения квиза клиенту будут показаны заданные в настройках результаты и кнопки.

<div data-with-frame="true"><img src="https://lh5.googleusercontent.com/FH38z-T6TecsPFPm1gdB62C6oGTZfZfQvOF6xHTYyieA5NPqVHKeVrjnC-993YeQ9cgDmgMkwpb5fWvEh03s1twFtW50l6egxg0_0fxojI648HgrfTFQMW1plAZLUwY-UxPkJGoN" alt=""></div>

{% hint style="warning" %}
Для того чтобы работала передача данных, в настройках квиза пункт “подставлять ответы на вопросы во внешние ссылки” нужно переключить в режим “добавлять”
{% endhint %}

<div data-with-frame="true"><img src="https://lh4.googleusercontent.com/HERjPrKWn4rIkhyohBSU4geIoMC6L6Oh1_Y3dQwXG4AC7qbr_xj-TeGhEZww_UibUZHLAL0TDXRPWxAYIACTyeoDtLWxRncNu3W1HDpMErHCLK4w5UAH6VQRTfjZ9I6WtQAWlqIc" alt=""></div>

После прохождения квиза введенные ответы, а также указанные контакты (если включена форма сбора контактов), будут переданы в чат-бот.&#x20;

<div data-with-frame="true"><img src="https://lh4.googleusercontent.com/g2dPlz60UsX-auRcB3_bLtl-zrFMc_Bcs5DZXbrfs-83pjxs1SnpqG6ZP6X5BJe0O3JqhcywN7BMecMHpoHcdehw8mvRNXSQgEPqBUMA7xJpaPKlsk4GrbJGfTNCMP-SH-LU2prt" alt=""></div>

<div data-with-frame="true"><img src="https://lh4.googleusercontent.com/9w9_IQftcMk6_-qD3fgEeJ-QlK3xhYdEf4UIs5iER6T_H4csrEt_Cg2-4cODA-3xo17aB8TPGwlQqXVvSI0ERDV0KR4bnAMo5O7c1wP1gZg0NNjNDkR27OTLsWO7DkucK1JSHK1Q" alt=""></div>

Дальше эти переменные вы можете использовать внутри чат-бота.
