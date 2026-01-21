# IPtelefon

## Как подключить сервис

Для подключения Iptelefon к Salebot необходимо обратиться к своему менеджеру и  запросить у него полный адрес сервера, секретный ключ. \
Например,\
**server\_url = 'https://a00.abc.ru/b3/api/v2/start.php'** \
**secret = ‘1ySSeSSSgiS1S1111'**\
Далее в личном кабинете необходимо включить интеграцию **"Система" > "Магазин приложений" > "Salebot"** и заполнить данные для отправки результата звонка - секретный ключ и url вебхука (см. ниже в разделе настройка вебхуков)

![](https://lh6.googleusercontent.com/780GDRsFJqaAoQD6aXd6RkhBqNeTr0rHUfsJJkjB163_TI5OgWP85EtYIyh6dN16JQVXD9-JXNI-mnoMZRZysb5EdAT3kodZtihMhM58x_-10nuItKFtb93pKJwDGgiPT0-TrtVBt9zU7nKIQa42eFY)

Далее  полученные данные вводим в Salebot, вкладка Телефония, окно Iptelefon:

![](https://lh5.googleusercontent.com/UIbBbHVQYBDPERdISY7DtTF5U2FleOcRXDTZDemqt_oVdlQ66PEHrumCB6WIsZvWuemkEkXSLN9aMCDY0ksn88mcORBvZAuaHXa7OL99MSLeZEKxj2D1cxAEuFRemdD-yElCrtGwni-dMHVaQFBF2ZU)

![](https://lh3.googleusercontent.com/5M0U6Hag85kgNmE2m7MFJpMSb0Vfclpby8geol6nn-BXHL069V_Q9e3p-BV2CcCMBiaB-qRm_lhbE8FnEWplNAIicHfCy4kZwz7XX2oNuSr_kpO1OYLsGYGXvccgogl7-Y6h0h-ZTw3qEWq7ZvjeyiI)

Iptelefon подключен! Но для успешной работы с телефонией требуется настройка под сотрудников и групповые звонки. Всю необходимую информацию для этого можно запросить у своего менеджера. \
Для совершения обратных звонков понадобится короткий номер сотрудника, например, ‘346’, а для совершения звонков группе понадобится указание номера группы, например, ‘3’

## **Как происходит сопоставление клиента**

Для работы с телефонией используются номера в формате 71234567890 (должен начинаться с 7( или с иного кода другой страны, например, 375), состоять из 11 и более цифр и не иметь лишних знаков и отступов).

Последовательность сопоставления данных о клиенте: \
1\. Осуществляется поиск клиента Телефонии. Если клиент не найден, то происходит поиск по значениям всех переменных по всему списку клиентов проекта. Первая найденная запись о клиенте считается тем самым "искомым" клиентом. \
2.Если клиент не найден среди клиентов Телефонии и:\
\* Если к проекту подключен любой мессенджер, например, Whatsapp, то будет создан клиент Whatsapp с данным номером телефона. \
\* Если к проекту не подключены иные виды мессенджеров (Whatsapp, Viber, Instagram и т.д.), то будет создан клиент Телефонии. Такому клиенту Вы сможете совершать только звонки с получением информации о них. Написать такому клиенту возможности нет.

## **Функция Salebot заказ обратного звонка**

Для того чтобы совершить звонок сотруднику из бота, необходимо использовать функцию **iptelefon\_employee\_call(client\_phone, short\_employee\_phone)** , которая принимает на вход следующие параметры: \
**client\_phone** - номер клиента, которому должен быть совершен звонок, строка, пример - '79004443322'. \
**short\_employee\_phone** - короткий номер сотрудника в системе Iptelefon, строка, пример - ‘346’&#x20;

Пример использования функции:

![](https://lh3.googleusercontent.com/jq4wez0bzisKlezqZCerxxTkbyra48dyL32o8EepKHXgfB0Xs8vcg3E2Er_VOq_ui0sNz6yK58328kz-i1OpAI11eCpioLyJWVckzLMcRoEJPqac006_xTta-mea-hLY8E2q3QB6bvxjevcAmodSzxM)

## Функция звонок группе в Salebot

Для того чтобы совершить звонок сотруднику из бота, необходимо использовать функцию **iptelefon\_group\_call(client\_phone, group\_id)**, которая принимает на вход следующие параметры: \
**client\_phone** - номер клиента, которому должен быть совершен звонок, строка, пример - '79004443322'. \
**group\_id** - идентификатор группы в системе Iptelefon, строка, например, ‘3’&#x20;

Пример использования функции:

![](https://lh5.googleusercontent.com/KxM2dqbZhfgifKb-QY0357dpE8438U57OFwiuqC-p6TaDPTvBwVVICuw8UlXxFaQ9JrNJnfLSvTJZlVzs9xJp04kavwWgb1UQ4D1akUPFcwwiKIE3FgF9_Smdb-FXBUMEGOqIzXjVPUpQJJ8d4Ppji0)

## **Настройка звонков из карточки клиента**

Для настройки возможности осуществлять звонки непосредственно из карточки клиента введите сотрудников в систему Salebot. После регистрации сотрудника зайдите в редактирование его данных.

![](https://lh6.googleusercontent.com/fT_65egkW1W2idXqKTyqrQy10PKBLZjY-4dVAwGvHMGsvPygautnyRQUboMJFz39JBmE0fTFGBOhbv2Gp6ZpbiUnEG0Ny4cuISaffQ602sWlVayPzMAd6-vDINlFmQ49luPC-s5Jt2aEto8mQrt6UFg)

В позиции **“Способ совершения телефонных звонков”** выберите звонки по API Iptelefon.&#x20;

* Если выбрать пункт **Отключить звонки**, то этот сотрудник не сможет совершать звонки и иконка телефона возле номеров телефона у него не будет отображаться.&#x20;
* **Звонки через приложение** - при нажатии на иконку телефона звонок будет перенаправлен в приложение, установленное для звонков на Вашем устройстве (Zopier и тд).&#x20;
* **Звонки по API Iptelefon** - при клике на иконку телефона АТС звонок поступит сначала сотруднику, чей id вы указали в карточке, а затем перенаправляет звонок клиенту.&#x20;

После выбора способа совершения телефонных звонков в “Звонки по API Iptelefon” появится дополнительное поле, в которое следует вписать короткий номер сотрудника в системе Iptelefon:

![](https://lh4.googleusercontent.com/acksRa31GG-lMX6pRB12sGeFCZFbvmACdn-zoTvfwhjNRl0XfjOGi4yT7lgbvjBZtEXI355dHhqt4CknKtWrT_rRC07jTvthyl_TPY-10S0jtQJAldguxDQCN18_pOYYQYH4V5YWxJwoLJRZs1nttw0)

Для осуществления звонка выбранным методом достаточно в карточке клиента нажать на иконку голубой телефонной трубки рядом с его номером телефона:

![](https://lh3.googleusercontent.com/OB9LzlnfmDXdKSU9ehWvvM9Y3fEYgfk-UJWu9_XXlax1T9RMMoJBqHzAciiYJ2V22xJCxlpFPUfAoPjMoFeOysDDw0ig5azfsY2qQy9yCV7XoQDlIETgDENjpQW_GRdk2_n7IrSJFv0_4qLzJOZaemU)

## **Настройка вебхуков**

Для того, чтобы настроить получение колбеков о завершении звонка, необходимо обратиться к менеджеру Iptelefon и попросить его прописать адрес для получения вебхуков по тип&#x443;**:** **https://chatter.salebot.pro/**&#x69;ptelefon\_webhoo&#x6B;**/<секретный-ключ>**, например, https://chatter.salebot.pro/iptelefon\_webhook/1ySSeSSSgiS1S1111

В результате при завершении звонков в Salebot будет приходить уведомление следующего вида:<br>

![](https://lh5.googleusercontent.com/zlyeXTYyCZhu8F3e5UI7DKwnDHKPoUCYG7Hy7KuQaE8W0po7LLoMgi2Fynxo8mWzE_MDQd3ec7bbNwropLJG_E0fCpXNyLaaLR38fWOfigpzi0IZRD1-CSp9C6s8TuLOYOE0lqO6ff_aRT69NJYiTT4)

При подключении функции **получение записи разговора** в переменные проекта добавится параметр **iptelefon\_call\_record\_link**,  в которой будет записана ссылка на запись разговора.
