Imports und Exports sind Schlüsselwörter in JavaScript, die verwendet werden, um Code zwischen verschiedenen Modulen zu teilen.
## Default exports vs. named exports: 
  - Default exports sind Exporte, die einen Standardwert für ein Modul bereitstellen. Es kann nur einen default export pro Modul geben. Die Syntax ist `export default <value>`.
```js
// Default export
// In module.js
export default function hello() {
  console.log("Hello");
}

// In main.js
import greet from "./module.js";
greet(); // Hello
```
  - Named exports sind Exporte, die einen oder mehrere benannte Werte für ein Modul bereitstellen. Es können mehrere named exports pro Modul geben. Die Syntax ist `export {<var1>, <var2> [, ...]}`.
```js
// Named exports
// In module.js
export const PI = 3.14;
export function add(x, y) {
  return x + y;
}

// In main.js
import { PI, add } from "./module.js";
console.log(PI); // 3.14
console.log(add(2, 3)); // 5
```
## Namespacing imports: 
Namespacing imports sind Importe, die alle Exporte eines Moduls unter einem einzigen Namen importieren. Dies ist nützlich, um Namenskonflikte zu vermeiden oder den Code übersichtlicher zu machen. Die Syntax ist `import <namespace> from <path>` oder `import * as <namespace> from <path>`.

```js
// Namespacing imports
// In module.js
export const PI = 3.14;
export function add(x, y) {
  return x + y;
}

// In main.js
import * as math from "./module.js";
console.log(math.PI); // 3.14
console.log(math.add(2, 3)); // 5
```
## Destructuring imports: 
Destructuring imports sind Importe, die nur bestimmte benannte Exporte eines Moduls importieren. Dies ist nützlich, um nur die benötigten Werte zu importieren oder sie umzubenennen. Die Syntax ist `import { <var1>, <var2 [, ...]} from <path>`.

```js
// Destructuring imports
// In module.js
export const PI = 3.14;
export function add(x, y) {
  return x + y;
}

// In main.js
import { PI as pi, add as sum } from "./module.js";
console.log(pi); // 3.14
console.log(sum(2, 3)); // 5
```