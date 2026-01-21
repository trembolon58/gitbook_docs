# Для работы с массивами

## Как создать массив

Создание массива - объявление массива

**имя\_массива = \[]**

## Как обнулить массив

Обнуление - это ничто иное как объявление пустого массива

**имя\_массива = \[]**

## Как получить элемент массива&#x20;

{% tabs %}
{% tab title="Описание" %}
**имя\[индекс] -** получение элемента массива по индексу или значению
{% endtab %}

{% tab title="Примеры" %}
Рассмотрим примеры работы с массивами:

**Пример на получение элемента массива по его индексу**

<figure><img src="../../../../.gitbook/assets/image (250).png" alt=""><figcaption></figcaption></figure>

Ответ:&#x20;

<figure><img src="../../../../.gitbook/assets/image (251).png" alt=""><figcaption></figcaption></figure>

итак, в сообщении будет выведено:![](<../../../../.gitbook/assets/image (252).png>)&#x20;

#### **Пример на получение последнего элемента массива**

<figure><img src="../../../../.gitbook/assets/image (253).png" alt=""><figcaption></figcaption></figure>

Ответ: ![](<../../../../.gitbook/assets/image (254).png>)


{% endtab %}

{% tab title="Пример кода для копирования" %}
```
/*получение по индексу*/
arrayI = [1, "2", 3, 4, 5]
k=arrayI[3]
/*получение по индексу из вложенного*/
arrayV = [[1, "2", 4, 5], "2", 3, 4, 5]
v=arrayV[0][1]

/*пример на получение последнего значения*/
array = [1, "2", 3, 4, 5]
/*Взятие последнего элемента массива*/
last = array[-1]
```
{% endtab %}
{% endtabs %}

## Как заменить значение в массиве

{% tabs %}
{% tab title="Описание" %}
**имя\[индекс] =** **значение** - замена значения элемента массива по заданному индексу
{% endtab %}

{% tab title="Примеры" %}
**Пример:**

Для замены значения конкретного элемента массива пишем обращение к нему _имя\_массива\[индекс] = значение_&#x20;

<figure><img src="../../../../.gitbook/assets/image (255).png" alt=""><figcaption></figcaption></figure>

Ответ:&#x20;

<figure><img src="../../../../.gitbook/assets/image (256).png" alt=""><figcaption></figcaption></figure>
{% endtab %}

{% tab title="Пример кода для копирования" %}
```
array = [1, "2", 3, 4, 5]

/*Заменить в массиве\словаре*/
array[2] = 888

/*Добавить в словарь   dicts['key'] = 'VVVVVVVVVVV'*/
dicts['m']=new

/*Заменить в массиве\словаре на число*/
array[3] = int('888')
dicts['a'] = int('555')
```


{% endtab %}
{% endtabs %}

## Как проверить наличие элемента в массиве

{% tabs %}
{% tab title="Описание" %}
**in\_array(mass, value)** - для проверки наличия элемента в массиве.&#x20;

**Параметры:** \
<mark style="color:red;">!</mark> **mass -** массив \
<mark style="color:red;">!</mark> **value -** значение для поиска.

Возвращаемое значение True или False, в зависимости найдено значение или нет.
{% endtab %}

{% tab title="Примеры" %}
Пример:

<figure><img src="../../../../.gitbook/assets/image (257).png" alt=""><figcaption></figcaption></figure>

Ответ:&#x20;

<figure><img src="../../../../.gitbook/assets/image (258).png" alt=""><figcaption></figcaption></figure>
{% endtab %}

{% tab title="Пример кода для копирования" %}
```
s = ["Вася", "Петя", "Лена"] 
q = if(in_array(s, 'Аня'), 'Найдено', 'Еще строка')
```
{% endtab %}
{% endtabs %}

## Как узнать длину массива&#x20;

{% tabs %}
{% tab title="Описание" %}
**arr\_len(mass)** - для определения длины массива.&#x20;

Параметр:\
<mark style="color:red;">!</mark> **mass -**  _массив_&#x20;

Результат: Возвращает число - длину массива.

{% hint style="warning" %}
Будьте внимательны при передаче параметра в функцию! Если вызвать функцию без параметров, вернет 0, если в параметрах не массив и не словарь, вернет -1.
{% endhint %}
{% endtab %}

{% tab title="Примеры" %}
Пример использования

<figure><img src="../../../../.gitbook/assets/image (259).png" alt=""><figcaption></figcaption></figure>

Результат:

<figure><img src="../../../../.gitbook/assets/image (260).png" alt=""><figcaption></figcaption></figure>
{% endtab %}

{% tab title="Пример кода для копирования" %}
```
s = ["Вася", "Петя", "Лена"] 
q = if(arr_len(s) > 5, 'Группа укомплектована', 'Присоединяйтесь в наши ряды!')
```
{% endtab %}
{% endtabs %}

## Как вставить элемент в конец массива

{% tabs %}
{% tab title="Описание" %}
**append(mass, element, priznak)** - для вставки элемента в конец массива.&#x20;

Параметры:

<mark style="color:red;">!</mark> **mass -** массив\
<mark style="color:red;">!</mark> **element -** вставляемый элемент\
**priznak** - признак добавления массива или словаря

Возвращает массив, в который добавлено значение в конец. Т.е. для добавление в этот же массив прописываем команду ввиде **mass = append(mass, element, priznak)**&#x20;

{% hint style="warning" %}
Данные по умолчанию вставляются как строки, **если вам надо вставить массив или словарь, передайте дополнительный парамтер True**. Он означает, что вы вставляете JSON.
{% endhint %}
{% endtab %}

{% tab title="Примеры" %}
Пример использования:



<figure><img src="../../../../.gitbook/assets/image (261).png" alt=""><figcaption></figcaption></figure>

<figure><img src="../../../../.gitbook/assets/image (262).png" alt=""><figcaption></figcaption></figure>

Пример добавления в массив и удаления из него:

<figure><img src="../../../../.gitbook/assets/image (263).png" alt=""><figcaption><p>В данном примере происходит добавление элемента массива project.vibpzdr и удаление из массива project.pzdr значения p</p></figcaption></figure>

Пример создания массива с массивами внутри:

<figure><img src="../../../../.gitbook/assets/image (264).png" alt=""><figcaption></figcaption></figure>

Результат выполнения функции:

<figure><img src="../../../../.gitbook/assets/image (265).png" alt=""><figcaption></figcaption></figure>
{% endtab %}

{% tab title="Пример кода для копирования" %}
```
s = ["Вася", "Петя", "Лена"]
q = append(s, 'Никита')
```
{% endtab %}
{% endtabs %}

## Как вставить значение в определенную позицию массива

{% tabs %}
{% tab title="Описание" %}
**insert(mass, index, value, priznak)** - для вставки элемента в определенную позицию массива.&#x20;

Параметры: \
<mark style="color:red;">!</mark> **mass -** массив\
<mark style="color:red;">!</mark> **index -** позиция для вставки \
<mark style="color:red;">!</mark> **value -** значение\
**priznak** - признак добавления массива или словаря

Результат:\
Возвращает массив, в который добавлено значение в указанную позицию. Т.е. для добавление в этот же массив прописываем команду ввиде **mass = insert(mass, index, value, priznak)**&#x20;

{% hint style="warning" %}
Данные по умолчанию вставляются как строки, **если вам надо вставить массив или словарь, передайте дополнительный параметр True**. Он означает, что вы вставляете JSON.
{% endhint %}
{% endtab %}

{% tab title="Примеры" %}
Пример:

<figure><img src="../../../../.gitbook/assets/image (266).png" alt=""><figcaption></figcaption></figure>

Результат:

<figure><img src="../../../../.gitbook/assets/image (267).png" alt=""><figcaption></figcaption></figure>

Разберем более сложный пример - добавление словаря t в массив s:

<figure><img src="../../../../.gitbook/assets/image (268).png" alt=""><figcaption></figcaption></figure>

В функции мы указали, что хотим добавить словарь на позицию 1. Смотрим результат:

<figure><img src="../../../../.gitbook/assets/image (269).png" alt=""><figcaption></figcaption></figure>
{% endtab %}

{% tab title="Пример кода для копирования" %}
```
s = ["Вася", "Петя", "Лена"]
q = insert(s, 1, 'Никита')
```
{% endtab %}
{% endtabs %}

## Как удалить элемент из массива

del() | del | remove()

{% tabs %}
{% tab title="Описание" %}
### <mark style="background-color:blue;">**По индексу**</mark>

**del(mass, key)** - для удаления элемента из массива  по индексу.&#x20;

Параметры: \
<mark style="color:red;">!</mark> **mass -** имя массива;\
<mark style="color:red;">!</mark> **key -** индекс значения, которое надо удалить.

Возвращает измененный массив, исходную строку не меняет. \
Т.е. для удаления и изменения этого же массива прописываем команду ввиде \
**mass = del(mass, key)**

{% hint style="warning" %}
Если в качестве значений массива используются числа, то для удаления элемента пользуйтесь функцией remove()
{% endhint %}

**del имя\['индекс']** - удаление значения из массива по индексу

Параметры: \
<mark style="color:red;">!</mark> **имя-** имя массива;\
<mark style="color:red;">!</mark> **индекс-** индекс значения, которое надо удалить.&#x20;

### <mark style="background-color:blue;">По значению</mark>

**remove(mass, value)** - для удаления значения _из массива_.&#x20;

Параметры: \
<mark style="color:red;">!</mark> **mass -** имя массива; \
<mark style="color:red;">!</mark> **value -** значение, которое необходимо удалить из массива.&#x20;

Результат:\
Возвращает измененный массив, исходную строку не меняет. Т.е. для удаления и изменения этого же массива прописываем команду ввиде \
**mass = remove(mass, key)**
{% endtab %}

{% tab title="Примеры" %}
Пример удаления по индексу элемента:

<figure><img src="../../../../.gitbook/assets/image (270).png" alt=""><figcaption></figcaption></figure>

Пример удаления элемента массива по его значению:

<figure><img src="../../../../.gitbook/assets/image (271).png" alt=""><figcaption></figcaption></figure>
{% endtab %}

{% tab title="Пример кода для копирования" %}
```
/*уаление элемента массива по его индексу*/
array = ["1",2, 3, "4"]
del array['1']

array1 = ["1",2, 3, "4"]
array1=del(array1,0)


/*удаление элемента по его значению*/
array = ["1",2, 3, "4"]
array=remove(array, '4') 

array1 = ["1",2, 3, "4"]
array1=remove(array1, 2) 
```
{% endtab %}
{% endtabs %}

## Как узнать позицию элемента в массиве

{% tabs %}
{% tab title="Описание" %}
**index(mass, value)**

Параметры: \
<mark style="color:red;">**!**</mark> **mass -** имя массива \
<mark style="color:red;">**!**</mark>**&#x20;value -** значение, позицию которого надо определить.&#x20;

Если элемента нет в массиве, то функция вернет -1.
{% endtab %}

{% tab title="Примеры" %}
Пример определения позиции элемента в массиве:

<figure><img src="../../../../.gitbook/assets/image (272).png" alt=""><figcaption></figcaption></figure>

Рассмотрим подробно результат:

<figure><img src="../../../../.gitbook/assets/image (273).png" alt=""><figcaption></figcaption></figure>

Как видим, поскольку цифры 5 в массиве нет, функция вернула нам значение -1.
{% endtab %}

{% tab title="Пример для копирования" %}
```
array = ["1",2, 3, "4"]
poisk1=index(array,"1")
poisk2=index(array,5)
```
{% endtab %}
{% endtabs %}

## Как перевести массив в человекочитаемый текст

{% tabs %}
{% tab title="Описание" %}
**massive\_to\_text(massive, header, numbered,delimiter1,delimiter2)**

Параметры:

<mark style="color:red;">**!**</mark>**&#x20;massive** – массив, который нужно вывести, \
**header** – заголовок, который появится в начале текста,\
**numbered** – при передаче любого значения элементы массива будут пронумерованы,\
**delimiter1** – символ, который проставляется в конце строки с элементом (по умолчанию знак ‘;’),\
**delimiter2** – символ, используемый после номера элемента, при использовании нумерации (по умолчанию знак ‘)’)
{% endtab %}

{% tab title="Примеры" %}
Простой пример:

![](https://lh3.googleusercontent.com/m90ZHz4QPCzKBLsfLkPMFk40cbnKmIbdpuVPvwsyGaQ-cVkb_CwbMIY8ZIXFGfTuEevIh0bpTLZL2Ggi4EBRJPbz_U6IxK8MZdneHu8N6dRQmf2xvX5XqiPbBXWo2BbQD5X0UpnxzXkt1-cyzoA)

В резултате массив будет выведен в виде нумерованного списка:

![](https://lh4.googleusercontent.com/kF0Gl_QbkRB5xIdWpmJMEh3JZ_u2lWn9xVWYVVdjONRFBaMyE_MnAYDPYcvp6tEpmQnCwBK16CrBg9q3W2A9OjiKkbK1rCVFlcETKwtDjTCNO4G3o8aO3xtidMWWld2xKkQyoQZtzNkO70ESi3o)


{% endtab %}

{% tab title="Пример кода для копирования" %}
```
Massive1 = [1, 2, 3, "a", "b", "c"] 
text = massive_to_text(Massive1, 'заголовок', 1) 
```
{% endtab %}
{% endtabs %}

## Как исключить один массив из другого

{% tabs %}
{% tab title="Описание" %}
**except\_arr(mas1, mas2)**&#x20;

Параметры:

<mark style="color:red;">**!**</mark>**&#x20;mas1** - массив, из которого будем исключать, \
<mark style="color:red;">**!**</mark>**&#x20;mas2** - массив, элементы которого будем исключать
{% endtab %}

{% tab title="Примеры" %}
Разберем на примере:

<figure><img src="../../../../.gitbook/assets/image (274).png" alt=""><figcaption></figcaption></figure>
{% endtab %}

{% tab title="Пример кода для копирования" %}
```
s1 = [1, 2, 3]
s2 = [2, 3]
s3 = except_arr(s1, s2)
```
{% endtab %}
{% endtabs %}

## Как выбрать пересечение массивов

{% tabs %}
{% tab title="Описание" %}
**cross\_arr(mas1, mas2)**

Параметры:

<mark style="color:red;">**!**</mark>**&#x20;mas1** - массив, в котором ищем, \
<mark style="color:red;">**!**</mark>**&#x20;mas2** - массив, элементы которого будем искать
{% endtab %}

{% tab title="Примеры" %}
<figure><img src="../../../../.gitbook/assets/image (275).png" alt=""><figcaption></figcaption></figure>
{% endtab %}

{% tab title="Пример кода для копирования" %}
```
s1 = [1, 2, 3]
s2 = [2, 3]
s3 = cross_arr(s1, s2)

mas1 = ["не", "ожидал,", "что", "всё", "так", "просто.", "спасибо"]
mas2 = ["все", "спасибо"]
mas3 = cross_arr(mas1, mas2)
```
{% endtab %}
{% endtabs %}

## Как объединить массивы

{% tabs %}
{% tab title="Описание" %}
Специальной функции для объединения массивов нет, но все достаточно просто решается:

Для объединения массивов выполните операцию конкатенации строк, далее выполните замену ']\[' на запятую - ','
{% endtab %}

{% tab title="Примеры" %}
<figure><img src="../../../../.gitbook/assets/image (276).png" alt=""><figcaption></figcaption></figure>
{% endtab %}

{% tab title="Пример кода для копирования" %}
```
a = [1,2,3,4] 
b = [5,6,7] 
sum = a + b 
answer = replace(sum, '][', ',') 
```
{% endtab %}
{% endtabs %}

## Как просуммировать элементы массива

{% tabs %}
{% tab title="Описание" %}
**sum\_array(array)**

**Параметры:**

**array** - массив, элементы которого необходимо просуммировать

{% hint style="warning" %}
<mark style="color:red;">**Внимание!**</mark>**&#x20;Функция работает с массивами определенного вида.**&#x20;

Принимаемый вид - \[1,2,3,4] или ‘\[1,2,3,4]’. \
Если внутри массива есть число, представленное в виде строки, оно должно быть заключено в двойные кавычки - например, \[1,2,3,”-4”].  \
Если среди значений массива есть строки с буквенными значениями, вычисления произведены не будут.

Пример неправильного использования:\
mas = \[1,2,3,"a"] \
result = sum\_array(mas)

В результате будет возвращена ошибка: **array has unsupported elements**
{% endhint %}

<figure><img src="../../../../.gitbook/assets/image (277).png" alt=""><figcaption><p>Пример ошибки при использовании массива с символами, а не числами</p></figcaption></figure>
{% endtab %}

{% tab title="Примеры" %}
<figure><img src="../../../../.gitbook/assets/image (278).png" alt=""><figcaption></figcaption></figure>

Результат:

<figure><img src="../../../../.gitbook/assets/image (279).png" alt=""><figcaption></figcaption></figure>
{% endtab %}

{% tab title="Пример кода для копирования" %}
```
mas = [1,2,3,4] 
result = sum_array(mas) 
```
{% endtab %}
{% endtabs %}

## Как перемешать элементы массива

{% tabs %}
{% tab title="Описание" %}
**shuffle\_massive(massive**

Параметры:

**massive** - это массив, элементы которого нужно перемешать.
{% endtab %}

{% tab title="Примеры" %}
<figure><img src="../../../../.gitbook/assets/image (280).png" alt=""><figcaption></figcaption></figure>

Результаты выполнения функции:

<figure><img src="../../../../.gitbook/assets/image (281).png" alt=""><figcaption></figcaption></figure>


{% endtab %}

{% tab title="Пример кода для копирования" %}
```
Massive1 = [1, 2, 3, "a", "b", "c"]
Massive2 = shuffle_massive(Massive1) 
```
{% endtab %}
{% endtabs %}

## Для сортировки массивов и словарей&#x20;

{% tabs %}
{% tab title="Описание" %}
<mark style="background-color:blue;">**Сортировка массива или словаря**</mark>

**sort(mass, b)** - сортирует массив по значению, а словарь по ключу

Параметры:

<mark style="color:red;">**!**</mark>**&#x20;mass** - массив/словарь

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

{% tab title="Пример кода для копирования" %}

{% endtab %}

{% tab title="Видеоразбор" %}

{% endtab %}
{% endtabs %}

## Перевод массива/словаря в кнопки&#x20;

**tools\_make\_button\_str\_checker() | tools\_check\_user\_input()**

{% tabs %}
{% tab title="Описание" %}
<mark style="background-color:blue;">**Перевод массива/словаря в кнопки**</mark>

tools\_make\_button\_str\_checker(values\_list, key, in\_line, button\_type, checker\_with\_numbers)

Параметры:

<mark style="color:red;">**!**</mark> values\_list - массив строк или словарей, данные которого будут использоваться для получения клавиатуры или нумерованного списка&#x20;

key - ключ, по которому будет производиться выборка из массива словарей&#x20;

in\_line - количество кнопок в строке (по умолчанию равен 1)&#x20;

button\_type - тип кнопок (по умолчанию reply-клавиатура). \
Возможные значения: \
0 - reply-клавиатура, \
1 - inline-клавиатура ( кнопки в тексте)&#x20;

checker\_with\_numbers - добавлять ли номера кнопок в массив "сhecker" . \
Возможные значения: \
0 - не добавлять номера, \
1 - добавлять номера. (По умолчанию: 1 - добавлять номера)

Результат исполнения функции - словарь вида:

{"**numbered\_list**":"1. Футболки\n2. Шорты\n3. Носки\n4. Кепки\n","**buttons**":\[{"type":"inline","text":"Футболки","line":0,"index\_in\_line":0},{"type":"inline","text":"Шорты","line":0,"index\_in\_line":1},{"type":"inline","text":"Носки","line":1,"index\_in\_line":0},{"type":"inline","text":"Кепки","line":1,"index\_in\_line":1}],"**checker**":"Футболки;1;Шорты;2;Носки;3;Кепки;4;"}

Значения словаря в дальнейшем можно подставлять в поля в конструкторе:

<figure><img src="../../../../.gitbook/assets/image (51) (2).png" alt=""><figcaption></figcaption></figure>

<figure><img src="../../../../.gitbook/assets/image (52) (2).png" alt=""><figcaption></figcaption></figure>



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

## Выборка данных из массива



{% tabs %}
{% tab title="Описание" %}
**array\_slice(array, start\_index, end\_index)**&#x20;

Параметры:

<mark style="color:red;">**!**</mark>**&#x20;array** - массив \
<mark style="color:red;">**!**</mark>**&#x20;start\_index** - начало среза \
**end\_index** - конец среза (по умолчанию до конца)
{% endtab %}

{% tab title="Пример" %}
Давайте выберем из массива подмассив, начиная с 1го элемента:&#x20;

<figure><img src="../../../../.gitbook/assets/image (291).png" alt=""><figcaption><p>Пример использования  array_slice()</p></figcaption></figure>

в res будет \["Шорты", "Носки", "Кепки"]&#x20;

Еще один пример выборки подмассива, начиная с 0 до 2го элемента массива:

<figure><img src="../../../../.gitbook/assets/image (292).png" alt=""><figcaption><p>Пример использования  array_slice()</p></figcaption></figure>

в res будет \["Футболки", "Шорты"]
{% endtab %}

{% tab title="Пример кода для копирования" %}
```
list = ["Футболки", "Шорты", "Носки", "Кепки"] 
res = array_slice(list, 1)

res = array_slice(list, 0, 2)
```
{% endtab %}
{% endtabs %}

## Распаковка элементов массива

{% tabs %}
{% tab title="Функция" %}
unpack\_list(array, var\_name) - этот метод перебирает массив и создает для каждого элемента в массиве отдельную переменную с названием var1, var2, var3 и т.д.

<mark style="color:red;">**!**</mark> array - обязательный параметр, массив элементов

var\_name - необязательный параметр, строка. Если передан, используется для имен распакованных элементов. Примеры:

Если передан var\_name, то названия для переменных формируются с использованием var\_name

var\_name должен соответствовать правилам наименования переменных.
{% endtab %}

{% tab title="Пример" %}
**Пример 1:**

`array1 = ["one", "two", "three"]`

`ans1 = unpack_list(array1)`

**Результат** - созданы переменные сделки:

`var1 = 'one'`

`var2 = 'two'`

`var3 = 'three'`

**Пример 2:**

`array2 = ["one", "two", "three"]`

`var_name = 'custom'`

`ans2 = unpack_list(array2, var_name)`

**Результат -** созданы переменные сделки:

`custom1 = 'one'`

`custom2 = 'two'`

`custom3 = 'three'`
{% endtab %}
{% endtabs %}

## Как вернуть список без повторяющихся элементов

{% tabs %}
{% tab title="Функция" %}
remove\_duplicates(array) - возвращает список без повторяющихся элементов.

<mark style="color:red;">**!**</mark> array - обязательный параметр. Исходный список элементов с дубликатами
{% endtab %}

{% tab title="Пример" %}
Пример:

arr = \[1, 2, 5, 1, 5, 3]

new\_arr = remove\_duplicates(arr)

Результат - в переменную new\_arr запишется список: \[1, 2, 5, 3]
{% endtab %}
{% endtabs %}
