HTML-Datei (index.html):
```html
<!DOCTYPE html>
<html lang="en">
    <head>
        <meta charset="UTF-8" />
        <meta http-equiv="X-UA-Compatible" content="IE=edge" />
        <meta name="viewport" content="width=device-width, initial-scale=1.0" />
        <title>JavaScript Events</title>
    </head>
    <body>
        <h1>JavaScript Events</h1>
        <button id="btn-click">Click me</button>
        <div id="element">Hover over me</div>
        <script src="app.js"></script>
    </body>
</html>
```

JS-Datei (app.js):
```js
// User Events (interaction)
const btnClick = document.getElementById('btn-click');
btnClick.addEventListener('click', function() {
  alert('Button clicked');
});

// Aufgabe => User Events (interaction)
btnClick.addEventListener('mousover', function() {
  console.log('Mouse-Over-Event getriggert!');
});

// --------------------------------------

// Browser Events
window.addEventListener('load', function() {
  console.log('Page loaded');
});

window.addEventListener('resize', function() {
  console.log('Window resized');
});

// Aufgab => Browser Events
window.addEventListener('resize', function() {
  console.log('Window-Reszie-Event getriggert!');
});


// -------------------------------------- 

// Higher-order Functions I: Functions that accept function values (Callbacks)
function greet(name, callback) {
  console.log('Hello ' + name);
  callback();
}

function sayGoodbye() {
  console.log('Goodbye!');
}

greet('John', sayGoodbye);


// Aufgabe => Higher-order Functions I: Functions that accept function values (Callbacks)

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


// --------------------------------------

// Listening to user actions: EventTarget.addEventListener(namespace, callback)
const btn = document.getElementById('btn-click');
btn.addEventListener('click', function() {
  console.log('Button clicked');
});

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

// Aufgabe => Mouse events: Click, Mouseenter, Mouseleave

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

// --------------------------------------

// Removing Event Listeners: EventTarget.removeEventListener(namespace, function reference)
function handleClick() {
  console.log('Button clicked');
  btn.removeEventListener('click', handleClick);
}


// Aufgabe => Removing Event Listeners: EventTarget.removeEventListener(namespace, function reference)

// Mouseover-Event-Listener, der sich selbst entfernt
const element = document.getElementById('element');
function handleMouseover() {
  console.log('Mouse entered element');
  element.removeEventListener('mouseover', handleMouseover);
}
element.addEventListener('mouseover', handleMouseover);

btn.addEventListener('click', handleClick);

// --------------------------------------

// Listening to browser events: Event DOMContentLoaded
document.addEventListener('DOMContentLoaded', function() {
  console.log('DOM fully loaded');
});
```