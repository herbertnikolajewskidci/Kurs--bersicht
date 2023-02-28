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

---

Ändern des Textes innerhalb eines Elements: Die Eigenschaft HTMLElement.innerText
```js
// Get the element
const element = document.getElementById("my-element");

// Change the text inside the element
element.innerText = "New text";
```

---

Ändern des HTML-Inhalts: Die Eigenschaft Element.innerHTML
```js
// Get the element
const element = document.getElementById("my-element");

// Change the HTML content inside the element
element.innerHTML = "<h1>New Heading</h1><p>New paragraph</p>";
```

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

---

