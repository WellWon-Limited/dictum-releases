# Dictum Nothy — changelog

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
