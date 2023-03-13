# Introduction Modules

Module sind Dateien, die eine Klasse oder eine Bibliothek von Funktionen für einen bestimmten Zweck enthalten. Module können sich gegenseitig laden und spezielle Direktiven export und import verwenden, um Funktionalität auszutauschen oder Funktionen eines Moduls von einem anderen aus aufzurufe.

```javascript
// 📁 sayHi.js
function sayHi(user) {
    console.log(`Hello, ${user}!`);
}
module.exports = sayHi;

// 📁 main.js
const sayHi = require("./sayHi.js");

console.log(sayHi); // function…
sayHi("John"); // Hello, John!
```

## Module für kleinere Dateien
Module helfen dabei, den Code in kleinere Dateien aufzuteilen, die leichter zu warten und zu testen sind. Jedes Modul hat seinen eigenen Gültigkeitsbereich und vermeidet Namenskonflikte mit anderen Modulen.

```javascript
// 📁 admin.js
const admin = {
    name: "John",
};
module.exports = admin;

// 📁 user.js
const admin = require("./admin.js");

admin.name = "Pete"; // changed by user.js

// 📁 main.js
const admin = require("./admin.js");
require("./user.js"); // only run the code

console.log(admin.name); // Pete
```
