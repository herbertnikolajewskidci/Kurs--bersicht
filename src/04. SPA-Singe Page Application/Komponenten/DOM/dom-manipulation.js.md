---
title: "dom-manipulation"
theme: "white"
---

## Manipulating: Changing the DOM tree

---


Manipulation von Klassen: Element.classList-Methoden
```js
// Get the element
const element = document.getElementById("my-element");

// Add a class to the element
element.classList.add("new-class");

// Remove a class from the element
element.classList.remove("old-class");

// Toggle a class on the element
element.classList.toggle("active");
```
Die Manipulation von Klassen (Klassenattribute) wird durch die Verwendung der Eigenschaft `classList` des HTML-Elements durchgeführt. `classList` ist ein Objekt, das eine Reihe von Methoden enthält, mit denen Klassen hinzugefügt, entfernt oder umgeschaltet werden können. In dem Beispielcode wird zunächst ein Element mit einer bestimmten ID ausgewählt, dann wird eine neue Klasse hinzugefügt, eine alte Klasse entfernt und eine Klasse umgeschaltet (wenn sie bereits vorhanden ist, wird sie entfernt, andernfalls wird sie hinzugefügt).

---

Ändern des Textes innerhalb eines Elements: Die Eigenschaft HTMLElement.innerText
```js
// Get the element
const element = document.getElementById("my-element");

// Change the text inside the element
element.innerText = "New text";
```
Das Ändern des Textes innerhalb eines Elements wird durch die Verwendung der Eigenschaft `innerText` des HTML-Elements durchgeführt. In dem Beispielcode wird zunächst ein Element mit einer bestimmten ID ausgewählt, dann wird der Text im Inneren des Elements durch einen neuen Text ersetzt.

---

Ändern des HTML-Inhalts: Die Eigenschaft Element.innerHTML
```js
// Get the element
const element = document.getElementById("my-element");

// Change the HTML content inside the element
element.innerHTML = "<h1>New Heading</h1><p>New paragraph</p>";
```
Das Ändern des HTML-Inhalts wird durch die Verwendung der Eigenschaft `innerHTML` des HTML-Elements durchgeführt. In dem Beispielcode wird zunächst ein Element mit einer bestimmten ID ausgewählt, dann wird der Inhalt des Elements durch eine neue HTML-Darstellung ersetzt. Beachten Sie, dass durch die Verwendung von `innerHTML` auch andere HTML-Elemente innerhalb des Elements eingefügt werden können, wie z.B. Überschriften und Absätze im Beispielcode.

---

Elemente erstellen: document.createElement(Tagname)
```js
// Create a new element
const newElement = document.createElement("div");

// Set attributes on the new element
newElement.id = "new-element";
newElement.className = "new-class";

// Add text to the new element
newElement.innerText = "New element created!";

// Add the new element to the page
document.body.appendChild(newElement);
```
Das Erstellen von Elementen wird durch die Verwendung der Methode `document.createElement` durchgeführt. In dem Beispielcode wird eine neue `div`-Element erstellt, dann werden der Element-ID und die Klassenattribute festgelegt und schließlich wird Text im Inneren des Elements hinzugefügt. Die `appendChild`-Methode wird verwendet, um das neue Element zum Ende des `body`-Elements hinzuzufügen.

---

Hinzufügen von Elementen auf der Seite: Element.append(Element object), siehe MDN-Dokumente für .append()
```js
// Get the parent element
const parent = document.getElementById("parent-element");

// Create a new element
const newElement = document.createElement("div");

// Set attributes on the new element
newElement.id = "new-element";
newElement.className = "new-class";

// Add text to the new element
newElement.innerText = "New element created!";

// Add the new element to the parent element
parent.append(newElement);
```
Das Hinzufügen von Elementen auf der Seite wird durch die Verwendung der Methode `Element.append` durchgeführt. In dem Beispielcode wird zunächst das Elternelement mit einer bestimmten ID ausgewählt, dann wird ein neues `div`-Element erstellt und ihm eine ID, Klassenattribute und Text zugewiesen. Schließlich wird das neue Element zum Ende des Elternelements hinzugefügt.

---

