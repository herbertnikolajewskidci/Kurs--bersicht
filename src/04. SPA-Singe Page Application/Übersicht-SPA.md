# Single-Page-Application

> Duration: **36 days** or **9 weeks**

-   [x] [DOM](#DOM)
    -   [x] [[#Introduction: Javascript in the browser]]
    -   [x] [[#Adding javascript to HTML]]
    -   [x] [[#The 'window' object]]
    -   [x] [[#Querying: Getting elements from 'document']]
    -   [x] [[#Manipulating: Changing the DOM tree]]
    -   [x] [[#Traversing: Jumping from one element to its relative]]
    -   [x] [[#Events]]
    -   [x] [[#Listening]]
    -   [x] [[#The Event Object]]
    -   [x] [[#Propagation, Delegation:]]
-   [ ] [Modules](#Modules)
    -   [x] [[#Introduction Modules]]
    -   [x] [[#Module Basics]]
    -   [x] [[#Imports and Exports]]
    -   [ ] [[#Transpiling & Bundling]]
    -   [ ] [[#Npm workflow]]
-   [ ] [[#Asynchronous Programming]]
    -   [ ] [[#Introduction Asynchronous Programming]]
    -   [ ] [[#Non-Blocking Promises]]
    -   [ ] [[#JSON: "JSON is JS Objects in text"]]
    -   [ ] [[#Debug]]
    -   [ ] [[#Runtime errors]]
    -   [ ] [[#Blocking parsing and rendering]]
    -   [ ] [[#Simplifying Asynchronous Code]]
    -   [ ] [[#Getting data: Fetch examples]]
    -   [ ] [[#Posting data: JSONPlaceholder examples]]
    -   [ ] [[#CORS]]
    -   [ ] [[#Saving Data: Use Cases for saving data in the browser]]

---

-   [ ] [[#SPA - Assessment I]]
-   [ ] [[#SPA - Exam I]]

---

-   [ ] [Boilerplate](#Boilerplate)
    -   [ ] [[#Introduction SPA]]
    -   [ ] [[#Framework]]
    -   [ ] [[#Quickstart with Create React App]]
    -   [ ] [[#Component Anatomy: Dissecting `App.js`]]
    -   [ ] [[#Debugging React with "React Developer Tools"]]
    -   [ ] [[#Templating with JSX: Slightly different html]]
-   [ ] [Component](#Component)
    -   [ ] [[#Introduction Component]]
    -   [ ] [[#Nesting Components]]
    -   [ ] [[#Interaction]]
    -   [ ] [[#Data flow]]
    -   [ ] [[#Handling Forms]]
    -   [ ] [[#Styling]]
    -   [ ] [Lifecycle in React](#lifecycle+in+React)
        -   [ ] [[#Introduction lifecycle]]
        -   [ ] [[#Lifecycle events in a React component]]
        -   [ ] [[#Basic Use Case: Retrieving data on load]]
        -   [ ] [[#Lifecycle Pitfalls:]]
    -   [ ] [[#Additional hooks - Unique IDs with `useId`]]
-   [ ] [Router](#Router)
    -   [ ] [[#Introduction Router]]
    -   [ ] [[#3rd party component libraries]]
    -   [ ] [[#Route Components: Setting up react-router-dom]]
    -   [ ] [[#Route Matching Components: Our first routes]]
    -   [ ] [[#Building Navigation]]
    -   [ ] [[#Route Parameters]]
-   [ ] [Store](#Store)
    -   [ ] [[#Basic State Management Concepts]]
    -   [ ] [[#Context API]]
    -   [ ] [[#Advanced Implementation]]
-   [ ] [Hooks](#Hooks)
    -   [ ] [[#Advanced hooks]]
-   [ ] [Deployment](#Deployment)
    -   [ ] [[#Deployment of React Apps]]

---

-   [ ] [[#SPA - Assessment II]]
-   [ ] [[#SPA - Exam II]]

---

-   [ ] [Workshops](#Workshops)
    -   [ ] [[#Redux]]
    -   [ ] [[#Gatsby]]
    -   [ ] [[#Next.js]]
    -   [ ] [[#Expo]]
    -   [ ] [[#Testing]]

## DOM

### Introduction: Javascript in the browser

-   [x] Historischer Kontext f??r JS: Browser-Kriege, Actionscript, jQuery, ES6
-   [x] Kurze Erw??hnung der JS-Engines: V8 (Chrome, Node, Edge) vs. SpiderMonkey (Firefox)

[??????](#Single-Page-Application)

### Adding javascript to HTML

-   [x] Der `<script>`-Tag
-   [x] Externes JS mit `<script src="...">`

[??????](#Single-Page-Application)

### The 'window' object

-   [x] Host-Objekte vs. native Objekte: Kurzer Vergleich mit `window`
-   [x] `window` als globaler Bereich: Variablen auf dem `window`-Objekt sehen
-   [x] Benutzereingaben und Meldungen an das Fenster: `window.prompt()` und `window.alert()`
-   [x] Das `document`-Objekt: schneller ??berblick
-   [x] HTML DOM Dokumentation: MDN

[??????](#Single-Page-Application)

### Querying: Getting elements from 'document'

-   [x] Ausw??hlen von Elementen auf die alte Art mit `document.getElementById(<id string>)`
-   [x] Ausw??hlen per CSS-Abfrage: `document.querySelector(<selector string>)`
-   [x] Mehr als ein Element abrufen: `document.querySelectorAll(<selector string>)`
-   [x] Element-Stil: Css-Stile mit der Eigenschaft `HTMLElement.style` ??ndern

[??????](#Single-Page-Application)

### Manipulating: Changing the DOM tree

-   [x] Manipulation von Klassen: `Element.classList`-Methoden
-   [x] ??ndern des Textes innerhalb eines Elements: Die Eigenschaft `HTMLElement.innerText`
-   [x] ??ndern des HTML-Inhalts: Die Eigenschaft `Element.innerHTML`
-   [x] Elemente erstellen: `document.createElement(<Tagname>)`
-   [x] Hinzuf??gen von Elementen auf der Seite: `Element.append(<Element object>)`, siehe MDN-Dokumente f??r .append()

[??????](#Single-Page-Application)

### Traversing: Jumping from one element to its relative

-   [x] Node vs. Element:
        Vergleich von `Node.previousSibling` und `Element.previousElementSibling`
-   [x] Ermitteln des n??chstgelegenen ??bergeordneten Elements: `Element.closest(<selector string>)`
-   [x] Testen eines Elements gegen einen Selektor: `Element.matches(<Selektorstring>)`
-   [x] Alle Kinder eines Elements ermitteln: `ParentNode.children`
-   [x] Auswahl bestimmter Kinder: `ParentNode.querySelector(<selector string>)`
-   [x] Suche nach weiteren Traversaltechniken: MDN

[??????](#Single-Page-Application)

### Events

-   [x] User Events (interaction)
-   [x] Browser Events (loading, etc...)

[??????](#Single-Page-Application)

### Listening

-   [x] Funktionen h??herer Ordnung I recap:
        Funktionen, die Funktionswerte akzeptieren (Callbacks)
-   [x] Abh??ren von Benutzeraktionen:
        `EventTarget.addEventListener(<Namensraum>, <Callback>)`
-   [x] Maus-Ereignisse: `Klick`, `Mouseenter`, `Mouseleave`
-   [x] Entfernen von Ereignislistenern:
        `EventTarget.removeEventListener(<Namensraum>, <Funktionsreferenz>)`
-   [x] Abh??ren von Browser-Ereignissen: Ereignis `DOMContentLoaded`
-   [x] Weitere Ereignisse auf MDN finden

[??????](#Single-Page-Application)

### The Event Object

-   [x] Tastatur-Ereignisse: `keydown`, `keyup`
-   [x] Die Eigenschaften des Ereignisobjekts: Ein Konsolenbeispiel
-   [x] Das Ziel des Ereignisses ermitteln: `Event.target`
-   [x] Formular-Ereignisse: `submit`, `reset`, `Event.preventDefault()`
-   [ ] Abrufen von Formularwerten beim Absenden:
        `target.elements[<id>]`, `target.elements[<name>]`, `Element.value`

[??????](#Single-Page-Application)

### Propagation, Delegation:

#### `<ul>`, `<li>` examples

-   [x] Konzept der Ereignisblasenbildung: "Ereignisse sprudeln (bubble) vom innersten zum ??u??ersten Element"
-   [x] H??ufige Probleme mit Bubbling: `Event.stopPropagation()` als L??sung
-   [x] Unterschiedliche Ziele: `Event.target` vs. `Event.currentTarget`
-   [x] Probleme mit Ereignis-Listenern: Auswirkungen auf die Leistung, Hinzuf??gen von Ereignissen zu dynamischen Listen
-   [x] L??sung der Ereignisdelegation: Delegieren von Ereignissen vom Elternteil zum Kind
-   [x] Umkehrung der Ausbreitung:
        Die Option `useCapture` in `addEventListener()`,
        Anwendungsfall `DOMContentLoaded`

[??????](#Single-Page-Application)

## Modules

### Introduction Modules

-   [x] Module f??r kleinere Dateien

[??????](#Single-Page-Application)

### Module Basics

-   [x] Kurzer ??berblick ??ber IIFE und das Modulmuster
-   [x] Vorteile von Scope Isolation und Encapsulation
-   [x] Verwendung von Modulen im Browser: `<script type="module" src="...">`
-   [x] Verbinden von Dateien: Die Schl??sselw??rter `import` und `export`

[??????](#Single-Page-Application)

### Imports and Exports

-   [x] Standard-Exporte vs. benannte Exporte: `export default`, `export {<var1>, <var2> [, ...]}`
-   [x] Namespacing-Importe: `import <namespace> aus <path>`, `import * as <namespace> from <path>`
-   [x] Destrukturierung von Importen: `import { <var1>, <var2 [, ...]} from <path>`

[??????](#Single-Page-Application)

### Transpiling & Bundling

-   [ ] Browser-Kompatibilit??t und Module: Transpilieren von ES mit Babel
-   [ ] ??berblick ??ber Bundling Tools: Verpackung unseres verarbeiteten Codes mit Webpack (NUR Einf??hrung, keine Notwendigkeit, Configs zu schreiben)

[??????](#Single-Page-Application)

### Npm workflow

-   [ ] Hinzuf??gen von Modulen zu unserem Projekt: `npm install <Modulname>`
-   [ ] Abh??ngigkeitsliste: `package.json` lesen, `dependencies` vs. `devDependencies`
-   [ ] Module von Drittanbietern verwenden: `import <namespace> from <dependency-space>`

[??????](#Single-Page-Application)

## Asynchronous Programming

### Introduction Asynchronous Programming

-   [ ] Der request response cycle
-   [ ] Perspektive des Clients

[??????](#Single-Page-Application)

### Non-Blocking Promises

-   [ ] Blocking vs. Non-Blocking Code: Ein kurzes Beispiel, `window.setTimeout()`
-   [ ] Race conditions: Lesen von nicht blockierendem Code
-   [ ] Promises: `new Promise(<Funktion>)`, `Promise.resolve()`, `Promise.then()`
-   [ ] Promisifying: Umwandlung von `setTimeout()` in ein Promis
-   [ ] Breaking Promises: `Promise.reject()`, `Promise.catch()`, `Promise.finally()`

[??????](#Single-Page-Application)

### JSON: "JSON is JS Objects in text"

-   [ ] Umwandlung von Objekten in JSON: `JSON.stringify(<Objekt>)`
-   [ ] Parsen von JSON-Objekten: `JSON.parse(<JSON string>)`
-   [ ] JSON-Fallen: Strikte Notation, `JSON.parse()` verursacht Laufzeitfehler

[??????](#Single-Page-Application)

### Debug

-   [ ] Fehlersuche in Javascript mit Node und vscode
-   [ ] Debuggen von Node-Skripten mit Chrome: "Node inspect <Dateiname>".
-   [ ] Die Anweisung `debugger;`
-   [ ] Den Status im Auge behalten: Inspektion von Bereichen in Chrome

[??????](#Single-Page-Application)

### Runtime errors

-   [ ] Fehler auffangen: `try { ... } catch (e) { ... }`
-   [ ] Ausl??sen von Laufzeitfehlern: `throw <Ausdruck>;`
-   [ ] Das Fehlerobjekt (kurze Einf??hrung): `new Error(<Meldung>);`

[??????](#Single-Page-Application)

### Blocking parsing and rendering

-   [ ] Verwendung der Skript-Elementattribute async und defer zur Steigerung von Geschwindigkeit und Leistung
-   [ ] Das domInteractive-Ereignis
-   [ ] Dynamische Skriptinjektion

[??????](#Single-Page-Application)

### Simplifying Asynchronous Code

-   [ ] Warum Promises verwenden: Callback-H??lle, Pyramide des Todes
-   [ ] Probleme mit Promises: Scoping-Probleme, endlose Kette
-   [ ] Modernes Verwenden von Promises:
        Async-Funktionen, das Schl??sselwort "await",
        Async-Funktionen geben immer ein Promise zur??ck"

[??????](#Single-Page-Application)

### Getting data: Fetch examples

-   [ ] APIs von Drittanbietern:
        Kurze Einf??hrung, warum sollten Anfragen asynchron gestellt werden
-   [ ] Informationen abrufen: `window.fetch(<url>)`, der ??berblick ??ber das Antwortobjekt
-   [ ] Parsen von JSON: `response.json()`
-   [ ] Daten verwenden: `fetch(<url>).then(<callback>)` vs. `await fetch(<url>)`

[??????](#Single-Page-Application)

### Posting data: JSONPlaceholder examples

-   [ ] Wiederholung der HTTP-Methoden: GET vs. POST
-   [ ] Senden von Daten mit Fetch: `fetch(<url>, <options>)`, die Option `method`
-   [ ] Analysieren des Textk??rpers: die Option `body` in Fetch
-   [ ] Senden von Formularen mit JS: Erstellen einer Post-Anfrage beim Absenden

[??????](#Single-Page-Application)

### CORS

-   [ ] Was sind Cross Origin Requests
-   [ ] Anfragen an andere Domains stellen: Die gleiche Herkunftspolitik
-   [ ] CORS: Cross Origin Resource Sharing, Akzeptierte CORS-Header
-   [ ] Hinzuf??gen von CORS-Headern zur Anfrage:
        die Option fetch `headers`, der `Origin`-Header
-   [ ] CORS umgehen: Verwendung eines Proxy-Skripts f??r die Entwicklung, `cors-anywhere`

[??????](#Single-Page-Application)

### Saving Data: Use Cases for saving data in the browser

-   [ ] Methoden zum Speichern von Daten im Browser: `localStorage` vs. `sessionStorage`
-   [ ] Daten setzen: Schl??ssel-Wert-Paare, `Storage.setItem(<Schl??ssel>, <Wert>)`
-   [ ] Daten abrufen: `Storage.getItem(<Schl??ssel>)`
-   [ ] Vermeiden von Fehlern: Erstellen eines Promise-Wrappers f??r localStorage

[??????](#Single-Page-Application)

---

## SPA - Assessment I

## SPA - Exam I

[??????](#Single-Page-Application)

---

## Boilerplate

### Introduction SPA

-   [ ] Was ist eine Single Page Application?
-   [ ] Warum brauchen wir sie?

[??????](#Single-Page-Application)

### Framework

-   [ ] MVC-Konzepte: V steht f??r View (Kurzdefinition)
-   [ ] Framework-Besessenheit: ??berblick ??ber die JS-Framework-Landschaft
-   [ ] React-Einf??hrung: Warum React? React vs. Web-Komponenten-Standard
-   [ ] React-??kosystem: React, Native, Expo Framework, Gatsby, Nextjs
-   [ ] Moderne React-Entwicklung mit Hooks

[??????](#Single-Page-Application)

### Quickstart with Create React App

-   [ ] Starten eines React-Projekts: "npx create-react-app <Anwendungsname>".
-   [ ] Was in der Box ist: ??berpr??fung von package.json
-   [ ] Package.json-Skripte - [ ] was und warum, Erstellung eines Beispielskripts
-   [ ] Projektstruktur: `src` vs. `public` Ordner, der `build` Ordner
-   [ ] Rendering in React: `index.js`
-   [ ] Einbindung von Stilen: `import <Pfad zu css>`

[??????](#Single-Page-Application)

### Component Anatomy: Dissecting `App.js`

-   [ ] Einstiegspunkt: "App.js", die "App"-Komponente (Boilerplate)
-   [ ] Bilder importieren: `importiere <Bildname> von <Pfad zum Bild>`
-   [ ] Bilder verwenden: `<img src={Bildname} alt="..." />`

[??????](#Single-Page-Application)

### Debugging React with "React Developer Tools"

[??????](#Single-Page-Application)

### Templating with JSX: Slightly different html

-   [ ] Mehrzeilige Vorlagen: `const <Komponentenname> = () => (<JSX>)`
-   [ ] Ein Element pro Komponente: "React.Fragment" f??r mehrere HTML-Tags
-   [ ] JS in JSX: Verwendung von `{}` f??r die Interpolation von JS-Ausdr??cken
-   [ ] Kommentare in JSX
-   [ ] Bedingtes Rendering
-   [ ] Erzeugen von Listen mit Array-Map, der Eigenschaft "key".

[??????](#Single-Page-Application)

## Component

### Introduction Component

-   [ ] Das Denken in Komponenten
-   [ ] Unterschied zwischen Klasse und Funktionskomponente

[??????](#Single-Page-Application)

### Nesting Components

-   [ ] Projektorganisation II: Der Ordner "components".
-   [ ] Exportieren und Importieren von Komponenten
-   [ ] Verwendung von Komponenten in JSX
-   [ ] Wann zu verwenden: Grundlegende Richtlinien f??r die Erstellung von Komponenten

[??????](#Single-Page-Application)

### Interaction

-   [ ] Festlegen von event handlern in JSX:
-   [ ] Definieren von event handlern in Komponenten
-   [ ] Bindung der Komponentenklasse an handler und Pfeilfunktionen
-   [ ] Manipulation von Zust??nden in Ereignissen

[??????](#Single-Page-Application)

### Data flow

-   [ ] Definitionen und Unterschiede zwischen Props und States
-   [ ] Akzeptieren von Props
-   [ ] ??bergabe von Props
-   [ ] Initialisieren und Aktualisieren von Zust??nden mit useState
-   [ ] Verwendung eines Reduzierers vom Typ useReducer
-   [ ] Lazy Initialisierung

[??????](#Single-Page-Application)

### Handling Forms

-   [ ] Ein Konflikt zwischen Zust??nden: Zustand in HTML-Formularen vs. Zustand in React-Komponenten
-   [ ] Kontrollierte Komponenten: React-Status als einzige Quelle der Wahrheit
-   [ ] Kontrolle des Wertes von Eingaben
-   [ ] Behandlung mehrerer Eingaben mit einem "onChange"-Handler
-   [ ] ??bermittlung von Formularen: API-Aufrufe bei ??bermittlung mit Daten aus dem Status
-   [ ] Kontrollierte Komponente
-   [ ] Ver??nderbare Ref-Objekte

[??????](#Single-Page-Application)

### Styling

-   [ ] Hinzuf??gen von Unterst??tzung f??r sass
-   [ ] Einbindung von Bootstrap in unser Projekt
-   [ ] Gestaltete Komponenten

[??????](#Single-Page-Application)

### lifecycle in React

[??????](#Single-Page-Application)

#### Introduction lifecycle

-   [ ] Jede Komponente hat einen lifecycle

[??????](#Single-Page-Application)

#### Lifecycle events in a React component

-   [ ] Ausf??hren von Code in Lebenszyklusphasen: erstes Rendering, Abkopplung
-   [ ] Verwendung des Effect Hook zur Ausf??hrung von Seiteneffekten in Funktionskomponenten

[??????](#Single-Page-Application)

#### Basic Use Case: Retrieving data on load

-   [ ] Erstellen einer einfachen Spinner-Komponente mit fontawsome
-   [ ] Bedingtes Rendern einer Komponente mit Spinner, bevor Daten abgerufen werden

[??????](#Single-Page-Application)

#### Lifecycle Pitfalls:

-   [ ] Fehler bei abgekoppelten Komponenten
-   [ ] Vermeiden von Endlosschleifen
-   [ ] Veraltete Methoden und UNSAFE

[??????](#Single-Page-Application)

### Additional hooks - Unique IDs with `useId`

[??????](#Single-Page-Application)

## Router

### Introduction Router

-   [ ] Routing in einer Single Page Application mit React Router

[??????](#Single-Page-Application)

### 3rd party component libraries

-   [ ] Container-Komponenten (Zustandsverwaltung) vs. Display-Komponenten (Renderdom)
-   [ ] Bibliotheken f??r Display-Komponenten: reactstrap (Dokumentation und einfaches Beispiel)
-   [ ] Container-Komponenten: react-router-dom (Dokumentation)

[??????](#Single-Page-Application)

### Route Components: Setting up react-router-dom

-   [ ] Kurzer ??berblick: Die Browser History API (was ist sie, wo kann man mehr lesen)
-   [ ] Einschlie??en unserer Anwendung mit einer `<BrowserRouter>` Container-Komponente
-   [ ] `<BrowserRouter>` vs. `<HashRouter>`: wann zu verwenden

[??????](#Single-Page-Application)

### Route Matching Components: Our first routes

-   [ ] Bedingtes Rendern je nach URL: die Komponente `<Route>`
-   [ ] Nur eine Route zum Rendern ausw??hlen: `<Switch>`
-   [ ] Fallstricke: Reihenfolge der Pfade in `<Switch>`, Rendering exakter Pfade mit `exact`
-   [ ] Projektorganisation III: Der Ordner `views` f??r Seitenkomponenten
-   [ ] Den Pfad weglassen: Rendering von 404 Komponenten

[??????](#Single-Page-Application)

### Building Navigation

-   [ ] Verwendung von `<Link>` zur Navigation zu einem Pfad
-   [ ] Erstellen einer Navigationsleiste mit `<NavLink activeClassName="[...]">`
-   [ ] Bibliothekskonflikt: Verwendung von reactstrap `<NavLink>` mit react-router `<NavLink>`  
        https://github.com/reactstrap/reactstrap/issues/1285#issuecomment-446592497
-   [ ] Komponenten umleiten: `<Redirect>`

[??????](#Single-Page-Application)

### Route Parameters

-   [ ] Dynamische Routenpfade mit Routenparametern erstellen: die `/:<param>`-Notation
-   [ ] Props f??r Routen: Zugriff auf Routen-Parameter mit dem `match.params` Props

[??????](#Single-Page-Application)

## Store

### Basic State Management Concepts

-   [ ] Lokaler Zustand & globaler Zustand
-   [ ] Der Albtraum vom Bohren des Zustands durch Props
-   [ ] Was ist ein Zustandscontainer?

[??????](#Single-Page-Application)

### Context API

-   [ ] Provider und Consumer Komponente
-   [ ] Den Kontext `useContext` nutzen
-   [ ] den Kontext mit einem Reducer erweitern `useReducer`

[??????](#Single-Page-Application)

### Advanced Implementation

-   [ ] Aktionstypen definieren
-   [ ] Umgang mit Seiteneffekten
-   [ ] CRUD-App mit React Hooks und der Context API

[??????](#Single-Page-Application)

## Hooks

### Advanced hooks

-   [ ] Memoisierung mit `useMemo` und `useCallback`

[??????](#Single-Page-Application)

## Deployment

### Deployment of React Apps

-   [ ] JAM-Stack und serverlose Infrastruktur
-   [ ] GitHub, GitHub-Seiten und Aktionen
-   [ ] Vercel: Architektur, Cli-Setup und Bereitstellung
-   [ ] OR Heroku: Architektur, Cli-Einrichtung und Bereitstellung
-   [ ] OR Firebase: Architektur und Bereitstellung
-   [ ] OR Netlify: Architektur und Bereitstellung

[??????](#Single-Page-Application)

---

## SPA - Assessment II

## SPA - Exam II

[??????](#Single-Page-Application)

---

## Workshops

### Redux

-   [ ] Implementing Redux with React
-   [ ] The `react-redux` component library
-   [ ] Providing a store to our app
-   [ ] The `store` directory, The `actions` and `reducers` sub directories
-   [ ] Splitting reducers: Using `redux.combineReducers()` for complex stores
-   [ ] Connecting to the store: The connect higher order function
-   [ ] Mapping the state to props in a callback:
-   [ ] Mapping action creator to dispatch functions
-   [ ] Redux Middleware: Thunk and Saga

[??????](#Single-Page-Application)

### Gatsby

-   [ ] Development of static websites using Gatsby
-   [ ] What is Gatsby
-   [ ] Bootstrap a Gatsby site & Gatsby starters
-   [ ] Building with components
-   [ ] Styling
-   [ ] Data Flow: unstructured data vs GraphQL
-   [ ] Source & Transformer plugins
-   [ ] Taxonomies
-   [ ] Deployment

[??????](#Single-Page-Application)

### Next.js

-   [ ] Next.js Overview & Main Features
-   [ ] Hybrid static & server rendering with Next.js
-   [ ] Routing and dynamic pages
-   [ ] API Routes
-   [ ] Deployment on Vercel
-   [ ] Authentication
-   [ ] Advanced Features

[??????](#Single-Page-Application)

### Expo

-   [ ] Universal React applications with Expo
-   [ ] Using the Expo CLI and setting up the enviroment
-   [ ] Initialize a Expo app and work with elements
-   [ ] Expo workflow
-   [ ] Building with components
-   [ ] Styling
-   [ ] Routing & Navigation
-   [ ] Fetch data
-   [ ] Building and deploying
-   [ ] Advanced Implementation:
    -   [ ] Distributing Apps on the App Store and Play Store
    -   [ ] Push Notifications
    -   [ ] Using GraphQL

[??????](#Single-Page-Application)

### Testing

-   [ ] Testing tools and patterns for React applications
-   [ ] Basic concepts: what is testing, why test, what & what not to test, how
-   [ ] Tradeoffs: iteration speed, environment and mocks
-   [ ] Tools: React testing library, Jest, Enzyme, Cypress
-   [ ] Design tests: Unit test, Component test, Snapshot test
-   [ ] Snapshot Testing
-   [ ] Mocking Function
-   [ ] Testing function calls
-   [ ] Testing state or prop updates

[??????](#Single-Page-Application)
