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
Die Verwendung von `document.getElementById(<id string>)` ermöglicht es, ein Element auf der Seite durch die Angabe seiner eindeutigen ID zu finden und eine Referenz auf dieses Element zu erstellen. Das zurückgegebene Objekt kann dann zur weiteren Verwendung in der JavaScript-Logik verwendet werden.

---

Auswählen per CSS-Abfrage: `document.querySelector(<selector string>)`:
```js
// Beispiel: Das erste Element mit der Klasse 'myClass' auswählen
const myElement = document.querySelector('.myClass');
```
`document.querySelector(<selector string>)` ermöglicht das Auffinden von Elementen mithilfe von CSS-Selektoren. Mit diesem Befehl können Elemente durch ihre Klassen, IDs oder andere Attributwerte ausgewählt werden. Das zurückgegebene Objekt ist das erste Element, das der Abfrage entspricht.

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
`document.querySelectorAll(<selector string>)` funktioniert ähnlich wie `querySelector`, gibt jedoch alle Elemente zurück, die der Abfrage entsprechen. Die zurückgegebenen Elemente werden in einer NodeList gespeichert, auf die mithilfe von `forEach` zugegriffen werden kann.

---

Element-Stil: CSS-Stile mit der Eigenschaft HTMLElement.style ändern:
```js
// Beispiel: Die Hintergrundfarbe eines Elements ändern
const myElement = document.getElementById('myElement');

myElement.style.backgroundColor = 'red';
```
Das Ändern von CSS-Stilen von Elementen kann über die Eigenschaft `style` des HTMLElements erfolgen. Durch Zuweisung von neuen Werten zu diesen Stileigenschaften können Elemente im Dokument dynamisch gestaltet werden.

---

