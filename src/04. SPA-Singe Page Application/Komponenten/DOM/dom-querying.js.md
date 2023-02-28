---
title: "dom-querying"
theme: "white"
---
 
## Querying: Getting elements from 'document'
---

Auswählen von Elementen auf die alte Art mit `document.getElementById(<id string>)`:
```js
// Beispiel: Ein Element mit der ID 'myElement' auswählen
const myElement = document.getElementById('myElement');
```

---

Auswählen per CSS-Abfrage: `document.querySelector(<selector string>)`:
```js
// Beispiel: Das erste Element mit der Klasse 'myClass' auswählen
const myElement = document.querySelector('.myClass');
```

---

Mehr als ein Element abrufen: `document.querySelectorAll(<selector string>)`:
```js
// Beispiel: Alle Elemente mit der Klasse 'myClass' auswählen
const myElements = document.querySelectorAll('.myClass');
// Auf jedes Element in der NodeList zugreifen
myElements.forEach(function(element) {
  console.log(element);
});
```

---

Element-Stil: CSS-Stile mit der Eigenschaft HTMLElement.style ändern:
```js
// Beispiel: Die Hintergrundfarbe eines Elements ändern
const myElement = document.getElementById('myElement');

myElement.style.backgroundColor = 'red';

```

---

