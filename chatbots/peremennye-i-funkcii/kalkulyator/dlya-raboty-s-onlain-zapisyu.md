# Для работы с онлайн-записью

## Получение информации о филиалах

Для создания воронки онлайн-записи и получения информации о филиалах проекта воспользуйтесь функцией get\_companies\_for\_booking.

Функция вернёт список с данными по каждому филиалу с услугами:

<figure><img src="../../../.gitbook/assets/Снимок экрана 2025-08-28 в 17.05.35.png" alt="" width="563"><figcaption></figcaption></figure>

Данные представлены в виде пары “ключ: значение” и состоят из идентификатора филиала (id), его наименования (name) и адреса (address).&#x20;

Функция не принимает параметров.

### Пример использования:

Вызов функции в блоке:

<figure><img src="https://lh7-us.googleusercontent.com/docsz/AD_4nXfie9FvjorsnTaTuVgx-Sa-5m1SeL45ew6WwxA6Lxi1N7IXOXSE0dnh4uVj4YoVHHhEUvhjPf5PBAruFCNuOeKTKWhdsoUzfwOpCOWfgS2JvLUbeP1HO-73pZML-LZb66lQ8nGC_rKC-J3Nogiz-fQLaj3p99_XGsS4Uut0PQ?key=KyjJFgzVYb53MOCGur8CUg" alt=""><figcaption></figcaption></figure>

Пример возвращаемых данных:

<figure><img src="https://lh7-us.googleusercontent.com/docsz/AD_4nXcYKmIuNGesi8idKs2vIuiwqunLaQu9rslCGgc1z58ljW9AJbDpAl-CYoI1u7Iu8V79reD-YzIgOSObFbrHFzSmfJMXYQ7h2S4XyhM65LfN0yUsj_PUB2YI3i4DBF3vHIOew6CbIS4b2demqMLgVK_ZkOy76TxnRIPVsUUtzQ?key=KyjJFgzVYb53MOCGur8CUg" alt=""><figcaption></figcaption></figure>

## Получение информации о должностях или категориях услуг

Функция get\_categories\_for\_booking)company\_id) дает возможность получить список данных о всех типах специалистов или о категориях услуг филиала.

Каждый элемент полученного списка состоит из идентификатора (id), наименования (name) и описания (description) должности или категории услуг. Данные представлены в виде пар “ключ: значение”.

#### Параметры:

<table><thead><tr><th width="310"></th><th></th></tr></thead><tbody><tr><td>company_id (обязательный) </td><td>идентификатор филиала, ожидаемый формат - целое число;</td></tr></tbody></table>

### Пример использования:

Вызов функции в блоке:

<figure><img src="../../../.gitbook/assets/Снимок экрана 2025-08-28 в 17.06.34.png" alt="" width="563"><figcaption></figcaption></figure>

## Получение информации о сотрудниках

Если вам необходимо предоставить информацию о сотрудниках филиала, воспользуйтесь функцией get\_employees\_for\_booking.

Вызов вернет список данных, содержащих идентификатор (id), имя (name), информацию (information) и должность (job\_title) сотрудников филиала.

Вы также можете отфильтровать сотрудников по списку услуг, должности или категории оказываемых услуг. Для этого вам необходимо передать в вызов функции дополнительный параметр service\_ids,  job\_title\_id или service\_category\_id.

#### Порядок следования параметров:

company\_id -> service\_ids ->  job\_title\_id -> service\_category\_id

#### **Параметры:**

<table><thead><tr><th width="287"></th><th></th></tr></thead><tbody><tr><td>company_id (обязательный)</td><td>идентификатор филиала, ожидаемый формат - целое число;</td></tr><tr><td>service_ids (опциональный)</td><td>идентификатор или список идентификаторов услуг, ожидаемый формат - целое число или список целых чисел в квадратных скобках через запятую, напр [844, 845]</td></tr><tr><td>job_title_id (опциональный)</td><td>идентификатор должности, ожидаемый формат - целое число;</td></tr><tr><td>service_category_id (опциональный) </td><td>идентификатор категории услуг, ожидаемый формат - целое число;</td></tr></tbody></table>

**Примечание:**

Если вы хотите получить всех сотрудников филиала, оставьте значения service\_ids, job\_title\_id и service\_category\_id пустыми.

* Пример вызова: get\_employees\_for\_booking(14275391)

Чтобы отфильтровать сотрудников по списку идентификаторов услуг, передайте его вторым параметром, а job\_title\_id и service\_category\_id оставьте пустыми.

* Пример вызова: get\_employees\_for\_booking(14275391, \[844, 845])

Если вы хотите отфильтровать сотрудников по должности, передайте идентификатор в параметр job\_title\_id, а service\_ids и service\_category\_id оставьте пустыми.

* Пример вызова: get\_employees\_for\_booking(14275391, “”, 1021)

Если вам нужно получить сотрудников, оказывающих услуги определенной категории, заполните параметры service\_ids и job\_title\_id пустой строкой, а в параметр service\_category\_id передайте идентификатор выбранной категории услуг.

* Пример вызова: get\_employees\_for\_booking(14275391, “”, “”, 1019)

### Пример использования:

Вызов функции в блоке:

<figure><img src="https://lh7-us.googleusercontent.com/docsz/AD_4nXdimX83P37_V7HH-Ps159KuuiXmmasGAfWKfYFBK4NbTdsk6atOAWcJVSrgaain4T-2F2ApQgUKWI87_VawNVPEgu_qAh624rwWtRxtzTuft7JFQlIFyYz7RzMUxHusfZaYIG-Lu2xzukF3tKVERhj_tvBqVgPJhYMqw0Zm?key=KyjJFgzVYb53MOCGur8CUg" alt=""><figcaption></figcaption></figure>

Пример возвращаемых данных:

<figure><img src="https://lh7-us.googleusercontent.com/docsz/AD_4nXdjfGy226vzyDvt1_0JHdr64UlknFwkO1l3ek7wLa8lhNsgg90QXovHClYaw8k5BbIy8slIrlSna7y5vlqk7JkWgnKbabTDxN0txN0y10-4wMWmHPDRUiWzXDbao__oNqBvAYsflGQS_DZ07nUa5lr1YibnbmydGqhDIvDxug?key=KyjJFgzVYb53MOCGur8CUg" alt=""><figcaption></figcaption></figure>

## Получение информации об услугах

Чтобы получить информацию о предоставляемых филиалом услугах, воспользуйтесь функцией get\_services\_for\_booking.

В результате вызова бот вернёт список с данными об услугах. Данные по каждой услуге содержат идентификатор (id), наименование (title), описание (description), стоимость (price) и длительность услуги в минутах (duration).

Вы можете отфильтровать результирующий список по категории услуг, по сотруднику или по категории услуг и сотруднику одновременно. Для этого при вызове функции необходимо передать дополнительные параметры service\_category\_id и/или employee\_id.

#### Порядок следования параметров:

company\_id -> service\_category\_id -> employee\_id

**Параметры:**

<table><thead><tr><th width="310"></th><th></th></tr></thead><tbody><tr><td>company_id (обязательный) </td><td>идентификатор филиала, ожидаемый формат - целое число</td></tr><tr><td>service_category_id (опциональный) </td><td>идентификатор категории услуг, ожидаемый формат - целое число;</td></tr><tr><td>employee_id (опциональный) </td><td>идентификатор сотрудника, ожидаемый формат - целое число;</td></tr></tbody></table>

#### Примечание к разделу “Параметры”:

Если вы хотите получить все услуги филиала, оставьте значения service\_category\_id и employee\_id пустыми.

* Пример вызова: get\_services\_for\_booking(14275391)

Если вы хотите отфильтровать услуги по категории и/или сотруднику, передайте соответствующий идентификаторы в параметры service\_category\_id и employee\_id. Для фильтрации по одному параметру, заполните пустой строкой значение второго параметра.&#x20;

Примеры вызова:

* get\_services\_for\_booking(14275391, 1018) - фильтр по категории услуг;
* get\_services\_for\_booking(14275391, “”, 512978) - фильтр по сотруднику;
* get\_services\_for\_booking(14275391, 1018, 463665) - фильтрация по обоим параметрам;

### Пример использования:

Вызов функции в блоке:

<figure><img src="https://lh7-us.googleusercontent.com/docsz/AD_4nXf_UIYeiaWyVVDBlaQU89sa4TPriucXc5OAsAh45vLNl9lat34z3RuCvQUTa8cdackzW0Ypb397ilmP9jwaapMNpQTvUkr5A0fA-eztroAuj08smtBX6QQUMcBmlSF479Mzvbf5NDjop1vFuJ6ySu84x8vWhnHqLeM8kyEX8g?key=KyjJFgzVYb53MOCGur8CUg" alt=""><figcaption></figcaption></figure>

Пример возвращаемых данных:

<figure><img src="https://lh7-us.googleusercontent.com/docsz/AD_4nXdUNkPPqd5ApoXI41Lt6zozlslD6SdW3IvYk6jnnxLkiHnmpxS3T9gyYIKEtzdg429QhzJgXzY_vWXl6aJTNmfKKYpRpPLDGxfXTmx8g8muj5BJELb_o7d_LdzP6MqMUvdu1iLJn8r27iL0MBO_hLRCPuN_z_0U4V4HWMaD?key=KyjJFgzVYb53MOCGur8CUg" alt=""><figcaption></figcaption></figure>

## Получение доступных для записи дат

После того как клиент выбрал услуги для записи, ему необходимо получить список доступных для записи дат.

Чтобы сформировать данный список используйте функцию get\_dates\_for\_booking.

Функция проверит наличие свободного для записи времени и вернёт перечень подходящих дат в формате “день.месяц.год”.

#### Порядок следования параметров:

company\_id -> service\_ids -> employee\_id -> days\_limit

#### Параметры:

<table><thead><tr><th width="308"></th><th></th></tr></thead><tbody><tr><td>company_id (обязательный) </td><td>идентификатор филиала, ожидаемый формат - целое число;</td></tr><tr><td>service_ids (обязательный)</td><td>список идентификаторов услуг для записи, ожидаемый формат - целое число или список целых чисел в квадратных скобках через запятую (напр. 842 или [842, 843]);</td></tr><tr><td>employee_id (опциональный)</td><td>идентификатор сотрудника, ожидаемый формат - целое число. Если оставить значение параметра пустым или передать пустую строку “” - ищет свободные даты у всех сотрудников, оказывающих полный перечень услуг из списка service_ids;</td></tr><tr><td>days_limit (опциональный)</td><td>количество дней от текущей даты, в числе которых осуществляется поиск свободных дат, ожидаемый формат - целое число, значение по умолчанию - 14 (дней);</td></tr><tr><td>max_dates_count</td><td>Позволяет ограничить количество дат в результате работы функции, указывается числом</td></tr></tbody></table>

### Пример использования:

Вызов функции в блоке:

<figure><img src="https://lh7-us.googleusercontent.com/docsz/AD_4nXfzx4i2Q8PcaGc-3k3yuo4YHSe93krexxhbzYwrQbruYQ1rMJbaX4hlC6ej6NJEZ1pZruzABbqpG0zCHGBUuIrRb3QGAS5n1ROsXcWgqOeE-m31IW1PWt0bhsw84_Qki5ODZ51RepvGxlGuT8L1Uwou_dIc8w6gwrPNJn-jLA?key=KyjJFgzVYb53MOCGur8CUg" alt=""><figcaption></figcaption></figure>

Пример возвращаемых данных:

<figure><img src="https://lh7-us.googleusercontent.com/docsz/AD_4nXdpScSHxXjiaFOkc-jsHuFsyIsxZ_KbSJetwnDhspO0LzL8ZdqLW70UGg7gzNmDUR92s2lPjmxuBJvAboa5dQAxoPJKSZtmap_1AQ2cy-POvUPMKpHBUNzOPwn263ZaA86ylRuS_7U5b7J4KN_-ojj6NR67LJMzaV8Pjekk?key=KyjJFgzVYb53MOCGur8CUg" alt=""><figcaption></figcaption></figure>

## Получение доступных для записи слотов

Чтобы получить список доступных для записи слотов, необходимо воспользоваться функцией get\_slots\_for\_booking.

Функция проверит наличие доступного времени в выбранную дату и вернёт список свободных слотов в формате “часы:минуты”, например \[“09:00”, “11:00”, “14:30”, “16:00”].

#### Порядок следования параметров:

company\_id -> service\_ids -> employee\_id -> slot\_interval

#### Параметры:

<table><thead><tr><th width="284"></th><th></th></tr></thead><tbody><tr><td>company_id (обязательный)</td><td>идентификатор филиала, ожидаемый формат - целое число;</td></tr><tr><td>service_ids (обязательный) - </td><td>список идентификаторов услуг для записи, ожидаемый формат - целое число или список целых чисел (напр. 842 или [842, 843]);</td></tr><tr><td>date (обязательный) - </td><td>дата для проверки слотов, ожидаемый формат - строка в виде “число.месяц.год”,  например “01.01.2024”;</td></tr><tr><td>employee_id (опциональный)</td><td>идентификатор сотрудника, ожидаемый формат - целое число. Если оставить значение параметра пустым или передать пустую строку - ищет свободные слоты в расписаниях всех сотрудников, работающих в выбранную дату и оказывающих полный перечень услуг из списка service_ids;</td></tr><tr><td>slot_interval (опциональный) </td><td>интервал в минутах между свободными слотами, ожидаемый формат - целое число, значение по умолчанию - 30 (минут);</td></tr></tbody></table>

### Пример использования:

Вызов функции в блоке:

<figure><img src="https://lh7-us.googleusercontent.com/docsz/AD_4nXc7GJ9EjdCro_idrF14dVYscslN653oUESQaAFjHBWZrSO8q4joGD95kXjFfaX-E2oRT_nLCdKNrGdN9j5wBVJFKOgiyG2ZGDJNjR-l3OAhvP2E0pPTA0dOiYD3WxGdxdD57bRO-UC3CoGVVO4XV3Cq5BNpc8cZ1S6S0lsnlw?key=KyjJFgzVYb53MOCGur8CUg" alt=""><figcaption></figcaption></figure>

Пример возвращаемых данных:

<figure><img src="https://lh7-us.googleusercontent.com/docsz/AD_4nXe6V_i1iPe4C6A6CDJPu6GNK4fFLzUzq4ktYRRf01jRRgvRl87Ir3hWs2GbWRsYatbz0o8srDyE6pHklrvZ129tilNr5fuR9C_lhQP75MO-_Mfi9JVgcTvHoldK6Y8dcZ_cQamJp2JDxBfA8OU3a9cDgPavncaz-9aU_p31qg?key=KyjJFgzVYb53MOCGur8CUg" alt=""><figcaption></figcaption></figure>

## Создание записи

Для создания онлайн записи используйте функцию create\_booking.

При успешной записи функция вернёт информацию о статусе совершения операции (status) со значением True и данными о записи (booking) в формате“ключ: значение”.

Данные о новой записи содержат:

* идентификатор (id),&#x20;
* дату (booking\_date),&#x20;
* время (booking\_time),&#x20;
* наименования услуг (services),&#x20;
* длительность записи (service\_duration),&#x20;
* общую стоимость (total\_cost),&#x20;
* имя назначенного сотрудника (employee\_name), его должность (job\_title),&#x20;
* наименование филиала (company\_name) и адрес филиала (company\_address)&#x20;

в формате “ключ: значение”.

#### Порядок следования параметров:&#x20;

company\_id -> service\_ids -> booking\_date -> booking\_time -> employee\_id

Параметры:

<table><thead><tr><th width="288"></th><th></th></tr></thead><tbody><tr><td>company_id (обязательный)</td><td>идентификатор филиала, ожидаемый формат - целое число;</td></tr><tr><td>service_ids (обязательный)</td><td>список идентификаторов услуг для записи, ожидаемый формат - целое число или список целых чисел (напр. 5 или [5, 10, 15]);</td></tr><tr><td>booking_date (обязательный)</td><td>дата записи, ожидаемый формат - строка в виде “число.месяц.год”,  например “15.01.2024”;</td></tr><tr><td>booking_time (обязательный) </td><td>время записи, ожидаемый формат - строка в виде “часы:минуты”, например “12:30”;</td></tr><tr><td>employee_id (опциональный)</td><td>идентификатор сотрудника, ожидаемый формат - целое число. Если оставить значение параметра пустым или передать пустую строку “” - записывает к случайному сотруднику, оказывающему полный перечень услуг из списка service_ids, если он свободен в указанное дату и время;</td></tr></tbody></table>

### Пример использования:

Вызов функции в блоке:

<figure><img src="https://lh7-us.googleusercontent.com/docsz/AD_4nXdb3Fq2gqGtJ-QK342Hr12Ckv-krW_04_uAeJsCcnKpCq_iTC8mAxXjXvc_UqOVAOfm7WGcHYlfcvZjImoZXoNuPYCctsZOPB35toHI4zWMmK-sr3GoEdujlh8YQRxXsF_qN-I836wsU3AKhMvP8t0KiF0h6syWhECIxsynkQ?key=KyjJFgzVYb53MOCGur8CUg" alt=""><figcaption></figcaption></figure>

Пример ответа об успешной записи:

<figure><img src="https://lh7-us.googleusercontent.com/docsz/AD_4nXfsZPfW9v1VoJqC3nNqtnlLQJS-KhAaEi3uUzhz26vYmcxajMRMwd7NnZVZB2LpmavglbNibSpAAJIlo0mbge1_K6rguZTf1tE4NxkBPmKQ1GCy0x47vzfkIV5DTN-R-RlYpMZ-bfAQ-vrZ_tEM6mugSbn0E5BAjHCVN2Gdmw?key=KyjJFgzVYb53MOCGur8CUg" alt=""><figcaption></figcaption></figure>

При создании записей и повторном запросе свободных слотов вы увидите, что списки сократились, например для 05.02.2024 больше нет слота на 18:00 (он был свободен только в расписании Виктории), а к Павлу Тихонову на мужскую стрижку и моделирование бороды теперь можно записаться с 9 до 14, так как общая длительность процедур равна 1 часу и 45 минутам, а в 16:00 у Павла уже есть другая запись.

<figure><img src="https://lh7-us.googleusercontent.com/docsz/AD_4nXfglzV1DHx8clVfshVMInDi9MOS6sAlPGG8Axr6FYKBAeINwRaj2gvJMRYNcec7ZmDCnFKYCkU64AQqz2mgMWxCnp4G4YPRPb6C9D9g9KLKFM2e2bCVpBA2refY_fChq-W1uNy196r5d8dNZUudGRg-2qgN9NX20lCteL8AZw?key=KyjJFgzVYb53MOCGur8CUg" alt=""><figcaption></figcaption></figure>

## Получение информации о предстоящих записях клиента

Актуальные записи клиента можно посмотреть, вызвав функцию get\_bookings\_info.

В ответ вернётся перечень активных записей, а также подробная информации о каждой записи.

Информация о записи представлена в формате “ключ: значение” и включает:&#x20;

* идентификатор записи (booking\_id),&#x20;
* дату (booking\_date),&#x20;
* время (booking\_time),&#x20;
* идентификаторы (service\_ids) и наименования (service\_names) выбранных услуг,&#x20;
* длительность записи (booking\_duration),&#x20;
* суммарная стоимость услуг (total\_cost),&#x20;
* идентификатор (employee\_id) и имя  (employee\_name) назначенного сотрудника, его должность (job\_title),&#x20;
* идентификатор филиала (company\_id)&#x20;
* наименование филиала (company\_name) и адрес (company\_address).

#### Параметры:

<table><thead><tr><th width="253"></th><th></th></tr></thead><tbody><tr><td>client_id (опциональный)</td><td>идентификатор клиента, ожидаемый формат - целое число. Данный параметр нужен, если вы хотите получить записи интересующего вас клиента, по умолчанию - идентификатор клиента в чате с ботом.</td></tr></tbody></table>

### Пример использования:

Вызов функции в блоке:

<figure><img src="https://lh7-us.googleusercontent.com/docsz/AD_4nXeKlJcFxIx3cc_3vb8g0MARiqu6iNE4eW8BEmVY21MjT74GxS2U7JKFaAn6Sia99v4kQ4O8HuHFYkQJs8jCNmtpZHIkKq1SZ3_3BCBSA7mCs_iXVk6Ucu8hWTOHN7mPa0J5LGG5QSRK8TSP9BEZracVVNQBZKuZkLJx36r_TA?key=KyjJFgzVYb53MOCGur8CUg" alt=""><figcaption></figcaption></figure>

Пример возвращаемых данных:

<figure><img src="https://lh7-us.googleusercontent.com/docsz/AD_4nXcHzfzRWdUXAmr-iwrHhcdpHYraOD--i4jjI5ftsc-KRzzEOOFArT3hKZE--WucI4m3_b2v0DK99dV4EL2BQ9d0U2q-2fGHM6RiCHX_YUl7kgI-SA4zJIHs4zFte6GhgQAMfUY9Qim4THusxMhKielEnXQuHzapLqmh_oZm?key=KyjJFgzVYb53MOCGur8CUg" alt=""><figcaption></figcaption></figure>

## Получение информации об услуге, которая назначена в активной сделке

функция get\_active\_order\_booking\_info() - функция без параметров, возвращает информацию о записи клиента на услуги из активной сделки в виде словаря

Информация о записи представлена в формате “ключ: значение” и включает:&#x20;

* идентификатор записи (booking\_id),&#x20;
* дату (booking\_date),&#x20;
* время (booking\_time),&#x20;
* идентификаторы (service\_ids) и наименования (service\_names) выбранных услуг,&#x20;
* длительность записи (booking\_duration),&#x20;
* суммарная стоимость услуг (total\_cost),&#x20;
* идентификатор (employee\_id) и имя  (employee\_name) назначенного сотрудника, его должность (job\_title),&#x20;
* идентификатор филиала (company\_id)&#x20;
* наименование филиала (company\_name) и адрес (company\_address).

## Изменение даты и времени записи

Клиент может самостоятельно изменить дату и время записи.  Для этого ему необходимо попасть в блок воронки, где происходит вызов функции modify\_booking\_time.

&#x20;При успешной операции, функция вернет информацию о статусе совершения операции (status) со значением True и сообщение (message)  “Booking time modified” в формате “ключ: значение”.

#### Порядок следования параметров:&#x20;

order\_id -> new\_date -> new\_time

#### Параметры:

<table><thead><tr><th width="300"></th><th></th></tr></thead><tbody><tr><td>order_id (обязательный) </td><td>идентификатор записи, ожидаемое значение - целое число;</td></tr><tr><td>new_date (обязательный)</td><td>новая дата записи, ожидаемый формат - строка в виде “число.месяц.год”,  например “16.01.2024”;</td></tr><tr><td>new_time (обязательный)</td><td>новое время записи, ожидаемый формат - строка в виде “часы:минуты”, например “14:30”;</td></tr></tbody></table>

### Пример использования:

Вызов функции в блоке:

<figure><img src="https://lh7-us.googleusercontent.com/docsz/AD_4nXcDyllYwQDcuLOWIAFTCHb4A765baTgyFrir86V0h3ja3OQpECP2D5TszmK-M_PbKmQRVbp1LFLUMc_JIU4m9562kGnWz9WILVhjpMhf1jZw5bOUXCuBbUasMKWeaTo0pATOPujX4QK6laEk2TlXPU6Qycc7xlih1KbEBxK?key=KyjJFgzVYb53MOCGur8CUg" alt=""><figcaption></figcaption></figure>

Ответ бота при успешной операции:

<figure><img src="https://lh7-us.googleusercontent.com/docsz/AD_4nXdKqYrp28WS18aq3-_0I_3iDJUc2FmzwsilP1-5do9jmVjjVJ3Igfflo9rMnU_KEWWdAUYSZtjp6B0bVxwBcc7P21RvWVIeCOEAq0pNEh1KYDxJATu71S1Fiil4gicJeFuq5MAcp7bnQdUqRf8kjrWMXuA2_Fl09tjKwEPI?key=KyjJFgzVYb53MOCGur8CUg" alt=""><figcaption></figcaption></figure>

Ранее занятый слот 16:00 теперь доступен для записи, а создать новую запись на аналогичные услуги теперь можно только с 11:00.

<figure><img src="https://lh7-us.googleusercontent.com/docsz/AD_4nXeM-8-vu5dfYf4DlMnzlWTk08tQm80ne-qTBJleANK0Mjn-TuZWyMbO13Hex4FzdwvCgQspNeErgWwQkTZIejzDWK1BItCGxrLpAi9D0XFx75rqFvUF9UChQ_LoZqUNozZzKwubmGkx7XSgsTm-_1CBORCt5Nidh5X4ohbx?key=KyjJFgzVYb53MOCGur8CUg" alt=""><figcaption></figcaption></figure>

В информации о записях клиента вы также увидите измененное время записи:

<figure><img src="https://lh7-us.googleusercontent.com/docsz/AD_4nXeCyMMrRSlqAdCpmu0-HWsS6iKxW6xHjdtcnZ2NjxLTaRy7W_w3mhyLZQ2PjZgpvbmHRnRML-5A6hTwHpgpLaTerklX-opM8_UTQAeuT-ev2bd7AvC6N1ynPf50EUVRs6m4hZU4YIKnWQRamRcGbror5uJ7ElZ2v2KPtX1NxQ?key=KyjJFgzVYb53MOCGur8CUg" alt=""><figcaption></figcaption></figure>

## Отмена записи

Клиент может самостоятельно отменить существующую запись. Для этого ему необходимо попасть в блок, где происходит вызов функции cancel\_booking.

Успешное удаление вернет информацию о статусе совершения операции (status) со значением True и сообщение (message)  “Booking deleted” в формате “ключ: значение”.

Порядок следования параметров:&#x20;

pipeline\_id -> order\_id

Параметры:

<table><thead><tr><th width="321"></th><th></th></tr></thead><tbody><tr><td>pipeline_id (обязательный)</td><td>идентификатор филиала, ожидаемое значение - целое число;</td></tr><tr><td>order_id (обязательный)</td><td> идентификатор записи, ожидаемое значение - целое число; идентификатор записи, ожидаемое значение - целое число;</td></tr></tbody></table>

### Пример использования:

Вызов функции в блоке:

<figure><img src="https://lh7-us.googleusercontent.com/docsz/AD_4nXdWFqf619l5j1eQoe4p6QCPqGGsqcyEefKLs5PJxPwecillJaxUnQSC5eHFcT2olsrM62PHJDVGyxeD6Tl2xg3id27f-p51spmVZFjlDhSwzw3TwMx-CbQT9n3fnjYLPCO4wlqtKdB0cd1W36dp9wXYg4gEVJh6eketyDUQ?key=KyjJFgzVYb53MOCGur8CUg" alt=""><figcaption></figcaption></figure>

Ответ бота при успешной отмене:

<figure><img src="https://lh7-us.googleusercontent.com/docsz/AD_4nXe7FcrjKQxzoEgo3wfMuUt0a9zkPVkb02ojx5pZ3KYWU5NfLazmLhgCaNxvigreYXXfzYFEhd5KyF7D3808VLBGl5Cte7YRXI0cWQK3J9ZV05G5y5XUIXGq1Arcac2KrPmHnCCakarcTFXd_9X5_4yYsI6j4rpMySaZr3lA?key=KyjJFgzVYb53MOCGur8CUg" alt=""><figcaption></figcaption></figure>

После отмены слоты “09:00” и “10:00” снова доступны для записи:

<figure><img src="https://lh7-us.googleusercontent.com/docsz/AD_4nXcRLLDJ0un8QPUj11yC8VDy2TlbbgUHuDd13YSQ3AZU3ey4Cg00SMEke5LFPKWGHR8em7BWHiH8l-bSqGICNAU5CP9ORBGI9CFMKziB0JQLZA0QUvYJ8q-SXXQGQsPCnEWdNrDZ1G7bZupR4zOLgGpJt9TgZBxG_R1MPf9f?key=KyjJFgzVYb53MOCGur8CUg" alt=""><figcaption></figcaption></figure>

## Для работы онлайн-записи с AI-ассистентом

### Для работы с переменной и знаниями бота

get\_info\_for\_booking() - функция без параметров, предназначена для чтения данных по услугам настроенной онлайн-записи.&#x20;

Функция не принимает параметров.&#x20;

### Пример использования:

Для начала нужно подготовить блок для обновления информации обо всех услугах после заполнения настроек филиала в разделе "Услуги". Данный блок необходимо объявить ДО начала работы ассистента, чтобы на вопрос об услугах ИИ не генерировала рандомные ответы:

<figure><img src="../../../.gitbook/assets/2024-06-18 17.19.04.jpg" alt=""><figcaption><p>Рис. Первый блок</p></figcaption></figure>

Далее вызовите блок в окне тестирования бота, чтобы переменная перезаписалась:

<figure><img src="../../../.gitbook/assets/2024-06-18 17.20.43.jpg" alt="" width="425"><figcaption></figcaption></figure>

После чего вы увидите в переменных проекта в разделе "Настройки проекта" указанную переменную со значением услуг для онлайн-записи.&#x20;

<figure><img src="../../../.gitbook/assets/image_2024-06-18_21-13-05.png" alt=""><figcaption></figcaption></figure>

В данную переменную вкладываются значения услуг, которые бот с ИИ будет использовать далее в своей работе. Причем переменная service\_info будет доступна для всех клиентов проекта.&#x20;

Далее переходим к настройке следующего блока:

<figure><img src="../../../.gitbook/assets/2024-06-18 17.24.14.jpg" alt=""><figcaption><p>Рис. Второй блок</p></figcaption></figure>

Данный блок преследует следующие функции:

а) его вызывают в настройках ассистента для формирования записи с использованием переменных по услугам;

б) он создает запись клиента;

в) обновляет переменные проекта после записи: то есть убирает уже несвободные окошки в графике.&#x20;

Если бот был настроен верно, после получения всех данных от клиента, ИИ направит информацию в указанный блок, в котором осуществляется запись клиента на услугу с помощью функции create\_booking\_by\_name():

<figure><img src="../../../.gitbook/assets/Снимок экрана 2024-06-18 в 17.31.43.png" alt="" width="563"><figcaption><p>Рис. Второй блок</p></figcaption></figure>

В параметры create\_booking\_by\_name() записываются значения, собранные ботом.

Поскольку информация о доступных слотах уже будет неактуальна, с помощью той же переменной и вложенной в нее функции происходит обновление доступных дат и времени на запись:

<figure><img src="../../../.gitbook/assets/Снимок экрана 2024-06-18 в 17.32.42.png" alt="" width="563"><figcaption><p>Рис. Второй блок</p></figcaption></figure>

{% hint style="warning" %}
Обращаем внимание!

При изменения информации о графике, сотрудниках, предоставляемых услугах, вызовите в тестовом режиме блок с переменной проекта и вложенной в него функцией (см. рис. Первый блок).&#x20;
{% endhint %}

### Для создания записи в CRM

Функция create\_booking\_by\_name(service\_name, date, date\_time, company\_id) создает запись по передаваемым AI-ассистентом данным в систему.

Функция принимает три обязательных параметра для формирования записи:

<table><thead><tr><th width="297">параметры</th><th>описание</th></tr></thead><tbody><tr><td>! service_name</td><td>обязательный параметр, название услуги</td></tr><tr><td>! date</td><td>дата в формате дд.мм.гггг</td></tr><tr><td>! date_time</td><td>время услуги в формате чч:мм</td></tr><tr><td>company_id </td><td>ID филиала, необязательный<br>Если указан, то запись будет создана на услугу с указанным названием, которая принадлежит именно этому филиалу<br>Параметр может понадобиться для случаев, если в нескольких филиалах есть услуги с одинаковым названием. </td></tr></tbody></table>

<figure><img src="https://lh7-us.googleusercontent.com/docsz/AD_4nXdG79FHAftyPBgsMqSROJXVm-yhnavQEQIYP19GvaCp7CALHwVa-KYn4LjkEtjryrSprn4DAvLtFzOasbShegmz1_ivq-sK97SdXIsU2qqyDxo-4q-HyB6hSHoMOGA4KrY12bWhRQBHfMGRdGecySbGs9Gy?key=g9-j53ENQsA_W1hDFrramA" alt=""><figcaption></figcaption></figure>

<figure><img src="../../../.gitbook/assets/Снимок экрана 2024-06-19 в 18.06.04.png" alt="" width="375"><figcaption></figcaption></figure>

{% hint style="info" %}
Подробнее о том, как создавать [чат-бота с ИИ для онлайн записи](/broken/pages/5Sy40v9I0JB04H9dIJ4V), читайте в одноименной статье
{% endhint %}
