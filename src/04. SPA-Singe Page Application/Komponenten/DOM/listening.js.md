### Funktionen höherer Ordnung I recap: Funktionen, die Funktionswerte akzeptieren (Callbacks)
```js
function greet(name, callback) {
  console.log('Hello ' + name);
  callback();
}

function sayGoodbye() {
  console.log('Goodbye!');
}

greet('Alice', sayGoodbye);
```

---

Das nächste Beispiel zeigt eine Funktion höherer Ordnung in JavaScript. `greet` ist eine Funktion, die einen Namen und eine weitere Funktion `callback` als Argumente akzeptiert. In diesem Beispiel wird die `sayGoodbye`-Funktion als `callback` übergeben. `greet` gibt "Hello " und den Namen aus und ruft dann die übergebene `callback`-Funktion auf, die "Goodbye!" ausgibt.

---

### Abhören von Benutzeraktionen: `EventTarget.addEventListener(<Namensraum>, <Callback>)`
```js
const button = document.getElementById('button');

button.addEventListener('click', function(){
  alert('Button clicked');
});
```

---

Dieses Codebeispiel zeigt, wie man einen Ereignislistener auf ein HTML-Element setzt, um auf eine Benutzeraktion zu reagieren. Das `addEventListener`-Methode wird auf das Button-Element angewendet, und wenn der Button geklickt wird, wird die angegebene Funktion ausgeführt.

---

### Maus-Ereignisse: `Klick`, `Mouseenter`, `Mouseleave`
```js
const button = document.getElementById('button');

button.addEventListener('click', function(){
  alert('Button clicked');
});

const element = document.getElementById('element');
element.addEventListener('mouseenter', function(){
  console.log('Mouse entered');
});

element.addEventListener('mouseleave', function(){
  console.log('Mouse left');
});
```


---

Diese Codebeispiele zeigen, wie man auf verschiedene Mausereignisse wie Klicks, das Betreten und Verlassen eines Elements reagieren kann. Hier werden die `addEventListener`-Methoden verwendet, um Ereignislistener auf das Button-Element und das Element mit der ID `element` zu setzen. Wenn das Ereignis ausgelöst wird, wird die angegebene Funktion ausgeführt.

---

### Entfernen von Ereignislistenern: `EventTarget.removeEventListener(<Namensraum>, <Funktionsreferenz>)`

```js

const button = document.getElementById('button');

function handleClick() {
  alert('Button clicked');
  button.removeEventListener('click', handleClick);
}

button.addEventListener('click', handleClick);
```

---

Dieses Codebeispiel zeigt, wie man einen Ereignislistener von einem HTML-Element entfernt. Zunächst wird ein Ereignislistener auf das Button-Element gesetzt, und wenn der Button geklickt wird, wird die `handleClick`-Funktion ausgeführt. Die `handleClick`-Funktion entfernt dann den Ereignislistener von dem Button-Element.

---

### Abhören von Browser-Ereignissen: Ereignis `DOMContentLoaded`

```js
const button = document.getElementById('button');

document.addEventListener('DOMContentLoaded', function() {
  console.log('DOM fully loaded and parsed');
});
```

---

Dieses Codebeispiel zeigt, wie man auf das Ereignis `DOMContentLoaded` reagieren kann, das ausgelöst wird, wenn das HTML-Dokument vollständig geladen und analysiert wurde. Hier wird das `addEventListener`-Methode auf das `document`-Objekt angewendet, um einen Ereignislistener auf `DOMContentLoaded` zu setzen. Wenn das Ereignis ausgelöst wird, wird die angegebene Funktion ausgeführt, die in diesem Beispiel eine Meldung in der Konsole ausgibt, die besagt, dass das DOM geladen wurde. Dies kann nützlich sein, wenn Sie sicherstellen möchten, dass alle Elemente auf der Seite vollständig geladen wurden, bevor Sie mit der Ausführung Ihres JavaScript-Codes beginnen.

---

### Weitere Ereignisse auf MDN finden

MDN bietet eine umfangreiche Dokumentation über Ereignisse in JavaScript: [https://developer.mozilla.org/en-US/docs/Web/Events](https://developer.mozilla.org/en-US/docs/Web/Events). Sie können weitere Ereignisse und deren Verwendung auf dieser Seite finden.

---