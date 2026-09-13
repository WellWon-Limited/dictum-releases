# Dictum Nothy — changelog

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
