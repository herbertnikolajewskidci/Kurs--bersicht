---
title: "Promise"
theme: 'white'
---

# "Promise"

![Pinky swear](https://media2.giphy.com/media/GFtJhEvG3681y/giphy.gif)

---

1. "Promise" auf Deutsch "Versprechen"

2. "Promises" sind nicht optional. Wir MÜSSEN sie lernen. Welche Bibliothek / API wir auch immer verwenden, wir werden mit "Promises" interagieren

<small>Frage: Was ist ein Versprechen (in menschlichen Begriffen?)</small>

---

## Wir werden folgende Themen behandeln:

- Was ist ein "Promise"?
- Warum verwenden wir "Promises" und wo können wir sie finden?
- Wie erstellt man ein "Promise" im Code?
- Zustände von "Promises"

---

## Was ist ein "Promise"?

---

> Wenn Du jemandem etwas versprichst, hältst Du das Versprechen entweder ein oder Du brichst es.

\- Eine Weise Person 🧐
<!-- .element: align="right" -->

---

In der Programmierung kann die Person, die das "Promise" abgibt, entweder:

dieses Versprechen halten/auflösen => `resolve` 🙂
oder  
das Versprechen brechen/ablehnen => `reject` 😑.

---

Je nachdem, wie ein Versprechen ausgeht, reagierst Du unterschiedlich:

Wenn es gehalten wurde, **dann** reagierst Du mit `then` 😀👍

Wenn das Versprechen aber gebrochen wurde, war das ein Fehler, den Du **fangen** kannst => `catch` ☹️👎

---

### Stellen wir uns das mal vor:

---

### Wenn die Dinge gut laufen...

Person A 👩 wird von Person B etwas versprochen 👨

Person B 👨 erfüllt das Versprechen mit `resolve()`

Person A 👩 ist glücklich und benutzt `then()`

👩 💗 👨

---

### Wenn die Dinge schief gehen...

Person A 👩 wird von Person B etwas versprochen 👨

Person B 👨 erfüllt das Versprechen nicht und verwendet `reject()`

Person A 👩 ist NICHT zufrieden und benutzt `catch()`.

👩 💔 👨

---

## Warum benutzen wir "Promises" und wo können wir sie finden?

---

### Warum Promises?
- wenn wir eine asynchrone Operation durchführen, zum Beispiel beim Zugriff auf Ressourcen von einem anderen Server
- um Fehler besser und vorhersehbarer zu behandeln
- um uns zu helfen, saubereren Code zu schreiben

___


<small>

Anmerkungen:

Wir haben uns noch nicht mit asynchronem JavaScript beschäftigt, also mach' Dir darüber nicht zu viele Gedanken.
Das Wichtigste ist, dass wir mit einem Promise einen Vertrag zwischen zwei Parteien schließen. Es entsteht eine formale Beziehung.
Löst Probleme, auf die Du wahrscheinlich noch nicht gestoßen bist
</small>

---

## Wie erstellen wir einen "Promise" im Code?

---

Einführung in das `Promise`-Objekt

---

Genau wie `Date` oder jede andere ES6-Klasse müssen wir `new` verwenden, um das `Promise`-Objekt zu instanzieren.

`Promise` ruft einen Konstruktor auf.


---

Ein `Promise` braucht einen Callback.

Dieser Callback hat zwei Argumente, `resolve` und `reject`, die beide Funktionen sind:

```Javascript
const promise = new Promise((resolve, reject) => {});
```

---
Normalerweise findest Du das `Promise`-Objekt in der `Return`-Anweisung einer Funktion:

```Javascript
function studyJavaScript() {
    const promise = new Promise((resolve, reject) => {});

    return promise;
}
```



```javascript
function studyJavaScript() {
    return new Promise((resolve, reject) => {});
}
```

---

Wir benutzen die Funktion `reject()`, um zu sagen:  
Etwas ist NICHT in Ordnung,  
wir werden das `Promise` NICHT erfüllen:

```javascript
function studyJavaScript() {
    return new Promise((resolve, reject) => {
        reject();
    });
}
```

---

Wenn wir `reject()` verwenden, sollten wir einen Fehler übergeben:

```javascript
function studyJavaScript() {
    return new Promise((resolve, reject) => {
        reject(new Error('Nein, ich bin zu müde'));
    });
}
```

---

Wir benutzen die Funktion `resolve()`, um zu sagen:  
Alles ist in Ordnung,  
wir halten das `Promise`:

```javascript
function studyJavaScript() {
    return new Promise((resolve, reject) => {
        if(1 === 1) {
            resolve();
        } else {
            reject(new Error('Nein, ich bin zu müde'));
        }
    });
}
```

---

Jetzt haben wir gesehen, wie man ein `Promise` erstellt, aber wie reagieren wir auf ein solches im Code?

---

Auf der Verbraucherseite wird das `Promise` verwendet.
Dort kann das Promise auf zwei Arten behandelt werden:

---

1.

Wenn das `Versprechen` gehalten/erfüllt wurde, wird die Methode `then()` ausgeführt, was bedeutet: "Das Versprechen wurde gehalten, lass uns das tun".

---

2.

Wenn das `Promise` gebrochen/abgelehnt wurde, können wir anderen Code durch die Methode `catch()` laufen lassen, um zu sagen: "Das Versprechen wurde NICHT gehalten, lass uns stattdessen dies tun".

---

Auf ein `Promise` mit `then` und `catch` reagieren:
```javascript
    const shouldIStudy = studyJavaScript();

    shouldIStudy.then(() => {
        console.log("woohoo!")
    });

    shouldIStudy.catch(() => {
        console.log("NOOOOO!")
    });
```

---

### Schauen wir uns ein vollständiges Beispiel im Code an:

---

Wir benutzen die Funktionen  
`resolve()`, wenn alles in Ordnung ist, und  
`reject()`, wenn etwas nicht in Ordnung ist:

```javascript
    // Person B 👨

    function iWillGetYouFlowers(flowersAreInSeason) {
        return new Promise((resolve, reject) => {
            if(flowersAreInSeason) {
                resolve();
            } else {
                reject();
            }
        });
    }
```

---

Behandlung mit `then` und `catch`:

```javascript
    // Person A 👩

    const doIGetFlowers = iWillGetYouFlowers();

    doIGetFlowers.then(() => {
        console.log('💗');
    });

    doIGetFlowers.catch((error) => {
        console.log('💔');
    });
```

<small>

**Frage:** Siehst Du etwas, das in diesem Code fehlt?  
**Antwort:** Es fehlt der Eingabeparameter `flowersAreInSeason`.
</small>

---

Verkettete Behandlung mit `then` und `catch`:

```javascript
    // Person A 👩 (mit Verkettung)

    iWillGetYouFlowers()
        .then(() => {
            console.log('💗');
        })
        .catch((error) => {
            console.log('💔');
        });
```

<small>

**Frage:** Siehst Du etwas, das in diesem Code fehlt?  
**Antwort:** Es fehlt der Eingabeparameter `flowersAreInSeason`.
</small>

---

## Promise States

---

**Ein Versprechen kann sich in einem von 3 Zuständen befinden:**

- _pending_ - (wartend) der Ausgangszustand. Von hier aus können wir in einen der anderen Zustände wechseln  
- _fulfilled_ - das Versprechen wurde erfüllt  
- _rejected_ - das Versprechen wurde gebrochen

---

Informationen mit dem `Promise` Übergeben

👨 ➡️ 👩

Wenn ein `Promise` abgelehnt oder erfüllt wird,  
können wir zusätzliche Informationen mit ihm senden.

---

Wenn wir zum Beispiel ein `Promise` ablehnen, kann es nützlich sein zu wissen, warum:

```javascript
    function iWillGetYouFlowers(flowersAreInSeason) {
        return new Promise((resolve, reject) => {
            if(flowersAreInSeason) {
                resolve();
            } else {
                reject(new Error('Es gibt keine Blumen'));
            }
        });
    }
```

---

Wenn wir ein `Promise` mit `resolve()` auflösen,  
kann auch eine Information gesendet werden:

```javascript
    function iWillGetYouFlowers(flowersAreInSeason) {
        return new Promise((resolve, reject) => {
            if(flowersAreInSeason) {
                resolve('Du bekommst eine Tulpe');
            } else {
                reject(new Error('Es gibt keine Blumen'));
            }
        });
    }
```

---

Diese zusätzliche Information ist über den Parameter der jeweiligen Callback-Funktion verfügbar, bspw.:

```javascript
    const doIGetFlowers = iWillGetYouFlowers();

    doIGetFlowers.then((Nachricht) => {
        console.log('💗', message); 
        // '💗 Du bekommst eine Tulpe'
    });
```
