# Single-Page-Application

> Duration: **36 days** or **9 weeks**

- [ ] [DOM](#dom)
	- [ ] [[#Introduction: Javascript in the browser]] 
	- [ ] [[#Adding javascript to HTML]]
	- [ ] [[#The `window` object]]
	- [ ] [[#Querying: Getting elements from `document`]]
	- [ ] [[#Manipulating: Changing the DOM tree]]
	- [ ] [[#Traversing: Jumping from one element to its relative]]
	- [ ] [[#Events]]
	- [ ] [[#Listening]]
	- [ ] [[#The Event Object]]
	- [ ] [[#Propagation, Delegation: `<ul>`, `<li>` examples]] 
- [ ] [Modules](#modules)
	- [ ] [[#Introduction Modules]]
	- [ ] [[#Module Basics]]
	- [ ] [[#Imports and Exports]]
	- [ ] [[#Transpiling & Bundling]]
	- [ ] [[#Npm workflow]]
- [ ] [[#Asynchronous Programming]]
	- [ ] [[#Introduction Asynchronous Programming]]
	- [ ] [[#Non-Blocking Promises]]
	- [ ] [[#JSON: "JSON is JS Objects in text"]]
	- [ ] [[#Debug]]
	- [ ] [[#Runtime errors]]
	- [ ] [[#Blocking parsing and rendering]]
	- [ ] [[#Simplifying Asynchronous Code]]
	- [ ] [[#Getting data: Fetch examples]]
	- [ ] [[#Posting data: JSONPlaceholder examples]]
	- [ ] [[#CORS]]
	- [ ] [[#Saving Data: Use Cases for saving data in the browser]]
---
- [ ] [[#SPA - Assessment I]]
- [ ] [[#SPA - Exam I]]
---
- [ ] [Boilerplate](#boilerplate)
	- [ ] [[#Introduction SPA]]
	- [ ] [[#Framework]]
	- [ ] [[#Quickstart with Create React App]]
	- [ ] [[#Component Anatomy: Dissecting `App.js`]]
	- [ ] [[#Debugging React with "React Developer Tools"]]
	- [ ] [[#Templating with JSX: Slightly different html]]
- [ ] [Component](#component)
	- [ ] [[#Introduction Component]]
	- [ ] [[#Nesting Components]]
	- [ ] [[#Interaction]]
	- [ ] [[#Data flow]]
	- [ ] [[#Handling Forms]]
	- [ ] [[#Styling]]
	- [ ] [Lifecycle in React](#lifecycle+in+React)
		- [ ] [[#Introduction lifecycle]]
		- [ ] [[#Lifecycle events in a React component]]
		- [ ] [[#Basic Use Case: Retrieving data on load]]
		- [ ] [[#Lifecycle Pitfalls:]]
	- [ ] [[#Additional hooks - Unique IDs with `useId`]]
- [ ] [Router](#router)
	- [ ] [[#Introduction Router]]
	- [ ] [[#3rd party component libraries]]
	- [ ] [[#Route Components: Setting up react-router-dom]]
	- [ ] [[#Route Matching Components: Our first routes]]
	- [ ] [[#Building Navigation]]
	- [ ] [[#Route Parameters]]
- [ ] [Store](#store)
	- [ ] [[#Basic State Management Concepts]]
	- [ ] [[#Context API]]
	- [ ] [[#Advanced Implementation]]
- [ ] [Hooks](#hooks)
	- [ ] [[#Advanced hooks]]
- [ ] [Deployment](#deployment)
	- [ ] [[#Deployment of React Apps]]
---
- [ ] [[#SPA - Assessment II]]
- [ ] [[#SPA - Exam II]]
---
- [ ] [Workshops](#workshops)
	- [ ] [[#Redux]]
	- [ ] [[#Gatsby]]
	- [ ] [[#Next.js]]
	- [ ] [[#Expo]]
	- [ ] [[#Testing]]

## DOM
### Introduction: Javascript in the browser
- [ ] Historischer Kontext für JS: Browser-Kriege, Actionscript, jQuery, ES6
- [ ] Kurze Erwähnung der JS-Engines: V8 (Chrome, Node, Edge) vs. SpiderMonkey (Firefox) 

[⬆️](#Single-Page-Application)
### Adding javascript to HTML
- [ ] Der `<script>`-Tag
- [ ] Externes JS mit `<script src="...">`

[⬆️](#Single-Page-Application)
### The `window` object
- [ ] Host-Objekte vs. native Objekte: Kurzer Vergleich mit `window`
- [ ] `window` als globaler Bereich: Variablen auf dem `window`-Objekt sehen
- [ ] Benutzereingaben und Meldungen an das Fenster: `window.prompt()` und `window.alert()`
- [ ] Das `document`-Objekt: schneller Überblick
- [ ] HTML DOM Dokumentation: MDN

[⬆️](#Single-Page-Application)
### Querying: Getting elements from `document` 
- [ ] Auswählen von Elementen auf die alte Art mit `document.getElementById(<id string>)`
- [ ] Auswählen per CSS-Abfrage: `document.querySelector(<selector string>)`
- [ ] Mehr als ein Element abrufen: `document.querySelectorAll(<selector string>)`
- [ ] Element-Stil: Css-Stile mit der Eigenschaft `HTMLElement.style` ändern

[⬆️](#Single-Page-Application)
### Manipulating: Changing the DOM tree
- [ ] Manipulation von Klassen: `Element.classList`-Methoden 
- [ ] Ändern des Textes innerhalb eines Elements: Die Eigenschaft `HTMLElement.innerText`
- [ ] Ändern des HTML-Inhalts: Die Eigenschaft `Element.innerHTML`
- [ ] Elemente erstellen: `document.createElement(<Tagname>)`
- [ ] Hinzufügen von Elementen auf der Seite: `Element.append(<Element object>)`, siehe MDN-Dokumente für .append()

[⬆️](#Single-Page-Application)
### Traversing: Jumping from one element to its relative
- [ ] Node vs. Element: 
  Vergleich von `Node.previousSibling` und `Element.previousElementSibling`
- [ ] Ermitteln des nächstgelegenen übergeordneten Elements: `Element.closest(<selector string>)`
- [ ] Testen eines Elements gegen einen Selektor: `Element.matches(<Selektorstring>)`
- [ ] Alle Kinder eines Elements ermitteln: `ParentNode.children`
- [ ] Auswahl bestimmter Kinder: `ParentNode.querySelector(<selector string>)`
- [ ] Suche nach weiteren Traversaltechniken: MDN 

[⬆️](#Single-Page-Application)
### Events
- [ ] User Events (interaction)
- [ ] Browser Events (loading, etc...)

[⬆️](#Single-Page-Application)
### Listening
- [ ] Funktionen höherer Ordnung I recap: 
  Funktionen, die Funktionswerte akzeptieren (Callbacks)
- [ ] Abhören von Benutzeraktionen:
  `EventTarget.addEventListener(<Namensraum>, <Callback>)`
- [ ] Maus-Ereignisse: `Klick`, `Mouseenter`, `Mouseleave`
- [ ] Entfernen von Ereignislistenern: 
  `EventTarget.removeEventListener(<Namensraum>, <Funktionsreferenz>)`
- [ ] Abhören von Browser-Ereignissen: Ereignis `DOMContentLoaded`
- [ ] Weitere Ereignisse auf MDN finden

[⬆️](#Single-Page-Application)
### The Event Object
- [ ] Tastatur-Ereignisse: `keydown`, `keyup`
- [ ] Die Eigenschaften des Ereignisobjekts: Ein Konsolenbeispiel
- [ ] Das Ziel des Ereignisses ermitteln: `Event.target`
- [ ] Formular-Ereignisse: `submit`, `reset`, `Event.preventDefault()`
- [ ] Abrufen von Formularwerten beim Absenden: 
  `target.elements[<id>]`, `target.elements[<name>]`, `Element.value`

[⬆️](#Single-Page-Application)
### Propagation, Delegation: `<ul>`, `<li>` examples
- [ ] Konzept der Ereignisblasenbildung:  "Ereignisse sprudeln vom innersten zum äußersten Element"
- [ ] Häufige Probleme mit Bubbling: `Event.stopPropagation()` als Lösung
- [ ] Unterschiedliche Ziele: `Event.target` vs. `Event.currentTarget`
- [ ] Probleme mit Ereignis-Listenern: Auswirkungen auf die Leistung, Hinzufügen von Ereignissen zu dynamischen Listen
- [ ] Lösung der Ereignisdelegation: Delegieren von Ereignissen vom Elternteil zum Kind
- [ ] Umkehrung der Ausbreitung: 
  Die Option `useCapture` in `addEventListener()`, 
  Anwendungsfall `DOMContentLoaded`

[⬆️](#Single-Page-Application)
## Modules
### Introduction Modules
- [ ] Module für kleinere Dateien 

[⬆️](#Single-Page-Application)
### Module Basics
- [ ] Kurzer Überblick über IIFE und das Modulmuster
- [ ] Vorteile von Scope Isolation und Encapsulation
- [ ] Verwendung von Modulen im Browser: `<script type="module" src="...">`
- [ ] Verbinden von Dateien: Die Schlüsselwörter `import` und `export`

[⬆️](#Single-Page-Application)
### Imports and Exports

- [ ] Standard-Exporte vs. benannte Exporte: `export default`, `export {<var1>, <var2> [, ...]}`
- [ ] Namespacing-Importe: `import <Namensraum> aus <Pfad>`, `import * als <Namensraum> aus <Pfad>`
- [ ] Destrukturierung von Importen: `import { <var1>, <var2 [, ...]} from `<path>`

[⬆️](#Single-Page-Application)
###  Transpiling & Bundling

- [ ] Browser-Kompatibilität und Module: Transpilieren von ES mit Babel
- [ ] Überblick über Bündelungswerkzeuge: Verpackung unseres verarbeiteten Codes mit Webpack (NUR Einführung, keine Notwendigkeit, Configs zu schreiben)

[⬆️](#Single-Page-Application)
### Npm workflow

- [ ] Hinzufügen von Modulen zu unserem Projekt: `npm install <Modulname>`
- [ ] Abhängigkeitsliste: `package.json` lesen, `dependencies` vs. `devDependencies`
- [ ] Module von Drittanbietern verwenden: `import <Namensraum> von <Abhängigkeitsname>`

[⬆️](#Single-Page-Application)
## Asynchronous Programming
### Introduction Asynchronous Programming
- [ ] Der request response cycle
- [ ] Perspektive des Clients  

[⬆️](#Single-Page-Application)
### Non-Blocking Promises
- [ ] Blocking vs. Non-Blocking Code: Ein kurzes Beispiel, `window.setTimeout()`
- [ ] Race conditions: Lesen von nicht blockierendem Code
- [ ] Promises: `new Promise(<Funktion>)`, `Promise.resolve()`, `Promise.then()`
- [ ] Promisifying: Umwandlung von `setTimeout()` in ein Promis
- [ ] Breaking Promises: `Promise.reject()`, `Promise.catch()`, `Promise.finally()` 

[⬆️](#Single-Page-Application)
### JSON: "JSON is JS Objects in text"
- [ ] Umwandlung von Objekten in JSON: `JSON.stringify(<Objekt>)`
- [ ] Parsen von JSON-Objekten: `JSON.parse(<JSON string>)`
- [ ] JSON-Fallen: Strikte Notation, `JSON.parse()` verursacht Laufzeitfehler

[⬆️](#Single-Page-Application)
### Debug
- [ ] Fehlersuche in Javascript mit Node und vscode
- [ ] Debuggen von Node-Skripten mit Chrome: "Node inspect <Dateiname>".
- [ ] Die Anweisung `debugger;`
- [ ] Den Status im Auge behalten: Inspektion von Bereichen in Chrome

[⬆️](#Single-Page-Application)
### Runtime errors
- [ ] Fehler auffangen: `try { ... } catch (e) { ... }`
- [ ] Auslösen von Laufzeitfehlern: `throw <Ausdruck>;`
- [ ] Das Fehlerobjekt (kurze Einführung): `new Error(<Meldung>);`

[⬆️](#Single-Page-Application)
### Blocking parsing and rendering
- [ ] Verwendung der Skript-Elementattribute async und defer zur Steigerung von Geschwindigkeit und Leistung
- [ ] Das domInteractive-Ereignis
- [ ] Dynamische Skriptinjektion

[⬆️](#Single-Page-Application)
### Simplifying Asynchronous Code
- [ ] Warum Promises verwenden: Callback-Hölle, Pyramide des Todes
- [ ] Probleme mit Promises: Scoping-Probleme, endlose Kette
- [ ] Modernes Verwenden von Promises: 
  Async-Funktionen, das Schlüsselwort "await",
  Async-Funktionen geben immer ein Promise zurück"

[⬆️](#Single-Page-Application)
### Getting data: Fetch examples
- [ ] APIs von Drittanbietern: 
  Kurze Einführung, warum sollten Anfragen asynchron gestellt werden
- [ ] Informationen abrufen: `window.fetch(<url>)`, der Überblick über das Antwortobjekt
- [ ] Parsen von JSON: `response.json()`
- [ ] Daten verwenden: `fetch(<url>).then(<callback>)` vs. `await fetch(<url>)`

[⬆️](#Single-Page-Application)
### Posting data: JSONPlaceholder examples
- [ ] Wiederholung der HTTP-Methoden: GET vs. POST
- [ ] Senden von Daten mit Fetch: `fetch(<url>, <options>)`, die Option `method`
- [ ] Analysieren des Textkörpers: die Option `body` in Fetch
- [ ] Senden von Formularen mit JS: Erstellen einer Post-Anfrage beim Absenden

[⬆️](#Single-Page-Application)
### CORS
- [ ] Was sind Cross Origin Requests
- [ ] Anfragen an andere Domains stellen: Die gleiche Herkunftspolitik
- [ ] CORS: Cross Origin Resource Sharing, Akzeptierte CORS-Header
- [ ] Hinzufügen von CORS-Headern zur Anfrage: 
  die Option fetch `headers`, der `Origin`-Header
- [ ] CORS umgehen: Verwendung eines Proxy-Skripts für die Entwicklung, `cors-anywhere`

[⬆️](#Single-Page-Application)
### Saving Data: Use Cases for saving data in the browser
- [ ] Methoden zum Speichern von Daten im Browser: `localStorage` vs. `sessionStorage`
- [ ] Daten setzen: Schlüssel-Wert-Paare, `Storage.setItem(<Schlüssel>, <Wert>)`
- [ ] Daten abrufen: `Storage.getItem(<Schlüssel>)`
- [ ] Vermeiden von Fehlern: Erstellen eines Promise-Wrappers für localStorage

[⬆️](#Single-Page-Application)

---
## SPA - Assessment I
## SPA - Exam I

[⬆️](#Single-Page-Application)

---
## Boilerplate
### Introduction  SPA
- [ ] Was ist eine Single Page Application?  
- [ ] Warum brauchen wir sie?

[⬆️](#Single-Page-Application)
### Framework  
- [ ] MVC-Konzepte: V steht für View (Kurzdefinition)  
- [ ] Framework-Besessenheit: Überblick über die JS-Framework-Landschaft  
- [ ] React-Einführung: Warum React? React vs. Web-Komponenten-Standard  
- [ ] React-Ökosystem: React, Native, Expo Framework, Gatsby, Nextjs  
- [ ] Moderne React-Entwicklung mit Hooks

[⬆️](#Single-Page-Application)
### Quickstart with Create React App  
- [ ] Starten eines React-Projekts: "npx create-react-app <Anwendungsname>".  
- [ ] Was in der Box ist: Überprüfung von package.json  
- [ ] Package.json-Skripte - [ ] was und warum, Erstellung eines Beispielskripts  
- [ ] Projektstruktur: `src` vs. `public` Ordner, der `build` Ordner  
- [ ] Rendering in React: `index.js`  
- [ ] Einbindung von Stilen: `import <Pfad zu css>`

[⬆️](#Single-Page-Application)
### Component Anatomy: Dissecting `App.js`  
- [ ] Einstiegspunkt: "App.js", die "App"-Komponente (Boilerplate)  
- [ ] Bilder importieren: `importiere <Bildname> von <Pfad zum Bild>`  
- [ ] Bilder verwenden: `<img src={Bildname} alt="..." />`

[⬆️](#Single-Page-Application)
### Debugging React with "React Developer Tools"

[⬆️](#Single-Page-Application)
### Templating with JSX: Slightly different html  
- [ ] Mehrzeilige Vorlagen: `const <Komponentenname> = () => (<JSX>)`  
- [ ] Ein Element pro Komponente: "React.Fragment" für mehrere HTML-Tags  
- [ ] JS in JSX: Verwendung von `{}` für die Interpolation von JS-Ausdrücken  
- [ ] Kommentare in JSX  
- [ ] Bedingtes Rendering  
- [ ] Erzeugen von Listen mit Array-Map, der Eigenschaft "key".

[⬆️](#Single-Page-Application)
## Component
### Introduction Component
- [ ] Das Denken in Komponenten  
- [ ] Unterschied zwischen Klasse und Funktionskomponente

[⬆️](#Single-Page-Application)
### Nesting Components  
- [ ] Projektorganisation II: Der Ordner "components".  
- [ ] Exportieren und Importieren von Komponenten  
- [ ] Verwendung von Komponenten in JSX  
- [ ] Wann zu verwenden: Grundlegende Richtlinien für die Erstellung von Komponenten

[⬆️](#Single-Page-Application)
### Interaction  
- [ ] Festlegen von event handlern in JSX:  
- [ ] Definieren von event handlern in Komponenten  
- [ ] Bindung der Komponentenklasse an handler und Pfeilfunktionen  
- [ ] Manipulation von Zuständen in Ereignissen

[⬆️](#Single-Page-Application)
### Data flow  
- [ ] Definitionen und Unterschiede zwischen Props und States  
- [ ] Akzeptieren von Props  
- [ ] Übergabe von Props  
- [ ] Initialisieren und Aktualisieren von Zuständen mit useState  
- [ ] Verwendung eines Reduzierers vom Typ useReducer  
- [ ] Lazy Initialisierung

[⬆️](#Single-Page-Application)
### Handling Forms  
- [ ] Ein Konflikt zwischen Zuständen: Zustand in HTML-Formularen vs. Zustand in React-Komponenten  
- [ ] Kontrollierte Komponenten: React-Status als einzige Quelle der Wahrheit  
- [ ] Kontrolle des Wertes von Eingaben  
- [ ] Behandlung mehrerer Eingaben mit einem "onChange"-Handler  
- [ ] Übermittlung von Formularen: API-Aufrufe bei Übermittlung mit Daten aus dem Status  
- [ ] Kontrollierte Komponente  
- [ ] Veränderbare Ref-Objekte

[⬆️](#Single-Page-Application)
### Styling  
- [ ] Hinzufügen von Unterstützung für sass  
- [ ] Einbindung von Bootstrap in unser Projekt  
- [ ] Gestaltete Komponenten

[⬆️](#Single-Page-Application)
### lifecycle in React

[⬆️](#Single-Page-Application)
#### Introduction  lifecycle
- [ ] Jede Komponente hat einen lifecycle

[⬆️](#Single-Page-Application)
#### Lifecycle events in a React component  
- [ ] Ausführen von Code in Lebenszyklusphasen: erstes Rendering, Abkopplung  
- [ ] Verwendung des Effect Hook zur Ausführung von Seiteneffekten in Funktionskomponenten

[⬆️](#Single-Page-Application)
#### Basic Use Case: Retrieving data on load  
- [ ] Erstellen einer einfachen Spinner-Komponente mit fontawsome  
- [ ] Bedingtes Rendern einer Komponente mit Spinner, bevor Daten abgerufen werden

[⬆️](#Single-Page-Application)
#### Lifecycle Pitfalls:  
- [ ] Fehler bei abgekoppelten Komponenten  
- [ ] Vermeiden von Endlosschleifen  
- [ ] Veraltete Methoden und UNSAFE

[⬆️](#Single-Page-Application)
### Additional hooks - Unique IDs with `useId`

[⬆️](#Single-Page-Application)
## Router
### Introduction  Router
- [ ] Routing in einer Single Page Application mit React Router

[⬆️](#Single-Page-Application)
### 3rd party component libraries  
- [ ] Container-Komponenten (Zustandsverwaltung) vs. Display-Komponenten (Renderdom)  
- [ ] Bibliotheken für Display-Komponenten: reactstrap (Dokumentation und einfaches Beispiel)  
- [ ] Container-Komponenten: react-router-dom (Dokumentation)

[⬆️](#Single-Page-Application)
### Route Components: Setting up react-router-dom  
- [ ] Kurzer Überblick: Die Browser History API (was ist sie, wo kann man mehr lesen)  
- [ ] Einschließen unserer Anwendung mit einer `<BrowserRouter>` Container-Komponente  
- [ ] `<BrowserRouter>` vs. `<HashRouter>`: wann zu verwenden

[⬆️](#Single-Page-Application)
### Route Matching Components: Our first routes  
- [ ] Bedingtes Rendern je nach URL: die Komponente `<Route>`  
- [ ] Nur eine Route zum Rendern auswählen: `<Switch>`  
- [ ] Fallstricke: Reihenfolge der Pfade in `<Switch>`, Rendering exakter Pfade mit `exact`  
- [ ] Projektorganisation III: Der Ordner `views` für Seitenkomponenten  
- [ ] Den Pfad weglassen: Rendering von 404 Komponenten

[⬆️](#Single-Page-Application)
### Building Navigation  
- [ ] Verwendung von `<Link>` zur Navigation zu einem Pfad  
- [ ] Erstellen einer Navigationsleiste mit `<NavLink activeClassName="[...]">`  
- [ ] Bibliothekskonflikt: Verwendung von reactstrap `<NavLink>` mit react-router `<NavLink>`  
https://github.com/reactstrap/reactstrap/issues/1285#issuecomment-446592497  
- [ ] Komponenten umleiten: `<Redirect>`

[⬆️](#Single-Page-Application)
### Route Parameters  
- [ ] Dynamische Routenpfade mit Routenparametern erstellen: die `/:<param>`-Notation  
- [ ] Props für Routen: Zugriff auf Routen-Parameter mit dem `match.params` Props

[⬆️](#Single-Page-Application)
## Store
### Basic State Management Concepts  
- [ ] Lokaler Zustand & globaler Zustand  
- [ ] Der Albtraum vom Bohren des Zustands durch Props  
- [ ] Was ist ein Zustandscontainer?

[⬆️](#Single-Page-Application)
### Context API  
- [ ] Provider und Consumer Komponente  
- [ ] Den Kontext `useContext` nutzen  
- [ ] den Kontext mit einem Reducer erweitern `useReducer`

[⬆️](#Single-Page-Application)
### Advanced Implementation  
- [ ] Aktionstypen definieren  
- [ ] Umgang mit Seiteneffekten  
- [ ] CRUD-App mit React Hooks und der Context API

[⬆️](#Single-Page-Application)
## Hooks
### Advanced hooks  
- [ ] Memoisierung mit `useMemo` und `useCallback`

[⬆️](#Single-Page-Application)
## Deployment
### Deployment of React Apps  
- [ ] JAM-Stack und serverlose Infrastruktur  
- [ ] GitHub, GitHub-Seiten und Aktionen  
- [ ] Vercel: Architektur, Cli-Setup und Bereitstellung  
- [ ] OR Heroku: Architektur, Cli-Einrichtung und Bereitstellung  
- [ ] OR Firebase: Architektur und Bereitstellung  
- [ ] OR Netlify: Architektur und Bereitstellung

[⬆️](#Single-Page-Application)

---
## SPA - Assessment II
## SPA - Exam II

[⬆️](#Single-Page-Application)

---



## Workshops
### Redux  
- [ ] Implementing Redux with React  
- [ ] The `react-redux` component library  
- [ ] Providing a store to our app  
- [ ] The `store` directory, The `actions` and `reducers` sub directories  
- [ ] Splitting reducers: Using `redux.combineReducers()` for complex stores  
- [ ] Connecting to the store: The connect higher order function  
- [ ] Mapping the state to props in a callback:  
- [ ] Mapping action creator to dispatch functions  
- [ ] Redux Middleware: Thunk and Saga

[⬆️](#Single-Page-Application)
### Gatsby  
- [ ] Development of static websites using Gatsby  
- [ ] What is Gatsby  
- [ ] Bootstrap a Gatsby site & Gatsby starters  
- [ ] Building with components  
- [ ] Styling  
- [ ] Data Flow: unstructured data vs GraphQL  
- [ ] Source & Transformer plugins  
- [ ] Taxonomies  
- [ ] Deployment

[⬆️](#Single-Page-Application)
### Next.js  
- [ ] Next.js Overview & Main Features  
- [ ] Hybrid static & server rendering with Next.js  
- [ ] Routing and dynamic pages  
- [ ] API Routes  
- [ ] Deployment on Vercel  
- [ ] Authentication  
- [ ] Advanced Features

[⬆️](#Single-Page-Application)
### Expo  
- [ ] Universal React applications with Expo  
- [ ] Using the Expo CLI and setting up the enviroment  
- [ ] Initialize a Expo app and work with elements  
- [ ] Expo workflow  
- [ ] Building with components  
- [ ] Styling  
- [ ] Routing & Navigation  
- [ ] Fetch data  
- [ ] Building and deploying  
- [ ] Advanced Implementation:  
	- [ ] Distributing Apps on the App Store and Play Store  
	- [ ] Push Notifications  
	- [ ] Using GraphQL

[⬆️](#Single-Page-Application)
### Testing  
- [ ] Testing tools and patterns for React applications  
- [ ] Basic concepts: what is testing, why test, what & what not to test, how  
- [ ] Tradeoffs: iteration speed, environment and mocks  
- [ ] Tools: React testing library, Jest, Enzyme, Cypress  
- [ ] Design tests: Unit test, Component test, Snapshot test  
- [ ] Snapshot Testing  
- [ ] Mocking Function  
- [ ] Testing function calls  
- [ ] Testing state or prop updates

[⬆️](#Single-Page-Application)