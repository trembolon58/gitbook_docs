# Как переехать с BotHelp

## **Как переехать с Bothelp на Salebot?**

1. [Подключаем мессенджеры к Salebot.](../../chatbots/channels/)
2. [Создаем лендинги или сайты.](../../websites/builder/kak-sozdat-sait.md)
3. Изучаем схожий функционал сервисов: Ниже в таблицах приведены скриншоты некоторых одинаковых функций. Данные скриншоты помогут вам понять основные принципы настройки чат-ботов и авторассылок через Salebot.
4. Загружаем клиентов из Bothelp

## **Как перенести клиентскую базу из Bothelp**

Переходим в подписчики

Выбираем канал, который нужно выгрузить

<div data-with-frame="true"><img src="https://lh5.googleusercontent.com/sbc60e6lg9w3W1Co3SHmqONXsIWmMA-3a750TlFvk3WB2hRCzHis-8PWSTxPcpm1-4dhJDO-EMCbQ4d-MApNAA8iLCAcKh0zHwGjf0rrFsrbSFnvg7R-1mAFmeO8V2d1cmmQNOFY" alt=""></div>

Жмем кнопку экспорт со всеми полями

<div data-with-frame="true"><img src="https://lh3.googleusercontent.com/o8Omr6I-Ph0cKaHOOVEAC1KkROq9i6PWkFa9OiMrk5z1iNGr0UeX1Y-hYVpMSYh8prGcywFOM2xmtOvJfiXF-viLN3F2KbtW9cmWnoFs_9_tNeGPSgzqWlkkeon3J7BDRYW-oz_Y" alt=""></div>

Скачиваем и открываем файл

<div data-with-frame="true"><img src="https://lh4.googleusercontent.com/N-A4AwAe01BuuavsIjW56jxHJhyY5NSa5_FQbC6c_ulEKoUe5XCWH-onHX0PzUxGI32GuJs_pEDJ9ttF8JVTLvBMR8slgYdxzINj-cXXz4lYqlRdhg2uFRzbs4hzEsLrnTIV59jS" alt=""></div>

Из полученных данных создаем файл csv

<div data-with-frame="true"><img src="https://lh6.googleusercontent.com/nrC52rhShRpBuYBtczujqn7HekVE0jkfGKiVYVl4VYnaH-GduDp752JTkQ3Fm8q4LTIWpfk0_bPHZt53Efn6ko97OxrK4J9pkrGgE8JjX7xRfSuPyEuDGaLrhbyyHAswXICANybe" alt=""></div>

Можно сделать в  Notepad++, для этого:

1. Выделяем нужные данные и копируем их
2. Создаем новый текстовый документ
3. Копируем туда нужные столбцы
4. Жмем Сохранить как
5. Имя файла пишем файл.csv (обязательно с расширением)
6. Сохраняем

Также можно проверить кодировку файла, если есть необходимость ее сменить.

<div data-with-frame="true"><img src="https://lh3.googleusercontent.com/a6QCK7vSRn7MUrRLs_AQwn__jzXDH0zvsgKOjbnG5V9u-E29hEkah1S1rg9oXwHr7MONTJRPNkZ1TvgDoCRzWK_B7_BpPUUilySLun9XAyaeqg0bwm8NV0CFkcQKCHnozVRIVP28" alt=""></div>

Открываем Salebot, переходим во вкладку "Каналы", где выбираем нужный мессенджер для загрузки список клиентов.&#x20;

{% hint style="success" %}
Как подключить любой представленный на платформе Salebot мессенджер, рассказали в разделе "[Подключение мессенджеров и каналов](../../chatbots/channels/)"
{% endhint %}

Далее увидим кнопку для загрузки списка клиентов:

<div data-with-frame="true"><figure><img src="../../.gitbook/assets/2024-01-08_16-31-47.png" alt=""><figcaption></figcaption></figure></div>

После нажатия на кнопку, открывается окошко загрузки файла, где выбираем кодировку и разделитель:

<div data-with-frame="true"><figure><img src="../../.gitbook/assets/2024-01-08_16-38-04.png" alt="" width="563"><figcaption></figcaption></figure></div>

Жмем готово.&#x20;

{% hint style="warning" %}
Рекомендуем для начала попробовать это сделать с одним клиентом, если что-то пойдет не так, то 1 контакт проще удалить чем 1000.
{% endhint %}

## **Как соотнести типы сообщений**

### **Обычное текстовое сообщение**

<div data-with-frame="true"><img src="https://lh4.googleusercontent.com/AV6-tnQBBlo7TgFpBCrk7VquXxH-qrpMYBWPkgShO3-1bQP4SVSXovhFKn3HTRJoFWnQl7_HPWTbWqNnuqJR46GHGSiEmFomwZ_59qPSEVkr5H7L_U5ztvsyMQlpWeTIW3t-ovsU" alt=""></div>

<div data-with-frame="true"><figure><img src="../../.gitbook/assets/2024-01-08_15-46-30.png" alt=""><figcaption></figcaption></figure></div>

### **Сообщение с кнопками инлайн**

<div data-with-frame="true"><img src="https://lh6.googleusercontent.com/WYWSBYUcBNzLxs8BdfGrobDxDuCppCYTk8fMTwakJeCH0fiHgFpVKXIQMp-zIvQR3M93qQm-YlW4KQwbTgzczUn64XpwC475Tjxr7vxMvRn_NTMoXef7Qkac0xtlUsFA_TWWv2xj" alt="Пример с BotHelper"></div>

Инлайн-кнопки вставляются в настройках блока:\
нажмите на блок с сообщением, в которое нужно добавить кнопки, затем в окне справа нажмите “настройки кнопок” и в поле “расширенные настройки кнопок” вставьте _\[{"type": "inline", "text": "название вашей кнопки", "line": 0, "index\_in\_line": 0}]_

<div data-with-frame="true"><figure><img src="../../.gitbook/assets/2024-01-08_15-50-30.png" alt="" width="563"><figcaption></figcaption></figure></div>

{% hint style="success" %}
Про подробные настройки и возможности кнопок, а также их виды рассказано в одноименной статье "[Кнопки](/broken/pages/xeepnRj969zW3xRimkdg)".
{% endhint %}

### **Сообщение с кнопками в тексте и клавиатурные кнопки**

Основное различные кнопок в тексте и клавиатурных кнопок в том, что клавиатурные исчезают после нажатия или ввода текста с клавиатуры, а кнопки в тексте - не пропадают после нажатия.

<div data-with-frame="true"><img src="https://lh5.googleusercontent.com/wkq7rtd318Him_jWuXY4ofTnn8Ql6Vyo2KL7OcRuUmzwaPKhOzuqQoR1CqqWCSNMlHs-DV4Vti2nO5gQdKyLDvm9Nuss9j8Bo6u-SkXXCTa1sW3q998ibHinQaqe_YlsNkdCg7bC" alt="Пример с BotHelper"></div>

В Salebot добавить кнопку с любой необходимой функцией можно в блоке, а также обозначить любое необходимое название. Для этого в блоке схемы выберите "Кнопки" и нажмите "Добавить кнопку":

<div><figure><img src="../../.gitbook/assets/2024-01-08_16-00-48.png" alt="" width="419"><figcaption><p>1) Добавляем функцию кнопки в блоке</p></figcaption></figure> <figure><img src="../../.gitbook/assets/2024-01-08_16-01-07.png" alt="" width="406"><figcaption><p>2) Добавляем саму кнопку</p></figcaption></figure></div>

Далее откроется окно с настройками кнопки, где можно выбрать ее функцию, а также прописать название и выбрать любой понравившийся цвет:

<div data-with-frame="true"><figure><img src="../../.gitbook/assets/кнопки.gif" alt=""><figcaption></figcaption></figure></div>

Далее при необходимости перехода клиента после нажатия кнопки в следующий блок, можно прописать условие с названием кнопки в стрелке:

<div data-with-frame="true"><figure><img src="../../.gitbook/assets/2024-01-08_16-11-44.png" alt=""><figcaption></figcaption></figure></div>

### **Сообщение с вложениями**

Настройка сообщения с вложениям для любого типа аналогична. Для этого перейдите в настройки блока, выберите "Вложение" и его "Тип":

<div><figure><img src="../../.gitbook/assets/2024-01-08_16-45-05.png" alt="" width="374"><figcaption></figcaption></figure> <figure><img src="../../.gitbook/assets/2024-01-08_16-45-25.png" alt="" width="368"><figcaption></figcaption></figure></div>

1. Вложение с типом "Ссылка";
2. Вложение с типом "Видеозапись";
3. Вложение с типом "Изображение";
4. Вложение с типом "Файловый документ";
5. Вложение с типом "Аудиозапись".&#x20;

В качестве примера выберем тип вложения "Изображение":

<div data-with-frame="true"><img src="https://lh5.googleusercontent.com/QzsgVjlhtAegD0rW2h3OC4Ooi4KTetqMfqydFqWDgFuGUoeeXWGAz4EwhcvU8BzXMF_Lgr-v8l6nhIA-vZr7B7cumcCnTHIW5ZKYoGEHeJ5yDLuGwf7bKp-pGOOgtcNQ0untPQns" alt=" BotHelper"></div>

Чтобы отправить сообщение с изображением, кликните на иконку изображения, где откроется возможность либо вставить ссылку изображения в поле URL, либо непосредственно его загрузить:

<div data-with-frame="true"><figure><img src="../../.gitbook/assets/2024-01-08_16-49-30.png" alt="" width="362"><figcaption></figcaption></figure></div>

Тестируем бота:

<div><figure><img src="../../.gitbook/assets/2024-01-08_16-53-15.png" alt=""><figcaption><p>Настройки вложения</p></figcaption></figure> <figure><img src="../../.gitbook/assets/2024-01-08_16-54-12.png" alt=""><figcaption><p>Тест бота</p></figcaption></figure></div>

Таким образом можно направить любое необходимое вам вложение. Для этого требуется сделать всего пару кликов.&#x20;

## **Какие есть типы переходов между блоками**

### **Сообщение-вопрос**

**Вариант 1.** Когда нужно запомнить, что ответил пользователь.&#x20;

<div data-with-frame="true"><img src="https://lh5.googleusercontent.com/POV4S2sOt6idd_41fbbbGjJEkU91-7_SlGLkmTIL5ZVSbUPVinRad3-RSXJQEQ8pAuqZfkTzdq5kA58PUyPrjzhYhnl218U8rhIQGTdGCmj1DYcTKZ5rs09O38De-bd3Sd_dLfE2" alt="BotHelper"></div>

Реализуем в Salebot: для этого в настройках стрелки нужно включить флажок “пользователь вводит данные” и в поле ниже указать, в какую переменную запишется его ответ.

<div data-with-frame="true"><figure><img src="../../.gitbook/assets/2024-01-08_17-00-05.png" alt="" width="563"><figcaption></figcaption></figure></div>

**Вариант 2** - выбор из нескольких ответов.

<div data-with-frame="true"><img src="https://lh3.googleusercontent.com/KUaWk_eNhzu_CRhHB65zGDaZUoiA1FJQ1fGLaGxPpBjeA_iSjWz4I3ycaCJq6zrBSJThD50cjMyqqtNTRSqeh_E6ojqH322uknMSUGGRCX_k0aNPOuWGF7gQpZqdQGLomkaxCN8O" alt="BotHelper"></div>

Функционал работает по аналогии с кнопками в условиях стрелок.\
\
Если вы используете в такой схеме инлайн-кнопки в первом блоке, то в каждой стрелке вам нужно отключить флажок “показывать как кнопку”.

Мы создадим кнопки в тексте, а дальше в условии каждой стрелки пропишем название кнопки:

<div data-with-frame="true"><figure><img src="../../.gitbook/assets/2024-01-08_17-08-19.png" alt=""><figcaption></figcaption></figure></div>

Как только клиент на жмет на любую из кнопок, он перейдет в следующий блок схемы в соответствии с со своим выбором.&#x20;

### **Отправить через**

<div data-with-frame="true"><img src="https://lh4.googleusercontent.com/zt_Xf6DIfRFG1h9WSnOVr8lkJPW-Jl8g4FX0lGAJjwC_AidqPhAAcMWq1tSC--k-U72ABv7K9RygtjmHPPbxciUdbigNgWpbITyLIhbaF15KOapAsSI80rR6RVtd44hg-hZBnnY-" alt="BotHelper"></div>

Настройки перехода по таймеру. Нажмите вверху окна настроек стрелки “настройки времени” и установите таймер, как показано на скрине ниже.

<div data-with-frame="true"><figure><img src="../../.gitbook/assets/2024-01-08_17-10-53.png" alt=""><figcaption></figcaption></figure></div>

### **Отправить завтра**

<div data-with-frame="true"><img src="https://lh6.googleusercontent.com/ZPtVom27pLLtBnjXOwOB8Rgq6zhhHbe80-yz2Ib1e1WfXOEC0wdLcn6ZyM6JCBUKq8IjstWVroA-2STFl-Axaxn32VGWfJJPZ81w3HHRiBMh6UHqJ7SdX63IMvi0s3aLG7840BCr" alt="BotHelper" width="563"></div>

Также в настройках времени отправки в стрелках. \
Для этого воспользуйтесь переменной _#{next\_day}_, вставьте ее в поле назначения даты.

<div data-with-frame="true"><figure><img src="../../.gitbook/assets/2024-01-08_17-16-39.png" alt=""><figcaption></figcaption></figure></div>

### **Добавить метку**

В Salebot клиенту можно присвоить метку, а также добавить в любой созданный вами список.&#x20;

<div data-with-frame="true"><img src="https://lh6.googleusercontent.com/sTW5LwMUDfAsNtOGimy6jbvEDYmmu5QRrOM19U77FpSPlZDKFdMfEOxViy9j8HrzS9Q50LxUGCblsJG65sdqeE1VPecSFZDHnaptrA1jLKOuKDaiwv9kQcXqxlx2_sdf2Szg9VvF" alt="BotHelper" width="563"></div>

Слева в разделе “_списки_” необходимо создать список (или метку). Затем в нужном блоке, в расширенных настройках выбрать “действие со списком” (например “добавить” будет означать добавить в список или присвоить метку) и в поле ниже выбрать название ранее созданного списка.&#x20;

<div data-with-frame="true"><figure><img src="../../.gitbook/assets/списки.gif" alt=""><figcaption></figcaption></figure></div>

Посмотреть всех пользователей из указанного списка (всех у кого есть эта метка) можно в разделе “клиенты”, поставив фильтр по названию нужного списка.\
Количество пользователей в каждом списке удобно смотреть в разделе “списки”.

Удалить метку (список) можно аналогичным способом с помощью добавления действия в блоке схемы.

<div data-with-frame="true"><img src="https://lh5.googleusercontent.com/pOx60j5CyvhB68EAQ1irfL4LLNwD3Okqw9PPXE863ivKGU4NVGK3OPe02nmIHbRvNX3knw40A8nGzVCOIvIoutY9xBhJJ4B151l1rCMhIDUylcZ6PvUMBmMhepAj-KZEFQg-Yp5X" alt="BotHelper" width="563"></div>

Если используете списки, то нужно выбрать “действие со списком” - “удалить”. Переходя в этот блок пользователь будет удален из указанного списка.

### **Действие установить/очистить поле**

<div><img src="https://lh5.googleusercontent.com/VzC7rOFm4rjznpry92IB09L7UKEHOksZjl9epRKgqWNFLMrOwxXSfzgyungVcX7kRfUe021vX5OFLEB-JhlCYwdO4Mxq3P46Limu6xtqHpMYZQ6JCvd4JOckeoZ3k21ppWLJtK1P" alt=""> <figure><img src="../../.gitbook/assets/2020-12-28_02-43-10.png" alt=""><figcaption></figcaption></figure></div>

Установить значение полю (а также очистить его) можно через переменную в калькуляторе в блоке схемы:

<div><figure><img src="../../.gitbook/assets/2024-01-08_17-33-01.png" alt="" width="392"><figcaption><p>Значение для поля</p></figcaption></figure> <figure><img src="../../.gitbook/assets/2024-01-08_17-33-54.png" alt="" width="397"><figcaption><p>Очистить поле</p></figcaption></figure></div>

### **Действия "Увеличить на" и  "Уменьшить на"**

<div><img src="https://lh6.googleusercontent.com/KrkcG5yPGqvrrDqNeMId5pCw7ON3_mi2d1r0qbUFXAKsnZ5ly37PcUj43_Bv8XuR4ZqtemkfE95lANtWq4BdEzRwkw1Lw-enyJDIH29FPTqJMAREc8sDT-l6Z7GXZHh_WIRqLoVq" alt="BotHelper"> <figure><img src="../../.gitbook/assets/2020-12-28_02-49-41.png" alt=""><figcaption><p>BotHelper</p></figcaption></figure></div>

Данные действия также можно осуществить в блоке схемы с помощью поля калькулятора. Для этого присвойте значение +1 или -1:

<div><figure><img src="../../.gitbook/assets/2024-01-08_17-37-34.png" alt="" width="407"><figcaption></figcaption></figure> <figure><img src="../../.gitbook/assets/2024-01-08_17-37-51.png" alt=""><figcaption></figcaption></figure></div>

{% hint style="success" %}
Описание полного функционала переменных рассказано в [одноименной статье](/broken/pages/-M1GeIkj_zt8NutUeaVF).
{% endhint %}

## **Как создать цепочки сообщений и авторассылок**

### **Действие добавить в рассылку**

**Вариант 1** - Ручная рассылка.&#x20;

<div data-with-frame="true"><img src="https://lh5.googleusercontent.com/cbHTI_L2shRYRqQKlgR8kSBVlh4UTYziTh-OowoJkGsmVlXXh1puZVE1tzIhLmoIXpRkXa6PRyrzD0nfNJenrAoeSI4UYpQEEY0RDF7Y3ApGsePXT00WVPkqDTo6OMlcBwO5StV7" alt=""></div>

Создайте блок с сообщением для рассылки или цепочку из нескольких блоков/сообщений, как на скрине ниже.\
Выберите блок, который нужно запустить в рассылку, в окне справа найти кнопку “создать рассылку” под кнопкой готово.\
Далее откроется окно рассылок, где необходимо выбрать нужную аудиторию из бота или загрузить созданный для рассылки файл с клиентами, запланируйте дату и время рассылки или оставьте их пустыми — если рассылку нужно отправить сразу.

<div data-with-frame="true"><img src="https://lh4.googleusercontent.com/QMUTik_wwUUIusffhjbdyMJT2ed8AUVSD-1RNhv03WOR5lNm-PO7in2hPHNJn_qhOj0kY2VVcJ_ic8q4DXv__rSy_1P0Anfp15DKVGfkDNV0ZKlPn0Q1VZnNPz1nwoINrGRaLXWF" alt=""></div>

Подробные настройки рассылок найдите здесь: &#x20;

**Вариант 2** - автоматически отправить рассылку всем кто дошел до нужного этапа в боте.\
Пример схемы показан на скрине ниже.\
Когда пользователь переходит в “этап 2”, его перекидывает (сразу или с нужной вам задержкой в настройках времени стрелки 2) в “блок ожидания”.\
В текст блока ожидания ставьте переменную _#{none}_ , тогда пользователю ничего не будет отправлено, но он перейдет в нужный нам блок и будет находиться в назначенные в стрелке 3 даты и времени рассылки.

<div data-with-frame="true"><figure><img src="../../.gitbook/assets/2024-01-08_17-43-59.png" alt=""><figcaption></figcaption></figure></div>

### **Цепочка сообщений**

На скриншоте серия писем, которая работает параллельно с другими цепочками сообщений, воронками, стрелками, блоками и тд.

Ее стоит использовать в случае, если у вас есть основной чат-бот в котором люди диалог ведут с чат-ботом, например заявки оставляют. И вам нужно вместе с этим людям рассылать серии сообщений). В остальных случаях можно просто использовать белые блоки.

{% hint style="info" %}
Клиент может находиться только в одном блоке (зеленые, белые, желтые, красные)
{% endhint %}

1. Создать цепочку из блоков Не состояние (светло-серые)

<div data-with-frame="true"><figure><img src="../../.gitbook/assets/2024-01-08_17-47-37.png" alt=""><figcaption></figcaption></figure></div>

2. Соединить блоки стрелкой с нужным таймером
3. Выключить переключатель Отменить сообщения с таймером (чтобы цепочка не прерывала другие сообщения с таймером в других блоках)
4. Включить переключатель Не отменять (чтобы другие стрелки не отменили это запланированное сообщение)

<div data-with-frame="true"><figure><img src="../../.gitbook/assets/2024-01-08_17-48-53.png" alt=""><figcaption></figcaption></figure></div>

В этой статье представлена лишь базовая информация о переносе чат-бота с Bothelp на Salebot. На данный момент функционал Salebot больше в десятки раз. Найдите время и изучите все страницы из обучающей платформы.

{% hint style="success" %}
Как создать простого чат-бота рассказано в [одноимнной статье](../../chatbots/builder/settings/main.md).&#x20;
{% endhint %}

Также у нас есть тех. поддержка клиентов. И очень дружелюбный чат в ВК, в котором вы можете задать свои вопросы о работе функционала, попросить помощи или помочь кому-то.
