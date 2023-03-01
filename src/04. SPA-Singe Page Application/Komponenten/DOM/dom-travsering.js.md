---
title: "dom-traversing"
theme: "black"
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

Hier wird der Unterschied demonstriert zwischen einem Knoten (Node) und einem Element (Element). Beide können über die DOM-Methoden previousSibling und previousElementSibling abgerufen werden, um das vorherige Geschwister-Element eines bestimmten Elements zu finden. Der **Unterschied** besteht darin, dass **previousSibling jedes beliebige vorherige Geschwister-Element** zurückgibt, einschließlich Textknoten, Leerzeichen und Kommentaren, während **previousElementSibling nur das vorherige Geschwister-Element** zurückgibt, das auch ein Elementknoten ist.

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

Dieser Code-Block zeigt die Verwendung der Methode closest, um das nächstgelegene übergeordnete Element zu finden, das einem gegebenen Selektor entspricht. Dies ist besonders nützlich, wenn Sie das Eltern-Element eines bestimmten Elements finden müssen, um beispielsweise ein Ereignis auszulösen oder das Eltern-Element zu modifizieren.

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

Dieser Code-Block zeigt die Verwendung der Methode matches, um zu testen, ob ein bestimmtes Element einem gegebenen Selektor entspricht. Diese Methode gibt true zurück, wenn das Element mit dem Selektor übereinstimmt, andernfalls false.

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

Dieser Block zeigt die Verwendung der Eigenschaft children, um eine HTML-Sammlung aller direkten Kinder eines bestimmten Elternelements zu erhalten. Diese Methode gibt nur Elementknoten zurück und ignoriert Textknoten und Kommentare.

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

Dieser Code-Block zeigt die Verwendung der Methode querySelector, um das erste Kind-Element eines Elternelements zu finden, das einem gegebenen Selektor entspricht.

---

Weitere Traversierungstechniken finden Sie in der MDN-Dokumentation: [https://developer.mozilla.org/en-US/docs/Web/API/Document_Object_Model/Traversing_an_HTML_table_with_JavaScript_and_DOM_Interfaces](https://developer.mozilla.org/en-US/docs/Web/API/Document_Object_Model/Traversing_an_HTML_table_with_JavaScript_and_DOM_Interfaces)

---