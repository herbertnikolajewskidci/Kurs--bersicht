
## Vor ES6 Update
### IIFE
IIFE steht für "Immediately Invoked Function Expression" und ist eine Funktion, die sich selbst aufruft. Sie wird oft verwendet, um Variablen vor dem globalen Scope zu schützen und Module zu erstellen. Ein Beispiel für eine IIFE ist:


```javascript
const ThirdPartySDK = (function() {
  var _export = {};
  // Add some methods to export
  return _export;
})();
```

Dieser Code exportiert ein Objekt mit einigen Methoden, die von der IIFE erstellt wurden.

### Modulmuster - Module Pattern
Das Modulmuster ist eine Möglichkeit, private und öffentliche Mitglieder in einem Objekt zu definieren, indem man eine IIFE verwendet. Das Modulmuster kann auch verwendet werden, um Abhängigkeiten zu verwalten und Namenskonflikte zu vermeiden. Ein Beispiel für das Modulmuster ist:

```javascript
const myModule = (function () {
  // Private variables and functions
  var counter = 0;
  function increment() {
    counter++;
  }
  // Public interface
  return {
    getCounter: function () {
      return counter;
    },
    setCounter: function (value) {
      counter = value;
    },
    addOne: function () {
      increment();
    }
  };
})();
```

Dieser Code erstellt ein Modul namens myModule, das einige private Variablen und Funktionen sowie einige öffentliche Methoden enthält.

### Scope Isolation
Scope Isolation bedeutet, dass Variablen und Funktionen nur innerhalb eines bestimmten Bereichs sichtbar sind. Dies verhindert Verschmutzung des globalen Scopes und Kollisionen zwischen verschiedenen Modulen oder Skripten. Eine Möglichkeit, Scope Isolation zu erreichen, ist die Verwendung von IIFEs oder Block Scopes mit let oder const.


### Encapsulation
Encapsulation bedeutet, dass Daten und Verhalten eines Objekts zusammengefasst werden und nur über eine definierte Schnittstelle zugänglich sind. Dies fördert die Modularität und Wartbarkeit des Codes. Eine Möglichkeit, Encapsulation zu erreichen, ist die Verwendung des Modulmusters oder von Klassen.
 
## Post ES6
#### Verwendung von Modulen im Browser: `<script type="module" src="...">`
Dies bedeutet, dass man JavaScript-Dateien als Module laden kann, die einen eigenen Gültigkeitsbereich haben und Funktionen oder Variablen exportieren oder importieren können. Zum Beispiel:

```html
<!-- index.html -->
<script type="module" src="main.js"></script>
```

```js
// main.js
import { sayHello } from "./module.js"; // import a function from another module
sayHello("World"); // call the function
```

```js
// module.js
export function sayHello(name) { // export a function
  console.log(`Hello, ${name}!`);
}
```

### Verbinden von Dateien: Die Schlüsselwörter import und export
Dies bedeutet, dass man Funktionen oder Variablen aus einem Modul in ein anderes Modul übertragen kann. Zum Beispiel:

```js
// module1.js
export const PI = 3.14; // export a constant
export function add(x, y) { // export a function
  return x + y;
}
```

```js
// module2.js
import { PI, add } from "./module1.js"; // import the constant and the function from another module

console.log(PI); // 3.14
console.log(add(2, 3)); // 5

```
