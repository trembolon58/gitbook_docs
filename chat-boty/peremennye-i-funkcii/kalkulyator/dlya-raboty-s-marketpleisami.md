# Для работы с маркетплейсами

### OZON

### Как собрать отзывы о товаре с OZON

Функция **ozon\_goods\_feedbacks(goods\_id, name)** позволяет собрать последние 20 отзывов с карточки товара маркетплейса ozon по артикулу товара \
**goods\_id** - обязательный параметр, артикул товара \
**name** - необязательный параметр, позволяет искать по имени пользователя, указанный при регистрации на маркетплейсе.

#### **Пример:**&#x20;

Рассмотрим внимательно ссылку на товар:

https://www.ozon.ru/product/jacobs-monarch-kofe-v-zernah-800-g-<mark style="color:orange;">138218835</mark>/, \
последние цифры это необходимый нам артикул.

name = "Виктор" \
oz = ozon\_goods\_feedbacks(138218835, name)

<figure><img src="../../../.gitbook/assets/image (238).png" alt=""><figcaption></figcaption></figure>

В результате выполнения функции придет ответ в виде массива со словарями: \[{"author":"Юлия Л.","comment":"","positive":"","negative":"","videos":\[],"photos":\[],"score":4},{"author":"Лилия К.","comment":"","positive":"","negative":"","videos":\[],"photos":\[],"score":5},{"author":"Кричевская Елена","comment":"мой любимый кофе. ","positive":"","negative":"","videos":\[],"photos":\[],"score":5},{"author":"Пользователь предпочёл скрыть свои данные","comment":"","positive":"","negative":"","videos":\[],"photos":\[],"score":5},{"author":"Ульяна Ш.","comment":"","positive":"","negative":"","videos":\[],"photos":\[],"score":5}]

## Wildberries

### Собрать  отзывы Wildberries

Функция **wildberries\_goods\_feedbacks(wildberries\_api\_key, is\_answered, nm\_id, take, skip, date\_from, date\_to, full\_data)** позволяет собрать последние  отзывы с карточки отзывов товара маркетплейса Wildberries по артикулу

<mark style="color:orange;">**Обязательные параметры функции:**</mark>

**wildberries\_api\_key** - обязательный, API ключ с Wildberries

<mark style="color:green;">**Дополнительные необязательные параметры:**</mark>

**isAnswered** - Обработанные отзывы (True) или необработанные отзывы(False)

**nm\_id** - Артикул товара Wildberries можно получить из ссылки на товар или скопировать в кабинете WB<br>

<figure><img src="../../../.gitbook/assets/image (239).png" alt=""><figcaption></figcaption></figure>

**take** - Количество отзывов (max. 5 000), по умолчанию 20

**skip** - Количество отзывов для пропуска (max. 199990), по умолчанию 0

**date\_from** - Дата начала периода в формате дд.мм.гггг (пример: 22.10.2022)

**date\_to** - Дата конца периода в формате дд.мм.гггг (пример: 23.10.2022)

**full\_data** - вернуть полный ответ от Wildberries. Чтобы получить полный ответ от Wildberries передайте значение для данного параметра 1

<mark style="color:blue;">**Пример 1:**</mark>&#x20;

Чтобы получить последние 20 неотвеченных отзывов достаточно в функции передать только обязательный параметр **wildberries\_api\_key**

Пример для копирования:&#x20;

```
request_WB1 = wildberries_goods_feedbacks('wildberries_api_key')
```

<mark style="color:blue;">**Пример 2:**</mark>

Получить отвеченные отзывы за 25 мая 2023 года:&#x20;

```
wildberries_api_key = "h***************************************kl"
/*замените значение wildberries_api_key на апи ключ из WB*/
request_WB = wildberries_goods_feedbacks(wildberries_api_key, True, nm_id, 20, 0, '25.05.2022', '26.05.2022')
```

В результате выполнения функции в переменную (название переменной -на ваше усмотрение, кроме встроенных и служебных переменных)  будет записан массив со словарями ответ похожий на этот:&#x20;

`request_WB = [{"id":"1h-2RikBC75Dkq7NjfNN","nmId": 123456,"author":"Татьяна","content":"Отличный товар"},{"id":"wTy2RokBXuXi8PE1d4kE","nmId": 123456,"author":"Вася","content":"Хороший товар"}, {"id":"s5W0RokBl47N78Z1D758","nmId": 123456, "author":"Мира","content":"Все ок."}]`



После этого можно <mark style="color:green;">**получить идентификатор отзыва**</mark> из значения переменной.

Для примера получим значение feedback\_id первого отзыва.  В Калькуляторе блока укажите:&#x20;

<pre><code><strong>/* сохраним идентикатор отзыва,который указан первым в массиве request_WB*/
</strong><strong>feedback_id = request_WB['0']['id']
</strong></code></pre>

Подробнее как получать значение элементов из массива  описано в этой статье:

{% embed url="https://docs.salebot.pro/peremennye-1/rabota-s-massivami-i-slovaryami/rabota-s-massivami#kak-poluchit-element-massiva" %}

Получение значение из словаря здесь:

{% embed url="https://docs.salebot.pro/peremennye-1/rabota-s-massivami-i-slovaryami/rabota-so-slovaryami#kak-poluchit-znachenie-slovarya-po-klyuchu" %}

#### **Пример настройки схемы:**&#x20;

Пользователь запускает бота, в ответ на сообщение бота присылает номер артикула, например <mark style="color:orange;">68952198.</mark>

В примере с помощью стрелки со сбором данных сохраняем значение в переменную nm\_id и в следующем блоке указываем следующий запрос:

```
wildberries_api_key = "h***************************************kl"
/*замените значение wildberries_api_key на апи ключ из WB*/
request_WB = wildberries_goods_feedbacks(wildberries_api_key, True, nm_id, 20, 0, '25.05.2022', '26.05.2022')
```

<figure><img src="../../../.gitbook/assets/image (240).png" alt=""><figcaption></figcaption></figure>

### Отправить ответ на отзыв Wildberries

С помощью функции **wildberries\_answer\_to\_feedback(wildberries\_api\_key, feedback\_id, text)** можно отправить ответ на отзыв Wildberries.

Для функции **wildberries\_answer\_to\_feedback(wildberries\_api\_key, feedback\_id, text)&#x20;**<mark style="color:orange;">**ВСЕ параметры**</mark> являются <mark style="color:orange;">**обязательными**</mark>:

**wildberries\_api\_key** - обязательный, API ключ с Wildberries

**feedback\_id** - идентификатор отзыва можно получить из массива словарей, полученного при выполнении функции [**wildberries\_goods\_feedbacks()** ](dlya-raboty-s-marketpleisami.md#sobrat-otzyvy-wildberries)

**text** - текст ответа на отзыв

### Список вопросов

&#x20;С помощью функции можно получить список вопросов по заданным параметрам с пагинацией и сортировкой.\
За один запрос можно получить 10 000 вопросов, максимум.

#### Функция wildberries\_questions(api\_key, is\_answered, take, skip, order, date\_from, date\_to, nm\_id)

&#x20;Параметры функции:

<mark style="color:orange;">**pi\_key**</mark> - обязательный параметр, API ключ с Wildberries

&#x20;**is\_answered** — true (Отвеченные вопросы) или  false (неотвеченные вопросы)

**take** - Количество запрашиваемых вопросов, при этом максимально допустимое значение для параметра - 10 000, а сумма значений параметров take и skip не должна превышать 10 000)

**skip** - Количество вопросов для пропуска, при этом максимально допустимое значение для параметра - 10 000, а сумма значений параметров take и skip не должна превышать 10 000)

**order** - Сортировка вопросов по дате, значение параметра может быть либо dateAsc (по возрастанию), либо dateDesc (по убыванию)

**date\_from** - Дата начала периода

**date\_to** - Дата конца периода

&#x20;**nm\_id** — артикул Wildberries

### &#x20;Работа с вопросами

&#x20;**Просмотреть вопрос**: функция **wildberries\_question\_mark\_viewed(api\_key, id, was\_viewed)**

&#x20;Параметры:

&#x20;<mark style="color:orange;">**api\_key**</mark> - обязательный, API ключ с Wildberries

&#x20;**id** — обязательный, id вопроса

&#x20;**was\_viewed** — может иметь следующие значения: true (просмотрен), false (не просмотрен)

**Отклонить вопрос**: функция wildberries\_answer\_question(api\_key, id, text, state)

&#x20;Параметры:

&#x20;api\_key - обязательный, API ключ с Wildberries

&#x20;id — обязательный, id вопроса

&#x20;text — обязательный, текст ответа

&#x20;state — чтобы отклонить вопрос, значение параметра должно быть "none"

**Ответить на вопрос или отредактировать ответ:** функция wildberries\_answer\_question(api\_key, id, text, state)

{% hint style="success" %}
Отредактировать ответ на вопрос можно в течение 2 месяцев (60 дней), после предоставления ответа и только 1 раз.
{% endhint %}

Параметры:

**api\_key** - обязательный, API ключ с Wildberries

**id** — обязательный, id вопроса

**text** — обязательный, текст ответа

**state** — чтобы ответить на вопрос или отредактировать ответ, значение параметра должно быть "wbRu"
