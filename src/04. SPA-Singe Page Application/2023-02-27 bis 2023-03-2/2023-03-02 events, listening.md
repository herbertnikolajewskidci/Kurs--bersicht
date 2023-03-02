## ==🌞 <font style="color:green">20 Minuten Auftauen</font>==

## Vorschau auf die/den Woche/Tag:

- [[Übersicht-SPA#Events]]
- [[Übersicht-SPA#Listening]]

## Wiederholung Vortag  - 📖

[[2023-03-01 DOM querying, manipulation and traversing]]

---

## Pause 10:30 Uhr - ⏯️

---

## Hauptthema - 🔍

### Curriculum 📚

![[Übersicht-SPA#Events]]
![[Übersicht-SPA#Listening]]


### [Live Coding -  💻](https://github.com/FBW-WD-22-D07/Single-Page-Application-SPA/tree/main)

-   [[events.js]]
-   [[listening.js]]
- [[events-listening-live-coding]]
---

### [Übungen](https://classroom.github.com/classrooms/113973596-fbw-wd-22-d07-ubungsaufgaben) - 🏋️‍♂️

- [https://github.com/DigitalCareerInstitute/Browser-PasswordField/](https://github.com/DigitalCareerInstitute/Browser-PasswordField/)  
- [https://github.com/DigitalCareerInstitute/Browser-DynamicPills](https://github.com/DigitalCareerInstitute/Browser-DynamicPills)  (Optional)  
- [https://github.com/DigitalCareerInstitute/Browser-QuoteOfTheDay/](https://github.com/DigitalCareerInstitute/Browser-QuoteOfTheDay/) (Optional)  
- [https://github.com/DigitalCareerInstitute/Browser-ToggleItems/](https://github.com/DigitalCareerInstitute/Browser-ToggleItems/)   (Optional)  
- [https://github.com/DigitalCareerInstitute/Browser-NewsletterSubscription/](https://github.com/DigitalCareerInstitute/Browser-NewsletterSubscription/)   (Optional)  
- [https://github.com/DigitalCareerInstitute/Browser-Calculator/](https://github.com/DigitalCareerInstitute/Browser-Calculator/)   (Optional)  
- [https://github.com/DigitalCareerInstitute/SPA-DOM-Carousel/](https://github.com/DigitalCareerInstitute/SPA-DOM-Carousel/)   (Optional)

### Ablauf

Titel: Einführung in JavaScript Events

Zielgruppe: Anfänger in JavaScript-Programmierung

Dauer: 1 Stunde

Materialien: Computer, Texteditor, Webbrowser

Lernziele:

- Grundlegende Konzepte von Events in JavaScript verstehen
- Verschiedene Arten von Events kennen und wie man auf sie reagieren kann
- Verwendung von Event-Listenern und Callback-Funktionen

---

1.  Einleitung (5 Minuten)

-   Begrüßen Sie die Klasse.
-   Erklären Sie, dass wir heute über **JavaScript-Events** sprechen werden.
-   Erklären Sie, dass Events in **JavaScript Ereignisse** sind, die **im Browser oder auf der Seite** auftreten und dass **JavaScript-Code darauf reagieren** kann.

---

2.  User Events (interaction) (15 Minuten)

-   Erklären Sie, dass **User Events Ereignisse** sind, die durch **Interaktionen des Benutzers mit der Seite** ausgelöst werden.
-   Zeigen Sie ein einfaches Beispiel eines **Click-Events mit einem Button** und einer **Alert-Box.**
```js
// User Events (interaction)
const btnClick = document.getElementById('btn-click');
btnClick.addEventListener('click', function() {
  alert('Button clicked');
});
```
-   Lassen Sie die Klasse ein ähnliches Beispiel mit einem Mouseover-Event und einer Konsolenausgabe schreiben.  - (5 Minuten)
```js
btnClick.addEventListener('mouseover', function() {
  console.log('Mouse-Over-Event getriggert!');
});
```

---

3.  Browser Events (15 Minuten)

-   Erklären Sie, dass **Browser Events Ereignisse** sind, die **vom Browser ausgelöst** werden, wie das **Laden einer Seite** oder das **Ändern der Größe des Fensters.**
-   Zeigen Sie ein Beispiel eines **Load-Events,** das eine **Konsolenausgabe** ausgibt, wenn die **Seite vollständig** geladen ist.
```js
// Browser Events
window.addEventListener('load', function() {
  console.log('Page loaded');
});

window.addEventListener('resize', function() {
  console.log('Window resized');
});
```
-   Lassen Sie die Klasse ein ähnliches Beispiel mit einem Resize-Event und einer Konsolenausgabe schreiben. - (5 Minuten)
```js
window.addEventListener('resize', function() {
  console.log('Window-Reszie-Event getriggert!');
});
```

4.  Funktionen höherer Ordnung I recap: Funktionen, die Funktionswerte akzeptieren (Callbacks) (10 Minuten)

-   Erklären Sie, dass **Funktionen höherer Ordnung Funktionen** sind, die **andere Funktionen als Argumente** akzeptieren oder **als Rückgabewerte liefern.**
-   Zeigen Sie ein Beispiel einer Funktion höherer Ordnung, die eine Callback-Funktion als Argument akzeptiert und ausführt.
```js
// Higher-order Functions I: Functions that accept function values (Callbacks)
function greet(name, callback) {
  console.log('Hello ' + name);
  callback();
}

function sayGoodbye() {
  console.log('Goodbye!');
}

greet('John', sayGoodbye);
```

-   Lassen Sie die Klasse ein ähnliches Beispiel schreiben, das eine Funktion höherer Ordnung und eine Callback-Funktion enthält. - (5 Minuten)
```js
// Funktion höherer Ordnung, die eine Callback-Funktion akzeptiert
function addButtonClickListener(callback) {
  const button = document.getElementById('btn-click');
  button.addEventListener('click', callback);
}

// Callback-Funktion, die bei einem Klick auf den Button aufgerufen wird
function handleClick() {
  alert('Du hast den Button geklickt!');
}

// Aufruf der Funktion höherer Ordnung mit der Callback-Funktion
addButtonClickListener(handleClick);
```


5.  Abhören von Benutzeraktionen (20 Minuten)

-   Erklären Sie, dass man mit **Event-Listenern auf Benutzeraktionen hören** und **darauf reagieren** kann.
-   Zeigen Sie ein Beispiel eines Click-Event-Listeners, der eine Konsolenausgabe ausgibt, wenn ein Button geklickt wird.
```js
// Listening to user actions: EventTarget.addEventListener(namespace, callback)
const btn = document.getElementById('btn-click');
btn.addEventListener('click', function() {
  console.log('Button clicked');
});
```
-   Zeigen Sie ein Beispiel einer Mouseover-Event-Listener-Kette, die eine Konsolenausgabe ausgibt, wenn die Maus über ein Element bewegt wird.
```js
// Mouse events: Click, Mouseenter, Mouseleave
const element = document.getElementById('element');
element.addEventListener('click', function() {
  console.log('Element clicked');
});

element.addEventListener('mouseenter', function() {
  console.log('Mouse entered element');
});

element.addEventListener('mouseleave', function() {
  console.log('Mouse left element');
});
```
-   Lassen Sie die Klasse ein ähnliches Beispiel schreiben, das einen Event-Listener für ein benutzerdefiniertes Ereignis enthält. - (10 Minuten) Tipp: https://developer.mozilla.org/en-US/docs/Web/API/Event/Event?retiredLocale=de
```js
// Benutzerdefiniertes Ereignis
const customEvent = new Event('customEvent');

// Event-Listener für das benutzerdefinierte Ereignis
document.addEventListener('customEvent', function() {
  console.log('Benutzerdefiniertes Ereignis ausgelöst');
});

// Button-Event-Listener, der das benutzerdefinierte Ereignis auslöst
const customEventBtn = document.getElementById('customEventBtn');
customEventBtn.addEventListener('click', function() {
  document.dispatchEvent(customEvent);
});
```

6.  Entfernen von Ereignislistenern (10 Minuten)

-   Erklären Sie, dass man mit removeEventListener() Event-Listener von einem Element entfernen kann.
-   Zeigen Sie ein Beispiel eines Click-Event-Listeners, der sich selbst entfernt, nachdem er ausgeführt wurde.
```js
// Removing Event Listeners: EventTarget.removeEventListener(namespace, function reference)
function handleClick() {
  console.log('Button clicked');
  btn.removeEventListener('click', handleClick);
}

btn.addEventListener('click', handleClick);
```
- Lassen Sie die Klasse ein ähnliches Beispiel schreiben, das einen Mouseover-Event-Listener entfernt, nachdem er ausgeführt wurde. - (5 Minuten)
```js
// Mouseover-Event-Listener, der sich selbst entfernt
const element = document.getElementById('element');
function handleMouseover() {
  console.log('Mouse entered element');
  element.removeEventListener('mouseover', handleMouseover);
}
element.addEventListener('mouseover', handleMouseover);

```

7.  Abhören von Browser-Ereignissen (5 Minuten)

-   Erklären Sie, dass man mit dem **DOMContentLoaded-Event** auf das Laden des DOM warten und dann auf JavaScript reagieren kann.
-   Zeigen Sie ein Beispiel eines DOMContentLoaded-Event-Listeners, der eine Konsolenausgabe ausgibt, wenn der DOM vollständig geladen ist.
```js
// Listening to browser events: Event DOMContentLoaded
document.addEventListener('DOMContentLoaded', function() {
  console.log('DOM fully loaded');
});
```

8.  Zusammenfassung und Ausblick (5 Minuten)

-   Fassen Sie die wichtigsten Punkte der Lektion zusammen.
-   Geben Sie einen Ausblick auf mögliche nächste Schritte im Umgang mit JavaScript-Events, wie das Verwenden von Event-Objekten oder das Schreiben von eigenen Event-Listenern.

