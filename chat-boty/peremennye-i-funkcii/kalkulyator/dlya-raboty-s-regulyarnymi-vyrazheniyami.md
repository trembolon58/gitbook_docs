# Для работы с регулярными выражениями

{% hint style="danger" %}
Напоминаем, что время выполнения регулярного выражения - 5 секунд.
{% endhint %}

**findall() | similar()**

<mark style="color:red;">**ОБОЗНАЧЕНИЯ:**</mark>

<mark style="color:red;">**!**</mark> - Обязательные параметры

{% tabs %}
{% tab title="Описание" %}
#### <mark style="background-color:blue;">Поиск в строке по регулярному выражению</mark>

**findall(reg, str, index) —** для поиска всех вхождений группы в строку. &#x20;

Параметры:

<mark style="color:red;">**!**</mark>**&#x20;reg** - регулярное выражение

<mark style="color:red;">**!**</mark>**&#x20;str** - строка, в которой происходит поиск

&#x20;**index** - индекс найденного результата. Индекс считается с нуля. То есть первый найденный результат будет иметь индекс 0.

<mark style="background-color:blue;">**Сравнение строк с учетом описок**</mark>

**similar(str1, str2)** - для сравнения строк с учетом описок. Возвращает True, если строки отличаются менее чем на 30%.&#x20;
{% endtab %}

{% tab title="Примеры" %}
Рассмотрим пример поиска строки по заданному регулярному выражению:

<figure><img src="../../../.gitbook/assets/image (112).png" alt=""><figcaption><p>Пример использования findall()</p></figcaption></figure>

Результат:

<figure><img src="../../../.gitbook/assets/image (113).png" alt=""><figcaption><p>Результат вычисления функции findall()</p></figcaption></figure>

Пример использования функции сравнения строк с учетом описок: &#x20;

<figure><img src="../../../.gitbook/assets/image (114).png" alt=""><figcaption><p>Простой пример применения similar()</p></figcaption></figure>

<figure><img src="../../../.gitbook/assets/image (115).png" alt=""><figcaption></figcaption></figure>
{% endtab %}

{% tab title="Пример кода для копирования" %}
```
findall('.ru\/(.+)\/', 'https://payform.ru/ab252acn/', 0)

ответ = if(similar(загадка, question) == True , "супер!", "Неет! это - #{загадка}")
```
{% endtab %}
{% endtabs %}
