# Настройка Карусели товаров и рекламы Вконтакте

## Как создать Карусель ВКонтакте

**Карусель Вконтакте** - это создание поста или рекламы с фотографиями или видеозаписями, которые пользователь может пролистывать в поисках необходимого продукта, для рекламы и продажи Вашего товара или услуги.&#x20;

{% hint style="warning" %}
В карточках могут использоваться фотографии с соотношением сторон ТОЛЬКО 13:8 (Например, 1300 на 800 пикселей). Если взять другие фото, сообщение от бота НЕ придет

Требования:

•Пропорции изображения: 13/8;

•Минимальный размер: 221х136;

•Заголовок, максимум 80 символов;

•Подзаголовок, максимум 80 символов;

•Один элемент карусели может содержать не больше 3-х кнопок
{% endhint %}

Рассмотрим на примере карусели из 3 карточек. Для создания карточек вам нужно в поле "Калькулятор" написать следующее:

p = \[{"title":"заголовок", "description": "ОПИСАНИЕ КАРТОЧКИ 1", "image": "ССЫЛКА НА КАРТИНКУ 1", "buttons":\[{"text":"ТЕКСТ КНОПКИ 1"}]},{"title":"заголовок", "description": "ОПИСАНИЕ КАРТОЧКИ 2", "image": "ССЫЛКА НА КАРТИНКУ 2", "buttons":\[{"text":"ТЕКСТ КНОПКИ 2"}]}, {"title":"заголовок", "description": "ОПИСАНИЕ КАРТОЧКИ 3", "image": "ССЫЛКА НА КАРТИНКУ 3", "buttons":\[{"text":"ТЕКСТ КНОПКИ 3"}]}]\
r = send\_carousel(p, 'ТЕКСТ ПЕРЕД КАРУСЕЛЬЮ')

То есть сначала записываем массив с title, description, image, buttons в переменную **p** (вы можете назвать переменную иначе), а далее используем ее в методе **send\_carousel**(p, 'ТЕКСТ ПЕРЕД КАРУСЕЛЬЮ')

Вы можете воспользоваться табличкой и просто вставить нужные значения заголовков, ссылок и тд, а потом просто скопировать в ваш блок

<figure><img src="https://lh7-rt.googleusercontent.com/docsz/AD_4nXf3Q4SKIrkBWN2J0jlwNW8ucF7LEIxDcDqVz-FCKjQKJe6MByk2-HgAhSSNBUp3QeNIWKiX6WmTKLujF37vV-Mvg46j5akWdVI70oilcqVlD6unkIQNzQM-hL1iP9IHUNhNljRTVw?key=jpoKmlVz5BjGtxmgtNRTdw" alt=""><figcaption></figcaption></figure>

В поле "Сообщение" оставляем #{none}

<figure><img src="https://lh7-rt.googleusercontent.com/docsz/AD_4nXf0psI1-icTYYVjzh9ZdnCbSwrGXaMSIFEvIhm7wbIIe3BJSb-IBvC7jc6val-JvY3KfW0ZQ_MoSFWXZCtHVyigDdaYn0OA4dAug3YmR_gig-d944vVnAJohvO-XcpXvscfi5Pc5g?key=jpoKmlVz5BjGtxmgtNRTdw" alt=""><figcaption><p>Карусель во ВКонтакте</p></figcaption></figure>

{% hint style="info" %}
В кнопки карточек карусели вы можете вставлять ссылки, тогда при нажатии на кнопку пользователь перейдет по ссылке
{% endhint %}

Чтобы вставить ссылку в кнопку на карточке, запишите в массив так (на примере одной карточки)

p = \[{"title":"заголовок", "description": "ОПИСАНИЕ КАРТОЧКИ 1", "image": "ССЫЛКА НА КАРТИНКУ 1", "buttons":\[{"text":"ТЕКСТ КНОПКИ 1", "url":"ССЫЛКА ДЛЯ КНОПКИ" }]}]

<figure><img src="https://lh7-rt.googleusercontent.com/docsz/AD_4nXc5Uzue5MxwnkxANXadQKjU9NZujKwUaJk5LzPb1k89gV9aJBFoMGLmmDlXzpIRLj7KhxefvFAwxX6D-qKtz_gHtx0-wGxPO4p6_Um2BbWCXARCyOug5Qgy66M5z4RxLFDwrZWuEA?key=jpoKmlVz5BjGtxmgtNRTdw" alt=""><figcaption><p>Пример настройки карусели для ВКонтакте</p></figcaption></figure>

## Обработка откликов на товары Вконтакте

Магазин ВКонтакте — бесплатный инструмент, который помогает превратить сообщество в полноценный интернет-магазин и продавать товары и услуги.

Настроить Магазин можно довольно просто: Управление → Настройки → Разделы → Товары. После этого вам нужно выбрать режим работы — базовый или расширенный. Подробнее Вы можете ознакомиться [тут](https://vk.com/@business-magazin-2-0-step-by-step)

После настройки карточек товаров клиенты смогут написать Вам (откликнуться):

<figure><img src="https://lh7-rt.googleusercontent.com/docsz/AD_4nXd_hxQcSgf4ljrGDVO_1oQhpWp26MZ7uIZaVtUNAvc04mTGPRv_dJJq4D1AmbsGkgRyMj8FRXSKscIOl_Y-kbISeLr9PmXnLKzj3chJWwT-6xTbc42e2X4BkyBlcCnGhqG3mXO-Fg?key=jpoKmlVz5BjGtxmgtNRTdw" alt=""><figcaption><p>Добавление карточки товара</p></figcaption></figure>

При клике на товар вашему подписчику откроется страница с описанием товара:

<figure><img src="https://lh7-rt.googleusercontent.com/docsz/AD_4nXeVWn8BmpAg5fNGcUh9eT6ghasdPsivVIaRjc5s3ky36HMERlAOxTYLGdCjdf7kDKB8k26Xo_TwyZR7mtBxWXyZuKF_zyUHLaWnJI7DlX58GD4wRlwupO8UdgiEmYsgMyqFVCTK?key=jpoKmlVz5BjGtxmgtNRTdw" alt=""><figcaption></figcaption></figure>

При нажатии на кнопку “Написать” откроется окно для отклика на понравившийся товар:

<figure><img src="https://lh7-rt.googleusercontent.com/docsz/AD_4nXe-uFsXMVe1RDEtwTgPkwi5OqRkinUou8T3dhLwnkhlPgN5E_vLN2Oabrm0xIfXkHm5oYA7r1ME_lHfeChEkJ1SQI44yhAjzCa4DnjY24f5fWugpqQE5l04CvrSSA1HcYwRbMX-mg?key=jpoKmlVz5BjGtxmgtNRTdw" alt=""><figcaption></figcaption></figure>

При этом в карточке клиента появятся переменные, соответствующие товару:

<figure><img src="https://lh7-rt.googleusercontent.com/docsz/AD_4nXcA7q53iL51tVh-uiTlSO3OJQNpFBikz-4SHMmzTZc90Qu4c89tCpdxu8tfp3VrUDAnbKYquxaDS__uFBQSSSJiKaCyNYazGsW10kPIZG9XvpDbPweu2HjQT1QMLYIFroncp5BtWA?key=jpoKmlVz5BjGtxmgtNRTdw" alt=""><figcaption><p>Скрин раздела переменных клиента</p></figcaption></figure>

**market\_description** —  описание товара (берется из карточки товара)

**market\_title** — заголовок товара

**market\_price** — стоимость товара

**market\_id** — id товара

Остаётся настроить реакцию и Ваш магазин автоматизирован!

## Ретаргетинг Вконтакте

### Основные данные

Для каждого запроса в проекте должен быть авторизованный VK пользователь, у которого есть нужный рекламный кабинет. Ниже приведен пример авторизации. После чего будет выдан токен для работы с API ретаргетинга.

<figure><img src="https://lh7-rt.googleusercontent.com/docsz/AD_4nXd2ZawqAdRfbhcPuIUPUibBpkHortHM38doddDDfnQX0dzKtIypAwbzOc24L9s7nkjcO-X_TZjygaX5d_BgVgfRt32Xi2ZseH3nHNpLpi-jXWQq91GSUTDPch7YOnDpwSDq2MQQAw?key=jpoKmlVz5BjGtxmgtNRTdw" alt=""><figcaption></figcaption></figure>

При попытке добавления сотрудника ранее неавторизованного в Salebot будет предложено создать новый аккаунт:

<figure><img src="https://lh7-rt.googleusercontent.com/docsz/AD_4nXfMr5MMe588JGiFDwkcctLrg2gRqyJNKCQ2yvZJDd04BqD5BfXJ6EWG2-voohKuqwyhfGgOa7TzWlWMsxxIwaGVTLg_l2qnjnQ4lP3Xps3HvZ-pH_wEb1_o58YTjF6s0ijV2_ZYKQ?key=jpoKmlVz5BjGtxmgtNRTdw" alt=""><figcaption></figcaption></figure>

<figure><img src="https://lh7-rt.googleusercontent.com/docsz/AD_4nXeXSQ9-7-ziCdBpILEcgVk5z2uMBA6AftyjRFTJPVkg2XrJx0GJ6vLWzEkYZz1iMN3RWJkamYMCyhQJMHBRIXduk85DEBd9KvxVH5EAY1WEV60XBC8AyerzgwbsMdqXgzdZs27T?key=jpoKmlVz5BjGtxmgtNRTdw" alt=""><figcaption></figcaption></figure>

<figure><img src="https://lh7-rt.googleusercontent.com/docsz/AD_4nXcmmSvb9eusymbWWa7oppW2uSLXnro8-YW-ivymErmAyxXp-eWHZO49BewUL4C_ZgS4-ZJ_8mrrnhIsrTwSHWvbSPcI-YIEeYT5tJqCuD7g55rC1opiWuNUCuHJCf2-By6cCT16Tw?key=jpoKmlVz5BjGtxmgtNRTdw" alt=""><figcaption></figcaption></figure>

### **Идентификатор рекламного кабинета (account\_id)**

Идентификатор рекламного кабинета можно найт&#x438;**,** перейдя в настройки. Скопируйте его: он понадобится для использования функций ретаргетинга.

<figure><img src="https://lh7-rt.googleusercontent.com/docsz/AD_4nXfapno5GZNT_Chx8txWAIA5FbLEdIWqFtPyhNWVLVYaVDIW3CCOV1iqXlG-eHqE3BH-UC5cAJn6fQhTwLn2XnN2nflpZmWyMeF2hCPr8lKqURzzmmQNvRBgm67wHz9eRL5rKPj1?key=jpoKmlVz5BjGtxmgtNRTdw" alt=""><figcaption></figcaption></figure>

<figure><img src="https://lh7-rt.googleusercontent.com/docsz/AD_4nXdYyFiDO3cK2Ju_xiP3Ipxvjb7xMxzDXNChEuf5loow9sp58pQA2XIHIUz6E7K1qGO4N6E2AtFSZOx8wzPH-g9MxoWumNf4byVAtfpwhLYg86rEfIShKWcZ0tT7gcyWNWk-yvuS9Q?key=jpoKmlVz5BjGtxmgtNRTdw" alt=""><figcaption></figcaption></figure>

<figure><img src="https://lh7-rt.googleusercontent.com/docsz/AD_4nXfkAsCFhgSjz21xCKUuGORprKjWBnwlXqsCUfnvXxHiOGWMl1b9bAyjHJOU3cmwYg06d14zUmWeX0_kVXWISyv0EyCjTHcQa_u-VIU4CqQo35jCC_KGkv99MOFxnsOFl77QuAfw?key=jpoKmlVz5BjGtxmgtNRTdw" alt=""><figcaption></figcaption></figure>

Также ID кабинета вы можете найти в своем кабинете ВК рекламы

<figure><img src="https://lh7-rt.googleusercontent.com/docsz/AD_4nXeP73ywz6VYQNrIFLXcnK6IwITyTBt-hNAtP5inxUk6LOvRCWtwrt_AJCuz2IiVjUM0OVHxWhAknf-hnNKLxs9QUcAzlwaAc-pUEFtHS7rXqekLLiFMOIHsswS_-mXUFLP-9364?key=jpoKmlVz5BjGtxmgtNRTdw" alt=""><figcaption></figcaption></figure>

### Идентификатор аудитории таргетинга (target\_group\_id)

Идентификатор нужной аудитории таргетинга, можно найти перейдя в свой кабинет ВК рекламы в раздел “Аудитории”:

<figure><img src="https://lh7-rt.googleusercontent.com/docsz/AD_4nXcOyiipnnlft3i-OCxwsxCnvaruoqoWzRYauN78uBhUiuS2dwRfZLH0C8k_aTJsSsfBQ6z4O3z6RoahD7hHGLTIDXBto9WMp8PbAV28nUWppHU869JE7tdcpxQhJOEj-xRkl-bSjg?key=jpoKmlVz5BjGtxmgtNRTdw" alt=""><figcaption></figcaption></figure>

Если у вас еще нет аудиторий нажимаем “Создать аудиторию”.

Во всплывающем окне добавляем источник:

<figure><img src="https://lh7-rt.googleusercontent.com/docsz/AD_4nXdt46Xndr93GUEK0ioVONb0209lkSq9chbXrnbHJ6C0ZPvnrRqNhmbr09mU96iDFQk1R6G-4ISEQFOibK-eXLPSY6JRea1W2JQW92IHEgXckiO_jVad-9U03GfqHlOFaDkQKcyN?key=jpoKmlVz5BjGtxmgtNRTdw" alt=""><figcaption></figcaption></figure>

После добавления источника нажимаем сохранить.

После сохранения ваша новая аудитория появится в списке всех аудиторий, здесь вы можете скопировать ID.

<figure><img src="https://lh7-rt.googleusercontent.com/docsz/AD_4nXfQ4dxloqtyNck6EvbhdyvX9Uju6idlkbN6-HiMbcr9OYu-2v1hnCP4NxxBqdS--DAz1VnM-W7o9Ot21qkzD-6pSCOmSgZKacctEee06pbHsSyM0dzV0oO5GIJWICXAY4wgNEFB?key=jpoKmlVz5BjGtxmgtNRTdw" alt=""><figcaption></figcaption></figure>

{% hint style="success" %}
Внимание!&#x20;

Все функции для вк рекламы актуальны как для старого, так и для нового кабинета.&#x20;
{% endhint %}

### Как добавить пользователя в аудиторию ретаргетинга ВК: параметр **vk\_add\_to\_target\_group()**

{% tabs %}
{% tab title="Описание" %}
**vk\_add\_to\_target\_group(email, account\_id, target\_group\_id, contacts, ads\_client\_id)**

Параметры:

<mark style="color:red;">**!**</mark>**&#x20;email** - email сотрудника в проекте

<mark style="color:red;">**!**</mark>**&#x20;account\_id** - идентификатор рекламного кабинета.

<mark style="color:red;">**!**</mark>**&#x20;target\_group\_id** - идентификатор аудитории таргетинг&#x430;**.**

**contacts** - список телефонов, email адресов, мобильные рекламные идентификаторы (IDFA, GAID) или идентификаторов пользователей, указанных через запятую.

По умолчанию передается идентификатор пользователя во ВКонтакте.

**ads\_client\_id** - только для рекламных агентств. id клиента, в рекламном кабинете которого будет редактироваться аудитория.
{% endtab %}

{% tab title="Примеры" %}
Пример вызова функции:

<figure><img src="../../../.gitbook/assets/image (174) (1).png" alt=""><figcaption></figcaption></figure>

Примеры вызова функции: \
result = vk\_add\_to\_target\_group('example@example.com', '1606728577', '38572961')

с ads\_client\_id для рекламного агентства: \
result = vk\_add\_to\_target\_group('example@example.com', '1606728577', '38572961', '', '1234567')

Передача собственных данных вместо идентификатора клиента: \
result = vk\_add\_to\_target\_group('example@example.com', '1606728577', '38572961', '#{phone}')

Передача одновременно нескольких собственных данных, например,  номеров телефонов:

result = vk\_add\_to\_target\_group('example@example.com', '1606728577', '38572961', '78111111111, 782222222, 7833333333')
{% endtab %}

{% tab title="Пример кода для копирования" %}
```
 result = vk_add_to_target_group('example@example.com', '1606728577', '38572961')
```
{% endtab %}
{% endtabs %}



### Как удалить пользователя из аудитории ретаргетинга ВК: параметр **vk\_remove\_from\_target\_group()**

{% tabs %}
{% tab title="Описание" %}
**vk\_remove\_from\_target\_group(email, account\_id, target\_group\_id, contacts, ads\_client\_id)**

Параметры

<mark style="color:red;">**!**</mark>**&#x20;email** - email сотрудника в проекте

<mark style="color:red;">**!**</mark>**&#x20;account\_id** - идентификатор рекламного кабинета.

<mark style="color:red;">**!**</mark>**&#x20;target\_group\_id** - идентификатор аудитории таргетинга.

**contacts** - список телефонов, email адресов или идентификаторов пользователей, указанных через запятую. По умолчанию передается идентификатор пользователя в вк.

**ads\_client\_id** - только для рекламных агентств. id клиента, в рекламном кабинете которого будет редактироваться аудитория.
{% endtab %}

{% tab title="Примеры" %}
Примеры вызова функции: \
result = vk\_remove\_from\_target\_group('example@example.com', '1606728577', '38572961')

с ads\_client\_id для рекламного агентства: \
result = vk\_remove\_from\_target\_group('example@example.com', '1606728577', '38572961', '', '1234567')

передача собственных данных вместо идентификатора клиента: \
result = vk\_remove\_from\_target\_group('example@example.com', '1606728577', '38572961', '#{phone}')

удаление из аудитории пользователей одновременно по нескольким параметрам, в примере номеров телефонов: \
result = vk\_remove\_from\_target\_group('example@example.com', '1606728577', '38572961', '78111111111, 782222222, 7833333333')
{% endtab %}

{% tab title="Пример кода для копирования" %}
```
result = vk_remove_from_target_group('example@example.com', '1606728577', '38572961')
result = vk_remove_from_target_group('example@example.com', '1606728577', '38572961', '', '1234567')
result = vk_remove_from_target_group('example@example.com', '1606728577', '38572961', '#{phone}')
result = vk_remove_from_target_group('example@example.com', '1606728577', '38572961', '78111111111, 782222222, 7833333333')
```
{% endtab %}
{% endtabs %}



### **Как добавить новую аудиторию ретаргетинга ВК: параметр vk\_add\_new\_target\_group()**

{% tabs %}
{% tab title="Описание" %}
**vk\_add\_new\_target\_group(email, account\_id, name, lifetime, ads\_client\_id)**

Параметры

<mark style="color:red;">**!**</mark>**&#x20;email** - email  сотрудника в проекте, который подключил свой аккаунт к проекту и у которого находится нужный рекламный кабинет

<mark style="color:red;">**!**</mark>**&#x20;account\_id** - идентификатор рекламного кабинета

<mark style="color:red;">**!**</mark>**&#x20;name** - название аудитории ретаргетинга — до 64 символов

<mark style="color:red;">**!**</mark>**&#x20;lifetime** - количество дней, через которое пользователи, добавляемые в аудиторию, будут автоматически исключены из нее. Число от 1 до 720

**ads\_client\_id** - только для рекламных агентств. id клиента, в рекламном кабинете которого будет редактироваться аудитория.



При успешном исполнении запроса в ответ получите идентификатор созданной аудитории: {'id': 41333076}
{% endtab %}

{% tab title="Примеры" %}
<figure><img src="../../../.gitbook/assets/image (175) (1).png" alt=""><figcaption></figcaption></figure>

result = vk\_add\_new\_target\_group('example@example.com', '1606728577', 'Новая аудитория', 120)

result = vk\_add\_new\_target\_group('example@example.com', '1606728577', 'Новая аудтория', 120, '1234567')
{% endtab %}

{% tab title="Пример кода для копирования" %}
```
result = vk_add_new_target_group('example@example.com', '1606728577', 'Новая аудитория', 120)
result = vk_add_new_target_group('example@example.com', '1606728577', 'Новая аудтория', 120, '1234567')
```
{% endtab %}
{% endtabs %}



## Автоматическая маркировка рекламы Вконтакте

{% hint style="info" %}
С 1 сентября 2023 года вся реклама размещенная в интернете на территории Российской федерации должна маркироваться, в случае отсутствия маркировки, грозят штрафы.
{% endhint %}

Что нужно маркировать?

* Закрепленный пост, если в нем есть призыв к действию
* Акции и специальные условия&#x20;
* Реферальные программы&#x20;
* Посты, которые призывают что-то покупать \
  \
  Для вашего удобства мы создали готовый шаблон, который можно скопировать в ваш проект или использовать отдельно.\
  Внедряйте его в любые проекты и автоматизируйте процесс маркировки.\
  \
  Чтобы установить шаблон себе в проект перейдите в раздел и нажмите кнопку "Установить"

<figure><img src="https://lh7-rt.googleusercontent.com/docsz/AD_4nXcYjztbZIr1-eXrLnLX0WTzrTI7NQciLjWS0FpXSGTBILN080H1a9SskHJLy3dOgb9V79xbGwFFSbLx8aN9egsyaSzEBqeOOqMB0ppojbMotcwdHgBmEwWVcdyIz9he0_RJD-yc_w?key=jpoKmlVz5BjGtxmgtNRTdw" alt=""><figcaption></figcaption></figure>

### Настройка маркировки в кабинете [ВК ОРД](https://ord.vk.com/) и Salebot

Для настройки маркировки понадобиться кабинет [ВК ОРД](https://ord.vk.com/)(Оператор рекламных данных VK)

Необходимо зарегистрироваться и создать два кабинета:

* Основной  через который будет маркироваться реклама.
* Демо-кабинет для тестирования маркировки.

<figure><img src="https://lh7-rt.googleusercontent.com/docsz/AD_4nXea4sEou8uFFsDXdwBo6iEdY0fFM-3J-HBkFHU1gC1QMB7KMNijorEcGb4u2xHCvdUQklOYlfPjEBb8z7vi_LqEv82IOsC5R1BP8AppFlubJBO7mXzMz2QQeTj0cp_AZ06r8ushWQ?key=jpoKmlVz5BjGtxmgtNRTdw" alt=""><figcaption></figcaption></figure>

Для этого переходим по ссылке: https://ord.vk.com/&#x20;

### **Получение Api токена для** основного аккаунта

Заходим в кабинет, выбираем меню настроек и генерируем токен и сразу сохраните его себе. Важно сохранить токен так как он показывается один раз.

<figure><img src="https://lh7-rt.googleusercontent.com/docsz/AD_4nXdcyFFt0swNkKlvDk46U8Yu2LRoCxbqZ9ovpLylJlFE3fk4uk5YoEWVPSlck34IWYbuZfG-cwa2FcM_S_avsVi-DL43qSXOE_Wme2KkLOizDBATXudywtRTUN0dTkkQve4Fvl_JFw?key=jpoKmlVz5BjGtxmgtNRTdw" alt=""><figcaption></figcaption></figure>

<figure><img src="https://lh7-rt.googleusercontent.com/docsz/AD_4nXc-7RALvmz7BMPhiN5A3NUmTgRnCu6eSmng5hQ98zhReXzawph6xpwOWky80iyo95R41A-WHA4s6lc9cI0Tz6Qv76EjFKd16AxEL77PlWol9gEQSfc_VwTNq6JCZnDGvtPFPq9U?key=jpoKmlVz5BjGtxmgtNRTdw" alt=""><figcaption></figcaption></figure>

<figure><img src="https://lh7-rt.googleusercontent.com/docsz/AD_4nXeQ8gvwrA3_v1Wqq8npfWUKYp6cxoJJLqA5rNgRrxHAhFRlDZTOb34ZuTqxQ-RRcDkcUNBSkxXLbo19tDsmnVPDJY2-CxaJyXIQizj7a5M-M4exnqfR51oodLz-jyDEibbfYGMk8g?key=jpoKmlVz5BjGtxmgtNRTdw" alt=""><figcaption></figcaption></figure>

### **Получение Api токена для тестовой среды**

Выбираем меню настроек, выбираем демо-кабинет и генерируем токен и сохраняем его.

<figure><img src="https://lh7-rt.googleusercontent.com/docsz/AD_4nXehC7NUP6fz6aP-mQ2fWklFJYCHeUEoNrH7XSna1qy78sxC7-vL7Yl1Dfe_-Dxj1P5Givryj4wWrvTas3R-DWelwnger4MJVBNYMVJguBUw_D_orENICs7jlaQJgrc7d5aLjBoaRQ?key=jpoKmlVz5BjGtxmgtNRTdw" alt=""><figcaption></figcaption></figure>

## **Настройка ОРД в кабинете Salebot**

Заходим в настройки проекта → переменные → общие переменные

<figure><img src="https://lh7-rt.googleusercontent.com/docsz/AD_4nXc3ir5wqkr616MGxyGKVmTGBECq32AcAuuTdujOTFEgcEAwnsxEhVDsuOcBqFZWGli6-lWLpv20UxZ4Raxl9dii_wWScvLV-SxmFsx7r2VTptManj5nImai-rMPxhbF8oA_A6Ls?key=jpoKmlVz5BjGtxmgtNRTdw" alt=""><figcaption></figcaption></figure>

В общих переменных задаем переменную vk\_ord\_token и в значение ставим токен демо кабинета из ОРД ВКА. Сначала ставим токен демо-кабинета для тестирования, как только мы закончим все настройки кабинета и будем готовы передавать данные меняем токен на основной.

<figure><img src="https://lh7-rt.googleusercontent.com/docsz/AD_4nXeobNk0jHk5SDenRwrbg3-0LcR8ClTodUbtJ-H1M84pW02iwxbxWHRuwwFYMhC7RDjmeGLZdXcDpLcU2RYMIia_hBsR8v1Bh0rQFEFtIx3fTLUwlU10jgb1WlUS2v2TLEvBhdvHlw?key=jpoKmlVz5BjGtxmgtNRTdw" alt=""><figcaption></figcaption></figure>

Мы записали видео инструкцию, где подробно объяснили, как работать с шаблоном.

### **Настройка маркировки постов в схеме бота**

Собираем все необходимые данные от клиента для его регистрации в ОРД как контрагента.

{% hint style="info" %}
Если ранее вы не сталкивались с созданием чат-ботов, рекомендуем изучить раздел [Основы ботостроения](https://docs.salebot.pro/osnovnye-ponyatiya.-kak-sozdavat-botov-na-salebot.pro).
{% endhint %}

Собираем бота который запрашивает необходимые данные.\
Для граждан РФ нам понадобиться:&#x20;

* ФИО
* ИНН
* Номер телефона

{% hint style="info" %}
Для вашего удобства мы создали готовый шаблон, скопируйте его к себе в проект.
{% endhint %}

**Уточняем форму организации обратившегося**

<figure><img src="https://lh7-rt.googleusercontent.com/docsz/AD_4nXcl5wEnyQF1qCGoM4d6OLt5LElgJmifV6HDOkS7N56_5D4eBr5gt-Buu-LHBNoq73F7WHQH3OXiRelGOw1pFXMWuCFqVLB3IkLNzHvpgCCw7sjNj9ogM6Qsno9d0UqgP1r2R3vmJg?key=jpoKmlVz5BjGtxmgtNRTdw" alt=""><figcaption></figcaption></figure>

Далее стрелка пропускает пользователя по схеме бота только при условии:\
У меня ИП; У меня ООО; Я физ.лицо

<figure><img src="https://lh7-rt.googleusercontent.com/docsz/AD_4nXebDjWspCOiTlsSvi4JD09j5j54z7sm4y3D1n4LxRTNLAGVT5YLRp1r_6mMGOQvVTzRSSLvx5APvQkM5I1JwNlJlFqmtedFftfE724kvCCwBpWneT6QG6AY3U5ljwFhBGy97lAsPQ?key=jpoKmlVz5BjGtxmgtNRTdw" alt=""><figcaption></figcaption></figure>

При нажатии кнопки определился тип контрагента (пользователя, который регистрируется в нашем чат-боте). Записали его в переменную type в калькуляторе блока. В текстовом поле запрашиваем ИНН у пользователя.\
<br>

<figure><img src="https://lh7-rt.googleusercontent.com/docsz/AD_4nXfAvkYNflcbhGAB_CeaPu4YnSihWrBdHd02CuxkojtvMgqau-bOfc5FRME_51EBmqO6AwIctH5KJD14GvZKYlOnMNVLY44GzRlVJzgDOAG9otjnanJOPfIS3DB7uEovGtToGEH6_w?key=jpoKmlVz5BjGtxmgtNRTdw" alt=""><figcaption></figcaption></figure>

Для следующей стрелки ставим условие. Это условие проверяет введенный текст и сохраняет его в переменную inn. Ставим выбор соответствия - регулярное выражение.<br>

<figure><img src="https://lh7-rt.googleusercontent.com/docsz/AD_4nXd5ISr_7mlZauybuoIAX5Vp4g4BKNamZJ0b_BCrREqv5GhE-0wzyLklO8fQ2Fi2D9_vG0b9ZJXF93UYp1Re1jbHvvmO3avJYwHQHGUR_QCa-kDCYVTivOElY-k9iOGuFrZHc_dQmg?key=jpoKmlVz5BjGtxmgtNRTdw" alt=""><figcaption></figcaption></figure>

Запрашиваем номер телефона. По стрелке прописываем условие:&#x20;

<figure><img src="https://lh7-rt.googleusercontent.com/docsz/AD_4nXdFBuA53dvflGAcjrchuIMFKCI6g05DV7W703KAXlxpdFLh-ZgmYqZHACTZh-GGtXYRN_m9rzH9ONN5vFyZ-S35C_tSk5DXFBIJObI0Dq_psX6od1VI18ApRkSOrUVl7waVZ7c-?key=jpoKmlVz5BjGtxmgtNRTdw" alt=""><figcaption></figcaption></figure>

<figure><img src="https://lh7-rt.googleusercontent.com/docsz/AD_4nXdSw6kMEY-CBZL0cMdfAYwHw4fiI1sKD37uj484DLdvbtRE2ldcdR9W6vEWABCo88qJ8WMZ_Nhj2RIGedU2zcJt3zTpGCIh8bilAOxE1nFGyPve9Ak8-0F8HZU3MJ7QCFpAZt2Pkw?key=jpoKmlVz5BjGtxmgtNRTdw" alt=""><figcaption></figcaption></figure>

### **Регистрация контрагента**&#x20;

<figure><img src="https://lh7-rt.googleusercontent.com/docsz/AD_4nXefFVZ3Um1hEhPglaVb_D-Jv7P0jGPDdOFcRIScz_WUam8xMSMnRx5NOmx0RPvaI1DmG3V8PKed7B9kYj_YZuQRsnzN4cfbxxtff5MpmzTGDF9Y-RgemA6FkBZO6hvqKbxdp1ok?key=jpoKmlVz5BjGtxmgtNRTdw" alt=""><figcaption></figcaption></figure>

**Создаем блок , в текстовом поле пишем "Регистрируем в системе" в калькуляторе прописываем функцию:**\
\
vk\_ord\_create\_new\_publisher(name, publisher\_type, publisher\_inn, publisher\_phone, test, token, rs\_url)&#x20;

name - ФИО контрагента&#x20;

publisher\_type - это определяем кто он из списка\['juridical', 'ip', 'physical']&#x20;

test - если тестовый запрос, то передать 1, если нет, то 0&#x20;

token - необязателен, если не передать то ищет в переменных проекта переменную&#x20;

vk\_ord\_token rs\_url - необязательные параметры после выполнения создаст переменную сделки&#x20;

vk\_ord\_publisher\_data с данными по контрагенту\
\
Собранные данные отправляются в ord.

{% hint style="warning" %}
_ВАЖНО: ОРД ВК не присылает результатов загрузки. контрагента._\
&#xNAN;_&#x41F;оэтому если у вас не отображается переменная значит вы сделали все правильно если отображается ошибка, значит нужно внести поправки в функции и проверить правильность данных._
{% endhint %}

### **Регистрация договора с контрагентом**

Чтобы создать договор по которому данные пойдут дальше, в калькуляторе следующего блока прописываем функцию:\
\
vk\_ord\_add\_new\_distribution(amount, vat\_included, creatives\_reporter, test, token, client\_external\_id, date)&#x20;

<figure><img src="https://lh7-rt.googleusercontent.com/docsz/AD_4nXcpajLvHeP_4B50DimlQxkIDOCE1O7t_EsVEKW0NmhpkDhnCkArH33deq3D0WOGR4iPaFshub6YlJl_WTabydvOKErxHZNvJtjSmZAjO4vUqRefUOXqIt6N0FpHrWFwy0rHN6pTsw?key=jpoKmlVz5BjGtxmgtNRTdw" alt=""><figcaption></figcaption></figure>

amount - сумма (может быть равна 0)&#x20;

vat\_included - НДС ( 1- включен в стоимость, 0 не включен)

creatives\_reporter - 1 если контр агент передает, 0 если мы

test - если тестовый запрос, то передать 1, если нет, то 0&#x20;

token - необязателен, если не передать то ищет в переменных проекта переменную vk\_ord\_token&#x20;

client\_external\_id - необязателен, по умолчанию использует 'my'

date - по умолчанию ставит текущую дату всегда пересоздает переменную сделки vk\_ord\_contract\_id если переменная vk\_ord\_contract\_data есть, то дополняет ее, иначе создает эту переменную с данными по договору<br>

Возвращаем созданный id договора  клиенту в следующем блоке, он понадобиться в дальнейшем.

<figure><img src="https://lh7-rt.googleusercontent.com/docsz/AD_4nXeUEsHVAashyxMu6SISRYhm8IK_9f7yONh7VCEV4yYBdQNDKhnoRtBveJ1lsoAKZYD-r66rZ6vdwY2DO9KSn2Fdxc-4SEvJbI9silUVGYv9kM6Ti8gSW2EKxOkrZ0Znrlmj5d5Q?key=jpoKmlVz5BjGtxmgtNRTdw" alt=""><figcaption></figcaption></figure>

### **Регистрация рекламной площадки  контрагента**

Это место в котором будет выложена реклама.\
\
Создаем блок и запрашиваем имя площадки.

<figure><img src="https://lh7-rt.googleusercontent.com/docsz/AD_4nXdWnoGJ4YLFX-MqDLCTjE66Savi9lrB4iIko56vaR4tGeGpgyAuQLiKCRnaJBrMHhHl09h0_dD-e_aIauE7CJqWWGgwmw35y14sDp7k1Qjx4gYtDN94Rs5sHwBQmkXyg0vrCWOd?key=jpoKmlVz5BjGtxmgtNRTdw" alt=""><figcaption></figcaption></figure>

По стрелке сохраняем ответ пользователя как имя площадки в переменную pad\_name\
И в следующем блоке запрашиваем ссылку на площадку и сохраняем ее по стрелке.\
<br>

<figure><img src="https://lh7-rt.googleusercontent.com/docsz/AD_4nXezlmJxNwnI1gnJsdL-qWwF15rRp2bRtYRlQ2q_l9D6Os-yF3Sc8h0iYM_dbc5CySnKm9x4eNe4XmHjY2vMeWf4KkV-ST8o3fannJBnMzv4_es7ymfxp9bbm-l_V5LmrK2-MVArsA?key=jpoKmlVz5BjGtxmgtNRTdw" alt=""><figcaption></figcaption></figure>

### Функция по созданию рекламной площадки

Далее создаем блок и в калькуляторе указываем функцию:\
**vk\_ord\_add\_web\_pad(pad\_name, is\_owner, pad\_url, test, token)**

<figure><img src="https://lh7-rt.googleusercontent.com/docsz/AD_4nXdwJ4vHT6r6fWebOCIb1NfEV5thDxP6mjMb21fGuVTumGOR86fJF2Jm53O-ZOT1qYQhKb2ArenMQqMhV5Qrelta53LuOk9fALlFKADlblFcycuiiH7VbtopfmIXJn1zhPp-kNfg?key=jpoKmlVz5BjGtxmgtNRTdw" alt=""><figcaption></figcaption></figure>

**pad\_name** - имя площадки

**is\_owner** - владелец ли клиент, если да передать 1, если нет 0&#x20;

**pad\_url** - ссылка на площадку&#x20;

**test** - если тестовый запрос, то передать 1, если нет, то 0 token - необязателен, если не передать то ищет в переменных проекта переменную vk\_ord\_token

В следующем блоке уведомляем, что площадка создана и отдаем контрагенту его id

<figure><img src="https://lh7-rt.googleusercontent.com/docsz/AD_4nXcT3lKbeXQUZN-_3CqT1T6fxXlOvbFFzDHdVve7NrVFx6nCgrTQGn-WXAva1gOHvEgGc_iZ_YQe6ikRbEOSJ5n3X9GQF4jz8-KvtkhHriV73gUwFglX7LQ8_NVX_UToIlAO0zQ-Bw?key=jpoKmlVz5BjGtxmgtNRTdw" alt=""><figcaption></figcaption></figure>

### **Регистрация креатива**

Запрашиваем название креатива и по стрелке прописываем условие. Важно в каждой стрелке указать значение переменной, название вы можете увидеть на  изображениях.\
В данном случае - creative\_name

<figure><img src="https://lh7-rt.googleusercontent.com/docsz/AD_4nXe26zf0w9tgCUggiwqV8_RFixN6ZKf0JfbXDYhlia3gF1egrRGB2iU4A7RLjW1s1V4F85EX5RCdiA8F5Syr9W-35HmLhzfQvnVOY7j5bPMXp8NROmEyeQm3sO8z8fLXLbOrSz2F?key=jpoKmlVz5BjGtxmgtNRTdw" alt=""><figcaption></figcaption></figure>

<figure><img src="https://lh7-rt.googleusercontent.com/docsz/AD_4nXcNpZZyjIG3RlyCbJgGyWsfNNH_ArvJn8m2oADXx7PaNxvLEqtPPH4BRLORjFbZ7-VgDSfd_aA_6WnybLuyevIF9Iz9kUAYVdIcDmc7pzM2v5QGTz_Zb0GPBRNEmUChuctE6VkSqA?key=jpoKmlVz5BjGtxmgtNRTdw" alt=""><figcaption></figcaption></figure>

Далее в блоке  запрашиваем описание и прописываем условие в стрелке.

<figure><img src="https://lh7-rt.googleusercontent.com/docsz/AD_4nXetfUFpB4lBs430f_wH3LfpSRsP0ebZwUJZyI5NekE-NDXXtawiYE2w63iSDiGova-Kn_ludG_3DaIhDJwkqZLlq2gwB0cMf1-i8tlUovdHn_SuQedRXy0chaeHHuvM2UIJADsw?key=jpoKmlVz5BjGtxmgtNRTdw" alt=""><figcaption></figcaption></figure>

В следующем блоке в текстовом после запрашиваем текст креатива, также добавляем условие по стрелке.

<figure><img src="https://lh7-rt.googleusercontent.com/docsz/AD_4nXcuLA3Iyj7BaeGUx7yFKG1rf9RU0ZLpZbYDPb8lEHe8-MRQNeYorYHwVKIYlXWBR72_AcG-DolW6JFcJiTSsGg_6U1ac5yIm3IlVYlpMLQLIvRwTpV132cAjkbMWU3Vq2TiCmPXGw?key=jpoKmlVz5BjGtxmgtNRTdw" alt=""><figcaption></figcaption></figure>

Создаем еще один блок, в нем мы запросим ссылку на креатив. Это ссылка на то, что рекламируем или, если по репостам, на исходное сообщение с которого идут репосты.\
И прописываем условие по стрелке ниже.\
\
(https?):((//)|(\\\\))+\[\w\d:#@%/;$()\~\_?+-=\\.&]\*<br>

<figure><img src="https://lh7-rt.googleusercontent.com/docsz/AD_4nXfK53FZUxChe6QTr3j8LddX6TxyolWHe3ZdhWehLLEwIG6hI4ZFn1TGlxMzTLgZQ0i5V__Rp7seT27_52UsfLAoNCDhFTb-jrhsABaXN4wvMVAGCS5nYFoPI30wmY66Vn0N9P805Q?key=jpoKmlVz5BjGtxmgtNRTdw" alt=""><figcaption></figcaption></figure>

В следующем блоке запрашиваем целевую аудиторию.\
\
**И далее в следующем блоке регистрируем креатив с помощью функции:** \
\
**vk\_ord\_add\_new\_creative(creative\_name, description, text, url, targeting, okveds, test, token, media\_external\_ids, media\_urls, flags, form, pay\_type)**

<table><thead><tr><th width="252">Параметры функции </th><th>Значение параметра функции</th></tr></thead><tbody><tr><td>creative_name</td><td>название креатива</td></tr><tr><td>description</td><td>описание</td></tr><tr><td>text</td><td>текст креатива</td></tr><tr><td>url</td><td>ссылка</td></tr><tr><td>targeting</td><td>целевая аудитория</td></tr><tr><td>okveds</td><td>просто через запятую без пробелов перечисляем нужные ОКВЕДы (зависит от того, что рекламируем)</td></tr><tr><td>test</td><td>1 еслит тестовый запрос, 0 если боевой</td></tr><tr><td>token</td><td>если не нужен тут передать None и его будет искать в переменной</td></tr><tr><td>media_external_ids</td><td>id загруженных файлов через запятую без пробелов</td></tr><tr><td>media_urls </td><td>ссылки на медия через запятую без пробелов</td></tr><tr><td>flags </td><td>нужные флаги через запятую без пробелов</td></tr><tr><td>form</td><td>форма рекламы, по умолчанию 'text_graphic_block'</td></tr><tr><td>pay_type</td><td>тип оплаты, по умолчанию "cpc"</td></tr></tbody></table>

В текстовом после возвращаем Id креатива.

<figure><img src="https://lh7-rt.googleusercontent.com/docsz/AD_4nXcS9ztb5DE8uH5efdaQzc-d6egHJJiAgCecgXyTwsrMg6-2d1RMwakRjJ_TRKxcD4Ca4hJBqGwhHbyzpskXpPKMTiRvS9ecsyetoEpGVumJO_G6foj7isxCdjBPc5Kk00rUrYqL8A?key=jpoKmlVz5BjGtxmgtNRTdw" alt=""><figcaption></figcaption></figure>

### Функция загрузки картинки крео

Как загрузить картинку подробно описано в видео инструкции.\
\
В блоке прописываем функцию и в ней указываем ссылку на изображение загруженное на Salebot ( чтобы загрузить изображение создайте блок, добавьте в него изображение и скопируйте ссылку на него)\
\
vk\_ord\_upload\_media(external\_id, image\_url, description, test, token=None)

<figure><img src="https://lh7-rt.googleusercontent.com/docsz/AD_4nXdfVq5snOWUYzUxUZg_RPSylyf5Te0C8YAqMD6mQ_jZ4GkeE_FP5R1YCO2PCw1or9pojvysw-axmkDx293d6lU1YAPEuOltqWZ_gnNCsvk1RRuIHxQMlbO1PwygdRCDMjETUeSE7w?key=jpoKmlVz5BjGtxmgtNRTdw" alt=""><figcaption></figcaption></figure>

### **Создание актов выполненных работ**

Для создания акта запрашиваем id креатива, Id площадки, число просмотров за отчетный период. И в последнем блоке прописываем функцию:&#x20;

**vk\_ord\_create\_invoice(vk\_ord\_contract\_id, creative\_platform\_data, test, token)** <br>

<figure><img src="https://lh7-rt.googleusercontent.com/docsz/AD_4nXcM9yP6nE7wg-dwoqKDQ5d1zPNp_STROnJJYEKRSU65B4FxKGmXaZhwR-Ndoaa64rFZrNAnmF8YjYnB_ZUt2xUVg8LAj464TGPf_r9d0S8jNy83hNHVULCbB_X7FI3cl-jNYKEvBQ?key=jpoKmlVz5BjGtxmgtNRTdw" alt=""><figcaption></figcaption></figure>

<table><thead><tr><th width="296">Параметры функции</th><th>Описание параметра</th></tr></thead><tbody><tr><td>vk_ord_contract_id</td><td>договор по которому надо создать акт, должен быть в переменной vk_ord_contract_data, иначе не сработает и вернет ошибку</td></tr><tr><td>creative_platform_data</td><td><p>конструкция такого вида: [{"creative_external_id": "тут подставляете нужный id креатива", "platforms": [[pad_id, 500, 500, 0, 0], [pad2_id, 100, 150, 0, 0]]}] в данном примере данные для 1 креатива на 2 площадки. </p><p>[pad_id, 500, 500, 0, 0] первое - id площадки, потом идут по порядку - число показов общее, число показов за период на который создается акт, сумма (может быть равно 0), сумма за событие (может быть равно 0)</p></td></tr></tbody></table>

В словаре 'creative\_external\_id' - id креатива, а в platforms все нужные для него платформы. Схема заполнения такая в списке первый вложенный список - первая платформа, второй - вторая платформа для этого же креатива.&#x20;

Порядок параметров в списке по платформе pad\_external\_id, shows\_count, invoice\_shows\_count, amount, amount\_per\_event Флаги тянет с договора date\_start\_planned и date\_start\_actual - из контракта берет дату регистрации, date\_end\_planned и date\_end\_actual - берет текущую дату pay\_type - из контракта

Если вы работаете с маркированными реферальными программами, то для составления отчета вам будет необходимо передавать количество просмотров постов. В получении данных вам поможет функция: <br>

{% hint style="info" %}
Чтобы не копировать все функции используйте готовый шаблон. А в видео мы подробно объяснили, как работает схема бота и какие данные необходимо прописывать.
{% endhint %}



### Видео-инструкция Маркировка рекламы Вконтакте:

{% embed url="https://youtu.be/Ra0CCXgNxWs" %}
