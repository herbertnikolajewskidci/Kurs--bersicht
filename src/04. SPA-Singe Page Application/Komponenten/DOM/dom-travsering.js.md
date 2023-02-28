---
title: "dom-traversing"
theme: "white"
---


## Traversing: Jumping from one element to its relative

---

Node vs. Element: Vergleich von Node.previousSibling und Element.previousElementSibling

```js
// Get the element
const element = document.getElementById("my-element");

// Get the previous sibling (node)
const prevSiblingNode = element.previousSibling;

// Get the previous sibling (element)
const prevSiblingElement = element.previousElementSibling;

console.log(prevSiblingNode); // Text node
console.log(prevSiblingElement); // Element node
```

---

Ermitteln des nächstgelegenen übergeordneten Elements: Element.closest(selector string)

```js
// Get the element
const element = document.getElementById("my-element");

// Find the nearest ancestor element that matches the selector
const closestAncestor = element.closest(".parent-class");

console.log(closestAncestor); // The ancestor element
```

---

Testen eines Elements gegen einen Selektor: Element.matches(selector string)
```js
// Get the element
const element = document.getElementById("my-element");

// Test if the element matches the selector
const isMatch = element.matches(".my-class");

console.log(isMatch); // true or false
```

---

Alle Kinder eines Elements ermitteln: ParentNode.children

```js
// Get the parent element
const parent = document.getElementById("parent-element");

// Get all child elements of the parent
const children = parent.children;

console.log(children); // A HTMLCollection of child elements
```

---

Auswahl bestimmter Kinder: ParentNode.querySelector(selector string)

```js
// Get the parent element
const parent = document.getElementById("parent-element");

// Get the first child element that matches the selector
const child = parent.querySelector(".child-class");

console.log(child); // The child element
```

---

Weitere Traversierungstechniken finden Sie in der MDN-Dokumentation: [https://developer.mozilla.org/en-US/docs/Web/API/Document_Object_Model/Traversing_an_HTML_table_with_JavaScript_and_DOM_Interfaces](https://developer.mozilla.org/en-US/docs/Web/API/Document_Object_Model/Traversing_an_HTML_table_with_JavaScript_and_DOM_Interfaces)

---