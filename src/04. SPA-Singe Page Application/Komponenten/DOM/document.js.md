---

---
 
## Querying: Getting elements from 'document'
---

1.  Auswählen von Elementen auf die alte Art mit `document.getElementById(<id string>)`:
```js
// Beispiel: Ein Element mit der ID 'myElement' auswählen
const myElement = document.getElementById('myElement');
```

---

2.  Auswählen per CSS-Abfrage: `document.querySelector(<selector string>)`:
```js
// Beispiel: Das erste Element mit der Klasse 'myClass' auswählen
const myElement = document.querySelector('.myClass');
```

---

3.  Mehr als ein Element abrufen: `document.querySelectorAll(<selector string>)`:
```js
// Beispiel: Alle Elemente mit der Klasse 'myClass' auswählen
const myElements = document.querySelectorAll('.myClass');
// Auf jedes Element in der NodeList zugreifen
myElements.forEach(function(element) {
  console.log(element);
});
```

---

4.  Element-Stil: CSS-Stile mit der Eigenschaft HTMLElement.style ändern:
```js
// Beispiel: Die Hintergrundfarbe eines Elements ändern
const myElement = document.getElementById('myElement');

myElement.style.backgroundColor = 'red';

```

---

## Manipulating: Changing the DOM tree

---


1. Manipulation von Klassen: Element.classList-Methoden
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

---

2. Ändern des Textes innerhalb eines Elements: Die Eigenschaft HTMLElement.innerText
```js
// Get the element
const element = document.getElementById("my-element");

// Change the text inside the element
element.innerText = "New text";
```

---

3. Ändern des HTML-Inhalts: Die Eigenschaft Element.innerHTML
```js
// Get the element
const element = document.getElementById("my-element");

// Change the HTML content inside the element
element.innerHTML = "<h1>New Heading</h1><p>New paragraph</p>";
```

---

4. Elemente erstellen: document.createElement(Tagname)
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

---

5. Hinzufügen von Elementen auf der Seite: Element.append(Element object), siehe MDN-Dokumente für .append()
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

---
