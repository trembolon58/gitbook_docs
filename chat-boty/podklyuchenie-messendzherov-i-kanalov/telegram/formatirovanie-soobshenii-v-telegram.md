# Форматирование сообщений в Telegram

## Разметка Markdown

Для правильной разметки текста в нужном блоке (разметка находится под полем для ввода текста сообщения) строго соблюдайте следующие шаги:

<figure><img src="../../../.gitbook/assets/Снимок экрана 2025-04-24 в 16.37.46.png" alt=""><figcaption></figcaption></figure>

1. Ставим нужный текст в поле ответ.

Если вы используете переменные в тексте, то на данном этапе их указывать <mark style="color:red;">**не нужно**</mark>. В противном случае синтаксис переменных будет нарушен и знаки #{} также будут экранированы, а переменная не отобразится в тексте.

2. Включаем "Markdown в Telegram". Так в ваш текст будут добавлены символы экранирования.
3. Выделяем текст \*\* либо \_ \_ и т.п.

{% hint style="danger" %}
Если в этом блоке встречаются символы из перечисленных: '\_', '\*', '\[', ']', '(', ')', '\~', '\`', '>', '#', '+', '-', '=', '|', '{', '}', '.', '!'  — их нужно экранировать, добавлять перед ними обратный слэш \\&#x20;

Иначе сообщение не отправится вообще. При этом не имеет значения, какой участок текста вы размечаете.

&#x20;Пример: привет\\. Рады \*тебя\* видеть\\!
{% endhint %}

Спецсимволы:

**Жирный текст** — с обеих сторон ставите звездочки: \*тут текст\*\
**Курсив** — нижнее подчёркивание: \_текст\_\
**Подчеркнутый текст** — два нижних подчеркивания с обеих сторон: \_\_текст\_\_\
**Зачеркнутый текст** — тильда с обеих сторон текста: \~текст\~\
**Ссылка в тексте**: \[текст в квадратных скобках]\(ссылка в круглых скобках) \
\[inline URL]\([http://www.example.com/](https://vk.com/away.php?to=http%3A%2F%2Fwww.example.com%2F\&cc_key=))\
**Упоминание пользователя ТГ**: \[текст в квадратных скобках]\(ссылка на пользователя в круглых скобках). В ссылке после знака равно можно использовать #{platform\_id} \
\[inline mention of a user]\(tg://user?id=123456789)\
**Текст в виде кода** — с обеих сторон текста поставить обратный апостроф: \`inline fixed-width code\`\
**Скрытый текст или spoiler** - с обеих сторон от текста используйте ||&#x20;

4. Далее размечаете нужный текст при помощи спецсимволов.&#x20;

**Пример:**

<figure><img src="../../../.gitbook/assets/Снимок экрана 2025-04-24 в 16.46.04.png" alt=""><figcaption><p>Пример разметки</p></figcaption></figure>

Результат:

<figure><img src="../../../.gitbook/assets/Снимок экрана 2025-04-24 в 16.47.00.png" alt="" width="432"><figcaption></figcaption></figure>

При работе с Markdown необходимо не забывать, что спецсимволы следует экранировать, заменить в тексте управляющие символы на соответствующие текстовые подстановки. Делается это достаточно просто - перед спецсимволом добавляется **обратный слэш \\**  или  при помощи функции Калькулятора

**txt = tg\_escape(s), где** **s** - строка с исходным текстом.&#x20;

{% hint style="info" %}
Чтобы в переменную записать текст с переносами строк, укажите значение следующим образом:

`ваша_переменная = "Текст первой строки" + "\n" + "Текст второй строки" + "\n" +"Третья строка"`
{% endhint %}

На выходе в **txt** приходит строка уже с вставленными слешами в нужных местах.&#x20;

**Пример:**

<figure><img src="../../../.gitbook/assets/Снимок экрана 2025-04-17 в 13.11.00.png" alt=""><figcaption><p>Пример экранирования</p></figcaption></figure>

<figure><img src="../../../.gitbook/assets/Снимок экрана 2025-04-17 в 13.12.22.png" alt=""><figcaption><p>Как выглядит текст в Telegram</p></figcaption></figure>

Далее размечаете нужный текст.

#### Пример с длинным текстом:

<figure><img src="../../../.gitbook/assets/Снимок экрана 2025-04-24 в 17.00.44.png" alt="" width="364"><figcaption></figcaption></figure>

Для этого в калькуляторе необходимо:

Шаг 1. Вставить текст в поле сообщения:

<figure><img src="../../../.gitbook/assets/Снимок экрана 2025-04-24 в 16.54.42.png" alt="" width="563"><figcaption></figcaption></figure>

Шаг 2. Включить кнопку разметки Marldown:

<figure><img src="../../../.gitbook/assets/Снимок экрана 2025-04-24 в 16.55.37.png" alt="" width="563"><figcaption><p>При включении кнопки разметки, экранируются спецсимволы</p></figcaption></figure>

Шаг 3. Расставляем спецсимволы для форматирования сообщения по тексту:

<figure><img src="../../../.gitbook/assets/Снимок экрана 2025-04-24 в 16.59.33.png" alt="" width="563"><figcaption></figcaption></figure>

Если после отправки сообщения, оно не дошло в мессенджер, а в диалоге в разделе Клиенты вы видите ошибку, значит вы неверно экранировали символы.&#x20;

При этом вы увидите ошибку при отправке сообщения в разделе "Клиенты", в ней будет указан символ, который не был экранирован.

Сообщения об ошибках, которые вы можете встретить:

1. Нет закрывающего символа:

<div><figure><img src="../../../.gitbook/assets/2.jpg" alt="" width="542"><figcaption></figcaption></figure> <figure><img src="../../../.gitbook/assets/3.jpg" alt="" width="560"><figcaption></figcaption></figure></div>

2. Отсутствует экранирование символа:

<figure><img src="../../../.gitbook/assets/1.jpg" alt="" width="563"><figcaption></figcaption></figure>



Ознакомьтесь с особенностями разметки текста в видео ниже и выполните экранирование правильно:

{% embed url="https://www.youtube.com/watch?v=yzGHBrBywOo" %}
Форматирование текста в редакторе блока для Telegram: markdown
{% endembed %}



## Разметка HTML

Чтобы разметка HTML работала, не забудьте нажать на кнопку HTML под текстовым полем для сообщения:

<figure><img src="../../../.gitbook/assets/Снимок экрана 2024-09-25 в 18.20.40.png" alt="" width="563"><figcaption></figcaption></figure>

1. \<a href="https://google.com">ссылка\</a> - вшивает ссылку в определенное слово.&#x20;

Пример заполнения:

<figure><img src="../../../.gitbook/assets/2024-04-26_13-52-22.png" alt="" width="563"><figcaption></figcaption></figure>

2. \<u>underlined\</u> - подчеркнутый шрифт

Пример:

<div><figure><img src="../../../.gitbook/assets/2024-04-26_13-55-06.png" alt=""><figcaption></figcaption></figure> <figure><img src="../../../.gitbook/assets/2024-04-26_13-56-20.png" alt=""><figcaption></figcaption></figure></div>

3. \<ins>underlined\</ins> - подчеркнутый шрифт

Пример:

<div><figure><img src="../../../.gitbook/assets/2024-04-26_14-20-34.png" alt=""><figcaption></figcaption></figure> <figure><img src="../../../.gitbook/assets/2024-04-26_13-59-01.png" alt="" width="472"><figcaption></figcaption></figure></div>

4. \<em>italic\</em> - курсивный шрифт

Пример:

<div><figure><img src="../../../.gitbook/assets/2024-04-26_14-19-05.png" alt=""><figcaption></figcaption></figure> <figure><img src="../../../.gitbook/assets/2024-04-26_14-04-50.png" alt=""><figcaption></figcaption></figure></div>

5. \<i>italic\</i> - курсивный шрифт

Пример:

<div><figure><img src="../../../.gitbook/assets/2024-04-26_14-17-28.png" alt=""><figcaption></figcaption></figure> <figure><img src="../../../.gitbook/assets/2024-04-26_14-07-58.png" alt=""><figcaption></figcaption></figure></div>

\<strong>strong\</strong> - жирный шрифт

<div><figure><img src="../../../.gitbook/assets/2024-04-26_14-16-01.png" alt=""><figcaption></figcaption></figure> <figure><img src="../../../.gitbook/assets/2024-04-26_14-11-21.png" alt=""><figcaption></figcaption></figure></div>

\<strike>strike\</strike> - зачеркнутый шрифт

<div><figure><img src="../../../.gitbook/assets/2024-04-26_14-14-54.png" alt=""><figcaption></figcaption></figure> <figure><img src="../../../.gitbook/assets/2024-04-26_14-14-20.png" alt=""><figcaption></figcaption></figure></div>

\<span class="tg-spoiler">hidden\</span> - скрытый шрифт

Пример:

<figure><img src="../../../.gitbook/assets/2024-04-26_14-22-14.png" alt="" width="464"><figcaption></figcaption></figure>

\<code>Prerfomatted\</code> - форматированный шрифт

Пример:

<div><figure><img src="../../../.gitbook/assets/2024-04-26_14-28-08.png" alt=""><figcaption></figcaption></figure> <figure><img src="../../../.gitbook/assets/2024-04-26_14-27-54.png" alt=""><figcaption></figcaption></figure></div>

\<pre>Preformatted\</pre> - форматированный шрифт

Пример:

<div><figure><img src="../../../.gitbook/assets/2024-04-26_14-29-50.png" alt=""><figcaption></figcaption></figure> <figure><img src="../../../.gitbook/assets/2024-04-26_14-29-36.png" alt=""><figcaption></figcaption></figure></div>

## Как включить защищенный режим для контента

Чтобы защитить контент от распространения можно включить защищенный режим для сообщений. Для этого в разделе "Сообщение" включите "Защитить контент":

<figure><img src="../../../.gitbook/assets/image (82) (1).png" alt=""><figcaption></figcaption></figure>

{% hint style="info" %}
Защищенные сообщения нельзя переслать, на телефоне нельзя сделать скриншот.
{% endhint %}

{% embed url="https://www.youtube.com/watch?v=mBSG2RY2y1k" %}
Telegram: защита контента, редактор блока
{% endembed %}
