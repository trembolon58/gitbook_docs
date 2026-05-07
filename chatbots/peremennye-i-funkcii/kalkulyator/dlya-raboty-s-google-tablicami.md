# Для работы с Google-таблицами

{% hint style="danger" %}
Внимание! Устаревшее!&#x20;

Для лучшей работы с данными загрузите их в [Таблицы Salebot,](/broken/pages/m12tQghvK3rMwVuiUNYr) тогда Ваши боты будут работать намного быстрее и без ошибок, связанных с запросами к google-таблицам.
{% endhint %}

## Для работы с буквами колонок&#x20;

**c2n() | n2c() | addCols()**

{% tabs %}
{% tab title="Описание" %}
<mark style="background-color:blue;">**Получение номера колонки по буквенному обозначению**</mark>

**c2n(str)**

Параметры:

<mark style="color:red;">**!**</mark> **str** - номер колонки в буквенном обозначении

<mark style="background-color:blue;">**Получение буквенного обозначения колонки по цифре**</mark>

**n2c(n)**

Параметры:

<mark style="color:red;">**!**</mark> **n**- номер колонки  виде числа

<mark style="background-color:blue;">**Получение буквенного обозначения колонки по смещению от заданного**</mark>

**addCols(str, n)**

Параметры:

<mark style="color:red;">**!**</mark> **str** - номер колонки в буквенном обозначении

**n** - смещение. Для получения номера колонки слева от обозначенного передайте отрицательное значение смещения
{% endtab %}

{% tab title="Примеры" %}
<figure><img src="../../../.gitbook/assets/image (221) (1).png" alt=""><figcaption></figcaption></figure>

<figure><img src="../../../.gitbook/assets/image (222) (1).png" alt=""><figcaption></figcaption></figure>
{% endtab %}

{% tab title="Пример кода для копирования" %}
```
число=c2n('AAB')
строка=n2c(54)
смещение=addCols('AA',-1)
```
{% endtab %}
{% endtabs %}
