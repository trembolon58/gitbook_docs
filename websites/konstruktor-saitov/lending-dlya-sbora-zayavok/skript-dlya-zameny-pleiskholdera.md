# Скрипт для замены плейсхолдера

{% hint style="success" %}
Обращаем внимание!&#x20;

Данный скрипт необязателен для использования в настройках вашего сайта.&#x20;

Поменять плейсхолдер вы сможете в настройках контента без применения скрипта
{% endhint %}

<figure><img src="../../../.gitbook/assets/Снимок экрана 2025-07-16 в 13.18.04.png" alt=""><figcaption></figcaption></figure>

## Работа со скриптом

Нажмите на лендинг (форму), где нужно заменить плейсхолдер:

<figure><img src="../../../.gitbook/assets/Снимок экрана 2025-07-16 в 12.57.55.png" alt=""><figcaption></figcaption></figure>

Затем в основных настройках лендинга с формами, перейдите в настройки:

<figure><img src="../../../.gitbook/assets/Снимок экрана 2025-07-16 в 12.51.48.png" alt=""><figcaption></figcaption></figure>

Далее вкладка "Цвета, шрифты и HTML":

<figure><img src="../../../.gitbook/assets/Снимок экрана 2025-07-16 в 12.54.04.png" alt=""><figcaption></figcaption></figure>

В поле JS-код вносятся следующий скрипт:

`document.addEventListener("DOMContentLoaded", function () {`&#x20;

`var input = document.querySelector(".name_input");`&#x20;

`input.placeholder = "Новый текст placeholder"; })` &#x20;

<figure><img src="../../../.gitbook/assets/Снимок экрана 2025-07-16 в 12.56.10.png" alt="" width="563"><figcaption></figcaption></figure>

<table><thead><tr><th width="308"></th><th></th></tr></thead><tbody><tr><td>name_input</td><td>замена в поле запроса имени </td></tr><tr><td>phone_input</td><td>замена в поле запроса телефона </td></tr><tr><td>email_input</td><td>замена в поле запроса почты </td></tr><tr><td>ml_quiz_textarea</td><td>замена в поле запроса произвольной информации</td></tr></tbody></table>

&#x20;Результат выполнения скрипта:

<figure><img src="../../../.gitbook/assets/Скриншот-12-02-2024 10_39_22.jpg" alt=""><figcaption></figcaption></figure>

а
