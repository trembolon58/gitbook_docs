# Для работы с переменными

## Как получить значения переменных клиента

**get\_client\_var() | get\_client\_vars()**

{% tabs %}
{% tab title="Описание" %}
<mark style="background-color:blue;">**Для получения значения одной переменной**</mark>

**get\_client\_var(client\_id, variable)**

Параметры:

<mark style="color:red;">**!**</mark>**&#x20;client\_id -** идентификатор клиента

<mark style="color:red;">**!**</mark>**&#x20;variable -** имя переменной

<mark style="background-color:blue;">**Для получения значения нескольких переменных**</mark>

**get\_client\_vars(client\_id, names)**

Параметры:

<mark style="color:red;">**!**</mark>**&#x20;client\_id -** идентификатор клиента

<mark style="color:red;">**!**</mark>**&#x20;names-** массив переменных
{% endtab %}

{% tab title="Пример" %}
Давайте менеджеру отправим сообщение с номером урока, который проходит один из участников нашего проекта:

<figure><img src="../../../.gitbook/assets/image (232) (1).png" alt=""><figcaption><p>Пример использования функции получения значения переменной</p></figcaption></figure>

<figure><img src="../../../.gitbook/assets/image (233) (1).png" alt=""><figcaption><p>Результат работы функции</p></figcaption></figure>

Тот же вариант но с выводом, например, уровня и урока в нем:

<figure><img src="../../../.gitbook/assets/image (234) (1).png" alt=""><figcaption><p>Пример использования функции получения нескольких значений</p></figcaption></figure>

<figure><img src="../../../.gitbook/assets/image (235) (1).png" alt=""><figcaption><p>результат работы функции</p></figcaption></figure>
{% endtab %}

{% tab title="Пример кода для копирования" %}
```
/*Получение одной переменной*/
probno=get_client_var(64732310, 'urok')

/*Получение нескольких переменных*/
names=["level","urok"]
probno=get_client_vars(64732310, names)
```
{% endtab %}
{% endtabs %}

## Как присвоить переменную клиента

**set\_client\_var() | set\_client\_vars()**

{% tabs %}
{% tab title="Описание" %}
<mark style="background-color:blue;">**Для присвоения значения одной переменной**</mark>

**set\_client\_var(client\_id, variable, value)**

Параметры:&#x20;

**client\_id** — id клиента в Salebot\
**variable** — название переменной, которая будет присваиваться\
**value** — значение этой переменной

<mark style="background-color:blue;">**Для присвоения нескольких переменных**</mark>

**set\_client\_vars(client\_id, variables\_dict)**

Параметры:

**client\_id** — id клиента в Salebot \
**variables\_dict** — словарь, содержащий названия всех добавляемых переменных и их значения. \
Формат:\
'{"var\_name1": "var\_value1", "var\_name2": "var\_value2", "var\_name3": "var\_value3"}'
{% endtab %}

{% tab title="Пример" %}
Пример1:

set\_client\_var(client\_id, "novoe", "да")

![](<../../../.gitbook/assets/image (236) (1).png>)

![](<../../../.gitbook/assets/image (237) (1).png>)

Пример2:

set\_client\_vars(1136, '{"var\_name1": "var\_value1", "var\_name2": "var\_value2", "var\_name3": "var\_value3"}')
{% endtab %}
{% endtabs %}
