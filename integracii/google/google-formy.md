---
hidden: true
---

# Google-формы

{% hint style="danger" %}
**ОБРАЩАЕМ ВНИМАНИЕ! УСТАРЕВШАЯ ИНФОРМАЦИЯ!**&#x20;

Методы, описанные в данной статье, больше не поддерживаются!&#x20;

Рекомендуем использовать конструктор сайтов и сайты Сейлбот.&#x20;

Подробнее в документации в разделе "[Конструктор сайтов](../../saity-dlya-biznesa/konstruktor-saitov/)".
{% endhint %}

{% hint style="warning" %}
Запрос к Google -формам входит  в суточный лимит сообщений.
{% endhint %}

{% hint style="info" %}
Данные обрабатываются только в том случае, если клиент уже есть в боте и ему была отправлена ссылка на заполнение формы. Это означает, что если заполнить форму перед попаданием в чат-бот, то данные из формы не попадут в Salebot.
{% endhint %}

## Как отправить данные из Google Form в бота

Сначала создайте форму как обычно, а потом добавьте в конце формы вопрос и в поле **Вопрос** введите **“client\_id”** как в примере или, если есть желание скрыть факт передачи некоего идентификатора, по которому можно узнать пользователя, введите **“Номер анкеты”**.&#x20;

![](https://lh6.googleusercontent.com/j8kwex5VEV7O5afKa2u4Pv1X1wsb2OOoQzkmm9EmlO-1mxgzAed4cldyJK02tPMIb5lG7U8-uTh1Gb3wyG-Hl6_g1yIIBHkhRXE5RO-9OsoGM4fktI9rHTxCtRECbHIzGHdbPJkq)

После этого добавьте описание. Для этого нужно нажать на 3 вертикальные точки и выбрать в списке пункт **Описание**.

![](https://lh6.googleusercontent.com/NC_EwADhm9COXpFwXX2OerZ33WkEj2MDLKZd2-glqJeWE_dn3Ire04gEFLTMiljEPNmr80RrZ9ZQBUpzZi_27ipdun5vot5-RTeSpwk9VBN7t9ntULtpmxa7D13wHsrSejQ2s3kq)

После чего напишите в появившемся поле текст, предупреждающий клиентов, что это поле трогать не нужно, а также сделайте этот вопрос обязательным. В это поле будем добавлять идентификатор клиента в salebot - **client\_id** .

![](https://lh3.googleusercontent.com/LATi9g--DCemfqZWNTkVBzfQjzhRchCnIseEFOJXME2ZBLR4d6vp1cY_aLOsLMVGlK8pNKNTvJybo3kZJwwIJKSIrMTNfFY8dQHDnLwD-QwTY8xsXKc4pH_RXC8kOS0YLL2rDb6i)

Следующим шагом загрузите скрипты, следуя рекомендациям ниже, и после этого создайте триггер, который будет отправлять результаты заполнения формы в бот. \
\
Если скрипты еще не будут заданы, то создать триггер вы не сможете и выбрать функцию при его создании будет невозможно.&#x20;

### **Установка скриптов**

{% hint style="danger" %}
**ОБРАЩАЕМ ВНИМАНИЕ! УСТАРЕВШАЯ ИНФОРМАЦИЯ!**&#x20;

Методы, описанные в данной статье, больше не поддерживаются!&#x20;

Рекомендуем использовать конструктор сайтов и сайты Сейлбот.&#x20;

Подробнее в документации в разделе "[Конструктор сайтов](/broken/pages/F5coOJRGH75d0ZQLzkuN)".
{% endhint %}

Вам потребуются два файла:

1. [https://drive.google.com/file/d/1Cozn6QHwwHUWvPw6PctoBtqEub1do7A-/view?usp=sharing](https://drive.google.com/file/d/1Cozn6QHwwHUWvPw6PctoBtqEub1do7A-/view)
2. [https://drive.google.com/file/d/16tPU2VK66C8qu247lVkAgrh\_gs6nKpRh/view?usp=sharing](https://drive.google.com/file/d/16tPU2VK66C8qu247lVkAgrh_gs6nKpRh/view)

Затем зайдите в Редактор скриптов:

![](https://lh6.googleusercontent.com/pvnS5T3Iao2yi0Yk6WbdNaqvJqVsgYqkHIbXwFEsUzwK2tbZKkQ14TnMJub-QlSeqr2ACekN5uBnyts5i0I-RJXREFlvubWLe41wPYdtXha2dMWITQwgL1y_OoR8XFjRVHt-IPcM)

В Редакторе скриптов -> Триггеры добавьте новый триггер со следующими настройками:

![](<../../.gitbook/assets/image (83) (1).png>)

В нем в поле для ввода удалите все, что будет, и скопируйте туда полностью содержимое первого файла:

![](https://lh6.googleusercontent.com/HOwaQ9eILfHKDvNVoqwu5IzZMqt8m1bGh5btDCiEPlwPf5Ni7avjl60DrSURREdH54z0dIYM7Z8bj62GYB4OZbvn9UvY8GSIVv4ZeUpr9cyZFzuMM1UpI5D1Svy5ivJ1zYP6Jy3J)

Также добавьте файл HTML, нажав по указанной кнопке, и назовите его sidebar. После этого по аналогии удалите все содержимое и скопируйте в него содержимое второго файла.

![](https://lh3.googleusercontent.com/2hCK9ls7_K8-jI8OsTu2lP3fNg1QU2wzljdP6jODjbwC8oijIBlBnxVJo6CN775azsxirjkwIfjjkxrlpxsgzrWD85UwAx8Xw-q_RjpvOrrLQWayg6AW9PQlOGTLGAjIKZcbiAt6)

После этого нажмите на файл Код.gs и найдите строчку вида:

`var url = 'https://chatter.salebot.pro/google_form/Ключ_доступа_к_APISalebot'`

Ориентировочно это будет 46 строка. после знака равенства в кавычках записана ссылка. Нужно заменить `Ключ_доступа_к_APISalebot` на Ваш ключ доступа к API в проекте Salebot.

После этого строка будет выглядеть так:

`var url = 'https://chatter.salebot.pro/google_form/c3c5af1e34dd0603a3dfcf1cfbe35'`

Взять Ключ доступа к API вы можете в настройках проекта Salebot. Нужно зайти в настройки и в конце списка увидите это поле:

![](https://lh4.googleusercontent.com/RtIsafkxGx4ZQFbGd359OBzUJVYdEdq3zXgFWXhHNz3xcR1Xw5EC6vUuvCCNxDVk-pN4l7y0GnA1BLPANx5qv_uZWiiaZlzdihfrUjDxPM1ONw2ZZNuBEX7rmRz-Dt67sttgVONu)

После этого нужно назвать проект. Для удобства назовите его Salebot. Для переименования проекта нужно нажать на строку **Проект без названия**.

![](https://lh4.googleusercontent.com/Kf2ZbrWzlFUNtHgkqg0eaJ8i1Cc9nWpjQlAq-OwIurtxulYGqJZFBRsEsnqkCYqdXV1ukFDjaM4hzUbOCgaHOBxodFpqrb0rny97ll-0C-UaE8InVaQR-YPRmJeJDRGMWS9CPGyC)

После этого сохраните проект, нажав на иконку сохранить.

![](https://lh6.googleusercontent.com/mTtGblmkDpDr9QIiSvgFLwq-AWQ7_vwsy12wW-9q4w0eHRZFtDG1ixWdLKu8ntE3VFCVXAq8jcA-bE8DfsYkV3-InkslV9FyvB8wrJH5QSq37nGFrtlxZMb0sOu-CZQYa2S6lU9o)

После сохранения нажмите кнопку **выполнить**.

![](https://lh3.googleusercontent.com/SozgHEUIN5YjxgiV2BEgLq8mfFnc72yY-CwwubXrzjkZLaMztZbizkWhulBuxREhW12fxjXl9TDzsoN5ha0I_KayzLfOuqtTkyHqTLaWA7FrXDGAhCn5IiIsgEHYP7vTkvUGAGkQ)

Спустя некоторое время появится окно с запросом авторизации. Нажмите **Проверить разрешения**.

![](https://lh4.googleusercontent.com/Woj4WdaFvRZV5yvHpHaZ60VV90Nv7pdisgpfadXFbsbHp-YQqMG2YDPsE0nkxC1Zbauvk9IRWAICdJEgFgJyi3EuBNQkef211N2KNSTuK0ck8qtZCH1b5uwcjZ7reB369UuNy4P-)

Откроется дополнительное окно, в котором нужно выбрать аккаунт, где была создана форма. После чего окно будет выглядеть так:

![](https://lh4.googleusercontent.com/pvlJdwCT7Xm37VQBL_vKWV5Zfr63t2ZcJahasdtqy-7o3oY4rZykdnuBgNiYa8unwZrSr8_4S8Q7GSrFR2Idwn8sfr-7apDpsWQIVoX8AaFPM5Fb3ZNLwjbgzzqrCDsK8O1prbQ_)

Нажимаем **Дополнительные настройки**.

![](https://lh3.googleusercontent.com/1grWQrP0q93HjIbvMZTDXWDsCxPvwHzdj2Mh3IAbANpatKsxL0IiSuUFjp08cfnRPJhwmFHGbb-_hHpuin0bYTCsga9vQWcPDYGnTrcQrEg5VWe10479ImUvBji0xxJg9Nb2PCIo)

Выбираем пункт **Перейти на страницу "Salebot" (небезопасно)** и в нижней части нового окна жмем кнопку **Разрешить**.

![](https://lh3.googleusercontent.com/5hLmTfevg3-EMarN1AATxG1KMMnVshKs_P65aGeFY02TbP0hnkD_RPJhNgFS1QvgfjEwU8Z46RP4rdALGR4BdoRa-KZtTJ5TAEOY4dMYJZWfQoiGdkpjbSSlzjrZgUX9Eg5GXNuL)

После этого вернитесь на окно со скриптом и увидите такие сообщения.

![](https://lh5.googleusercontent.com/FHAchdqRVy_A13zAOqWfWR4ZZsdTnqfegsh3NHvTtSKhDBNozCrtOzku7xPGAMs1zmLhFVm0cWZvT0JDPEMMSBl9d5StjiAXHFSZ3MPEI9P5c0GLpAFpWt2NhaSbBjKA6p6DbkLc)

Осталось подключить скрипт. Вернитесь на страницу формы и обновите страницу. Должна появиться иконка, при нажатии на которую появится надпись **Salebot**. Нажмите на название левой кнопкой мыши.

![](https://lh5.googleusercontent.com/ggAAOgpEin7GwuDXdbUNZ6_em6PPQTDKNL-fT1x28REPo2NJG2x-2NWvBrZ-ABF0vBZ90vaSs6Gihx3aKwMEA1QcSoHsB_LGbxR7vC_3jl1zLf-el1OzqX63I2_CYn-E7l_j1kIA)

В появившемся окне нажмите на пункт **Установить**.

![](https://lh4.googleusercontent.com/nQRbwNxwlivcllgIgKg93TQUsEw74VT46jEz5m7drZCMFlF3HqIBGGyJb8qvBkK327x19Pa5wavs64b2A_Z_LdKrOLNcHoNKWVhtHrEKUMU5gr2FwV0RdXa47Pmh8BgfXg)

### Как настроить автоматическое заполнение client\_id

Прежде чем переходить к следующему шагу, обратите внимание на ссылку той страницы, в которой сейчас работали. Она имеет такой вид: https://docs.google.com/forms/d/**1lKSCvTfQb54DtFkk1YQGKj\_WxOUrPPU6dhBvM6mDGPw**/edit

Выделенная часть - это идентификатор опроса, который позволит отличить ответы на разные формы между собой. Именно эта часть ссылки при получении колбека после отправки формы попадет в переменную **google\_form\_id** .

Чтобы получить ссылку, перейдя по которой это поле заполнится автоматически нужными данными, перейдем к созданию образца заполнения. Для этого нажмите на три вертикальные точки в верхнем правом углу окна редактирования формы и в открывшемся списке выберите пункт **Создать образец заполнения**.

![](https://lh5.googleusercontent.com/gKsXpGL1mBp9I7QLVAki9-k7NB1wnzg9uz78S-Z6bal6r5jSanlD85dCkJmnQjEeDdk3QJzGEX2sXAYcD7kmHDNr_ca0VtwmHjE516jLwQADoC2UtfdeisbNnQjlZvNhDR69GzPb)

В открывшемся меню введите любую информацию в качестве ответа на вопрос **client\_id** после чего нажмите кнопку **Получить ссылку**. Обратите внимание на подсказку слева внизу.

![](https://lh6.googleusercontent.com/8YQxZIZmuZofujv4JFKIkHFjhXJFmTjZ1EJ_JQQ7S8QDE1OMyDTAdYf_QmpQjtdJ6KquL8oRidobOA0RyGWm8OwdgmnRT3-1lHdPwb1OiObuYYW0MenrRK3rIy7aUbAqb6JP8bZW)

После этого подсказка поменяет вид:

![](https://lh3.googleusercontent.com/__Pe_p3xFj3OWWD31NYOg6ZdmMa8M8VeyNcZTia3Oq-cfyVTIpafJyY3Xukaaeds-moVBZY9y6xNmNwJcXrthr9PJua7ONkd-0rb5w8aB64zuKJc3K-WR3SyfO91JFn0ARlzPti2)

Нажмите копировать ссылку и получите ссылку такого вида:

[https://docs.google.com/forms/d/e/1FAIpQLSes-3-UbSrC6BHnEio0oti1CwdF433pwunVjHQWlSumTpp0Ww/viewform?usp=pp\_url\&entry.644014553=1](https://docs.google.com/forms/d/e/1FAIpQLSes-3-UbSrC6BHnEio0oti1CwdF433pwunVjHQWlSumTpp0Ww/viewform?usp=pp_url\&entry.644014553=1)

Нам нужна последняя часть ссылки **entry.644014553=1**. Это идентификатор поля и значение, которое необходимо в него поместить. При отправке клиенту ссылки на опрос необходимо в боте создать переменную ссылки, добавить к ней в нужном месте **client\_id**. Выглядеть это будет примерно так:&#x20;

google\_form\_url = ‘https://docs.google.com/forms/d/e/1FAIpQLSes-3-UbSrC6BHnEio0oti1CwdF433pwunVjHQWlSumTpp0Ww/viewform?usp=pp\_url\&entry.644014553=**#{client\_id}**'

![](https://lh3.googleusercontent.com/VTlDf-fPlAayPPYAkt8i1nG0E5rcDxedOTeCTnh4B1G6P8lW4XApPUt_D3291cNog11XSHxbrU0SztGtEmFAqjVbWsV1IrTbvbTFqr2mGZGusxUfLl2lYSLocgM9Yb7BJSXjm2KI)

Клиент перейдет по ссылке, заполнит форму и после отправки вы увидите результат в окне клиента.&#x20;

На коллбэк вы можете настроить реакцию бота (либо на любой колбек от форм, либо на конкретный опрос)

Имеет следующий вид:&#x20;

**google\_form\_received (неизменяемая часть) + идентификатор формы**

Пример:

`google_form_received` \
`1lKSCvTfQb54DtFkk1YQGKj_WxOUrPPU6dhBvM6mDGPw`

![](https://lh5.googleusercontent.com/unMc5woGYwcIp3yFhvSTbS1chznoADCGDj8Os-ZStBO7Bi8362UDt7HYrWsLfAJD6_mrwvXAblvxvglOzw5ElBNLNCF93PvqHl0DMDVIgucmAcEt09DQZOv_lA_5h9VJ58ZXvQYM)

Справа от диалога добавятся новые переменные:

![](https://lh6.googleusercontent.com/wT34wgZCnJwedhMvgHlK_gkl-4TOZC24sgk6r_gjj53j61L3vgo5UQagdon0TeLfbOyE9OdzsCUHKPF9FAy3Jqg9SjxVEYt1Rbyk95KcjYVujLWykzXVw2yyhIG04kqhi3eb8TK2)

**google\_form\_url** - ссылка на опрос с предварительно заполненным полем с client\_id

**google\_form\_id** - идентификатор формы, имеющая такой вид: 1lKSCvTfQb54DtFkk1YQGKj\_WxOUrPPU6dhBvM6mDGPw

**google\_form\_answers** - ответы из формы в виде словаря, чтобы можно было обратится к отдельным ответам, если это необходимо

**google\_form\_submission\_time** - время завершения заполнения формы.
