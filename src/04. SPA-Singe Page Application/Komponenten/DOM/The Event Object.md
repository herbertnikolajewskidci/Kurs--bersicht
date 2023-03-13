# The Event Object

## Tastatur-Ereignisse: `keydown`, `keyup`
Diese Ereignisse werden ausgelöst, wenn der Benutzer eine Taste auf der Tastatur drückt oder loslässt. Das Ereignisobjekt ist ein KeyboardEvent, das eine Eigenschaft key hat, die angibt, welche Taste gedrückt wurde.

```javascript
// Ein Element auswählen, das den Fokus erhalten kann
const input = document.getElementById("textBox");

// Eine Funktion definieren, die das Ereignisobjekt als Parameter erhält
function logKey(event) {
  // Die gedrückte Taste in der Konsole ausgeben
  console.log(event.key);
}

// Einen Listener für das keydown-Ereignis hinzufügen
input.addEventListener("keydown", logKey);

// Einen Listener für das keyup-Ereignis hinzufügen
input.addEventListener("keyup", logKey);
```

## Die Eigenschaften des Ereignisobjekts: Ein Konsolenbeispiel
Das Ereignisobjekt hat viele Eigenschaften, die Informationen über das Ereignis enthalten. Zum Beispiel hat es eine Eigenschaft type, die den Namen des Ereignisses angibt. Ein einfaches Beispiel wäre, den Typ des Ereignisses in der Konsole auszugeben.

```javascript
// Ein beliebiges Element auswählen
const button = document.querySelector("button");

// Eine Funktion definieren, die das Ereignisobjekt als Parameter erhält
function logType(event) {
  // Den Typ des Ereignisses in der Konsole ausgeben
  console.log(event.type);
}

// Einen Listener für verschiedene Ereignisse hinzufügen
button.addEventListener("click", logType);
button.addEventListener("mouseover", logType);
button.addEventListener("mouseout", logType);
```

## Das Ziel des Ereignisses ermitteln: `Event.target`
Die Eigenschaft target des Ereignisobjekts gibt das Element zurück, auf dem das Ereignis ursprünglich ausgelöst wurde. Dies kann nützlich sein, um zu wissen, welches Element vom Benutzer interagiert wurde. Zum Beispiel könnte man den Text eines Elements ändern, wenn es angeklickt wird.

```javascript
// Alle Elemente mit der Klasse "item" auswählen
const items = document.querySelectorAll(".item");

// Eine Funktion definieren, die das Ereignisobjekt als Parameter erhält
function changeText(event) {
  // Das Ziel des Ereignisses ermitteln und seinen Text ändern
  event.target.textContent = "Clicked";
}

// Einen Listener für das click-Ereignis zu jedem Element hinzufügen
items.forEach(item => item.addEventListener("click", changeText));
```

## Formular-Ereignisse: `submit`, `reset`, `Event.preventDefault()`
Das submit-Ereignis wird ausgelöst, wenn ein Formular abgesendet wird. Man kann einen Ereignis-Listener für dieses Ereignis hinzufügen, um eine Funktion auszuführen, bevor das Formular an den Server gesendet wird. Zum Beispiel:

```javascript
// Ein Formular mit der ID "myForm" auswählen
let form = document.getElementById("myForm");

// Eine Funktion definieren, die beim Absenden des Formulars ausgeführt werden soll
function handleSubmit(event) {
  // Das Standardverhalten des Formulars verhindern (z.B. Neuladen der Seite)
  event.preventDefault();
  // Einen Hinweis anzeigen oder eine andere Aktion ausführen
  alert("Formular abgesendet!");
}

// Einen Ereignis-Listener für das submit-Ereignis hinzufügen
form.addEventListener("submit", handleSubmit);
```

- Das reset-Ereignis wird ausgelöst, wenn ein Formular zurückgesetzt wird. Das heißt, wenn ein Benutzer auf einen Reset-Button klickt oder das Element form.reset() aufruft. Man kann auch einen Ereignis-Listener für dieses Ereignis hinzufügen, um eine Funktion auszuführen, bevor das Formular zurückgesetzt wird. Zum Beispiel:

```javascript
// Ein Formular mit der ID "myForm" auswählen
let form = document.getElementById("myForm");

// Eine Funktion definieren, die beim Zurücksetzen des Formulars ausgeführt werden soll
function handleReset(event) {
  // Das Standardverhalten des Formulars verhindern (z.B. Löschen aller Felder)
  event.preventDefault();
  // Einen Hinweis anzeigen oder eine andere Aktion ausführen
  alert("Formular zurückgesetzt!");
}

// Einen Ereignis-Listener für das reset-Ereignis hinzufügen
form.addEventListener("reset", handleReset);
```

## Abrufen von Formularwerten beim Absenden: `target.elements[<id>]`, `target.elements[<name>]`, `Element.value`
- Um die Werte der einzelnen Felder eines Formulars beim Absenden zu erhalten, kann man die Eigenschaft target.elements des Ereignisobjekts verwenden. Diese Eigenschaft gibt eine Sammlung von allen Elementen innerhalb des Formulars zurück.
- Man kann dann auf jedes Element entweder nach seiner ID oder seinem Namen zugreifen und seine value-Eigenschaft lesen. Zum Beispiel:

```javascript
// Ein Formular mit der ID "myForm" auswählen
let form = document.getElementById("myForm");

// Eine Funktion definieren, die beim Absenden des Formulars ausgeführt werden soll
function handleSubmit(event) {
  // Das Standardverhalten des Formulars verhindern (z.B. Neuladen der Seite)
  event.preventDefault();
  // Die Sammlung von allen Elementen innerhalb des Formulars erhalten
  let elements = event.target.elements;
  // Auf jedes Element nach seiner ID oder seinem Namen zugreifen und seinen Wert lesen
  let name = elements["name"].value; // oder elements.name.value;
  let email = elements["email"].value; // oder elements.email.value;
  let message = elements["message"].value; // oder elements.message.value;
  
  // Die Werte anzeigen oder eine andere Aktion ausführen
  console.log(`Name: ${name}, Email: ${email}, Message: ${message}`);
}

// Einen Ereignis-Listener für das submit-Ereignis hinzufügen
form.addEventListener("submit", handleSubmit);
```

