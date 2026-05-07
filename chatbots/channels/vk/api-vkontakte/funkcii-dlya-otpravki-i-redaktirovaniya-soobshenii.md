# Функции для отправки и редактирования сообщений

## Как отправить сообщение во Вконтакте&#x20;

**Описание:**

**vk\_send\_message(platform\_id, message, keyboard, reply\_to, forward\_messages, sticker\_id, dont\_parse\_links, disable\_mentions, attachments\_photo, attachments\_files, parse\_mode)**

Параметры:

<table><thead><tr><th width="274.390625">Параметр</th><th>Описание</th></tr></thead><tbody><tr><td><mark style="color:red;"><strong>!</strong></mark><strong> platform_id</strong></td><td>id клиента в мессенджере <a href="funkcii-dlya-otpravki-i-redaktirovaniya-soobshenii.md#gde-vzyat-platform_id-owner_id-klienta-dlya-otpravki-uvedomlenii">*</a></td></tr><tr><td><mark style="color:red;"><strong>!</strong></mark><strong> message</strong></td><td>текст сообщения</td></tr><tr><td><strong>keyboard</strong></td><td>кнопки в сообщении <a href="funkcii-dlya-otpravki-i-redaktirovaniya-soobshenii.md#kak-propisyvat-knopki-v-parametre-keyboard">**</a></td></tr><tr><td><strong>reply_to</strong></td><td>id сообщения для ответа/цитаты</td></tr><tr><td><strong>forward_messages</strong></td><td> id пересылаемых сообщений (формат списка                                       "{#айдипервогосообщения}, #{второго}, #{итакдалее}"</td></tr><tr><td><strong>sticker_id</strong></td><td>id стикера  </td></tr><tr><td><strong>dont_parse_links</strong></td><td>создавать сниппет или нет, может принимать значение 1 — создавать, 0 — нет </td></tr><tr><td><strong>disable_mentions</strong></td><td>отключить уведомление об упоминании в сообщении, для отключения уведомлений передайте в этот параметр что угодно, иначе оставьте пустым</td></tr><tr><td><strong>attachments_photo</strong></td><td>добавить в медиавложения сообщения фотографии, которые пока не загружены во ВКонтакте, в виде списка ссылок на фотографии в формате:<br>                                       <code>'["#{url1}","#{url2}"]'</code>, где <br><code>url</code> - это ссылка на фотографию на доступных ресурсах в Интернете. </td></tr><tr><td><strong>attachments_files</strong></td><td><p>различные вложения из ВКонтакте. Для использования attachments_files потребуется строка с вложениями, перечисленными через запятую и уже находящимися во ВКонтакте, имеющая следующий вид: <br>                     <code>'doc-182762603_638918266, photo-182762603_638918266'</code><br><em>Каждое вложение описываем следующим образом:</em><br>                          <em><code>&#x3C;type>-&#x3C;owner_id>_&#x3C;media_id></code> - где:</em> <br><code>&#x3C;type></code> — тип медиа-вложения:</p><ul><li><code>photo</code> — фотография;</li><li><code>video</code> — видеозапись;</li><li><code>audio</code> — аудиозапись;</li><li><code>doc</code> — документ;</li><li><code>wall</code> — запись на стене; </li><li><code>market</code> — товар; </li><li><code>poll</code> — опрос.</li></ul><p><code>&#x3C;owner_id></code> — идентификатор владельца медиа-вложения.<br><code>&#x3C;media_id></code> — идентификатор медиа-вложения.<br><br><em>Обратите внимание, если прикрепляется объект, принадлежащий другому пользователю, следует добавлять к вложению его access_key в формате</em></p><p><em>-&#x3C;owner_id></em>&#x3C;media_id>_&#x3C;access_key> </p></td></tr><tr><td><strong>parse_mode</strong></td><td>необязательный параметр. Включает разметку текста в сообщении. Возможные значения - "html" и "markdown"</td></tr></tbody></table>

Если присвоить функцию переменной, то в переменную будет помещен id сообщения, который будет необходим для возможно последующего редактирования сообщения.

**Примеры:**

Отправим сообщение с кнопками и с картинкой, заранее загруженной в нашу группу:

<figure><img src="https://lh7-rt.googleusercontent.com/docsz/AD_4nXfNb8qdJXoYOU8b_dLhJ8y-nVpJ5WlzoEpezALiGKUFC4SKH45M4x2pwKMzzZOw9PKqDFzxG3gDkR4_E4hUybmrdF_5RAJJWMtVvyb2PGOylLQ7euDEaaw4hyF6hmyMDWCo5CYpBg?key=1ymrafKI__z0HYZ-Sj5M2A" alt=""><figcaption><p>Настройка блока отправки сообщения</p></figcaption></figure>

Тестируем

<div data-with-frame="true"><figure><img src="https://lh7-rt.googleusercontent.com/docsz/AD_4nXebn0v4E59ak--hw3JPJI60DIaskReqBHwsUA7DYG-xnWWTLg-cFBSSXEui2oHZCMYWrFWJnk7ToqsAYNmreWEyvDy3uLzexDVtgvhAC8q9mXKAv5lBxZX4savWC1XJneOKNRXArA?key=1ymrafKI__z0HYZ-Sj5M2A" alt="" width="375"><figcaption><p>Отправка сообщения в чат ВКонтакте</p></figcaption></figure></div>

Обратите внимание на значение переменной soob, в которую мы записали результат отправки сообщения

<div data-with-frame="true"><figure><img src="https://lh7-rt.googleusercontent.com/docsz/AD_4nXeJAdBvl_XhC5oKonekDEx4SiIsJWZjAModmU1iU4PGDFWikx4rzxkMQp8hsu9awt_AiXqNsgJQufbqewMUGJa8uD8tU8C00XArIKIiHyMK-g5octV6pJjdpO-c2camApnTQD5C?key=1ymrafKI__z0HYZ-Sj5M2A" alt="" width="563"><figcaption></figcaption></figure></div>

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

**vk\_edit\_message(platform\_id, message\_id, text, attachments\_photo, attachments\_files, keyboard, keep\_forward\_messages, keep\_snippets, dont\_parse\_links, disable\_mentions, parse\_mode)**

Параметры:

<table><thead><tr><th width="234.41015625">Параметры</th><th>Описание</th></tr></thead><tbody><tr><td><mark style="color:red;"><strong>!</strong></mark><strong> platform_id</strong></td><td>id клиента в мессенджере <a href="funkcii-dlya-otpravki-i-redaktirovaniya-soobshenii.md#gde-vzyat-platform_id-owner_id-klienta-dlya-otpravki-uvedomlenii">*</a></td></tr><tr><td><mark style="color:red;"><strong>!</strong></mark><strong> message_id</strong></td><td>id редактируемого сообщения</td></tr><tr><td><strong>text</strong></td><td>текст сообщения</td></tr><tr><td><strong>attachments_photo</strong></td><td>добавить в медиа вложения сообщения фотографии, которые пока не загружены во ВКонтакте, в виде списка ссылок на фотографии в формате:<br>                                       <code>'["#{url1}","#{url2}"]'</code>, где <br><code>url</code> - это ссылка на фотографию на доступных ресурсах в Интернете. </td></tr><tr><td><strong>attachments_files</strong></td><td><p>различные вложения из ВКонтакте. Для использования attachments_files потребуется строка с вложениями, перечисленными через запятую и уже находящимися во ВКонтакте, имеющая следующий вид: <br>                     <code>'doc-182762603_638918266, photo-182762603</code><em><code>638918266'.</code></em> <br><em>Каждое вложение описываем следующим образом:</em><br>                          <em><code>&#x3C;type>-&#x3C;owner_id>_&#x3C;media_id></code> - где:</em> <br><code>&#x3C;type></code> — тип медиа-вложения:</p><ul><li><code>photo</code> — фотография;</li><li><code>video</code> — видеозапись;</li><li><code>audio</code> — аудиозапись;</li><li><code>doc</code> — документ;</li><li><code>wall</code> — запись на стене; </li><li><code>market</code> — товар; </li><li><code>poll</code> — опрос.</li></ul><p><code>&#x3C;owner_id></code> — идентификатор владельца медиа-вложения.<br><code>&#x3C;media_id></code> — идентификатор медиа-вложения.<br></p><p><em>Обратите внимание, если прикрепляется объект, принадлежащий другому пользователю, следует добавлять к вложению его access_key в формате</em> <br>                              <em>-&#x3C;owner_id></em>&#x3C;media_id>_&#x3C;access_key> </p></td></tr><tr><td><strong>keyboard</strong></td><td>кнопки в сообщении <a href="funkcii-dlya-otpravki-i-redaktirovaniya-soobshenii.md#kak-propisyvat-knopki-v-parametre-keyboard">**</a></td></tr><tr><td><strong>keep_forward_messages</strong></td><td>признак необходимости сохранить прикреплённые пересланные сообщения (любое значение)</td></tr><tr><td><strong>keep_snippets</strong></td><td>признак необходимости сохранить прикреплённые внешние ссылки (сниппеты)(любое значение)  </td></tr><tr><td><strong>dont_parse_links</strong></td><td>признак того, что не надо создавать сниппет (любое значение)</td></tr><tr><td><strong>disable_mentions</strong></td><td>признак того, что надо отключить уведомление об упоминании в сообщении (любое значение)</td></tr><tr><td><strong>parse_mode</strong></td><td>необязательный параметр. Включает разметку текста в сообщении. Возможные значения - "html" и "markdown"</td></tr></tbody></table>

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
