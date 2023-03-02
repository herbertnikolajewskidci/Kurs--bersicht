# Non-Blocking Promises
## Blocking vs. Non-Blocking code: A brief example, `window.setTimeout()`

Blocking Code ist Code, der die Ausführung anderer Teile des Programms blockiert, bis er abgeschlossen ist. Nicht-blockierender Code hingegen erlaubt es anderen Teilen des Programms, während seiner Ausführung weiterzulaufen.

Ein Beispiel für blockierenden Code wäre eine Schleife, die sehr lange läuft, während der restliche Code wartet:

```js
for (let i = 0; i < 1000000000; i++) {
  // Schleife läuft sehr lange...
}
console.log("Fertig!");
```

Ein Beispiel für nicht-blockierenden Code ist `window.setTimeout()`, der eine Funktion nach einer bestimmten Verzögerung ausführt, während der restliche Code weiterläuft:

```js
console.log("Start");
window.setTimeout(() => {
  console.log("Verzögert");
}, 1000);
console.log("Ende");
```

## Race conditions: Reading non blocking code
Race-Conditions treten auf, wenn mehrere Tasks gleichzeitig ausgeführt werden und es unklar ist, welche zuerst ausgeführt werden wird. In JavaScript kann eine Race-Condition bei asynchronem Code auftreten, der um die Wette ausgeführt wird. Zum Beispiel:
```js
let result;

setTimeout(() => {
  result = "Done";
}, 2000);

console.log(result);
```
In diesem Beispiel wird "undefined" ausgegeben, da `result` noch nicht definiert ist, bevor `console.log()` ausgeführt wird. Die Zuweisung von `result` erfolgt asynchron in der `setTimeout()`-Funktion.

## Promises: `new Promise(<function>)`, `Promise.resolve()`, `Promise.then()`
Promises sind ein asynchrones Konzept, das es ermöglicht, asynchronen Code zu schreiben, der leichter zu lesen und zu verstehen ist. Ein Promise ist ein Objekt, das eine asynchrone Operation darstellt und eine Methode zum Umgang mit dem Ergebnis dieser Operation bietet.
```js
const promise = new Promise((resolve, reject) => {
  // Async operation
  if (/* success condition */) {
    resolve("Success!");
  } else {
    reject("Error!");
  }
});

promise.then(result => {
  console.log(result);
}).catch(error => {
  console.log(error);
});
```
In diesem Beispiel wird ein Promise erstellt, das entweder erfolgreich (`resolve`) oder mit einem Fehler (`reject`) beendet wird. Der `then`-Block wird ausgeführt, wenn die Operation erfolgreich war, und der `catch`-Block wird ausgeführt, wenn ein Fehler aufgetreten ist.

## Promisifying: Converting `setTimeout()` to a promise

Promisifying ist der Prozess, eine asynchrone Funktion in eine Promise-basierte Funktion umzuwandeln. Das kann z.B. hilfreich sein, um Callback-Hell zu vermeiden. Hier ein Beispiel, wie man `setTimeout()` in ein Promise umwandelt:

```js
function delay(ms) {
  return new Promise(resolve => setTimeout(resolve, ms));
}

delay(2000).then(() => {
  console.log("Done!");
});
```
In diesem Beispiel wird die Funktion `delay()` definiert, die eine Verzögerung von `ms` Millisekunden verursacht und dann das Promise auflöst. Der `then`-Block wird ausgeführt, wenn die Verzögerung abgeschlossen ist.

## Breaking Promises: `Promise.reject()`, `Promise.catch()`, `Promise.finally()`
Promises können auch absichtlich "gebrochen" werden, um einen Fehler zu signalisieren. Hier sind einige Methoden, um ein Promise zu brechen:

```js
const promise = new Promise((resolve, reject) => {
  // Async operation
  if (/* success condition */) {
    resolve("Success!");
  } else {
    reject("Error!");
  }
});

promise.catch(error => {
  console.log(error);
}).finally(() => {
  console.log("Finished!");
});
```

In diesem Beispiel wird `Promise.reject()` verwendet, um das Promise mit einem Fehler zu beenden. Der `catch`-Block wird ausgeführt, wenn das Promise abgelehnt wurde, und der `finally`-Block wird unabhängig davon ausgeführt, ob das Promise erfolgreich war oder nicht.