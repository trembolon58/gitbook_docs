# Как подключить VK Pay и получать уведомления VK Donut

## Подключение VK Pay

Salebot поддерживает возможность создания кнопки об оплате через VK Pay. Для этого в Salebot необходимо включить соответствующий рычажок при подключении канала

<figure><img src="https://lh7-rt.googleusercontent.com/docsz/AD_4nXcDIKu2zYNZ0BMQTaSFG4yhhVg67jCDFfDZYAlhmPaPW4HNL8zZmswKKGLfxq-QDI1rnr-cvMCSCh3C7QV_ck7S91G_FWSuBQ3wAFfCSYMwMjEeekjB0bWDw_4NwB5C2MRQTm7p?key=DP2cizoEy_BSE-uP8WYV6A" alt=""><figcaption></figcaption></figure>

<mark style="color:red;">**ВНИМАНИЕ!**</mark> И у Вас, и у отправителя средств должен быть[ расширенный статус VK Pay](https://vkpay.com/faq/id/). Чтобы получить его, укажите данные паспорта и ещё одного документа на выбор — ИНН или СНИЛС.

Для создания кнопки оплаты в меню выбора типа кнопки стоит выбрать “VK Pay”, после чего появится четыре типа оплаты: \
\- перевод заданной суммы пользователю \
&#x20;       \* сумма \
&#x20;       \* идентификатор пользователя \
\- перевод заданной суммы группе \
&#x20;       \* сумма \
&#x20;       \* идентификатор группы \
\- перевод произвольной суммы пользователю \
&#x20;        \* идентификатор пользователя \
\- перевод произвольной суммы группе \
&#x20;        \* идентификатор группы \
Где: \
Идентификатор пользователя - это id человека, которому будут перечислены деньги (например, 136856885)&#x20;

Идентификатор группы - это id группы, в которую будут поступать переводы (например, 230462869).

<figure><img src="https://lh7-rt.googleusercontent.com/docsz/AD_4nXchjBbVOzN18Zt0r6kirdXCXvOY7eBPRV9qjmmM_5p9sA7J7SbMRemgF4cmfqrSC9ELh-N_I5ygg6NS7TW_KdZQg8SRLWajDQ9B_WqHjXACfx4Rwpfo2ueHouUSV8T_4tw24KWAjQ?key=DP2cizoEy_BSE-uP8WYV6A" alt=""><figcaption><p>Настройка кнопки оплаты VK Pay</p></figcaption></figure>

<figure><img src="https://lh7-rt.googleusercontent.com/docsz/AD_4nXc0FFw45LVCdTDMJ92zBE2ObyPHxX3m4IAfaVfDKDzGzG00taOZy-UJb3AgT6rMCYR68c1crOBDKUt-1hT4QPwfYazm7ISV6-mtBGeXLbI2L7kYUVBZuquuS16HnWSfsIZPmwlGLQ?key=DP2cizoEy_BSE-uP8WYV6A" alt=""><figcaption><p>Настройка кнопки оплаты VK pay на заданную сумму клиенту с id 136856885</p></figcaption></figure>

После активации бота пользователь получит кнопку следующего вида, после клика по которой выведется окно сервиса VK Pay.

<mark style="color:red;">**Внимание!**</mark> Независимо от названия, указанного в настройках кнопки, во Вконтакте кнопка будет выглядеть только таким образом:

<figure><img src="../../../.gitbook/assets/image (176) (1).png" alt=""><figcaption><p> Кнопка оплаты во ВКонтакте</p></figcaption></figure>

## VK Donut

Для того чтобы подключить VK Donut нужно перейти в раздел “Монетизация” в вашем сообществе ВКонтакте.

<figure><img src="https://lh7-rt.googleusercontent.com/docsz/AD_4nXc6D8N-yIulfvnAe14Rq1s9-m4CTTXE8Byj_rKXxiRfIgYE9MQem4pxoUXrNaKkOF3DQFkeRgecJhJtJDDsRfBcjTDgtcUGPO5DJ2fjD3Gy56i7HetgW8zhiUNRHRS3QTF-UOfJ?key=DP2cizoEy_BSE-uP8WYV6A" alt=""><figcaption></figcaption></figure>

Далее выбираем инструмент получения средств от подписчиков:

<figure><img src="https://lh7-rt.googleusercontent.com/docsz/AD_4nXdJq9NfUs5pXOyf8HyWdECjp_IJPkrUW8GHFJ3JEsZBF_5274c7svkEcriC4zViO_oGFcICvLfzAHDO91H0tkBW4cgYDcn9fttWXsMr9bvRUX--MkuADuXcepZEkLD81nuTSHBDqA?key=DP2cizoEy_BSE-uP8WYV6A" alt=""><figcaption></figcaption></figure>

{% hint style="info" %}
Вы можете подключить все три инструмента при необходимости.
{% endhint %}

Также выбираем на какой счет будут поступать средства: на банковскую карту или VK Pay:

<figure><img src="https://lh7-rt.googleusercontent.com/docsz/AD_4nXfvE7oqAfIpWdenB74MHND1vcc5PDLMxiscvtc2XIm7YJagTZdKbFUFJL9kZAFDTlEuPx-REwDBo7CBA2RtiBDdw6PiDCUjqOxsNdI4w3D5fjtWid28d-wQDlD_DhleGuAIc5BGoA?key=DP2cizoEy_BSE-uP8WYV6A" alt=""><figcaption></figcaption></figure>

И выбираем получателя средств:

<figure><img src="https://lh7-rt.googleusercontent.com/docsz/AD_4nXeuMpwu1S36J1HN8XUEYaz5Xwow2T5o3gBOOca7Evho7BhGZsewx8HYqo0AyWR4d0E8eVLXSlAF9wtBx3j0fn_rXemWYTRDzrprvhiEujCCHdhM7Pcj4IayD73kG3hfgq9oeuxVPw?key=DP2cizoEy_BSE-uP8WYV6A" alt=""><figcaption></figcaption></figure>

Для примера выберем инструмент “Регулярная поддержка” и заполним необходимые данные, далее жмем кнопку “Создать уровень”

<figure><img src="https://lh7-rt.googleusercontent.com/docsz/AD_4nXf1qwfmJvmIHyFd3nb9V7vC1v8w2w6gDO2eEAt28x5jJXW2b5L5fRW1_7zjBqu3wvkED8bE9MRbvmyED3dtE9Jiz_x9BPtVmd7MgPVYvABL7OImKGWQWhsRrwWdHUMa9sLh3lAAFA?key=DP2cizoEy_BSE-uP8WYV6A" alt=""><figcaption></figcaption></figure>

Для активации VK Donat нажимаем “Включить поддержку”

<figure><img src="https://lh7-rt.googleusercontent.com/docsz/AD_4nXddYIyuSyZAHGBrV8MQ0TdyI47edh16u4oZJ7NeA4I6npTxsRaeALUu_1kUVpy4sjOOUuAmQMoRCh8nfRZuDiezzMXz922vgjeVvU_nqzFJuhcXzzEtXptk8lAzkKGHkilMP0p_jg?key=DP2cizoEy_BSE-uP8WYV6A" alt=""><figcaption></figcaption></figure>

VK Donat подключен:

<figure><img src="https://lh7-rt.googleusercontent.com/docsz/AD_4nXfHkL8lhQQYHFXBzpb25gfGfpCGZ6yEzvBjTmyHGrqyItkHiBtwwkSRCPNE0V9p8_wBEZsq4wW06gvw9Rql2IGRl71hLDin5GzShhgLFFUbYOE2k6lXKczDwBSXXsan48QsstcbGg?key=DP2cizoEy_BSE-uP8WYV6A" alt=""><figcaption></figcaption></figure>

Теперь ваши подписчики могут поддержать вас

<figure><img src="https://lh7-rt.googleusercontent.com/docsz/AD_4nXfX_2E8WkiuzWaJnpvz1t38uyrY8lKiUvc6Spb5D6EG_SC7bImtUUbiIhTukgk7EM3uTqafvRmdO0U1Rdw39JmerARaJ2OUvzwI8s5edjgI87Fcpv305H9xN3z-rNAXd0c18CzE1Q?key=DP2cizoEy_BSE-uP8WYV6A" alt=""><figcaption></figcaption></figure>

Если Ваше сообщество подключено к VK Donut, Вы будете получать callback-сообщения о следующих событиях: \
\- Оформлена подписка на группу - **client\_donut\_subscription\_create 50 RUB** \
\- Подписка продлена - **client\_donut\_subscription\_prolonged 50 RUB** \
\- Подписка отменена - **client\_donut\_subscription\_cancelled** \
\- Подписка закончилась - **client\_donut\_subscription\_expired**
