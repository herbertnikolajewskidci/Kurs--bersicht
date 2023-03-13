![DCI_Event_Listeners_03.png (1579×986) (raw.githubusercontent.com)](https://raw.githubusercontent.com/FBW-WD-22-D07/spa-jan/main/2023_03_09/DCI_Event_Listeners_03.png?token=GHSAT0AAAAAAB6AN4ZFM36RRTYIH6IB53V2ZAMJTPA)
# Propagation, Delegation: `<ul>`, `<li>` examples

## Anwendungsfall:

Ein typischer Anwendungsfall für diese Thematik ist, wenn man viele Elemente hat, die auf ähnliche Weise behandelt werden sollen, z.B. eine Liste von Buttons oder Links. Anstatt jedem Element einen eigenen Event-Listener zuzuweisen, kann man einen einzigen Event-Listener auf den gemeinsamen Vorfahren setzen und dann die Ereignisquelle mit Event.target oder Event.currentTarget überprüfen. Das spart Speicher und verbessert die Leistung.

Ein konkretes Beispiel wäre eine **Todo-Liste**, bei der man auf jedes Todo-Element klicken kann, um es zu löschen oder zu bearbeiten. Anstatt jedem Todo-Element einen Klick-Event-Listener hinzuzufügen, kann man einen Klick-Event-Listener auf das übergeordnete `<ul>`-Element setzen und dann die Ereignisdelegation verwenden, um zu bestimmen, welches Todo-Element angeklickt wurde.

## Konzept der Ereignisblasenbildung: "Ereignisse sprudeln vom innersten zum äußersten Element"

Das Konzept der Ereignisblasenbildung (Event Bubbling) bedeutet, dass ein Ereignis, das auf einem Element ausgelöst wird, auch auf seine übergeordneten Elemente übertragen wird. Zum Beispiel, wenn Sie auf einen Button klicken, wird das Klickereignis auch auf den div ausgelöst, der den Button enthält. Dies kann zu unerwünschten Effekten führen, wenn Sie verschiedene Aktionen für verschiedene Elemente haben.

## Häufige Probleme mit Bubbling: `Event.stopPropagation()` als Lösung

Um die Ereignisblasenbildung (Event Bubbling) zu verhindern, können Sie die Methode Event.stopPropagation() verwenden. Diese Methode verhindert, dass das Ereignis an die übergeordneten Elemente weitergegeben wird. Zum Beispiel:

```HTML
<!-- HTML-Code -->
<div id="div1">
  <button id="btn1">Click me</button>
</div>
```

```javascript
// JavaScript-Code
// Ein Listener für den Button
document.getElementById("btn1").addEventListener("click", function(event) {
  // Mach etwas mit dem Button
  console.log("Button clicked");
  // Verhindere die Blasenbildung
  event.stopPropagation();
});

// Ein Listener für den div
document.getElementById("div1").addEventListener("click", function(event) {
  // Mach etwas mit dem div
  console.log("Div clicked");
});
```

In diesem Beispiel wird nur "Button clicked" in der Konsole angezeigt, wenn Sie auf den Button klicken. Das Ereignis wird nicht an den div weitergegeben.

## Unterschiedliche Ziele: `Event.target` vs. `Event.currentTarget`

Der Unterschied zwischen Event.target und Event.currentTarget ist, dass Event.target das Element ist, das das Ereignis tatsächlich ausgelöst hat, während Event.currentTarget das Element ist, an das der Listener gebunden ist. Zum Beispiel:

```HTML
<!-- HTML-Code -->
<div id="div1">
  <button id="btn1">Click me</button>
</div>
```

```javascript
// JavaScript-Code
// Ein Listener für den div
document.getElementById("div1").addEventListener("click", function(event) {
  // Zeige die Ziele an
  console.log(event.target); // Der Button
  console.log(event.currentTarget); // Der div
});
```

In diesem Beispiel ist event.target der Button und event.currentTarget der div. Dies kann nützlich sein, um zu bestimmen, welches Element angeklickt wurde.

## Probleme mit Ereignis-Listenern: Auswirkungen auf die Leistung, Hinzufügen von Ereignissen zu dynamischen Listen

 Wenn es viele Ereignis-Listener gibt oder wenn sie an Elemente angehängt werden, die häufig hinzugefügt oder entfernt werden, kann dies die Leistung beeinträchtigen, da der Browser mehr Arbeit leisten muss, um die Ereignisse zu verarbeiten und zu verwalten. Ein Beispiel für ein solches Szenario ist eine Liste von Elementen, die dynamisch aktualisiert wird.

Code-Beispiel:

```js
// Eine Liste von Elementen erstellen
let list = document.createElement("ul");
document.body.appendChild(list);

// Eine Funktion definieren, die ein neues Listenelement mit einem Ereignis-Listener hinzufügt
function addListItem(text) {
  let item = document.createElement("li");
  item.textContent = text;
  // Ein Ereignis-Listener an das Listenelement anhängen
  item.addEventListener("click", function() {
    alert("Du hast auf " + text + " geklickt.");
  });
  list.appendChild(item);
}

// Die Liste mit einigen Elementen füllen
addListItem("Apfel");
addListItem("Banane");
addListItem("Orange");

// Die Liste alle zwei Sekunden mit einem neuen Element aktualisieren
setInterval(function() {
  addListItem(Math.random().toString());
}, 2000);
```

Dieser Code fügt jedem Listenelement einen eigenen Ereignis-Listener hinzu. Das bedeutet, dass jedes Mal, wenn ein neues Element hinzugefügt wird, ein neuer Listener erstellt und registriert wird. Das kann zu einer Verschwendung von Speicher und Rechenleistung führen.

Eine bessere Lösung ist es, einen einzigen Ereignis-Listener an das Elternelement anzuhängen und die Ereignisdelegation zu verwenden.

## Lösung der Ereignisdelegation: Delegieren von Ereignissen vom Elternteil zum Kind

Ereignisdelegation ist eine Technik, bei der man einen einzigen Ereignis-Listener an ein Elternelement anhängt und dann das Ziel des ausgelösten Ereignisses überprüft. Auf diese Weise kann man mehrere Kinderelemente mit einem einzigen Listener behandeln. Das spart Speicher und verbessert die Leistung.

Code-Beispiel:

```js
// Eine Liste von Elementen erstellen
let list = document.createElement("ul");
document.body.appendChild(list);

// Eine Funktion definieren, die ein neues Listenelement hinzufügt
function addListItem(text) {
  let item = document.createElement("li");
  item.textContent = text;
  list.appendChild(item);
}

// Die Liste mit einigen Elementen füllen
addListItem("Apfel");
addListItem("Banane");
addListItem("Orange");

// Die Liste alle zwei Sekunden mit einem neuen Element aktualisieren
setInterval(function() {
  addListItem(Math.random().toString());
}, 2000);

// Einen einzigen Ereignis-Listener an das Listenobjekt anhängen
list.addEventListener("click", function(event) {
  // Das Ziel des ausgelösten Ereignisses ermitteln
  let target = event.target;
  // Überprüfen Sie ob das Ziel ein Listenelement ist (und nicht die ganze Liste)
  if (target.tagName === "LI") {
    // Den Text des Ziels anzeigen
    alert("Du hast auf " + target.textContent + " geklickt.");
  }
});
```

Dieser Code verwendet nur einen Listener für alle Listenelemente. Das bedeutet weniger Arbeit für den Browser und eine bessere Skalierbarkeit.

Hier sind einige Erklärungen und Code-Beispiele für die ausgewählten Punkte:

## Umkehrung der Ausbreitung: 
Dies bedeutet, dass die Ereignisse vom äußersten zum innersten Element sprudeln (bubble), anstatt vom innersten zum äußersten. Dies kann erreicht werden, indem die Option useCapture in addEventListener auf true gesetzt wird. Zum Beispiel:

```javascript
// Das äußere Element
var outer = document.getElementById("outer");

// Das innere Element
var inner = document.getElementById("inner");

// Ein Ereignislistener für das äußere Element mit useCapture = true
outer.addEventListener("click", function(event) {
  console.log("Das äußere Element wurde geklickt");
}, true);

// Ein Ereignislistener für das innere Element mit useCapture = false (Standardwert)
inner.addEventListener("click", function(event) {
  console.log("Das innere Element wurde geklickt");
}, false);

// Wenn das innere Element geklickt wird, wird zuerst der Listener des äußeren Elements ausgelöst und dann der Listener des inneren Elements
```

### Die Option useCapture in addEventListener:
Dies ist ein boolescher Parameter, der angibt, ob der Ereignislistener die Ereignisse während der **Erfassungsphase** (Capture-Phase) oder der **Bubble-Phase** behandeln soll. Die Erfassungsphase ist die Phase, in der das Ereignis vom obersten Elternelement zum Zielobjekt propagiert wird. Die Bubble-Phase ist die Phase, in der das Ereignis vom Zielobjekt zum obersten Elternelement propagiert wird. Der Standardwert von useCapture ist false, was bedeutet, dass die Blasenphase verwendet wird. Wenn useCapture auf true gesetzt wird, wird die Erfassungsphase verwendet.


### Anwendungsfall DOMContentLoaded:
Dies ist ein Ereignis, das ausgelöst wird, wenn das HTML-Dokument vollständig geladen und analysiert wurde. Es kann verwendet werden, um Skripte auszuführen oder DOM-Manipulationen durchzuführen, ohne darauf zu warten, dass alle externen Ressourcen wie Bilder oder Stylesheets geladen werden. Um einen Listener für dieses Ereignis hinzuzufügen, kann man folgenden Code verwenden:

```javascript
document.addEventListener("DOMContentLoaded", function(event) {
  // Hier kann man den DOM manipulieren oder Skripte ausführen
});
```

Um sicherzustellen, dass dieser Listener vor allen anderen Listeners ausgeführt wird (die möglicherweise von anderen Skripten hinzugefügt wurden), kann man den Parameter useCapture auf true setzen:

```javascript
document.addEventListener("DOMContentLoaded", function(event) {
  // Hier kann man den DOM manipulieren oder Skripte ausführen
}, true);
```

Das DOMContentLoaded-Ereignis hängt mit der Ereignisausbreitung und -delegation zusammen, weil es ein Ereignis ist, das vom innersten zum äußersten Element sprudelt. Das bedeutet, dass Sie das Ereignis an einem übergeordneten Element abhören und dann das Ziel des Ereignisses überprüfen können, um zu sehen, welches Kinderelement ausgelöst hat. Dies ist nützlich, wenn Sie mehrere Elemente haben, die die gleiche Funktionalität benötigen oder wenn Sie dynamisch Elemente hinzufügen oder entfernen. Sie können auch die Option useCapture in addEventListener verwenden, um die Ausbreitungsrichtung umzukehren und das Ereignis vom äußersten zum innersten Element zu erfassen.

Das DOMContentLoaded-Ereignis wird ausgelöst, wenn das HTML-Dokument vollständig geladen und geparst wurde. Es wartet nicht darauf, dass andere Dinge wie Bilder oder Unterframes fertig geladen sind. Wenn Sie einen Ereignis-Listener für dieses Ereignis an das `<window>`-Objekt anhängen, können Sie sicher sein, dass alle Elemente im Dokument verfügbar sind. Dies ist nützlich für die Ereignisdelegation, da Sie keinen Listener an jedes einzelne Element anhängen müssen, das Sie überwachen möchten. Stattdessen können Sie einen Listener an den Container anhängen und dann das Ziel des Ereignisses überprüfen. Dies ermöglicht es Ihnen, die gleiche Behandlung für viele ähnliche Elemente hinzuzufügen oder dynamisch erzeugte Elemente zu erfassen.

