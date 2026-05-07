# Форматирование текста сообщений

## Как форматировать текст в месседжерах

### Как форматировать в Telegram

Для разметки текста в нужном блоке под полем для ввода текста сообщения включите "Markdown в Telegram":

<figure><img src="../../.gitbook/assets/Снимок экрана 2025-04-17 в 12.57.19.png" alt="" width="563"><figcaption></figcaption></figure>

{% hint style="danger" %}
Если в этом блоке встречаются символы из перечисленных: '\_', '\*', '\[', ']', '(', ')', '\~', '\`', '>', '#', '+', '-', '=', '|', '{', '}', '.', '!'  — их нужно экранировать, добавлять перед ними обратный слэш \\&#x20;

Иначе сообщение не отправится вообще. При этом не имеет значения, какой участок текста вы размечаете.

&#x20;Пример: привет\\. Рады \*тебя\* видеть\\!
{% endhint %}

Экранирование текста возможно как вручную, так и в калькуляторе при помощи функции

**txt = tg\_escape(s)**

На вход подается **s** - строка с исходным текстом.&#x20;

{% hint style="info" %}
Чтобы в переменную записать текст с переносами строк, укажите значение следующим образом:

`ваша_переменная = "Текст первой строки" + "\n" + "Текст второй строки" + "\n" +"Третья строка"`
{% endhint %}

На выходе в **txt** приходит строка уже с вставленными слешами в нужных местах.&#x20;

Пример:

<figure><img src="../../.gitbook/assets/Снимок экрана 2025-04-17 в 13.11.00.png" alt=""><figcaption><p>Пример экранирования</p></figcaption></figure>

<figure><img src="../../.gitbook/assets/Снимок экрана 2025-04-17 в 13.12.22.png" alt=""><figcaption><p>Как выглядит текст в Telegram</p></figcaption></figure>

![Как выглядит текст в других мессенджерах](../../.gitbook/assets/spaces--LxKl4rC_EcwBAz40Qn_-uploads-NIIRMPo2D2j37Z3doLld-image.png)

Далее размечаете нужный текст:

Чтобы сделать текст **жирным**, с обеих сторон ставите звездочки: \*тут текст\*

**Для курсива** — нижнее подчёркивание: \_текст\_

**Подчеркнутый текст** — два нижних подчеркивания с обеих сторон: \_\_текст\_\_

**Зачеркнутый текст** — тильда с обеих сторон текста: \~текст\~

**Ссылка в тексте**: \[текст в квадратных скобках]\(ссылка в круглых скобках) \
\[inline URL]\(http://example.com/)

**Упоминание пользователя ТГ**: \[текст в квадратных скобках]\(ссылка на пользователя в круглых скобках). В ссылке после знака равно можно использовать #{platform\_id} \
\[inline mention of a user]\(tg://user?id=123456789)

**Текст в виде кода** — с обеих сторон текста поставить обратный апостроф: \`inline fixed-width code\`

**Скрытый текст или spoiler** - с обеих сторон от текста используйте ||&#x20;

Пример:

<figure><img src="../../.gitbook/assets/Снимок экрана 2025-04-17 в 13.18.07.png" alt=""><figcaption><p>Пример экранирования</p></figcaption></figure>

Результат:

<figure><img src="../../.gitbook/assets/Снимок экрана 2025-04-17 в 13.18.46.png" alt=""><figcaption><p>Как выглядит текст в Telegram</p></figcaption></figure>

{% hint style="warning" %}
Экранировать переменные в тексте НЕ надо.
{% endhint %}

<figure><img src="../../.gitbook/assets/Снимок экрана 2025-04-17 в 13.23.27.png" alt=""><figcaption><p>Пример ошибки: экранированы символы переменной и разметки текста. </p></figcaption></figure>

<figure><img src="../../.gitbook/assets/Снимок экрана 2025-04-17 в 13.29.18.png" alt="" width="563"><figcaption><p>Пример сообщения с ошибкой экранирования</p></figcaption></figure>

Правильный вариант:

<figure><img src="../../.gitbook/assets/Снимок экрана 2025-04-17 в 13.30.34.png" alt=""><figcaption></figcaption></figure>

Сообщение в Телеграм:

<figure><img src="../../.gitbook/assets/Снимок экрана 2025-04-17 в 13.28.14.png" alt=""><figcaption></figcaption></figure>

В случае, если вы не экранируете спец. символы при использовании разметки, то сообщения из бота не будут направляться.&#x20;

Например:

<figure><img src="../../.gitbook/assets/Снимок экрана 2025-04-17 в 13.35.35.png" alt=""><figcaption><p>Не экранирован восклицательный знак, в то время как точка экранирована</p></figcaption></figure>

<figure><img src="../../.gitbook/assets/Снимок экрана 2025-04-17 в 13.37.41.png" alt=""><figcaption><p>Ошибка отправки сообщения</p></figcaption></figure>

### Видеоинструкция "Как форматировать текст в Telegram"

{% embed url="https://www.youtube.com/watch?feature=youtu.be&v=yzGHBrBywOo" %}

### Как форматировать ВКонтакте&#x20;

Какие теги доступны для форматирования текста Вконтакте:

HTML:\
\<b>жирный\</b>\
\<strong>жирный\</strong>\
\<em>курсив\</em>\
\<i>курсив\</i>\
\<u>подчеркнутый\</u>\
\<a href="url">текст ссылки\</a>

<div><figure><img src="../../.gitbook/assets/Снимок экрана 2025-07-18 в 15.32.14.png" alt="" width="563"><figcaption></figcaption></figure> <figure><img src="../../.gitbook/assets/2025-07-18 15.33.02.jpg" alt="" width="563"><figcaption></figcaption></figure></div>

Markdown:\
\_\_подчеркнутый\_\_\
\_курсив\_\
\*жирный\*\
\[текст ссылки]\(url)

<div><figure><img src="../../.gitbook/assets/Снимок экрана 2025-07-18 в 15.36.51.png" alt="" width="563"><figcaption></figcaption></figure> <figure><img src="../../.gitbook/assets/IMAGE 2025-07-18 153724.jpg" alt="" width="563"><figcaption></figcaption></figure></div>

### Как форматировать в Viber &#x20;

{% hint style="info" %}
В мессенджере Viber разметка текста не работает.
{% endhint %}

### Как форматировать в Whatsapp и Facebook<mark style="color:red;">\*</mark>&#x20;

{% hint style="danger" %}
<mark style="color:red;">**\***</mark>**На территории Российской Федерации&#x20;**<mark style="color:red;">**запрещена деятельность**</mark>**&#x20;социальных сетей&#x20;**<mark style="color:red;">**Facebook**</mark>**&#x20;и&#x20;**<mark style="color:red;">**Instagram**</mark>**, принадлежащих компании Meta Platforms Inc**., признанная экстремистской!
{% endhint %}

Whatsapp и Messenger Facebook<mark style="color:red;">\*</mark> поддерживают выделение текста при помощи символов:

<figure><img src="../../.gitbook/assets/Снимок экрана 2025-04-17 в 13.51.57.png" alt=""><figcaption><p>Форматирование текста в блоке</p></figcaption></figure>

<figure><img src="../../.gitbook/assets/Снимок экрана 2025-04-17 в 13.52.31.png" alt="" width="324"><figcaption><p>Как выглядит текст в Whatsapp</p></figcaption></figure>

{% hint style="info" %}
В Messenger Facebook<mark style="color:red;">\*</mark> форматирование работает только в веб-версии.

Неподдерживаемые теги в ФБ и whatsapp:

<img src="../../.gitbook/assets/Снимок экрана 2026-01-21 в 10.55.37.png" alt="" data-size="original"><img src="../../.gitbook/assets/Снимок экрана 2026-01-21 в 10.55.41.png" alt="" data-size="original">
{% endhint %}
