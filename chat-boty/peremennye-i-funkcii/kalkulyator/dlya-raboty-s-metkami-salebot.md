# Для работы с метками Salebot

**create\_label() |** add\_label() | remove\_label() | remove\_label\_everywhere() | count\_of\_clients\_with\_label() | has\_label()

{% tabs %}
{% tab title="Описание" %}
Метки Salebot отображаются как в карточке клиента:&#x20;

<figure><img src="../../../.gitbook/assets/Снимок экрана 2025-08-28 в 17.32.56.png" alt=""><figcaption></figcaption></figure>

так и в разделе "Списки":

<figure><img src="../../../.gitbook/assets/Снимок экрана 2025-08-28 в 17.31.12.png" alt=""><figcaption></figcaption></figure>

* **create\_label(label\_name)** - создание метки Salebot с указанным именем.&#x20;

Параметры:

<mark style="color:red;">**!**</mark>**&#x20;label\_name**- имя метки, задается в одинарных кавычках ''

* **add\_label(label\_name, client\_id)** - добавление метки Salebot клиенту.&#x20;

Параметры:

<mark style="color:red;">**!**</mark>**&#x20;label\_name** - имя метки, задается в одинарных кавычках ''

**client\_id** - идентификатор клиента. Если не передан, то  используется идентификатор текущего клиента&#x20;

* **remove\_label(label\_name, client\_id)** - удаление метки у клиента&#x20;

Параметры:

<mark style="color:red;">**!**</mark>**&#x20;label\_name** - имя метки, задается в одинарных кавычках ''

**client\_id** - идентификатор клиента. Если не передан, то  используется идентификатор текущего клиента&#x20;

* **has\_label(label\_name, client\_id**) - проверить наличие метки у клиента&#x20;

Параметры:

<mark style="color:red;">**!**</mark>**&#x20;label\_name** - имя метки, задается в одинарных кавычках ''

**client\_id** - идентификатор клиента. Если не передан, то  используется идентификатор текущего клиента&#x20;

* **remove\_label\_everywhere(label\_name)** - удаление метки у всех клиентов

Параметры:

<mark style="color:red;">**!**</mark>**&#x20;label\_name**- имя метки, задается в одинарных кавычках ''

* **count\_of\_clients\_with\_label(label\_name)** - получение общего количества клиентов с меткой

Параметры:

<mark style="color:red;">**!**</mark>**&#x20;label\_name**- имя метки, задается в одинарных кавычках ''
{% endtab %}

{% tab title="Пример" %}
Итак, разберем **как** же **создается метка Salebot**.&#x20;

Достаточно единожды выполнить функцию создания в сером блоке (блоке не состояние), например:

<figure><img src="../../../.gitbook/assets/image (208).png" alt=""><figcaption><p>Создание метки через функцию Калькулятора</p></figcaption></figure>

При этом в переменной _**a**_ можно проанализировать успех выполнения функции создания метки:

<figure><img src="../../../.gitbook/assets/image (209).png" alt=""><figcaption></figcaption></figure>

Далее метку можно **назначить любому из клиентов**, для этого пропишите функцию add\_label() в нужном блоке Вашей воронки:

<figure><img src="../../../.gitbook/assets/image (210).png" alt=""><figcaption><p>Добавление метки клиенту</p></figcaption></figure>

Проверить наличие метки у клиента можно при помощи функции has\_label():

<figure><img src="../../../.gitbook/assets/image (211).png" alt=""><figcaption><p>Проверка наличия метки у клиента</p></figcaption></figure>

Функция возвращает логическое значение True или False ![](<../../../.gitbook/assets/image (212).png>)

Аналогичным методом выполняются и другие действия над метками - удаление метки у конкретного клиента, удаление метки в целом у всех клиентов.

Можно посчитать **количество клиентов с заданной меткой** - воспользуйтесь функцией count\_of\_clients\_with\_label()&#x20;

<figure><img src="../../../.gitbook/assets/image (213).png" alt=""><figcaption><p>Подсчет количества клиентов по заданной метке</p></figcaption></figure>
{% endtab %}

{% tab title="Пример кода для копирования" %}
```
/*Создание метки*/
a=create_label('метка1') 

/*Прописать метку клиенту*/
a=add_label('этап 1')

/*Проверить есть ли метка у клиента*/
a=has_label('этап 1','73704021')

/*Подсчет количества клиентов по заданной метке*/
etap1=count_of_clients_with_label('этап 1')
tovar1=count_of_clients_with_label('1')
```
{% endtab %}
{% endtabs %}

### Создание метки из блока

**create\_label()**

{% tabs %}
{% tab title="Описание" %}
**create\_label(label\_name)** - создание метки Salebot с указанным именем.&#x20;

Параметры:

<mark style="color:red;">**!**</mark>**&#x20;label\_name**- имя метки, задается в одинарных кавычках ''
{% endtab %}
{% endtabs %}

### Создание метки из блока без создания дубля

**create\_label\_if\_not\_exist()**&#x20;

{% tabs %}
{% tab title="Описание" %}
**create\_label\_if\_not\_exist(name, color)** - создает новую метку, если с таким именем еще нет и возвращает идентификатор или вернет идентификатор существующей

**name** — название метки

**color** — цвет метки (по умолчанию 0)

Таблица цветов для параметра color:

0 — светло-серый&#x20;

1 — желтый&#x20;

2 — синий&#x20;

3 — красный

4 — розовый&#x20;

5 — бежевый&#x20;

6 — фиолетовый&#x20;

7 — голубой&#x20;

8 — серый&#x20;

9 - зеленый
{% endtab %}
{% endtabs %}

### Получить все метки клиента

get\_all\_client\_labels()

{% tabs %}
{% tab title="Параметры функции" %}
**get\_all\_client\_labels(client\_id)**&#x20;

_**Параметры:**_

**client\_id** - не обязателен, если не передан, будут получены метки текущего клиента.&#x20;

Функция возвращает ответ в формате json: {"161":"metka1","228":"metka2"},  где:

ключ - это id метки, значение -  ее название.
{% endtab %}

{% tab title="Пример" %}
<figure><img src="../../../.gitbook/assets/image (214).png" alt=""><figcaption><p>Получить все метки текущего клиента</p></figcaption></figure>
{% endtab %}
{% endtabs %}

### Удалить метки клиента массивом

remove\_multiple\_client\_labels()

{% tabs %}
{% tab title="Параметры функции" %}
**remove\_multiple\_client\_labels(labels\_array, names) -** функция удалит те метки, что указаны в массиве.&#x20;

**labels\_array** - массив меток. <mark style="color:orange;">**ИЛИ**</mark> массив <mark style="color:orange;">**идентификаторов,**</mark> <mark style="color:orange;">**ИЛИ**</mark> массив <mark style="color:orange;">**названий**</mark>.&#x20;

<mark style="color:orange;">Если</mark> передается <mark style="color:orange;">массив НАЗВАНИЙ</mark>, то дополнительно <mark style="color:orange;">❗Обязательно передать второй параметр(names) равный 1.</mark> &#x20;

**names** -  Указать 1, если **список названий меток**, а не идентификаторы. Это указание на то, что список имен.

{% hint style="danger" %}
НЕЛЬЗЯ в одной функции объединять и идентификаторы и названия меток!!!!
{% endhint %}
{% endtab %}

{% tab title="Пример" %}
`/*Удалить метки по идентификатору*/`

`r = remove_multiple_client_labels('[138,169,166]')`&#x20;

`/*Удалить метки по названию метки*/`

`r2 = remove_multiple_client_labels('["newTestTag","metka2"]', 1)`

В переменную запишется результат выполнения функции: или вернет текст ошибки, или число, сколько было удалено меток.

<figure><img src="../../../.gitbook/assets/image (215).png" alt=""><figcaption></figcaption></figure>
{% endtab %}
{% endtabs %}

### Найти клиентов по нескольким меткам

find\_clients\_by\_multiple\_labels()&#x20;

{% tabs %}
{% tab title="Параметры функции" %}
**find\_clients\_by\_multiple\_labels(labels\_array, names)** - Найти клиентов по нескольким меткам

{% hint style="warning" %}
ВАЖНО! Найдет только тех клиентов, у которых есть <mark style="color:orange;">**ВСЕ**</mark> переданные метки.
{% endhint %}

Параметры:

**labels\_array** - массив меток. <mark style="color:orange;">**ИЛИ**</mark> массив <mark style="color:orange;">**идентификаторов,**</mark> <mark style="color:orange;">**ИЛИ**</mark> массив <mark style="color:orange;">**названий**</mark>. &#x20;

<mark style="color:orange;">Если</mark> передается <mark style="color:orange;">массив НАЗВАНИЙ</mark>, то дополнительно <mark style="color:orange;">❗Обязательно передать второй параметр(names)</mark> равный 1. &#x20;

**names** - Указать 1, если **список названий меток**, а не идентификаторы. Это указание на то, что список имен.

{% hint style="danger" %}
НЕЛЬЗЯ в одной функции объединять и идентификаторы и названия меток!!!!
{% endhint %}

Вернет список идентификаторов клиентов (client\_id): \[41121, 41192, 41522]
{% endtab %}

{% tab title="Пример" %}
`/* Найти клиентов у кого есть все указанные метки, по идентификатору*/`

`r = find_clients_by_multiple_labels('[138,169,166]')`&#x20;

`/*Найти клиентов у кого есть все указанные метки, по названию меток*/`

`r2 = find_clients_by_multiple_labels('["newTestTag","metka2"]', 1)`

<figure><img src="../../../.gitbook/assets/image (216).png" alt=""><figcaption></figcaption></figure>
{% endtab %}
{% endtabs %}

### Проверка наличия списка меток у клиента

has\_client\_multiple\_labels()

{% tabs %}
{% tab title="Параметры функции" %}
**has\_client\_multiple\_labels(labels\_array, names)** - Проверка наличия списка меток у клиента.

{% hint style="warning" %}
ВАЖНО вернет True, если у клиента есть все переданные метки!
{% endhint %}

**labels\_array** - массив меток. <mark style="color:orange;">**ИЛИ**</mark> массив <mark style="color:orange;">**идентификаторов,**</mark> <mark style="color:orange;">**ИЛИ**</mark> массив <mark style="color:orange;">**названий**</mark>. &#x20;

<mark style="color:orange;">Если</mark> передается <mark style="color:orange;">массив НАЗВАНИЙ</mark>, то дополнительно <mark style="color:orange;">❗Обязательно передать второй параметр(names)</mark> равный 1. &#x20;

**names** - Указать 1, если **список названий меток**, а не идентификаторы. Это указание на то, что список имен.

{% hint style="danger" %}
НЕЛЬЗЯ в одной функции объединять и идентификаторы и названия меток!!!!
{% endhint %}

Возвращает либо ошибку, либо True - есть все метки из массива, или False, если не все метки есть у клиента
{% endtab %}

{% tab title="Пример" %}
`/*Проверить наличие у клиента всех указанных меткок, по идентификатору*/`

`r = has_client_multiple_labels('[138,169,166]')`

`/*Проверить наличие у клиента всех указанных меток, по названию меток*/`

&#x20;`r2 = has_client_multiple_labels('["newTestTag","metka2"]', 1)`

<figure><img src="../../../.gitbook/assets/image (217).png" alt=""><figcaption></figcaption></figure>
{% endtab %}
{% endtabs %}
