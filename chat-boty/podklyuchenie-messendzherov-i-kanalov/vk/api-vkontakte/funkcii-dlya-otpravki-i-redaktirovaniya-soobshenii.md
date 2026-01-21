# Функции для отправки и редактирования сообщений

Раздел находится на редактировании

## Как отправить сообщение во Вконтакте&#x20;

**Описание:**

**vk\_send\_message(platform\_id, message, keyboard, reply\_to, forward\_messages, sticker\_id, dont\_parse\_links, disable\_mentions, attachments\_photo, attachments\_files)**

Параметры:

<mark style="color:red;">**!**</mark>**&#x20;platform\_id** — id клиента в мессенджере [\*](funkcii-dlya-otpravki-i-redaktirovaniya-soobshenii.md#gde-vzyat-platform_id-owner_id-klienta-dlya-otpravki-uvedomlenii)

<mark style="color:red;">**!**</mark>**&#x20;message** — текст сообщения

**keyboard** — кнопки в сообщении [\*\*](funkcii-dlya-otpravki-i-redaktirovaniya-soobshenii.md#kak-propisyvat-knopki-v-parametre-keyboard)

**reply\_to** — id сообщения для ответа/цитаты

**forward\_messages** — id пересылаемых сообщений (формат списка                                       "{#айдипервогосообщения}, #{второго}, #{итакдалее}"

**sticker\_id** — id стикера &#x20;

**dont\_parse\_links** — создавать сниппет или нет, может принимать значение 1 — создавать, 0 — нет&#x20;

**disable\_mentions** — отключить уведомление об упоминании в сообщении, для отключения уведомлений передайте в этот параметр что угодно, иначе оставьте пустым

**attachments\_photo** — добавить в медиавложения сообщения фотографии, которые пока не загружены во ВКонтакте, в виде списка ссылок на фотографии в формате:\
&#x20;                                      `'["#{url1}","#{url2}"]'`, где \
`url` - это ссылка на фотографию на доступных ресурсах в Интернете.&#x20;

**attachments\_files** — различные вложения из ВКонтакте. Для использования attachments\_files потребуется строка с вложениями, перечисленными через запятую и уже находящимися во ВКонтакте, имеющая следующий вид: \
&#x20;                    `'doc-182762603_638918266, photo-182762603_638918266'`\
_Каждое вложение описываем следующим образом:_\
&#x20;                         _`<type>-<owner_id>_<media_id>` - где:_ \
`<type>` — тип медиа-вложения:

* `photo` — фотография;
* `video` — видеозапись;
* `audio` — аудиозапись;
* `doc` — документ;
* `wall` — запись на стене;&#x20;
* `market` — товар;&#x20;
* `poll` — опрос.

`<owner_id>` — идентификатор владельца медиа-вложения.\
`<media_id>` — идентификатор медиа-вложения.<br>

_Обратите внимание, если прикрепляется объект, принадлежащий другому пользователю, следует добавлять к вложению его access\_key в формате_ \
&#x20;                             _-\<owner\_id>_\<media\_id>\_\<access\_key> <br>

Если присвоить функцию переменной, то в переменную будет помещен id сообщения, который будет необходим для возможно последующего редактирования сообщения.

**Примеры:**

Отправим сообщение с кнопками и с картинкой, заранее загруженной в нашу группу:

<figure><img src="https://lh7-rt.googleusercontent.com/docsz/AD_4nXfNb8qdJXoYOU8b_dLhJ8y-nVpJ5WlzoEpezALiGKUFC4SKH45M4x2pwKMzzZOw9PKqDFzxG3gDkR4_E4hUybmrdF_5RAJJWMtVvyb2PGOylLQ7euDEaaw4hyF6hmyMDWCo5CYpBg?key=1ymrafKI__z0HYZ-Sj5M2A" alt=""><figcaption><p>Настройка блока отправки сообщения</p></figcaption></figure>

Тестируем

<figure><img src="https://lh7-rt.googleusercontent.com/docsz/AD_4nXebn0v4E59ak--hw3JPJI60DIaskReqBHwsUA7DYG-xnWWTLg-cFBSSXEui2oHZCMYWrFWJnk7ToqsAYNmreWEyvDy3uLzexDVtgvhAC8q9mXKAv5lBxZX4savWC1XJneOKNRXArA?key=1ymrafKI__z0HYZ-Sj5M2A" alt=""><figcaption><p>Отправка сообщения в чат ВКонтакте</p></figcaption></figure>

Обратите внимание на значение переменной soob, в которую мы записали результат отправки сообщения

<figure><img src="https://lh7-rt.googleusercontent.com/docsz/AD_4nXeJAdBvl_XhC5oKonekDEx4SiIsJWZjAModmU1iU4PGDFWikx4rzxkMQp8hsu9awt_AiXqNsgJQufbqewMUGJa8uD8tU8C00XArIKIiHyMK-g5octV6pJjdpO-c2camApnTQD5C?key=1ymrafKI__z0HYZ-Sj5M2A" alt=""><figcaption></figcaption></figure>

Как видите функция вернула идентификатор отправленного  сообщения. Это позволяет нам проводить дальнейшие манипуляции над сообщением

**Пример кода для копирования:**

```
knop={"inline": true, "buttons": [[{"action": {"type": "open_link", "link": "https://salebot.site/tutor_reg_1", "label": "Регистрируйся"}}, {"action": {"type": "text", "label": "Отмена"}}]]}
soob=vk_send_message(2000000001, "Выбирай", knop, None, None, None, None, None, None, "photo-217945289_457239047")
```

{% hint style="info" %}
Чтобы в переменную записать текст с переносами строк, укажите значение следующим образом:

`message = "Текст первой строки" + "\n" + "Текст второй строки" + "\n" +"Третья строка"`
{% endhint %}

## Как редактировать сообщение во  ВКонтакте&#x20;

**Описание:**

**vk\_edit\_message(platform\_id, message\_id, text, attachments\_photo, attachments\_files, keyboard, keep\_forward\_messages, keep\_snippets, dont\_parse\_links, disable\_mentions)**

Параметры:

<mark style="color:red;">**!**</mark>**&#x20;platform\_id** — id клиента в мессенджере [\*](funkcii-dlya-otpravki-i-redaktirovaniya-soobshenii.md#gde-vzyat-platform_id-owner_id-klienta-dlya-otpravki-uvedomlenii)

<mark style="color:red;">**!**</mark>**&#x20;message\_id** — id редактируемого сообщения

**text** — текст сообщения&#x20;

**attachments\_photo** — добавить в медиа вложения сообщения фотографии, которые пока не загружены во ВКонтакте, в виде списка ссылок на фотографии в формате:\
&#x20;                                      `'["#{url1}","#{url2}"]'`, где \
`url` - это ссылка на фотографию на доступных ресурсах в Интернете.&#x20;

**attachments\_files** — различные вложения из ВКонтакте. Для использования attachments\_files потребуется строка с вложениями, перечисленными через запятую и уже находящимися во ВКонтакте, имеющая следующий вид: \
&#x20;                    `'doc-182762603_638918266, photo-182762603`_`638918266'.`_ \
_Каждое вложение описываем следующим образом:_\
&#x20;                         _`<type>-<owner_id>_<media_id>` - где:_ \
`<type>` — тип медиа-вложения:

* `photo` — фотография;
* `video` — видеозапись;
* `audio` — аудиозапись;
* `doc` — документ;
* `wall` — запись на стене;&#x20;
* `market` — товар;&#x20;
* `poll` — опрос.

`<owner_id>` — идентификатор владельца медиа-вложения.\
`<media_id>` — идентификатор медиа-вложения.<br>

_Обратите внимание, если прикрепляется объект, принадлежащий другому пользователю, следует добавлять к вложению его access\_key в формате_ \
&#x20;                             _-\<owner\_id>_\<media\_id>\_\<access\_key>&#x20;

**keyboard** — кнопки в сообщении [\*\*](funkcii-dlya-otpravki-i-redaktirovaniya-soobshenii.md#kak-propisyvat-knopki-v-parametre-keyboard)

**keep\_forward\_messages** — признак необходимости сохранить прикреплённые пересланные сообщения (любое значение)

**keep\_snippets** — признак необходимости сохранить прикреплённые внешние ссылки (сниппеты)(любое значение) &#x20;

**dont\_parse\_links** — признак того, что не надо создавать сниппет (любое значение)

**disable\_mentions** — признак того, что надо отключить уведомление об упоминании в сообщении (любое значение)

**Примеры:**

Продолжим с Вами предыдущий пример - отредактируем сообщение через 5 секунд

<figure><img src="https://lh7-rt.googleusercontent.com/docsz/AD_4nXdCThody3vxqPp0z_NWsRv731Fi1dsNerSyaBO2U84vrc0jW6SwPoCjsP8mWsTsWtfdUX-s_0iagNAPntIdrZ5SuJv0_S4uZ1uj8euSdP715BUWp_4OOYYVGZaNY14dD5-uRH0F2w?key=1ymrafKI__z0HYZ-Sj5M2A" alt=""><figcaption><p>Настройка блока редактирования сообщения</p></figcaption></figure>

Тестируем:

<figure><img src="https://lh7-rt.googleusercontent.com/docsz/AD_4nXenomB0TLXdoHZC6bzVZbYUQDz9D2l_nAs2HTVWXF1PD8cnVQYrmNDHIclASe585NqALjeeeKZKu1SzoMQtt8JR9kioHK2_gh0cwqBFTH34ceF6JS4N1WzCQcX49RkUWkmStyem6A?key=1ymrafKI__z0HYZ-Sj5M2A" alt="" width="375"><figcaption><p>Редактирование отправленного сообщения в чате ВКонтакте</p></figcaption></figure>

**Пример кода для копирования:**

Блок отправки сообщения:

```
knop={"inline": true, "buttons": [[{"action": {"type": "open_link", "link": "https://salebot.site/tutor_reg_1", "label": "Регистрируйся"}}, {"action": {"type": "text", "label": "Отмена"}}]]}
soob=vk_send_message(2000000001, "Выбирай", knop, None, None, None, None, None, None, "photo-217945289_457239047")
```

Блок редактирования:

```
soob=vk_edit_message(2000000001, soob, 'Долго думаешь', None, 'photo-217945289_457239048', None, None, None, None, None
```

