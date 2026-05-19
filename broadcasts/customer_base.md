# Перенос клиентской базы. Загрузка номеров Whatsapp

### Как загрузить клиентов файлом

Перенос клиентов возможен из Telegram, Viber, Вконтакте, Whatsapp, Email&#x20;

Клиентов из Instagram\* можно загрузить только в список из файла в рамках одного проекта. Также можно загрузить всех Instagram-клиентов, с которыми был диалог. Загрузка через кнопку в разделе "Каналы".

{% hint style="danger" %}
\*Принадлежи Мета inc., которая признана экстремистской и запрещена на территории РФ
{% endhint %}

Для того чтобы загрузить клиентов, перейдите в раздел "Каналы":

<figure><img src="../.gitbook/assets/Снимок экрана 2025-05-06 в 18.55.24.png" alt="" width="438"><figcaption></figcaption></figure>

Далее выберите необходимый мессенджер (выделены на скриншоте ниже):

<figure><img src="../.gitbook/assets/Снимок экрана 2025-05-06 в 18.57.32.png" alt=""><figcaption></figcaption></figure>

Добавьте бота, если он еще не подключен к проекту. Затем нажмите на кнопку: "Загрузить список клиентов":

<figure><img src="https://lh7-rt.googleusercontent.com/docsz/AD_4nXfMZCG6yr41qFSXjL2IFR-GPFp4bRkEE_SZDSGwaoBi8yUXnOp3UfHX1th9qsNaaTO2gWP4QkpEKg5VXuNd_PO-RpViIv4lZTDNCf0pWCqKCnuRgHAGfAL1U_LsSFw-Lm_1EC1xUg?key=o5DRCqMFXEyXeycmGc9MdQ" alt=""><figcaption></figcaption></figure>

Далее в открывшейся форме можно загрузить файл в формате csv и сразу добавить клиентов в Список для дальнейшего удобства работы:

<figure><img src="https://lh7-rt.googleusercontent.com/docsz/AD_4nXfbFaz0hG3MeOua2pAQe7WwNhGAKEZIbQbt3Ge2dvbQOVBN3dCqbKhmwdfG7eRIqv4ooQRtcOCbdbDjjuCjeJ0MX8cAdjxB8vX70TwWQh_-S5M4z24LTlZEB3iNeRvNTvTcrS9h?key=o5DRCqMFXEyXeycmGc9MdQ" alt="" width="375"><figcaption></figcaption></figure>

{% hint style="warning" %}
Важно!&#x20;

При загрузке файла необходимо указать правильно кодировку и разделитель в файле. По умолчанию стоят значения, необходимые для загрузки файлов, сохраненных в Excel.
{% endhint %}

{% hint style="info" %}
Подробно о формате данных указано на форме, также на ней указаны особенности, специфичные для каждого мессенджера.
{% endhint %}

{% hint style="warning" %}
Важно!&#x20;

Файл при загрузке ДОЛЖЕН иметь имена колонок. Если не заданы имена колонок в документе, то файл с переменными загружен не будет, и загрузка пройдет неверно (см. пример ниже).
{% endhint %}

<figure><img src="https://lh7-rt.googleusercontent.com/docsz/AD_4nXfPGraYbeqWfSItBSkDYEgDiSWXaPja3a5yfJM99pASkyp5CQl-YxwPdhnZjXGoLc8mCAMwxE_uWL-3pA3CnT9wxVedeuJpcB75KIR1-pbhnNX2xEXHznNiuTz0KjhYS-v4Kxz0sA?key=o5DRCqMFXEyXeycmGc9MdQ" alt=""><figcaption><p>Имена колонок в файле</p></figcaption></figure>

### Возможные ошибки при загрузке клиентов файлом

Если при загрузке клиентов есть такая ошибка, то вероятно, что не все колонки имеют имена. Надо проверить это и дать названия колонкам.

<figure><img src="https://lh7-rt.googleusercontent.com/docsz/AD_4nXfIDXClLu2dU9oMDeLvDFdlH2ePhN0UxxHCnOOkP2Yv-0ExZKsTvRSKpe5KKiE4_Okk-35rCl4n4Z6s0Oave5mqMkjl48DGlD33Ad3oZtYJGDuxiclgMDHzMEhd9KsKbCEyO-eSmg?key=o5DRCqMFXEyXeycmGc9MdQ" alt="" width="563"><figcaption></figcaption></figure>

### Добавление в список

Вы можете добавить загружаемых клиентов сразу в один или несколько списков - для сегментации.

<figure><img src="https://lh7-rt.googleusercontent.com/docsz/AD_4nXc7U3lbE2H1VYic-Rk3_AGaDDBgU_WgRBHTeux6rtMxvrdAoFSVc7tZX7Lgrhf5r_lqnkVIkFFAwRS5FqkSmqJIuMxh_3WcnXm2RhW-Bx3g-5VHcWvDc-7OQa4eEqEv4OTYAq2q?key=o5DRCqMFXEyXeycmGc9MdQ" alt="" width="375"><figcaption></figcaption></figure>

### Перенос переменных

В первой колонке размещается идентификатор в мессенджере, во второй - имя клиента. Остальные данные из колонок будут записаны в переменные клиента. Название переменной берется из названия колонки. Названия колонок размещаются в первой строке.

Загрузка переменных произойдет автоматически.

## Особенности загрузки клиентов

Клиенты привязываются к мессенджеру, то есть подписчиков из одного телеграмм бота нельзя загружать в другой.

**Телеграм**

В Telegram -> platform\_id - это число.

**Viber**

В viber platform\_id - это строка, состоящая из букв и чисел, оканчивающаяся на два знака равно.

**Вконтакте**

Клиенты из Вконтакте загружаются автоматически при подключении группы. Те, кто подписался на сообщения, но не писали в группу, автоматически загружены не будут.

**Whatsapp**

Это единственный мессенджер, где клиенты не привязаны к боту, и вы можете загрузить их просто списком номеров. Формат номера телефона свободный. При загрузке он будет приведен к необходимому виду автоматически.

Важно! Если вы планируете сделать рассылку сообщений по базе номеров, то вам необходимо предварительно загрузить в список клиентов номера, а затем уже создавать рассылку.

### Видеоинструкция:&#x20;

{% embed url="https://www.youtube.com/watch?ab_channel=Salebot-%D0%9A%D0%BE%D0%BD%D1%81%D1%82%D1%80%D1%83%D0%BA%D1%82%D0%BE%D1%80%D1%87%D0%B0%D1%82%D0%B1%D0%BE%D1%82%D0%BE%D0%B2&v=9a7P4G_aBxM" %}
