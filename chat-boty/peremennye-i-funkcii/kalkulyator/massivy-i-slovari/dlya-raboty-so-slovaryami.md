# Для работы со словарями

## Как создать словарь

Создание словаря - объявление словаря

**имя\_словаря = {}**

## Как обнулить  словарь

Обнуление - это ничто иное как объявление пустого словаря

**имя\_словаря = {}**

## Как получить значение словаря по ключу

{% tabs %}
{% tab title="Описание" %}
**имя\[ключ] -** получение элемента  словаря по ключу
{% endtab %}

{% tab title="Примеры" %}
**Пример работы со словарем:**

&#x20;в данном конкретном случае идет обращение по ключу со значением a. То есть для того, чтобы получить значение словаря по конкретному ключу прописываем команду в формате: имя\_словаря\["ключ"]

<figure><img src="../../../../.gitbook/assets/image (293).png" alt=""><figcaption></figcaption></figure>

Ответ:

<figure><img src="../../../../.gitbook/assets/image (294).png" alt=""><figcaption></figcaption></figure>

На экран будет выведено&#x20;

<figure><img src="../../../../.gitbook/assets/image (295).png" alt=""><figcaption></figcaption></figure>
{% endtab %}

{% tab title="Пример кода для копирования" %}
```
dicts = {"a": "11", "d": "privet"}
/*получение из словаря*/
aa = dicts["a"]
```
{% endtab %}
{% endtabs %}

## Как получить список ключей из словаря

{% tabs %}
{% tab title="Описание" %}
**dict\_keys\_to\_array(data)** - для получения списка ключей словаря data
{% endtab %}

{% tab title="Примеры" %}
**Пример:** Получим список всех ключей словаря

<figure><img src="../../../../.gitbook/assets/image (296).png" alt=""><figcaption></figcaption></figure>

**Ответ**:&#x20;

<figure><img src="../../../../.gitbook/assets/image (297).png" alt=""><figcaption></figcaption></figure>
{% endtab %}

{% tab title="Пример кода для копирования" %}
`v={"A1":"апельсин","A2":"абрикос","A3":"мандарин","A4":"яблоко","A5":"груша","A6":"киви","A7":"банан","A8":"персик"} key= dict_keys_to_array(v)`
{% endtab %}
{% endtabs %}

## Как получить список значений из словаря

{% tabs %}
{% tab title="Описание" %}
**dict\_values\_to\_array(data)** - для получения списка значений из словаря data
{% endtab %}

{% tab title="Примеры" %}
Пример:

<figure><img src="https://docs.salebot.pro/~gitbook/image?url=https%3A%2F%2F4216716816-files.gitbook.io%2F%7E%2Ffiles%2Fv0%2Fb%2Fgitbook-x-prod.appspot.com%2Fo%2Fspaces%252F-LxKl4rC_EcwBAz40Qn_%252Fuploads%252FZSgrsbN6yIXHOfW1yOgP%252Fimage.png%3Falt%3Dmedia%26token%3De338ff03-050f-4713-b23f-7e212c85a2e3&#x26;width=768&#x26;dpr=4&#x26;quality=100&#x26;sign=44c62f04&#x26;sv=2" alt=""><figcaption></figcaption></figure>

Ответ:

<figure><img src="https://docs.salebot.pro/~gitbook/image?url=https%3A%2F%2F4216716816-files.gitbook.io%2F%7E%2Ffiles%2Fv0%2Fb%2Fgitbook-x-prod.appspot.com%2Fo%2Fspaces%252F-LxKl4rC_EcwBAz40Qn_%252Fuploads%252F2kS3uawRwriauaG1iVRY%252Fimage.png%3Falt%3Dmedia%26token%3Db1260c0c-ec5e-44b2-903b-feb925cb4890&#x26;width=768&#x26;dpr=4&#x26;quality=100&#x26;sign=af4699b5&#x26;sv=2" alt=""><figcaption></figcaption></figure>
{% endtab %}

{% tab title="Пример кода для копирования" %}
`v={"A1":"апельсин","A2":"абрикос","A3":"мандарин","A4":"яблоко","A5":"груша","A6":"киви","A7":"банан","A8":"персик"} value= dict_values_to_array(v)`
{% endtab %}
{% endtabs %}

### Как получить значения из списка словарей по указанному ключу

{% tabs %}
{% tab title="Описание" %}
**get\_values\_by\_key(data, key)** - позволяет получить значения из списка словарей по указанному ключу. Возвращает список значений.
{% endtab %}

{% tab title="Примеры" %}
Пример: Получим значения из списка словарей по ключу

<figure><img src="https://lh7-rt.googleusercontent.com/docsz/AD_4nXcxagAH-OPoHeCwd0eDdazge8yUmGwl2OtFWIES2htDRf42jezf-1WD9InQBWUqr2AihC-wd7z-7xGeZD4DxypcowYpkZ5S0uNt92KyuwOXLhL-vsua1JYNpjpX2Yje5y6dAbKn?key=ItVw1huKgUDmT8UO8bhwXA" alt=""><figcaption></figcaption></figure>

Ответ:

<figure><img src="https://lh7-rt.googleusercontent.com/docsz/AD_4nXeK9VUAHsy3a50Rp5nZXCwMj2EiGTcUc97PzhCDjlyzBBR9pWYCceFWtninKafDZllEiZZz5p7ZzuhOpX9RhPKuRIBSHAWx1ePajWhGiETgKh5AS9tEm1mmcT6UBZvPIK7zi70e?key=ItVw1huKgUDmT8UO8bhwXA" alt=""><figcaption></figcaption></figure>
{% endtab %}

{% tab title="Пример кода для копирования" %}
```
data = [{"Товар": "Товар№1", "Цена": 1500}, {"Товар": "Товар№2", "Цена": 6000}]
key = "Товар"
result = get_values_by_key(data, key)
```
{% endtab %}
{% endtabs %}

## Как заменить значение в словаре&#x20;

{% tabs %}
{% tab title="Описание" %}
**имя\['ключ'] = значение** - замена значения элемента словаря по заданному ключу. Если указан несуществующий ключ, то произойдет добавление нового элемента словаря
{% endtab %}

{% tab title="Примеры" %}
**Пример:**

Для замены значения конкретного элемента массива пишем обращение к нему _имя\_массива\[индекс] = значение или имя\__&#x441;ловаря\[ключ] = значение

<figure><img src="../../../../.gitbook/assets/image (298).png" alt=""><figcaption></figcaption></figure>

Ответ:&#x20;

<figure><img src="../../../../.gitbook/assets/image (299).png" alt=""><figcaption></figcaption></figure>
{% endtab %}

{% tab title="Пример кода для копирования" %}
```
dicts = {"a": "11", "d": "privet"}

/*Заменить в словаре*/
dicts['d'] = AAAAA

/*Добавить в словарь   dicts['key'] = 'VVVVVVVVVVV'*/
dicts['m']=new

/*Заменить в словаре на число*/
dicts['a'] = int('555')
```


{% endtab %}
{% endtabs %}

## Как добавить значение в словарь

{% tabs %}
{% tab title="Описание" %}
**имя\_**_**словаря\['ключ'] = 'значение'** -_ добавление нового значения в словарь.&#x20;

{% hint style="warning" %}
Если ключ ранее не существовал, то произойдет добавление пары ключ: значение, иначе - замена значения для указанного ключа
{% endhint %}
{% endtab %}

{% tab title="Примеры" %}
Пример:

<figure><img src="../../../../.gitbook/assets/image (300).png" alt=""><figcaption></figcaption></figure>

Результат:

<figure><img src="../../../../.gitbook/assets/image (301).png" alt=""><figcaption></figcaption></figure>
{% endtab %}

{% tab title="Пример кода для копирования" %}
```
/*Добавить в словарь   dicts['key'] = 'VVVVVVVVVVV'*/
dicts['m']=new
```
{% endtab %}
{% endtabs %}

## Как проверить наличие ключа в словаре

{% tabs %}
{% tab title="Описание" %}
**exist\_key(mass, key)** - для проверки наличия ключа в словаре.&#x20;

Параметры:&#x20;

**mass -** словарь&#x20;

**key -** ключ для поиска.&#x20;

Возвращаемое значение True или False, в зависимости найден ключ или нет.
{% endtab %}

{% tab title="Примеры" %}
Пример использования:

<figure><img src="../../../../.gitbook/assets/image (302).png" alt=""><figcaption></figcaption></figure>
{% endtab %}

{% tab title="Пример кода для копирования" %}
```
s = {"1": 123, "2": 234, "q": {"w": "e"}} 
q = if(exist_key(s, 'q'), 'Найдено', 'Еще строка')
```
{% endtab %}
{% endtabs %}

## Как проверить позицию ключа в словаре

{% tabs %}
{% tab title="Описание" %}
**key\_index(mass, key)** - для проверки позиции ключа в словаре.&#x20;

**Параметры:** \
**mass -** словарь  \
**key -** ключ для поиска.&#x20;

{% hint style="info" %}
Позиция в словаре считается с 0. Таким образом первый элемент будет 0, второй элемент будет 1 и так далее.
{% endhint %}
{% endtab %}

{% tab title="Примеры" %}
Пример использования:

<figure><img src="../../../../.gitbook/assets/image (303).png" alt=""><figcaption></figcaption></figure>

_Результат:_

<figure><img src="../../../../.gitbook/assets/image (304).png" alt=""><figcaption></figcaption></figure>
{% endtab %}

{% tab title="Пример кода для копирования" %}
```
s = {"1": 123, "2": 234, "q": {"w": "e"}} 
q = key_index(s, 'q')
```
{% endtab %}
{% endtabs %}

## Как узнать количество элементов в словаре

{% tabs %}
{% tab title="Описание" %}
**arr\_len(mass)** - для определения длины словаря.&#x20;

Параметр:\
**mass -** _словарь_&#x20;

Результат: Возвращает число - длину словаря.

{% hint style="warning" %}
Будьте внимательны при передаче параметра в функцию! Если вызвать функцию без параметров, вернет 0, если в параметрах не массив и не словарь, вернет -1.
{% endhint %}
{% endtab %}

{% tab title="Примеры" %}
Пример использования

<figure><img src="../../../../.gitbook/assets/image (305).png" alt=""><figcaption></figcaption></figure>

Ответ:&#x20;

<figure><img src="../../../../.gitbook/assets/image (306).png" alt=""><figcaption></figcaption></figure>
{% endtab %}

{% tab title="Пример кода для копирования" %}
`/`_`словарь`_`/ радуга = {"каждый":"красный","охотник":"оранжевый","желает":"желтый","знать":"зеленый","где":["бирюзовый","светло-голубой", "темно-голубой"],"сидит":"синий","фазан":"фиолетовый"}`

`dlina=arr_len(радуга)`
{% endtab %}
{% endtabs %}

## Как удалить элемент из словаря

### По индексу или ключу

**del(mass, key)** - для удаления элемента из массива  по индексу или из словаря по ключу. Принимает два параметра: массив/словарь, индекс/ключ, по которому будет удаление. Возвращает измененный словарь или массив, исходную строку не меняет.

Пример со словарем:

<figure><img src="../../../../.gitbook/assets/Снимок экрана 2025-08-29 в 10.31.23.png" alt=""><figcaption></figcaption></figure>

![](<../../../../.gitbook/assets/image (307).png>)

Пример с массивом:&#x20;

<figure><img src="../../../../.gitbook/assets/Снимок экрана 2025-08-29 в 10.38.37.png" alt=""><figcaption></figcaption></figure>

![](<../../../../.gitbook/assets/image (308).png>)

{% hint style="warning" %}
Если в качестве значений массива или словаря используются числа, то для удаления элемента пользуйтесь функцией remove()
{% endhint %}

## Как перевести словарь в человекочитаемый текст

{% tabs %}
{% tab title="Описание" %}
**humanize(dict, delimiter, from\_i, to\_i)**&#x20;

Параметры:

**dict** - имя словаря\
**delimiter** - разделитель между строками\
**from\_i** - индекс элемента, с которого начинать вывод (нумерация с 0)\
**to\_i** - индекс элемента, до которого выводить данные (не включительно)
{% endtab %}

{% tab title="Примеры" %}
Разберем на примере:

<figure><img src="../../../../.gitbook/assets/image (309).png" alt=""><figcaption></figcaption></figure>
{% endtab %}

{% tab title="Пример кода для копирования" %}
```
dict = {"[id146467928|Дмитрий]":"6","[id145255525|Матвей]":"20"}
r = humanize(dict, ': ')
```
{% endtab %}
{% endtabs %}

## Для сортировки  словарей&#x20;

sort() | sort\_by\_value()

{% tabs %}
{% tab title="Описание" %}
<mark style="background-color:blue;">**Сортировка словаря**</mark>

**sort(dict, b)** - сортирует массив по значению, а словарь по ключу

Параметры:

<mark style="color:red;">**!**</mark>**&#x20;dict**- словарь

**b** - направление сортировки (False - по возрастанию (по умолчанию), True - по убыванию)

<mark style="background-color:blue;">**Сортировка словаря по значению**</mark>

**sort\_by\_value(dict, b) -** сортировка словаря по значениям.

Параметры:

<mark style="color:red;">**!**</mark>**&#x20;dict**- словарь

**b** - направление сортировки (False - по возрастанию (по умолчанию), True - по убыванию)
{% endtab %}

{% tab title="Примеры" %}
Пример сортировки массива по убыванию и словаря по возрастанию:

<figure><img src="../../../../.gitbook/assets/image (282).png" alt=""><figcaption></figcaption></figure>

<figure><img src="../../../../.gitbook/assets/image (283).png" alt=""><figcaption><p>Результат сортировки</p></figcaption></figure>

Сортируем словарь по значениям:

<figure><img src="../../../../.gitbook/assets/image (284).png" alt=""><figcaption></figcaption></figure>

<figure><img src="../../../../.gitbook/assets/image (285).png" alt=""><figcaption><p>результат сортировки</p></figcaption></figure>
{% endtab %}
{% endtabs %}

## Перевод словаря в кнопки&#x20;

**tools\_make\_button\_str\_checker() | tools\_check\_user\_input()**

{% tabs %}
{% tab title="Описание" %}
<mark style="background-color:blue;">**Перевод массива/словаря в кнопки**</mark>

**tools\_make\_button\_str\_checker(values\_list, key, in\_line, button\_type)**&#x20;

Параметры:

<mark style="color:red;">**!**</mark>**&#x20;values\_list** - массив строк или словарей, данные которого будут использоваться для получения клавиатуры или нумерованного списка\
**key** - ключ, по которому будет производиться выборка из массива словарей values\_list \
**in\_line** - количество кнопок в строке (по умолчанию равен 1) \
**button\_type** - тип кнопок (по умолчанию reply-клавиатура).  \
Возможные значения: 0 - reply-клавиатура, 1 - inline-клавиатура ( кнопки в тексте)

Результат исполнения функции - словарь вида:

{"**numbered\_list**":"1. Футболки\n2. Шорты\n3. Носки\n4. Кепки\n","**buttons**":\[{"type":"inline","text":"Футболки","line":0,"index\_in\_line":0},{"type":"inline","text":"Шорты","line":0,"index\_in\_line":1},{"type":"inline","text":"Носки","line":1,"index\_in\_line":0},{"type":"inline","text":"Кепки","line":1,"index\_in\_line":1}],"**checker**":"Футболки;1;Шорты;2;Носки;3;Кепки;4;"}

Значения словаря в дальнейшем можно подставлять в поля в конструкторе:

<figure><img src="../../../../.gitbook/assets/image (51) (1).png" alt=""><figcaption></figcaption></figure>

<figure><img src="../../../../.gitbook/assets/image (52) (1).png" alt=""><figcaption></figcaption></figure>

<mark style="background-color:blue;">**Получение значения словаря на основе выбора клиента**</mark>&#x20;

**tools\_check\_user\_input(values\_list, user\_input, key, return\_key)**&#x20;

Параметры:

<mark style="color:red;">**!**</mark>**&#x20;values\_list** - массив строк или словарей, данные которого будут использоваться для получения клавиатуры или нумерованного списка\
<mark style="color:green;">Пример словаря:</mark> \[{"text":"Футболки","price":100},{"text":"Шорты","price":150},{"text":"Носки","price":20},{"text":"Кепки","price":50}]\
<mark style="color:red;">**!**</mark>**&#x20;user\_input** - значение введенное пользователем из числа значений, полученных из  словаря values\_list \
<mark style="color:green;">Пример значения:</mark> Кепки\
**key** - ключ, по которому будет производиться выборка из массива словарей values\_list \
<mark style="color:green;">Пример ключа:</mark> text\
**return\_key** -  возвращаемое  значение для заданного ключа key из словаря values\_list \
<mark style="color:green;">Пример возвращаемого значения:</mark> price
{% endtab %}

{% tab title="Пример" %}
Разберем использование функции на примере реализации корзины товаров:

1.Задаем массив и разбираем его на нумерованный список, кнопки и список возможных значений (для  мессенджеров без кнопок) при помощи функции tools\_make\_button\_str\_checker()

<figure><img src="../../../../.gitbook/assets/image (286).png" alt=""><figcaption><p>Пример использования функции <strong>tools_make_button_str_checker()</strong></p></figcaption></figure>

<figure><img src="../../../../.gitbook/assets/image (287).png" alt=""><figcaption><p>Реузльтат выполнения функции <strong>tools_make_button_str_checker()</strong></p></figcaption></figure>

2.Используем полученные значения buttons, numbered\_list для организации возможности выбора товара:

<figure><img src="../../../../.gitbook/assets/image (288).png" alt=""><figcaption><p>Пример использования функции <strong>tools_make_button_str_checker()</strong></p></figcaption></figure>

3.А список возможных значений checker используем для проверки вводимых клиентом данных:

<figure><img src="../../../../.gitbook/assets/image (289).png" alt=""><figcaption><p>Пример использования функции <strong>tools_make_button_str_checker()</strong></p></figcaption></figure>

4.Осталось вывести клиенту цену выбранного товара. Это удобно сделать при помощи функции tools\_check\_user\_input()

<figure><img src="../../../../.gitbook/assets/image (290).png" alt=""><figcaption><p>Пример использования функции <strong>tools_check_user_input()</strong></p></figcaption></figure>
{% endtab %}

{% tab title="Пример кода для копирования" %}
```
list = [{"text":"Футболки","price":100},{"text":"Шорты","price":150},{"text":"Носки","price":20},{"text":"Кепки","price":50}]
res = tools_make_button_str_checker(list, "text", "2", "1")
numbered_list = res['numbered_list']
buttons = res['buttons']
checker = res['checker']

res_check = tools_check_user_input(list, user_input, 'text', 'price')
```
{% endtab %}
{% endtabs %}
