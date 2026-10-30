# Dictum Nothy — changelog

## 2.1.95 — 2026-10-30

### Русский

Надёжное обновление: установка находит настоящую папку приложения даже при запуске из образа диска или временной копии, ждёт реального выхода, никогда не оставляет без работающего Dictum и не зависает в окне обновления; все шаги пишутся в диагностику.

- Если Dictum был открыт прямо из образа диска или скопирован без Finder, macOS запускает его из временной копии; раньше установка обновления завершала приложение, не могла заменить его и ничего не перезапускала. Теперь установщик находит настоящую папку приложения, а при запуске с образа диска или из папки без прав на запись заранее показывает, что нужно перетащить Dictum Nothy в «Программы».
- Замена приложения ждёт реального выхода старой версии, а не одну секунду; если приложение не завершилось само, оно завершается принудительно через 5–10 секунд. При любом сбое замены прежняя версия возвращается на место и перезапускается, новая открывается только пока резервная копия ещё цела.
- Окно обновления больше не блокируется навсегда на «Устанавливаем»: каждая проверка (подпись, версия, распаковка) ограничена по времени, ошибки установки всегда показываются с кнопкой «Повторить», а если приложение не перезапустилось, через 70 секунд окно сообщает об этом и даёт закрыть себя.
- Диагностика обновлений: проверка, загрузка, распаковка, проверка подписи, установка и выход записываются в папку Diagnostics/Updates с длительностью каждого шага, чтобы причину сбоя можно было установить по файлу.

### English

Reliable updates: the installer finds the real application folder even when launched from a disk image or a temporary copy, waits for the real exit, never leaves you without a running Dictum and never hangs in the update window; every step is recorded in diagnostics.

- If Dictum was opened straight from the disk image or copied without Finder, macOS runs it from a temporary copy; the update used to quit the app, fail to replace it and relaunch nothing. The installer now resolves the real application folder and, when running from a disk image or a folder without write access, tells you in advance to drag Dictum Nothy to Applications.
- The replacement waits for the old version to actually exit instead of one second; if the app does not quit on its own it is terminated after 5-10 seconds. On any replacement failure the previous version is put back and relaunched, and the new one is opened only while the backup copy still exists.
- The update window no longer stays stuck on "Installing": every check (signature, version, extraction) is time-limited, install errors are always shown with a Retry button, and if the app did not restart the window says so after 70 seconds and can be closed.
- Update diagnostics: check, download, extraction, signature check, install and exit are recorded in Diagnostics/Updates with the duration of each step, so a failure can be traced from the file.

### Español

Actualizaciones fiables: el instalador encuentra la carpeta real de la aplicación aunque se haya abierto desde una imagen de disco o una copia temporal, espera la salida real, nunca te deja sin un Dictum en marcha y nunca se queda colgado en la ventana de actualización; cada paso se registra en los diagnósticos.

- Si Dictum se abría directamente desde la imagen de disco o se copiaba sin Finder, macOS lo ejecuta desde una copia temporal; la actualización cerraba la aplicación, no podía reemplazarla y no relanzaba nada. Ahora el instalador localiza la carpeta real de la aplicación y, al ejecutarse desde una imagen de disco o una carpeta sin permiso de escritura, avisa de antemano que hay que arrastrar Dictum Nothy a Aplicaciones.
- El reemplazo espera a que la versión anterior salga de verdad en lugar de un segundo; si la aplicación no se cierra sola, se termina a los 5-10 segundos. Ante cualquier fallo del reemplazo, la versión anterior vuelve a su sitio y se relanza, y la nueva se abre solo mientras la copia de seguridad siga intacta.
- La ventana de actualización ya no se queda bloqueada en «Instalando»: cada comprobación (firma, versión, extracción) tiene un tiempo límite, los errores de instalación siempre se muestran con un botón «Reintentar» y, si la aplicación no se reinició, la ventana lo indica a los 70 segundos y se puede cerrar.
- Diagnóstico de actualizaciones: la comprobación, la descarga, la extracción, la verificación de firma, la instalación y la salida se registran en Diagnostics/Updates con la duración de cada paso, para poder rastrear un fallo desde el archivo.

## 2.1.94 — 2026-10-29

### Русский

Перенос панели всегда завершается после отпускания мыши, даже если страница не ответила; неудачное распознавание можно повторить; промпты и сниппеты сохраняются по одной записи, импорт резервной копии идёт одним шагом.

- Если ответ страницы о завершении переноса терялся, панель продолжала считаться перетаскиваемой и вся её область перехватывала клики. Теперь перенос завершается нативно через треть секунды после отпускания кнопки, а поздние ответы страницы игнорируются. Добавлена трасса, какое окно принимает клики.
- Сохранение настроек больше не держит главный поток во время записи на диск: перенос, прилипание и положение панели не подвисают при одновременном изменении настроек или импорте.
- Если распознавание не удалось, запись сохраняется две минуты и в сообщении об ошибке есть кнопка «Повторить». Отброшенная запись больше не попадает в движок.
- Промпты и сниппеты из Настроек и панелей сохраняются по одной записи: два открытых окна больше не затирают правки друг друга. Импорт резервной копии выполняется одним шагом под общими замками; при сбое отчёт в папке восстановления перечисляет заменённые разделы.

### English

Panel drags always finish after the mouse is released even if the page did not reply; a failed recognition can be retried; prompts and snippets save one record at a time; backup import runs as one step.

- If the page's drag-end reply was lost, the panel stayed in drag mode and its whole area swallowed clicks. The drag now ends natively a third of a second after the button is released, and late page replies are ignored. A trace records which window takes clicks.
- Saving settings no longer holds the main thread during disk writes: drag, attach and panel placement do not stall while settings change or an import runs.
- When recognition fails, the recording is kept for two minutes and the error message offers Retry. A discarded recording no longer reaches the engine.
- Prompts and snippets from Settings and the panels save one record at a time: two open windows no longer overwrite each other. Backup import runs as one step under shared locks; on failure the recovery folder lists the replaced sections.

### Español

El arrastre del panel siempre termina al soltar el ratón aunque la página no responda; un reconocimiento fallido se puede reintentar; los prompts y fragmentos se guardan de uno en uno; la importación de la copia de seguridad se ejecuta en un solo paso.

- Si se perdía la respuesta de la página al terminar el arrastre, el panel seguía en modo arrastre y toda su área capturaba los clics. Ahora el arrastre termina de forma nativa un tercio de segundo después de soltar el botón y las respuestas tardías se ignoran. Se añadió un registro de qué ventana recibe los clics.
- Guardar los ajustes ya no retiene el hilo principal durante la escritura en disco: el arrastre, el acople y la posición del panel no se congelan mientras cambian los ajustes o se importa.
- Si el reconocimiento falla, la grabación se conserva dos minutos y el mensaje de error ofrece Reintentar. Una grabación descartada ya no llega al motor.
- Los prompts y fragmentos de Ajustes y de los paneles se guardan de uno en uno: dos ventanas abiertas ya no se sobrescriben. La importación de la copia de seguridad se ejecuta en un solo paso con bloqueos compartidos; si falla, la carpeta de recuperación enumera las secciones reemplazadas.

## 2.1.93 — 2026-10-29

### Русский

Сохранность текста и файлов: исправление раскладки больше не стирает начало текста, Enter на «Отмена» не удаляет, ответ AI не затирает ваши правки; надёжнее окна, звук прилипания, диктовка и обновления.

- Автоисправление раскладки после паузы, тире, кавычек или длинного текста меняло не тот участок и могло удалить начало. Теперь оно сверяет своё место в тексте и при сомнении пропускает исправление.
- Enter на кнопке «Отмена» в диалогах удаления подтверждал удаление. Теперь Enter действует на ту кнопку, где стоит фокус.
- Ответ AI, выбранный промпт и восстановление после ошибки затирали текст, который вы дописали во время ожидания. Теперь ваши правки сохраняются.
- Редактор скриншотов: позднее сохранение предыдущего снимка могло подменить, удалить или закрыть новый. Каждое действие теперь проверяет, что снимок не сменился.
- Повреждённый или нечитаемый файл настроек, промптов или сниппетов больше не перезаписывается значениями по умолчанию: оригинал сохраняется в копию, запись блокируется. Редакторы промптов и сниппетов не закрываются при ошибке сохранения.
- Установка обновления во время диктовки или с открытой панелью теперь отклоняется с подсказкой, в том числе из меню в строке состояния. Отмена загрузки срабатывает сразу, размер загрузки ограничен.
- Панель: быстрое закрытие и повторное открытие больше не оставляет пустое или невидимое окно; открытие из Dock проходит штатный показ; звук прилипания звучит ровно один раз в момент прилипания и не звучит при отрыве.
- Диктовка: длинные записи больше не теряются из-за фиксированного таймаута распознавания; запись ограничена 30 минутами с уведомлением; сбой резервного движка сообщается как ошибка, а не как пустой результат; громкость восстанавливается при выходе и на том же устройстве.
- AI: русские буквы на стыке сетевых пакетов не превращаются в знаки вопроса, оборванный ответ не принимается за готовый, отмена действует только на отменённый запрос.
- Исправление выделения двойным Shift не вставляет старый результат в другое поле, если вы кликнули в другое место, и возвращает раскладку при отказе.

### English

Text and file safety: layout correction no longer deletes the start of your text, Enter on Cancel never deletes, an AI answer never overwrites your edits; more reliable windows, attach sound, dictation and updates.

- Layout auto-correction after a pause, a dash, quotes or a long text could replace the wrong span and delete the beginning. It now re-anchors itself and skips the correction when unsure.
- Enter on the Cancel button in delete dialogs confirmed the deletion. Enter now acts on the focused button only.
- An AI answer, a chosen prompt or an error recovery overwrote text you typed while waiting. Your edits are kept now.
- Screenshot editor: a late save of the previous image could replace, delete or close the new one. Every action now checks that the image has not changed.
- A corrupt or unreadable settings, prompts or snippets file is no longer overwritten with defaults: the original is preserved and writes are refused. Prompt and snippet editors stay open when saving fails.
- Installing an update during dictation or with the input panel open is now refused with a hint, including from the menu bar menu. Cancelling a download takes effect immediately and downloads are size-capped.
- Panel: a fast close and reopen no longer leaves an empty or invisible window; opening from the Dock uses the normal reveal; the attach sound plays exactly once at the moment of attaching and never on detach.
- Dictation: long recordings are no longer lost to a fixed recognition timeout; recording is capped at 30 minutes with a notice; a fallback engine failure is reported as an error instead of an empty result; volume is restored on quit and on the same device.
- AI: Cyrillic letters split across network packets no longer turn into replacement characters, a truncated answer is not accepted as complete, and cancel affects only the cancelled request.
- Double-Shift selection correction no longer types a stale result into another field after you clicked elsewhere, and restores the layout when refused.

### Español

Seguridad del texto y los archivos: la corrección de distribución ya no borra el inicio del texto, Intro en Cancelar nunca elimina, una respuesta de IA no sobrescribe tus cambios; ventanas, sonido de acople, dictado y actualizaciones más fiables.

- La corrección automática de distribución tras una pausa, un guion, comillas o un texto largo podía reemplazar el fragmento equivocado y borrar el inicio. Ahora verifica su posición y omite la corrección si hay dudas.
- Intro en el botón Cancelar de los diálogos de borrado confirmaba el borrado. Ahora Intro actúa solo sobre el botón enfocado.
- Una respuesta de IA, un prompt elegido o la recuperación tras un error sobrescribían el texto escrito mientras esperabas. Ahora se conservan tus cambios.
- Editor de capturas: un guardado tardío de la imagen anterior podía reemplazar, borrar o cerrar la nueva. Cada acción comprueba ahora que la imagen no cambió.
- Un archivo de ajustes, prompts o fragmentos dañado o ilegible ya no se sobrescribe con valores por defecto: el original se conserva y la escritura se rechaza. Los editores de prompts y fragmentos no se cierran si falla el guardado.
- Instalar una actualización durante el dictado o con el panel abierto ahora se rechaza con un aviso, también desde el menú de la barra de estado. Cancelar una descarga surte efecto de inmediato y las descargas tienen un límite de tamaño.
- Panel: cerrar y reabrir rápido ya no deja una ventana vacía o invisible; abrir desde el Dock usa la presentación normal; el sonido de acople suena exactamente una vez al acoplar y nunca al despegar.
- Dictado: las grabaciones largas ya no se pierden por un tiempo de espera fijo del reconocimiento; la grabación se limita a 30 minutos con aviso; un fallo del motor de respaldo se informa como error y no como resultado vacío; el volumen se restaura al salir y en el mismo dispositivo.
- IA: las letras cirílicas divididas entre paquetes de red ya no se convierten en signos de sustitución, una respuesta truncada no se acepta como completa y cancelar afecta solo a la solicitud cancelada.
- La corrección de selección con doble Shift ya no escribe un resultado antiguo en otro campo si hiciste clic en otro lugar, y restaura la distribución cuando se rechaza.

## 2.1.92 — 2026-10-28

### Русский

Новый звук прилипания панели: он звучит как пара к звуку отлипания.

- Когда панель прилипает обратно к верхнему краю, звучит тот же звук, что при отлипании, только ниже и чуть дольше, как «открыл — закрыл».

### English

A new panel attach sound that pairs with the detach sound.

- When the panel attaches back to the top edge it plays the detach sound, only lower and slightly longer, like an open–close pair.

### Español

Un nuevo sonido al acoplar el panel que hace pareja con el sonido al despegarlo.

- Cuando el panel vuelve a acoplarse al borde superior suena el mismo sonido que al despegarlo, solo que más grave y algo más largo, como un par abrir–cerrar.

## 2.1.91 — 2026-10-28

### Русский

Переключатель раскладки сам исправляет заметно больше слов и реже ошибается, исключения задаются парой «Было → Стало», а выученные слова теперь видны. Панель Dictum можно перетаскивать, диктовка быстрее под нагрузкой.

- Раскладка: на реальных исправлениях автоматическая замена справляется сама с 265 словами из 557 вместо 205, а ложных замен в обычном русском тексте стало почти вдвое меньше. Слова вроде «пдф», «сгенерировать», «дашборд», «субагенты» больше не портятся при наборе и возвращаются, если набраны в английской раскладке.
- Раскладка: адрес почты, набранный в русской раскладке, становится адресом (щты"пьфшдюсщь → ons@gmail.com); одиночная «Ю» между словами — знак «>»; 3в → 3d, 120и → 120b, 44зч → 44px; в начале строки /сд и Tab дают /cl.
- Исключения раскладки задаются двумя полями «Было» и «Стало»: «Стало» заполняется само. Противоречащие правила не сохраняются, а уже сохранённые помечаются «Не действует». Обычное слово (например «ту») сохраняется только после предупреждения. В исключениях можно использовать цифры и знаки: юутм → .env, /ку → /re.
- В реестре раскладки появилась вкладка «Выученные»: слова, которые Dictum выучил после двух одинаковых исправлений, можно увидеть и забыть. Исправления схлопываются по повторам, отмечено, что теперь исправляется само, а кнопка «В исключения» сохраняет исправление правилом.
- Двойной Shift после слова превращает русскую кавычку в @ и ; в $ (щты" → ons@), как и подсказывает клавиша; вопрос, запятая и двоеточие остаются.
- Панель Dictum можно перетащить за верхнюю строку: вдоль верхнего края, вниз в свободное положение или на другой монитор; у верхнего центра она примагничивается обратно, а место запоминается для каждого экрана.
- Диктовка остаётся быстрой и не теряет слова, когда Mac нагружен сборками и ему не хватает памяти; звук начала диктовки звучит один раз.
- Для обработки текста используется GPT-OSS 120B; в простое Dictum почти не тратит процессор, а замена раскладки укладывается в 60 мс и не задерживает клавиатуру.

### English

The layout switcher fixes noticeably more words on its own and errs less often, exceptions are set as a “Before → After” pair, and learned words are now visible. The Dictum panel can be dragged, and dictation is faster under load.

- Layout: on real corrections the automatic switch now handles 265 words out of 557 instead of 205, and false switches in ordinary Russian text dropped by almost half. Words such as «пдф», «сгенерировать», «дашборд», «субагенты» are no longer broken while typed and come back when typed in the English layout.
- Layout: an email address typed in the Russian layout becomes the address (щты"пьфшдюсщь → ons@gmail.com); a lone «Ю» between words is the “>” sign; 3в → 3d, 120и → 120b, 44зч → 44px; at the start of a line /сд and Tab give /cl.
- Layout exceptions are set with two fields, “Before” and “After”: “After” fills itself in. Contradicting rules are not saved, and ones already saved are marked “Inactive”. An ordinary word (such as «ту») is saved only after a warning. Exceptions may contain digits and signs: юутм → .env, /ку → /re.
- The layout registry has a new “Learned” tab: words Dictum learned after two identical corrections can be seen and forgotten. Corrections are grouped by repeats, marked when they are now fixed automatically, and the “To exceptions” button saves a correction as a rule.
- Double Shift after a word turns the Russian quote into @ and ; into $ (щты" → ons@), as the key says; a question mark, comma and colon stay.
- The Dictum panel can be dragged by its top row: along the top edge, down into a free position or to another display; near the top centre it snaps back, and its place is remembered for every screen.
- Dictation stays fast and keeps every word when the Mac is busy with builds and short of memory; the dictation start sound plays once.
- Text processing uses GPT-OSS 120B; Dictum barely uses the processor when idle, and a layout switch fits in 60 ms without holding up the keyboard.

### Español

El cambio de distribución corrige solo bastantes más palabras y se equivoca menos, las excepciones se definen como un par «Antes → Después» y las palabras aprendidas ahora son visibles. El panel de Dictum se puede arrastrar y el dictado es más rápido bajo carga.

- Distribución: en correcciones reales el cambio automático resuelve 265 palabras de 557 en lugar de 205, y los cambios erróneos en texto ruso normal bajaron casi a la mitad. Palabras como «пдф», «сгенерировать», «дашборд», «субагенты» ya no se estropean al escribirlas y vuelven si se escriben en la distribución inglesa.
- Distribución: una dirección de correo escrita en la distribución rusa se convierte en la dirección (щты"пьфшдюсщь → ons@gmail.com); una «Ю» suelta entre palabras es el signo «>»; 3в → 3d, 120и → 120b, 44зч → 44px; al inicio de una línea /сд y Tab dan /cl.
- Las excepciones de distribución se definen con dos campos, «Antes» y «Después»: «Después» se rellena solo. Las reglas contradictorias no se guardan y las ya guardadas se marcan «Inactiva». Una palabra común (como «ту») se guarda solo tras un aviso. Las excepciones admiten cifras y signos: юутм → .env, /ку → /re.
- El registro de distribución tiene una nueva pestaña «Aprendidas»: las palabras que Dictum aprendió tras dos correcciones iguales se pueden ver y olvidar. Las correcciones se agrupan por repeticiones, se marca cuándo ya se corrigen solas y el botón «A excepciones» guarda una corrección como regla.
- El doble Shift tras una palabra convierte la comilla rusa en @ y ; en $ (щты" → ons@), como indica la tecla; el signo de interrogación, la coma y los dos puntos se mantienen.
- El panel de Dictum se puede arrastrar por su fila superior: a lo largo del borde superior, hacia abajo a una posición libre o a otra pantalla; cerca del centro superior vuelve a acoplarse, y su lugar se recuerda en cada pantalla.
- El dictado sigue siendo rápido y no pierde palabras cuando el Mac está ocupado con compilaciones y le falta memoria; el sonido de inicio del dictado suena una vez.
- El procesamiento de texto usa GPT-OSS 120B; Dictum apenas usa el procesador en reposo, y el cambio de distribución cabe en 60 ms sin retener el teclado.

## 2.1.82 — 2026-10-15

### Русский

Снимки из истории вставляются картинкой, редактор скриншотов стал удобнее и быстрее, диктовка и улучшение текста запускаются быстрее, а у переключателя раскладки появились исключения для слов и фраз.

- Снимок, скопированный из истории, вставляется картинкой в чаты, редакторы и графические программы, а не только файлом в Finder. В строке каждого снимка появились кнопки редактирования и копирования ссылки на файл, а превью открывается кликом по значку глаза и закрывается повторным кликом.
- В редакторе скриншотов текст комментария снова выделяется мышью, а карточку перетаскивают за отдельную ручку. На узких снимках панель инструментов помещается целиком, а над ней больше не появляется красная плашка с ошибкой.
- Снимок области и распознавание текста с экрана запускаются быстрее. Редактор быстрее открывает и сохраняет большие снимки, тратит меньше памяти, а рисование на них стало плавнее.
- Диктовка начинается быстрее и не теряет начало речи, даже когда компьютер занят. Панель записи появляется быстрее, окончание фразы не обрезается, а звук одной записи не попадает в следующую.
- Улучшение текста отвечает быстрее: соединение с AI-сервисом используется повторно, что экономит примерно 0,1–0,3 секунды на каждом запросе, а перед автоматическим улучшением больше нет паузы.
- У переключателя раскладки появились исключения — слова и целые фразы вроде «plan b», которые он не трогает или всегда исправляет одинаково. Их можно добавить вручную в списке исключений, голосовой командой «Добавь в исключения» или сочетанием Shift + правый Command над словом. После двух одинаковых исправлений двойным Shift Nothy сама предложит добавить исключение, а список сохраняется даже после переустановки приложения.
- Переключатель лучше понимает одиночную букву по соседним словам: «пишу на rust b python» становится «пишу на rust и python», а «plan b» и «витамин c» остаются как есть. Двойной Shift над выделенным словом, уже набранным в другой раскладке, переводит его обратно вместо сообщения «Знак одинаков в обеих раскладках», а знак после слова исправляется вместе с ним (>hf? → Юра,).
- Если рядом работал другой переключатель раскладки, после его закрытия двойной Shift и автозамена Nothy снова включаются сами, без перезапуска приложения.
- Вкладка «Диктовки» в истории открывается сразу, не дожидаясь превью снимков. Список сохранённых заметок виден сразу, каждое изменение заметки сохраняет локальную резервную копию, а ошибка чтения больше не выглядит как пустая библиотека.
- Nothy больше не мешает Mac засыпать в простое: звуковое устройство освобождается после 15 секунд тишины. Забытый выбор области экрана закрывается сам через 3 минуты, а само приложение стало легче.

### English

Screenshots from the history paste as images, the screenshot editor is easier to use and faster, dictation and text improvement start sooner, and the layout switcher now supports exceptions for words and phrases.

- A screenshot copied from the history now pastes as an image into chats, editors and graphics apps, not only as a file in Finder. Each screenshot row has buttons to edit it and to copy a link to the file, and the preview opens with a click on the eye icon and closes with a second click.
- In the screenshot editor you can select comment text with the mouse again, and cards are moved by a separate handle. On narrow screenshots the toolbar fits completely, and a red error bar no longer appears above it.
- Area capture and on-screen text recognition start faster. The editor opens and saves large screenshots faster, uses less memory, and drawing on them is smoother.
- Dictation starts faster and no longer loses the beginning of your speech, even when the computer is busy. The recording panel appears sooner, the end of a phrase is not cut off, and audio from one recording no longer leaks into the next.
- Text improvement responds faster: the connection to the AI service is reused, saving roughly 0.1–0.3 seconds per request, and there is no longer a pause before automatic improvement.
- The layout switcher now has exceptions: words and whole phrases such as “plan b” that it leaves alone or always fixes the same way. You can add them manually in the exceptions list, with the voice command “Add to exceptions”, or with Shift + right Command over a word. After you fix a word the same way twice with a double Shift, Nothy offers to add an exception, and the list survives reinstalling the app.
- The switcher understands a lone letter better from the neighboring words: “пишу на rust b python” gets the Russian “и”, while “plan b” and “vitamin c” stay as they are. A double Shift over a selected word already typed in the other layout converts it back instead of saying the character is the same in both layouts, and a punctuation mark after the word is fixed together with it.
- If another layout switcher was running, Nothy’s double Shift and automatic correction turn back on by themselves once it is closed, without restarting the app.
- The Dictations tab in the history opens right away without waiting for screenshot previews. The list of saved notes is visible immediately, every note change keeps a local backup copy, and a read error no longer looks like an empty library.
- Nothy no longer keeps your Mac from sleeping when idle: the audio device is released after 15 seconds of silence. A forgotten screen area selection closes by itself after 3 minutes, and the app itself is lighter.

### Español

Las capturas del historial se pegan como imagen, el editor de capturas es más cómodo y rápido, el dictado y la mejora de texto arrancan antes, y el conmutador de distribución ahora admite excepciones para palabras y frases.

- Una captura copiada desde el historial se pega como imagen en chats, editores y programas gráficos, no solo como archivo en Finder. Cada fila de captura tiene botones para editarla y copiar el enlace al archivo, y la vista previa se abre con un clic en el icono del ojo y se cierra con otro clic.
- En el editor de capturas vuelves a poder seleccionar con el ratón el texto de los comentarios, y las tarjetas se mueven con un asa aparte. En capturas estrechas la barra de herramientas cabe entera y ya no aparece encima una franja roja de error.
- La captura de un área y el reconocimiento de texto en pantalla arrancan más rápido. El editor abre y guarda las capturas grandes más deprisa, usa menos memoria y dibujar sobre ellas es más fluido.
- El dictado empieza más rápido y ya no pierde el comienzo de lo que dices, incluso cuando el ordenador está ocupado. El panel de grabación aparece antes, el final de la frase no se corta y el audio de una grabación ya no pasa a la siguiente.
- La mejora de texto responde más rápido: la conexión con el servicio de IA se reutiliza, lo que ahorra unos 0,1–0,3 segundos por solicitud, y ya no hay una pausa antes de la mejora automática.
- El conmutador de distribución ahora tiene excepciones: palabras y frases enteras como «plan b» que no toca o que siempre corrige de la misma forma. Puedes añadirlas a mano en la lista de excepciones, con el comando de voz «Añadir a excepciones» o con Shift + Command derecho sobre una palabra. Después de corregir una palabra dos veces igual con un doble Shift, Nothy te propone añadir una excepción, y la lista se conserva aunque reinstales la aplicación.
- El conmutador entiende mejor una letra suelta a partir de las palabras vecinas: en «пишу на rust b python» la b se convierte en la «и» rusa, mientras que «plan b» y «vitamina c» se quedan como están. Un doble Shift sobre una palabra seleccionada ya escrita en la otra distribución la convierte de vuelta en lugar de decir que el carácter es igual en ambas distribuciones, y el signo de puntuación tras la palabra se corrige junto con ella.
- Si había otro conmutador de distribución en marcha, el doble Shift y la corrección automática de Nothy vuelven a activarse solos en cuanto se cierra, sin reiniciar la aplicación.
- La pestaña Dictados del historial se abre al instante sin esperar las vistas previas de las capturas. La lista de notas guardadas se ve de inmediato, cada cambio en una nota guarda una copia de seguridad local y un error de lectura ya no parece una biblioteca vacía.
- Nothy ya no impide que el Mac entre en reposo cuando está inactivo: el dispositivo de audio se libera tras 15 segundos de silencio. Una selección de área de pantalla olvidada se cierra sola a los 3 minutos, y la propia aplicación es más ligera.

## 2.1.47 — 2026-09-24

### Русский

Переключатель раскладки больше не портит длинные сообщения, работает во всех полях Nothy, понимает выделение в Chrome и учится на ваших исправлениях; распознавание текста с экрана больше не молчит при сбое.

- В длинных сообщениях переключатель больше не меняет окончания правильных слов («тут» → «тen») и по-прежнему исправляет слово, набранное не в той раскладке, в конце сообщения.
- Двойной Shift сразу после автоматической замены больше не запрещает навсегда исправлять это слово, а пробел после слова остаётся на месте.
- Английское слово перед точкой или запятой остаётся английским (it. больше не превращается в «шею»).
- Двойной Shift меняет раскладку выделенного слова в Chrome и приложениях на Electron, а короткое нажатие правого Command забирает оттуда выделенный текст вместо выбора области экрана.
- Распознавание текста с экрана показывает «Распознаю текст…» и сообщает, если распознать не удалось; при сбое системного распознавания оно повторяется на процессоре и в свежем процессе, без перезапуска Nothy.
- Enter в редакторе скриншота больше не отправляет текст панели, двойной правый Command в заметках улучшает саму заметку, а подписи внизу панели переведены на все языки.
- Двойной Shift и автоматическое переключение раскладки работают во всех полях Nothy: заметках, сниппетах, поиске, настройках и комментариях к скриншотам.
- Переключатель запоминает слова, которые вы дважды одинаково исправили двойным Shift, и дальше меняет их сам.
- Переключатель узнаёт больше: термины вроде PWA, CRM, SDD и названия моделей, команды Claude Code прямо при наборе (/ьщв → /mod), «и» после английского слова, запятую у слова, залипший Shift, заглавные Э, Ж, Б, Х, Ю, английские сокращения вроде I'm, знак доллара после суммы и вопрос в конце слова.
- В настройках можно выбрать модель OpenRouter по умолчанию, в том числе DeepSeek V4.1 Flash.

### English

The layout switcher no longer damages long messages, works in every Nothy field, understands selections in Chrome and learns from your corrections; screen text recognition no longer fails silently.

- In long messages the switcher no longer changes the endings of correct words and still fixes a word typed in the wrong layout at the end of the message.
- A double Shift right after an automatic correction no longer stops that word from ever being fixed again, and the space after the word stays.
- An English word before a period or comma stays English (it. no longer turns into Russian).
- A double Shift converts a selected word in Chrome and Electron apps, and a short right Command tap takes the selected text from them instead of starting a screen capture.
- Screen text recognition shows “Recognizing text…” and tells you when recognition failed; if the system recognizer fails it retries on the CPU and in a fresh process, without restarting Nothy.
- Enter in the screenshot editor no longer sends the panel text, a double right Command in notes improves the note itself, and the labels at the bottom of the panel are translated into every language.
- Double Shift and automatic layout switching work in every Nothy field: notes, snippets, search, settings and screenshot comments.
- The switcher remembers words you fixed the same way twice with a double Shift and converts them by itself from then on.
- The switcher recognizes more: terms such as PWA, CRM, SDD and model names, Claude Code commands while you type them, a lone letter after an English word, a comma glued to a word, a stuck Shift, capital letters on symbol keys, English contractions such as I'm, a dollar sign after an amount and a question mark after a word.
- Settings let you choose the default OpenRouter model, including DeepSeek V4.1 Flash.

### Español

El conmutador de distribución ya no estropea los mensajes largos, funciona en todos los campos de Nothy, entiende las selecciones en Chrome y aprende de tus correcciones; el reconocimiento de texto en pantalla ya no falla en silencio.

- En los mensajes largos el conmutador ya no cambia las terminaciones de palabras correctas y sigue corrigiendo una palabra escrita con la distribución equivocada al final del mensaje.
- Un doble Shift justo después de una corrección automática ya no impide para siempre corregir esa palabra, y el espacio después de la palabra se conserva.
- Una palabra inglesa antes de un punto o una coma sigue en inglés (it. ya no se convierte en ruso).
- Un doble Shift convierte una palabra seleccionada en Chrome y en apps Electron, y una pulsación corta del Command derecho toma de ellas el texto seleccionado en lugar de iniciar una captura de pantalla.
- El reconocimiento de texto en pantalla muestra «Reconociendo el texto…» y avisa si no se pudo reconocer; si el reconocedor del sistema falla, se reintenta en la CPU y en un proceso nuevo, sin reiniciar Nothy.
- Enter en el editor de capturas ya no envía el texto del panel, un doble Command derecho en las notas mejora la propia nota y las etiquetas de la parte inferior del panel están traducidas a todos los idiomas.
- El doble Shift y el cambio automático de distribución funcionan en todos los campos de Nothy: notas, fragmentos, búsqueda, ajustes y comentarios de capturas.
- El conmutador recuerda las palabras que corregiste dos veces de la misma forma con un doble Shift y a partir de entonces las convierte solo.
- El conmutador reconoce más: términos como PWA, CRM, SDD y nombres de modelos, comandos de Claude Code mientras los escribes, una letra suelta después de una palabra inglesa, una coma pegada a una palabra, un Shift atascado, mayúsculas en teclas de símbolos, contracciones inglesas como I'm, el signo de dólar tras un importe y el signo de interrogación tras una palabra.
- En los ajustes puedes elegir el modelo de OpenRouter predeterminado, incluido DeepSeek V4.1 Flash.

## 2.1.39 — 2026-09-18

### Русский

Открытая панель больше не пропускает клики в окно под ней после того, как приложение на пару секунд было занято.

- Если приложение хотя бы раз задерживалось на две секунды (диалог, долгая операция, сон и пробуждение Mac), панель навсегда застывала в режиме «пропускать клики»: щелчок по тексту уходил в браузер под ней, а клик снаружи не закрывал панель. Теперь такая пауза пропускает одну проверку курсора, и панель продолжает принимать клики.

### English

The open panel no longer lets clicks fall through to the window beneath it after the app was busy for a couple of seconds.

- If the app was ever stalled for two seconds (a dialog, a long operation, the Mac sleeping and waking), the panel froze in click-through mode for good: a click on the text went to the browser beneath it and a click outside no longer closed the panel. Such a pause now skips a single cursor check and the panel keeps accepting clicks.

### Español

El panel abierto ya no deja pasar los clics a la ventana de debajo después de que la aplicación estuviera ocupada un par de segundos.

- Si la aplicación se quedaba bloqueada dos segundos aunque fuera una vez (un diálogo, una operación larga, el Mac durmiendo y despertando), el panel se congelaba para siempre dejando pasar los clics: un clic en el texto iba al navegador de debajo y un clic fuera ya no cerraba el panel. Ahora esa pausa solo omite una comprobación del cursor y el panel sigue aceptando clics.

## 2.1.38 — 2026-09-17

### Русский

Панель диктовки открывается заметно быстрее, запись и промпт поверх открытого текста больше не сворачивают окно, Enter после удачной вставки закрывает панель молча.

- Диктовка по удержанию клавиши открывает панель примерно на 110 мс быстрее и без рывков: показ больше не ждёт кадр у скрытого окна, отрисовку по-прежнему гарантирует система (замер по трассе: от нажатия до панели 324 мс было, 211 мс стало).
- Додиктовка и голосовой промпт поверх уже открытого текста не сворачивают панель в маленькую плашку: запись, распознавание и ответ AI показываются строкой в шапке, поле и кнопки остаются на месте.
- Enter закрывает панель молча, если текст действительно вставлен в приложение; уведомление «Текст скопирован» остаётся для случая, когда вставить было некуда и текст ушёл только в буфер обмена.
- Подсказка распознавания текста читается «Выделите область для захвата текста», а заголовок «Улучшить через AI?» на экранах с вырезом прижат к левому краю панели.

### English

The dictation panel opens noticeably faster, recording or prompting over existing text no longer collapses the window, and Enter after a successful paste closes the panel quietly.

- Holding the dictation key brings the panel up about 110 ms sooner and without jitter: the show no longer waits for a frame from a hidden window, while painting is still guaranteed (traced: 324 ms from key press before, 211 ms now).
- Dictating more text or a voice prompt over an already open panel no longer shrinks it to a small pill: recording, recognition and the AI answer appear in the header line while the field and buttons stay put.
- Enter closes the panel quietly when the text really was pasted into the app; the “Text copied” notice stays for the case where there was nowhere to paste and the text only reached the clipboard.
- The text-capture hint now reads “Select an area to capture text”, and the “Enhance with AI?” caption hugs the left edge of the panel on screens with a cutout.

### Español

El panel de dictado se abre notablemente más rápido, grabar o dictar una instrucción sobre el texto abierto ya no colapsa la ventana y Enter tras un pegado correcto cierra el panel en silencio.

- Mantener la tecla de dictado abre el panel unos 110 ms antes y sin saltos: la aparición ya no espera un fotograma de una ventana oculta y el pintado sigue garantizado (medido: 324 ms desde la pulsación antes, 211 ms ahora).
- Dictar más texto o una instrucción de voz sobre el panel ya abierto deja de encogerlo a una píldora: la grabación, el reconocimiento y la respuesta de la IA se muestran en la línea de cabecera y el campo y los botones no se mueven.
- Enter cierra el panel en silencio cuando el texto se pegó de verdad en la aplicación; el aviso “Texto copiado” queda para cuando no había dónde pegar y el texto solo llegó al portapapeles.
- La pista de captura de texto dice ahora “Selecciona un área para capturar texto”, y el rótulo “¿Mejorar con IA?” se pega al borde izquierdo del panel en pantallas con muesca.

## 2.1.34 — 2026-09-16

### Русский

Двойной правый ⌘ снова улучшает текст, уведомления в одну строку по центру, OCR по тапу копирует текст и отменяется любым жестом, точнее правит раскладку по двойному Shift.

- Двойной правый ⌘ в открытой панели снова улучшает её текст (подпись «Улучшаю…»); вне панели по-прежнему исправляет раскладку по настройке.
- Одиночный тап правого ⌘ распознаёт выбранную область и кладёт текст в буфер обмена с уведомлением «Текст скопирован»; панель не открывается. Крестик выбора отменяется повторным тапом, клавишей диктовки или закрытием панели.
- Уведомления и подсказки в одну строку без кнопки «Подробнее»: у чёлки текст делится на два крыла («Выделите область» | «для скриншота», «Текст» | «скопирован»), на мониторах без чёлки — по центру; длинные уведомления раскрываются сразу с плавной анимацией.
- Мониторы без чёлки: индикатор распознавания и ответа по центру без точек, подпись и таймер записи дальше от краёв, волна по центру, шапка панели и поле ввода ближе к краям.
- Голосовой промпт: во время распознавания подпись «Распознаю…», затем кусок надиктованного промпта; «Улучшаю…» только у улучшайзера.
- Двойной Shift: одиночные знаки следуют клавише, смешанное слово в поле Dictum исправляется по хвосту, ручная замена отменяется своим же жестом, отказы записываются в реестр.
- Двойной Shift читает слово перед курсором через Accessibility, когда журнал клавиш пуст, переводит слово, набранное в другой раскладке, и при выделении возвращается к правилу клавиши.
- Иностранные слова по умолчанию подсвечиваются жёлтым. Бровь на мониторах без чёлки по-прежнему появляется по наведению.

### English

Double Right ⌘ enhances text again, one-line centred notices, tap-to-OCR copies text and cancels on any other gesture, more precise double-Shift layout repair.

- Double Right ⌘ inside the open panel enhances its text again (“Improving…”); outside the panel it still repairs the keyboard layout per the setting.
- A single Right ⌘ tap recognizes the selected region and copies the text with a “Text copied” notice; the panel stays closed. The crosshair is cancelled by another tap, the dictation key or closing the panel.
- Notices and hints on one line without a “Details” button: beside the notch the text is split across the two wings, on screens without a notch it is centred; long notices open at once with a smooth animation.
- Screens without a notch: the recognition and answer indicator is centred without dots, the recording label and timer sit further from the edges, the wave is centred, the panel header and text field reach closer to the edges.
- Voice prompt: “Recognizing…” while the engine works, then a snippet of what you dictated; “Improving…” belongs to the enhancer only.
- Double Shift: lone signs follow the key, a mixed word in the Dictum field is fixed by its tail, a manual retype is undone by the same gesture, refusals are recorded in the registry.
- Double Shift reads the word before the caret through Accessibility when the key journal is empty, converts a word typed in the other layout, and falls back to the key rule for a selection.
- Foreign words are highlighted in yellow by default. The brow on screens without a notch still appears on hover.

### Español

⌘ derecha doble vuelve a mejorar el texto, avisos de una línea centrados, el OCR con un toque copia el texto y se cancela con cualquier gesto, corrección de distribución con doble Shift más precisa.

- ⌘ derecha doble en el panel abierto vuelve a mejorar su texto (“Mejorando…”); fuera del panel sigue corrigiendo la distribución según el ajuste.
- Un toque de ⌘ derecha reconoce la zona seleccionada y copia el texto con el aviso “Texto copiado”; el panel no se abre. La cruz se cancela con otro toque, la tecla de dictado o al cerrar el panel.
- Avisos y pistas en una línea sin botón “Detalles”: junto al notch el texto se reparte en las dos alas, en pantallas sin notch va centrado; los avisos largos se abren de inmediato con animación suave.
- Pantallas sin notch: el indicador de reconocimiento y respuesta va centrado sin puntos, la etiqueta y el temporizador de grabación quedan más lejos de los bordes, la onda va centrada, la cabecera y el campo de texto llegan más cerca de los bordes.
- Prompt de voz: “Reconociendo…” mientras trabaja el motor y luego un fragmento de lo dictado; “Mejorando…” solo para el mejorador.
- Doble Shift: los signos sueltos siguen la tecla, una palabra mixta en el campo de Dictum se corrige por su cola, un reemplazo manual se deshace con el mismo gesto, los rechazos se registran.
- Doble Shift lee la palabra antes del cursor mediante Accesibilidad cuando el registro de teclas está vacío, convierte una palabra escrita en la otra distribución y vuelve a la regla de la tecla con una selección.
- Las palabras extranjeras se resaltan en amarillo por defecto. La ceja en pantallas sin notch sigue apareciendo al pasar el cursor.

## 2.1.27 — 2026-09-16

### Русский

Голосовой промпт по правому ⌘ работает всегда и открывается мгновенно, OCR по тапу приносит текст в Dictum, компактные статусы у чёлки и новая вкладка «Интерфейс».

- Удержание правого ⌘ всегда записывает голосовой промпт: панель появляется сразу в виде записи, выделенный текст в любом приложении становится контекстом, без выделения промпт выполняется как вопрос.
- Одиночный тап правого ⌘ выбирает область экрана для распознавания, и распознанный текст открывается в Dictum. С выделенным текстом тап переносит выделение в панель.
- Пока готовится ответ на голосовой промпт, в строке состояния виден кусок надиктованного промпта; распознавание и ответ показываются одним статусом.
- Компактные статусы по бокам чёлки: запись, промпт, распознавание и уведомления помещаются в одну строку. Новая вкладка «Настройки → Интерфейс»: компактный или полный вид статусов, язык, вид основного окна и бровь на экранах без чёлки.
- Единая высота статусов, широкая волна записи, распознавание и ответ — волна из семи точек, длинные уведомления раскрываются по наведению. На мониторах без чёлки волна по центру, таймер справа; таймер одного размера с подписью.
- Новый красный акцент записи и ошибок. Иностранные слова по умолчанию подсвечиваются жёлтым.
- После закрытия редактора скриншотов панель Dictum больше не всплывает. Панели заметок, сниппетов и истории открываются на экране активного окна. Исправлены отступы текста в окне обновления и пояснении разрешений.

### English

The Right ⌘ voice prompt always works and opens instantly, tap-to-OCR brings text into Dictum, compact statuses beside the notch and a new Interface tab.

- Holding Right ⌘ always records a voice prompt: the panel opens straight into the recording view, selected text in any app becomes the context, and without a selection the prompt runs as a question.
- A single Right ⌘ tap selects a screen region for OCR and the recognized text opens in Dictum. With a selection, the tap imports it into the panel.
- While a voice prompt is being answered, the status line shows a snippet of what you dictated; recognition and the answer share one status.
- Compact statuses beside the notch: recording, prompt, recognition and notices fit in a single row. New Settings → Interface tab: compact or standard statuses, language, main window view and the brow on screens without a notch.
- Unified status height, a wider recording wave, a seven-dot wave for recognition and answers, long notices expand on hover. On screens without a notch the wave is centered with the timer on the right; the timer matches the label size.
- A new red accent for recording and errors. Foreign words are highlighted in yellow by default.
- Closing the screenshot editor no longer pops up the Dictum panel. Notes, snippets and history open on the active window’s display. Text spacing in the update window and the permissions hint is fixed.

### Español

El prompt de voz con ⌘ derecha siempre funciona y se abre al instante, el OCR con un toque trae el texto a Dictum, estados compactos junto al notch y una nueva pestaña Interfaz.

- Mantener ⌘ derecha siempre graba un prompt de voz: el panel se abre directamente en modo grabación, el texto seleccionado en cualquier app se usa como contexto y sin selección el prompt se ejecuta como pregunta.
- Un toque de ⌘ derecha selecciona una zona de pantalla para OCR y el texto reconocido se abre en Dictum. Con texto seleccionado, el toque lo importa al panel.
- Mientras se prepara la respuesta a un prompt de voz, la línea de estado muestra un fragmento de lo dictado; el reconocimiento y la respuesta comparten un solo estado.
- Estados compactos junto al notch: grabación, prompt, reconocimiento y avisos caben en una sola fila. Nueva pestaña Ajustes → Interfaz: estados compactos o estándar, idioma, vista de la ventana principal y la ceja en pantallas sin notch.
- Altura uniforme de los estados, onda de grabación más ancha, onda de siete puntos para reconocimiento y respuestas, avisos largos se despliegan al pasar el cursor. En pantallas sin notch la onda va centrada con el temporizador a la derecha; el temporizador tiene el tamaño de la etiqueta.
- Nuevo acento rojo para grabación y errores. Las palabras extranjeras se resaltan en amarillo por defecto.
- Al cerrar el editor de capturas ya no aparece el panel de Dictum. Notas, fragmentos e historial se abren en la pantalla de la ventana activa. Se corrigen los márgenes del texto en la ventana de actualización y en la nota de permisos.

## 2.1.14 — 2026-09-15

### Русский

Более компактные панели, единый мягкий контур и быстрое появление без обрезания текста и кнопок.

- Единая гибридная форма панелей: короткие плашки имеют мягкий наклон, а высокие окна — плавно выпрямляющиеся боковые края.
- При переходе из записи и расшифровки в основное окно анимация больше не запускается повторно и не разрезает текст или кнопки.
- Поле ввода начинается с одной строки и растёт по мере набора. Запись, голосовой промпт, расшифровка и короткие уведомления используют одинаковую высоту.
- Тонкий контур стал темнее и плавно исчезает у верхнего края экрана. Отступы нижних кнопок основного окна стали аккуратнее.
- Первый запуск и окно обновления используют общий контур и быстрое появление. На экранах без чёлки они не оставляют лишний резерв под камеру.

### English

More compact panels, consistent soft curves, and fast opening without cutting through text or controls.

- Consistent hybrid panel shape: short panels have gently sloped sides, while taller windows smoothly transition to upright edges.
- Switching from recording or transcription to the main window no longer restarts the opening animation or cuts through text and controls.
- The input starts at one line and grows as you type. Recording, voice prompts, transcription and short notifications share the same height.
- The thin outline is darker and fades at the top of the screen. Spacing around the main window’s lower controls has been refined.
- Onboarding and the update window use the shared outline and fast opening. Displays without a notch no longer reserve unnecessary camera space in these panels.

### Español

Paneles más compactos, curvas suaves y uniformes y apertura rápida sin recortar texto ni controles.

- Forma híbrida uniforme: los paneles cortos tienen lados suavemente inclinados y las ventanas altas pasan gradualmente a bordes verticales.
- Al pasar de la grabación o transcripción a la ventana principal, la animación ya no se reinicia ni recorta texto o controles.
- El campo de entrada empieza con una línea y crece al escribir. La grabación, las instrucciones de voz, la transcripción y los avisos cortos tienen la misma altura.
- El contorno fino es más oscuro y se desvanece en el borde superior de la pantalla. Se han ajustado los márgenes de los controles inferiores.
- La configuración inicial y la ventana de actualización usan el contorno y la apertura rápida comunes. En pantallas sin muesca no reservan espacio innecesario para la cámara.

## 2.1.11 — 2026-09-14

### Русский

Плавное раскрытие панели, новый экран обновления и аккуратный интерфейс на дисплеях с чёлкой и без неё.

- Панель открывается одним движением: убрано краткое появление и втягивание лишней плашки под чёлкой перед основным окном.
- Новый экран обновления: версии, описание изменений и ход загрузки собраны в одной карточке; установка доступна после загрузки и проверки пакета.
- Дисплеи без выреза: основная панель, запись и настройки используют пространство у верхней кромки без лишнего резерва под камеру. Размеры текста, волны и кнопок сохранены.
- Определение дисплея и контур: внешний монитор не наследует вырез ноутбука, а тонкая обводка панели и скруглений снова читается целиком.

### English

Smoother panel opening, a redesigned update window, and a refined interface on displays with or without a notch.

- The panel opens in one motion: removed the brief extra strip that appeared and retracted under the notch before the main window.
- Redesigned update window: versions, release notes and download progress share one card; installation becomes available after the package is downloaded and verified.
- Displays without a notch: the composer, recording panel and settings use the top edge without unnecessary camera space. Text, waveform and control sizes are preserved.
- Display detection and panel border: external monitors no longer inherit the laptop notch, and the thin outline stays consistent around the panel and its curves.

### Español

Apertura fluida del panel, una nueva ventana de actualización y una interfaz cuidada en pantallas con o sin muesca.

- El panel se abre en un solo movimiento: se ha eliminado la franja que aparecía y se retraía bajo la muesca antes de la ventana principal.
- Nueva ventana de actualización: versiones, novedades y progreso de descarga en una sola tarjeta; la instalación se habilita tras descargar y verificar el paquete.
- Pantallas sin muesca: el editor, la grabación y los ajustes aprovechan el borde superior sin reservar espacio innecesario para la cámara. Se mantienen los tamaños del texto, la onda y los controles.
- Detección de pantalla y borde: los monitores externos no heredan la muesca del portátil y el contorno fino se mantiene uniforme en el panel y sus curvas.

## 2.1.4 — 2026-09-14

### Русский

Панель диктовки снова открывается поверх полноэкранных приложений, даже когда они запущены после Dictum.

- Панель переставала появляться в полноэкранном режиме через некоторое время работы: она оставалась привязанной к рабочим столам, которые существовали при её первом показе, и не попадала в полноэкранные пространства, созданные позже.
- Панель сама проверяет, находится ли она на текущем рабочем столе, и переносит себя на него, если система оставила её в стороне.

### English

The dictation panel opens over fullscreen apps again, even ones started after Dictum.

- The panel stopped appearing in fullscreen after a while: it stayed bound to the Spaces that existed when it was first shown and never reached fullscreen Spaces created later.
- The panel checks whether it is on the current Space and moves itself there when the system left it behind.

### Español

El panel de dictado vuelve a abrirse sobre aplicaciones a pantalla completa, incluso las iniciadas después de Dictum.

- El panel dejaba de aparecer a pantalla completa después de un rato: quedaba ligado a los espacios que existían en su primera aparición y no llegaba a los espacios a pantalla completa creados después.
- El panel comprueba si está en el espacio actual y se traslada allí cuando el sistema lo dejó fuera.

## 2.1.3 — 2026-09-13

### Русский

Панель диктовки открывается поверх полноэкранных приложений, на мониторах без выреза чёлка показывается по наведению или всегда — по выбору, а текст вставляется туда, где стоит курсор.

- Панель диктовки выпадает поверх приложений в полноэкранном режиме на любом дисплее.
- На дисплеях без выреза чёлка показывается по наведению курсора к верхней кромке или всегда — настройка «Экраны без выреза» в Основных; в полноэкранном режиме там ничего не отвлекает.
- Уведомления и панель на дисплеях без выреза выпадают с верхней кромки без чёрного блока камеры и без подписи с версией.
- Клик вне панели закрывает её, не переключая на другое приложение и его рабочий стол.
- Текст вставляется в приложение, в которое поставлен курсор, пока панель открыта.
- Если при запросе разрешения на запись экрана macOS не показал диалог, приложение само открывает нужный раздел Настроек.
- Чёлка над реальным вырезом больше не двоится при переключении рабочих столов, а её края совпадают с краями панели.

### English

The dictation panel opens over fullscreen apps, on displays without a notch the brow appears on hover or stays put — your choice, and text is pasted where the caret is.

- The dictation panel drops down over fullscreen apps on any display.
- On displays without a notch the brow appears when the pointer touches the top edge or stays visible — the “Displays without a notch” setting in General; nothing shows there in fullscreen.
- Notices and the panel on displays without a notch drop from the top edge without the black camera block and without the version label.
- A click outside the panel closes it without switching to another app and its Space.
- Text is pasted into the app where the caret was placed while the panel stayed open.
- If macOS shows no dialog for the Screen Recording request, the app opens the right System Settings pane itself.
- The brow over a real notch no longer doubles when switching Spaces, and its corners match the panel’s.

### Español

El panel de dictado se abre sobre aplicaciones a pantalla completa, en pantallas sin muesca la ceja aparece al pasar el cursor o se queda fija — a elección, y el texto se pega donde está el cursor.

- El panel de dictado se despliega sobre aplicaciones a pantalla completa en cualquier pantalla.
- En pantallas sin muesca la ceja aparece cuando el puntero toca el borde superior o permanece visible — ajuste «Pantallas sin muesca» en General; a pantalla completa no aparece nada.
- Los avisos y el panel en pantallas sin muesca se despliegan desde el borde superior sin el bloque negro de la cámara y sin la etiqueta de versión.
- Un clic fuera del panel lo cierra sin cambiar a otra aplicación y su espacio.
- El texto se pega en la aplicación donde se colocó el cursor mientras el panel seguía abierto.
- Si macOS no muestra el diálogo al solicitar la grabación de pantalla, la aplicación abre por sí misma la sección correcta de Ajustes.
- La ceja sobre una muesca real ya no se duplica al cambiar de espacio, y sus esquinas coinciden con las del panel.

## 2.1.2 — 2026-09-13

### Русский

Автопереключение раскладки пересобрано по механике Caramba, двойной Shift и Enter работают как в классическом Dictum, уведомления и панель диктовки стали быстрее.

- Автопереключение раскладки решает и перепечатывает слово синхронно внутри перехватчика клавиш, без чтения окна через Accessibility: ранняя замена до пробела, парковка спорных коротких слов до соседа, курируемый словарь разработчика.
- Реестр ручных исправлений: каждый двойной Shift записывает слово, замену, контекст и вердикт ядра; обратный двойной Shift помечается как отмена.
- Двойной Shift сохраняет знаки, которые целевая раскладка умеет набирать: /сщьзфсе становится /compact, а не |compact; слова с ё снова перепечатываются.
- Enter при открытой панели отправляет текст независимо от того, какое окно держит клавиатуру; если вставить некуда, текст остаётся в буфере и панель закрывается.
- Панель диктовки показывается сразу при подтверждении удержания клавиши, все всплывающие уведомления длятся полторы секунды.
- Служба автоподъёма перезапускает приложение после падения WebKit, чтобы автопереключение не пропадало молча.

### English

Layout auto-switching rebuilt on the Caramba mechanics, double Shift and Enter behave like classic Dictum, notifications and the dictation panel got faster.

- Layout auto-switching now decides and retypes a word synchronously inside the key interceptor, without reading the window through Accessibility: early switch before the space, ambiguous short words wait for their neighbour, curated developer vocabulary.
- Manual correction registry: every double Shift records the word, its replacement, the context and the core verdict; a reverse double Shift is marked as a revert.
- Double Shift keeps punctuation the target layout can type: /сщьзфсе becomes /compact instead of |compact; words with ё retype again.
- Enter with the panel open submits the text no matter which window owns the keyboard; when there is nowhere to paste, the text stays in the clipboard and the panel closes.
- The dictation panel appears as soon as the key hold is confirmed, and every pop-up notice lasts one and a half seconds.
- A keep-alive service relaunches the application after a WebKit crash so layout switching never disappears silently.

### Español

El cambio automático de distribución se reconstruyó con la mecánica de Caramba, doble Shift y Enter funcionan como en Dictum clásico, y las notificaciones y el panel de dictado son más rápidos.

- El cambio automático de distribución decide y reescribe la palabra de forma síncrona dentro del interceptor de teclas, sin leer la ventana mediante Accesibilidad: cambio temprano antes del espacio, las palabras cortas ambiguas esperan a su vecina, vocabulario de desarrollador curado.
- Registro de correcciones manuales: cada doble Shift guarda la palabra, su reemplazo, el contexto y el veredicto del núcleo; un doble Shift inverso se marca como reversión.
- Doble Shift conserva los signos que la distribución de destino puede escribir: /сщьзфсе pasa a /compact y no a |compact; las palabras con ё vuelven a reescribirse.
- Enter con el panel abierto envía el texto sin importar qué ventana tenga el teclado; si no hay dónde pegar, el texto queda en el portapapeles y el panel se cierra.
- El panel de dictado aparece en cuanto se confirma la pulsación mantenida, y cada aviso emergente dura un segundo y medio.
- Un servicio de reinicio vuelve a lanzar la aplicación tras un fallo de WebKit para que el cambio de distribución no desaparezca en silencio.
