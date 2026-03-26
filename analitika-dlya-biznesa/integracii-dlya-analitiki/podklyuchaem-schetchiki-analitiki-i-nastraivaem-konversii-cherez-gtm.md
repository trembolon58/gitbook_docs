# Подключаем счетчики аналитики и настраиваем конверсии через GTM

### Создаем GTM

Переходим на сайт: [https://tagmanager.google.com/](https://tagmanager.google.com/)

Нажимаем кнопку Создать аккаунт

![](https://lh3.googleusercontent.com/3p2c-5YsPg-WQNtEZiqyioH4fdFdXhXh1X7_6cS6-bzfgo1fyMfx1Xuk2TpPj0is3VHYz7z_388PHXnhid72WeWnMdGMgyX0GseqzLjYpY0E5gmF2bW81UMM0-rkiLkUNw8BImaZ)

Заполняем поля

![](https://lh6.googleusercontent.com/9DEKBfq9kcvvW44c5LiJYOB1UNWA9X_20wP943PFIg1IW2QIQSWZN4NbZ8mBNQDLhrWSoczqrazk9Lk4X9qIbM8xJWawtA4YdiaaHAQqIWAtkBZreXLAqDuXg5KBjHebpqCUgQCh)

Ниже нажимаем кнопку Создать

Соглашаемся с политикой

![](https://lh6.googleusercontent.com/zoGyqOweH5gujyK4m2wiH-zQCa25gMqZtMnA61Hk5F5ZYopRSG_1788GyqXcEFS66PNtfKsmKNI3wX6ULcQIdqhPkZ8ryok61st3YEejzR_m0hjn9OTLsHjsnHtWiOXyaUjPEhfI)

Копируем коды и вставляем их в соответствующие поля минилендингов

![](https://lh4.googleusercontent.com/z9rkTTUob9e0bA_e_S9ogAOO3WYuko8aopz28wNXywUcH75kp8MlDkiuWLbli8abB6dJrn4Px_eLN9A12kmAGB9LVhDRE4DDSVoby7UAFDwTLgbCK3hGiyzc6mr_QvK4lLzNJ4Vx)

![](https://lh6.googleusercontent.com/hI7lMlz3LUDHjCMbqbC7Z70PrO11xAm_iBy07aRidYznXnQ1CdKWIXNV0iIbXsz3xFnzqxZZD3v-pawAFeYrUC6yRMmUgb78dy-6LGgMpoMGuzlQVWOozSR2BVtcGwx23e_XpyMx)

Сохраняем минилендинг и возвращаемся в GTM

Переходим на вкладку Администрирование и нажимаем Импортировать контейнер

![](https://lh3.googleusercontent.com/EzC3Z8aiAiQrfiH6wnulHX-6kyiq9woKKupPw5eX5T3T6_HYhIWibNJI257e3bRS-TXnCUvlAX2Shz17iDMUWI2Ahktkpq1r0Fnz445QbUMP6TNtXmdBKCc0tyZcgKz2UkIRBe4T)

Скачиваем готовый контейнер: [https://yadi.sk/d/0nFKXE4m71\_D7w](https://yadi.sk/d/0nFKXE4m71_D7w)&#x20;

Загружаем контейнер и выбираем существующую рабочую область.&#x20;

![](https://lh5.googleusercontent.com/x4aZGSxgg8V-bXM4YD7Wu0-FNjAcCJM1GZSTFiax31j9eTPaeM1MENfUa4Q7s1BEyYkjRQWrPtVfF6XjxIU3tUwkkRBbzHEGV1R0f3SAlTPTT4PflYUL6QWsecltgcvB9gLkyERC)

Выбираем область

![](https://lh4.googleusercontent.com/H6mQnQ-zp5cldGXRh_9nNxpuzhUQws9vCD5h_JzXTM6S50M5ZRDCMl42qkiYPM4Sy1ZCXdcRmP3Gvu5M3n1Q8Ur-ykkjZsfT3Mi8vO6wVIqnsQt0n8irlcO2lKumyKbnlZnBLH8o)

Нажимаем кнопку Подтвердить

![](https://lh6.googleusercontent.com/RiW1dTxBIfRxpCZC2fkOg_ZvWHimcmihwaTRqi9nij9f3adZKHY1Lxq4gFW48MVD3TWV-5rSv0iFVLWoArgYQDipQhg50DpRM27kMqaW3O8dTcJjRn06LjGLEwo0qShH_oJBYCmq)

### Настройка контейнера

Переходим во вкладку Переменные и редактируем значения в переменных.

Пример заполнения переменных<br>

| GA4             | G-PC7MJCCPBK         |
| --------------- | -------------------- |
| Pixel\_FB       | 240369497014143      |
| Pixel\_TikTok   | BTNH5G8RQH53JI5RA600 |
| Pixel\_VK       | VK-RTRG-502975-YdQG  |
| TOP\_Mail.ru    | 3192512              |
| Yandex\_Counter | 56644959             |

Открываем переменную и вставляем значение

![](https://lh6.googleusercontent.com/vYxs2y-o9xI6-dUhqb5WAm2CvfSv7-dZNDRGdpbq0gc0lKZzoGf7fMogmUm6TVOZhmOkq53iaBwX9fBZegSuLTGzBuFzaq9CFvKm5_FEUnM7Oe2DAeuCY6UzWnysdC3UWT65Whxa)

По аналогии делаем с другими счетчиками и пикселями

После заполнения переменных нажать кнопку отправить

![](https://lh4.googleusercontent.com/fWVatIWiYFrT_ySYYy6wFzXzw6HRFvVc_93z7JOVkPjRYL3Wm1ehvvOiyosLW2CsW3hNy7lXkuz4-G1xPa84I2ngF1rYllCh0XPoemqmi_F5dEJyy0ylAvOFcTxav377PRfZ2VWs)

### Принимаем события в других системах

Произвести необходимые настройки в различных системах аналитики.

События, которые передает GTM в различные системы аналитики.

| Название         | Цели и события                                                                                                                               | Настройки в системах                                                                                                          |
| ---------------- | -------------------------------------------------------------------------------------------------------------------------------------------- | ----------------------------------------------------------------------------------------------------------------------------- |
| Конфигурация GA4 | subscribe                                                                                                                                    | Создать цель на событие subscribe                                                                                             |
| Яндекс метрика   | ym(\{{Yandex\_Counter\}},'reachGoal','subscribe');                                                                                           | Создать цель на событие subscribe                                                                                             |
| ВКонтакте        | <p>VK.Goal('subscribe');</p><p>VK.Retargeting.Event('subscribe');</p>                                                                        | <p>Создать аудиторию на событие subscribe<br>В объявлениях включить отслеживание конверсий на событие Оформление подписки</p> |
| Фейсбук          | fbq('track', 'CompleteRegistration');                                                                                                        | Данные передаются автоматически, событие Завершенная регистрация                                                              |
| ТикТок           | Настраивается в рекламном кабинете                                                                                                           | Создать цели внутри кабинета на клик по кнопке                                                                                |
| Топ маил ру      | <p>var _tmr = window._tmr || (window._tmr = []);</p><p>  _tmr.push({ id: "{{TOP_Mail.ru}}", type: "reachGoal", goal: "subscribe" });<br></p> | Создать цели на событие subscribe                                                                                             |

Проверить отслеживание конверсий

На этом настройка закончена.

### Добавляем реакции (триггеры) на другие кнопки.

Данный шаблон отправляет события только при нажатии на кнопки: ВКонтакте, Viber, Telegram, WhatsApp

Переходим в вкладку Триггеры и нажимаем создать

![](https://lh3.googleusercontent.com/ufaYg3mfWCCAPV41PzgYuF7G-5j0ZYNvGiWHPQ-aCKCIyhNgQkYX49hemNYCVQDa11VrOyhM7XXwiDiADBzYXi6V6A1fVb1i_qB_2NnnH4AuTvicL-N5KYeA45E-N8DyRgwNvPXH)

Задаем название, нажимаем настройка триггера

![](https://lh3.googleusercontent.com/TQ-sn2bVCQmcY1qIDPY1-KhOaNEtEd5mKpFGzbdiQCjnqGVKfJF0F18_W5KbsJN3J1tws0w6vh98x70p2vjPG4wOIi8G431WG7XmtCnkgArlhDqtjvY6DNpCFWWVWKC26ekKjgLa)

Выбираем Только ссылки

![](https://lh5.googleusercontent.com/_miXI57Nw_ITX46uANEO5JR3Mw2w6UUx-LEtZWpXTbtxxkGEuh8Y2BK0nsxARiugD6zGoED0MkFqLUHwtxbuu5q1PLLSTaror8U9IeFP9rIE_ENQrJppHnz3Q0dZObnRoqCxdemP)

Выбираем Некоторые клики по ссылкам, в пустое поле вводим Class кнопки

![](https://lh4.googleusercontent.com/j3DPnBeu2TXXKOYuVflo7foSrj59U2bASMXq5omy9CFjT5sZLQLS3YfSLlXVtX5PrzXJN8Yo9S-Gig0qFGFq3k-aEX5PbYy-RoPZFpSWidPEZyPMlJ_PHHbu4ndhyxrxxS0t5Lad)

Находим свой class кнопки. Открываем наш минилендинг

Нажимаем правой кнопкой мыши на нужную нам кнопку, выбираем посмотреть код и ищем в коде class кнопки, как на картинке ниже. В данном примере это ok\_link

![](https://lh6.googleusercontent.com/F0yEKfrC0NIxM4yZJRVhHHVZ197jbuLlllbLai2xrQwVY858CJjU4jXN9mDTrKmbnZsTnzrWYWA0EVODLbXMyjLD_iH7T7_wQ4oBtwTifHPSQqPojainsT-HrlVRvb1mALTlKHh-)

Копируем его и вставляем в поле Click Classses содержит ok\_link и нажимаем сохранить

![](https://lh5.googleusercontent.com/tPyGe8MxmizuefLZUwLSOh0r5EqQJ86RfdIi2XqiIjUS4_775-EO__itGpu6aqrw5_ajaykfrXUrUBVJhGy8QfFiMD1gH1rUOtXGgPEuJogP_ipvO6CFe02Yf9RCqanRgpKr8l8q)

Переходим в Теги и редактируем Отправка целей и События ГА4

![](https://lh5.googleusercontent.com/H0-mqwoSSMs5zKGw9dlxRSxw7Mh2oeQ50-Ml53cyJOejKh6FYpt_4a1J6UtwHSgMkV0yC7rEJDQWLldA8mGUq2_YJqYkLOf2iBhC1rHI7tSuK8MbkSJGG934KAj4GS3F0vthfunt)

Нажимаем на карандаш

![](https://lh4.googleusercontent.com/-yBsm_jniYdeodc-oA9jsofx2oC9Wotw-fI7h8wYSjopVTnYJtry96_JFusLlxXFkc2V-EKozyXXV15IUzQJsGFlYXZI1l-xxUrh8ML-ukkd8g7AzTFXEQ6MPu7WF1V-MOfgAFgN)

Нажимаем на плюс

![](https://lh4.googleusercontent.com/4yC-aXa60HHs7B_snZNCWQ9OfAO8FQtnNMSgJ582yZc6F_gpL28TwggqyZHpR2_JyKXx0DQbq64Z0pGplQUnwFsz11b4yyi5bSEAfA0e0DCPTVSEsZ5O5BD7QnmyrX0VrYKOQRl7)

Выбираем необходимый триггер

![](https://lh3.googleusercontent.com/8RJGLOI6SVN0B4C9D1py7XMnHc5cLuFl6x739FaohOqOrGCHmyXD4t8zaXy5OkqGpIbv-VAgsLx4imo7d9Owef9j_OEV5fA7a4hRItkNrySoQWa2jN7IpbsNesMRnbj4I9ovkHyi)

Нажимаем кнопку сохранить

![](https://lh5.googleusercontent.com/YAgXb9JeOEiBvFdtI60D2DUWpBVCWH6SH58QcZ_JtmyyvcalYeFxN8c0nseYr9E84dkXx6X_wV2W7xwvnlNFN3ZcKSG3nX-DpgIaj-fQj1MGI7X4KmhTxAwCjVg-X60R8EqZHsHv)

Проверяем, что триггер добавился

![](https://lh5.googleusercontent.com/N_QhBUtn7MECgG2CvGWHzxLyZwSG7XVnMKgnzlVtEu-_yO3LPAUq-QovFPfOKSknxbPzUyaoPGrpIix4uhDUWxlcvD2NfOAb6Y4TCRn5Xi5hqIyQKi5uFb6kGj0NCgM9Hcg_8P8e)

Сохраняем GTM

![](https://lh3.googleusercontent.com/r8lwtmyVTfmqiGPr_QH6yqXOnBEtHR9htWGxi5yMdAgSaFaUeZ7NTmKK-Oi_396Mqz5MFzCN1TKQPYzMw5-gE-Y84AznyvGueYDsD1Ia10_fKYMLSyFHNseb9zc63ZreTPs8zKyi)

### Как изменить событие, которые мы передаем

Открываем тег Отправка целей и заменяем события, на которые нам нужно.

![](https://lh3.googleusercontent.com/C29vvm-78d2_cQcfYaos1HrKYJaKJXIjeZLViaRD_whnxGYrZlL_LUuTN0SESxOQLlIQuECzRoXFw6KG3BwHI4Zn_FSWQI8IFSXX9jpF68DoI4KbfqXazzwyuRs0mQq0crx7J5lo)

Аналогично заменяем в теге События ГА4

### Резюме

Чтобы изменения вступили в силу необходимо нажимать кнопку отправить в правом верхнем углу.

Также вы можете протестировать работу GTM, нажав кнопку Предварительный просмотр

![](https://lh6.googleusercontent.com/QcsoYHnoZ-XQdhuHwtjF0Hsz5xzUExWADzNznlSUhaR7a6Drnx3VLOOKrER9rRbbGIS3vmOEVIekEtnQZEadKjDCdsXI3JzdXQBrsNSnUU3Fj28IJX0ovEvNmuucldWXbNtPFxQy)

Указываете ссылку на свой мл и тестируете события. Сначала у вас подгрузятся конфигурация и коды счетчиков (тег файред). А после нажатия на любую из кнопок тег с Отправкой целей также станет файред. Это значит все настроено верно
