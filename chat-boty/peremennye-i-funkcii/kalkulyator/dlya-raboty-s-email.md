# Для работы с email

## &#x20;Для отправки  email-сообщений&#x20;

{% hint style="warning" %}
Обратите внимание!

При исполнении функций для работы с email-сообщениями возвращается:

А) либо <mark style="color:green;">**NONE**</mark> - при успешном выполнении функции;

В) либо текст <mark style="color:red;">**статуса ошибки.**</mark>
{% endhint %}

**send\_email() | send\_email\_from\_bot() | send\_email\_template()**

{% tabs %}
{% tab title="Описание" %}
<mark style="background-color:blue;">**Для отправки email-сообщения**</mark>

**send\_email(to\_email, subject, message)**&#x20;

Параметры:

<mark style="color:red;">**!**</mark>**&#x20;to\_email -** email получателя

<mark style="color:red;">**!**</mark>**&#x20;subject -** заголовок письма

<mark style="color:red;">**!**</mark>**&#x20;message -** текст письма

<mark style="background-color:blue;">**Для отправки email-сообщений через бот**</mark>

**send\_email\_from\_bot(email\_bot, client\_email, email\_subject, text, attachment\_url)**&#x20;

Параметры:

<mark style="color:red;">**!**</mark>**&#x20;email\_bot** - почта, к которой подключен канал email-рассылок \
<mark style="color:red;">**!**</mark>**&#x20;client\_email** - почта клиента, куда отправится письмо \
<mark style="color:red;">**!**</mark>**&#x20;email\_subject** - тема письма, заголовок \
<mark style="color:red;">**!**</mark>**&#x20;text** - сообщение, передаваемое в теле письма \
**attachment\_url** - url с ссылкой на вложение&#x20;

<mark style="background-color:blue;">**Для пересылки черновика или отправленного письма email**</mark>

**send\_email\_template(mailing\_id, client\_email, email\_bot, date)**

Параметры:

<mark style="color:red;">**!**</mark>**&#x20;mailing\_id** - id шаблона рассылки - либо черновик, либо уже готовое письмо.&#x20;

<mark style="color:red;">**!**</mark>**&#x20;client\_email** - email получателя письма.

**email\_bot** - email отправителя. По умолчанию email, подключенный к проекту.&#x20;

**date** - дата отправки письма, в формате ‘dd.mm.yyyy HH:mm’.  Если указать уже прошедшую дату или не указать вовсе, письмо отправится сразу же после вызова функции.
{% endtab %}

{% tab title="Примеры" %}
Для отправки email-сообщения:

<figure><img src="../../../.gitbook/assets/image (223) (1).png" alt=""><figcaption></figcaption></figure>

После исполнения функции клиент получит письмо:

<figure><img src="../../../.gitbook/assets/image (224) (1).png" alt="" width="563"><figcaption><p>Скрин полученного письма</p></figcaption></figure>

Отправка через бот

<figure><img src="../../../.gitbook/assets/image (225) (1).png" alt=""><figcaption></figcaption></figure>

Пример отправки ранее отправленного письма:&#x20;

В списке писем для рассылок забираем переменную - id. \
В примере - 483, это будущая mailing\_id:

<figure><img src="../../../.gitbook/assets/image (226) (1).png" alt=""><figcaption></figcaption></figure>

Переходим в конструктор и вызываем функцию со следующими параметрами: \
вариант 1 - указание параметров в явном виде:\
e\_letter = send\_email\_template('483',"test@mail.ru", '', '09.08.2022 15:00')\
вариант 2 - указание параметров через переменные: \
mailing\_id = ‘483’ \
client\_email = ‘test@mail.ru’ (получатель письма) \
email\_bot =’ ’ \
date = '09.08.2022 15:00' (на момент рассылки уже просроченная дата, следовательно, письмо придет в момент вызова функции)\
e\_letter = send\_email\_template(mailing\_id ,client\_email , email\_bot, date)

<figure><img src="../../../.gitbook/assets/image (227) (1).png" alt=""><figcaption><p>пример настроек для отправки письма</p></figcaption></figure>

В итоге при вызове функции на почту test@mail.ru пришел шаблон уже заранее готового письм&#x430;**:**

<figure><img src="../../../.gitbook/assets/image (228) (1).png" alt=""><figcaption></figcaption></figure>
{% endtab %}

{% tab title="Пример кода для копирования" %}
```
send_email('spirin.dmitrij@list.ru', 'Это заголовок', 'А здесь я пишу текст')

/*через бот*/
mailing = send_email_from_bot('test_channel@test.com', 'test_client@yandex.ru', 'Тема письма. Совсем обычная', 'Привет, шлю тебе мое сообщение', 'https://sun9-82.userapi.com/impg/L3ZYWHnlseIQsqZO')
```
{% endtab %}
{% endtabs %}

## Для подтверждения рассылок на email-адрес клиента

**confirm\_email\_subscription()**

{% tabs %}
{% tab title="Описание" %}
**confirm\_email\_subscription(email, sender\_name, bot\_email, callback,client\_name)**

{% hint style="info" %}
Функция понадобится для того, чтобы собирать согласия с клиентов для направления рассылок.&#x20;

Если клиент в мессенджере указал почту, то отправляться будет согласие на рассылку, только после согласия будет создан email-клиент

При этом доверия к такому адресу электронной почты, владелец которого дал согласие, будет больше, то есть рейтинг рассылок будет выше.
{% endhint %}

{% hint style="warning" %}
Важно!&#x20;

Без согласия клиента нельзя отправлять рассылки с потенциально рекламным контентом, не пренебрегайте указанной информацией во избежание штрафов за нарушения.&#x20;
{% endhint %}

Параметры:

**email** - email-адрес клиента для подтверждения и добавления&#x20;

**sender\_name** - название компании, от имени которой просите подтвердить согласие на получение рассылок

**bot\_email** - адрес email-бота, к которому присоединить нового **email-**&#x43A;лиента&#x20;

**callback** - нужны ли колбеки клиентам, которые подтверждают **email**-адре&#x441;**,** и новому email-клиенту (по умолчанию False)

**client\_name** - имя, которое запишется email клиенту

Отправленные колбеки будут иметь вид:&#x20;

"client\_accept\_email\_subscription: #{email}" - колбек клиенту, подтверждающему email-адрес

"email\_client\_accepted\_by ID:#{@client.id}" - новому клиенту (id подтверждающего сохранится в переменную client\_father\_id)
{% endtab %}

{% tab title="Пример" %}
После того, как пользователь оставляет Вам email, отправьте письмо для верификации адреса.&#x20;

<figure><img src="../../../.gitbook/assets/image (229) (1).png" alt=""><figcaption></figcaption></figure>

После подтверждения пользователем согласия на получение рассылок от компании  Вам будет добавлен новый email-клиент.&#x20;

Таким образом, у Вас не будет "мертвых душ" при рассылках, а база email  будет содержать адреса действительно заинтересованных в вашей продукции клиентов.
{% endtab %}
{% endtabs %}
