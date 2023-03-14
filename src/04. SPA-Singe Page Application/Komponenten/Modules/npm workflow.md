# npm workflow

## npm install
Hallo zusammen,

heute möchte ich euch zeigen, wie ihr Module zu eurem Node.js-Projekt hinzufügen könnt. Module sind Pakete von Code, die von anderen Entwicklern geschrieben und auf der npm-Registry veröffentlicht wurden. Die npm-Registry ist ein Online-Repository für Open-Source-Node.js-Pakete, das über 1,3 Millionen Pakete enthält¹.

Um ein Modul zu eurem Projekt hinzuzufügen, braucht ihr den Befehl `npm install <Modulname>`. Dieser Befehl installiert das Modul und alle seine Abhängigkeiten in den lokalen node_modules Ordner eures Projekts². Zum Beispiel, wenn ihr das Modul express installieren wollt, das ein beliebtes Framework für Webanwendungen ist, könnt ihr einfach `npm install express` ausführen.

Ihr könnt auch mehrere Module auf einmal installieren, indem ihr ihre Namen durch Leerzeichen trennt. Zum Beispiel, wenn ihr express und mongoose installieren wollt, die beide für die Erstellung einer REST-API nützlich sind, könnt ihr `npm install express mongoose` ausführen.

Wenn ihr ein Modul nur für die Entwicklung eures Projekts braucht und nicht für die Produktion, könnt ihr den Parameter `-D` oder `--save-dev` verwenden. Dieser Parameter fügt das Modul zu den devDependencies in eurer package.json Datei hinzu². Die package.json Datei ist eine Datei, die wichtige Informationen über euer Projekt enthält, wie zum Beispiel den Namen, die Version, die Beschreibung und die Abhängigkeiten³. Zum Beispiel, wenn ihr das Modul nodemon installieren wollt, das euer Projekt automatisch neu startet, wenn ihr Änderungen an euren Dateien vornehmt, könnt ihr `npm install nodemon -D` ausführen.

Das war eine kurze Einführung zum Hinzufügen von Modulen zu unserem Projekt mit dem Befehl `npm install <Modulname>`. Ich hoffe, es war hilfreich für euch. Wenn ihr Fragen habt oder mehr erfahren wollt, könnt ihr gerne die offizielle Dokumentation von npm besuchen oder mir eine Nachricht schicken.

---

Quelle:
(1) Was ist npm? Eine Einführung in den Paketmanager von Node. https://kinsta.com/de/wissensdatenbank/was-ist-npm/ Zugegriffen 14.3.2023.
(2) npm-install | npm Docs. https://docs.npmjs.com/cli/v6/commands/npm-install/ Zugegriffen 14.3.2023.
(3) 5 Ways to Fix the Npm Install Not Working Issue. https://www.partitionwizard.com/partitionmanager/npm-install-not-working.html Zugegriffen 14.3.2023.

---

## Abhängigkeitsliste: `package.json` lesen, `dependencies` vs. `devDependencies`

Um die Module zu verwalten, die euer Projekt benötigt, müsst ihr sie als "dependencies" oder "devDependencies" in eurer package.json Datei auflisten. Die package.json Datei ist eine Datei, die wichtige Informationen über euer Projekt enthält, wie zum Beispiel den Namen, die Version, die Beschreibung und die Abhängigkeiten¹.

**"dependencies"** sind Pakete, die eure Anwendung in der Produktion benötigt. Das sind Module, die ihr direkt in eurem Code verwendet, um eure Anwendung zu erstellen und auszuführen. Zum Beispiel, wenn ihr eine Webanwendung mit express erstellt habt, müsst ihr express als eine dependency auflisten.

**"devDependencies"** sind Pakete, die nur für die lokale Entwicklung und das Testen benötigt werden. Das sind Module, die euch helfen, euren Code zu bearbeiten, zu bündeln, zu testen oder zu debuggen. Zum Beispiel, wenn ihr webpack verwendet habt, um euren Code zu bündeln und zu minimieren, müsst ihr webpack als eine devDependency auflisten.

Um ein Modul als eine dependency oder eine devDependency hinzuzufügen, könnt ihr entweder den Befehl `npm install` mit dem Parameter `--save-prod` oder `--save-dev` verwenden oder die package.json Datei manuell bearbeiten¹. Zum Beispiel:

```json
{
  "name": "mein_projekt",
  "version": "1.0.0",
  "dependencies": {
    "express": "^4.17.2"
  },
  "devDependencies": {
    "webpack": "^5.67.0"
  }
}
```

Wenn ihr `npm install` ohne Parameter ausführt, werden sowohl dependencies als auch devDependencies installiert². Wenn ihr jedoch nur die dependencies installieren wollt (zum Beispiel auf einem Server), könnt ihr den Parameter `--production` verwenden oder die Umgebungsvariable NODE_ENV auf production setzen².

---

Quelle: 
(1) Specifying dependencies and devDependencies in a package.json file - npm. https://docs.npmjs.com/specifying-dependencies-and-devdependencies-in-a-package-json-file/ Zugegriffen 14.3.2023.
(2) node.js - What's the difference between dependencies, devDependencies .... https://stackoverflow.com/questions/18875674/whats-the-difference-between-dependencies-devdependencies-and-peerdependencies Zugegriffen 14.3.2023.
(3) NPM: devDependencies vs dependencies in package.json. https://sumantmishra.medium.com/npm-devdependencies-vs-dependencies-in-package-json-d6c790edd725 Zugegriffen 14.3.2023.

---


## Module von Drittanbietern verwenden: import `<namespace> from <dependency-space>`

Um die Module zu verwenden, die ihr zu eurem Projekt hinzugefügt habt, müsst ihr sie in euren JavaScript-Dateien importieren. Dazu könnt ihr die import-Anweisung verwenden, die Teil des ES6-Modulsystems ist. Die import-Anweisung hat die folgende Syntax:

```javascript
import <namespace> from <dependency-space>;
```

**`<namespace>`** ist der Name, den ihr dem Modul geben wollt, um es in eurem Code zu verwenden. Ihr könnt einen beliebigen Namen wählen, aber es ist sinnvoll, einen Namen zu verwenden, der dem Modulnamen ähnelt oder ihn widerspiegelt.

**`<dependency-space>`** ist der Name des Moduls, wie er in der package.json Datei oder in der npm-Registry angegeben ist. Ihr müsst diesen Namen mit Anführungszeichen oder Hochkommas umschließen.

Zum Beispiel, wenn ihr das Modul express importieren wollt, das ihr als eine dependency installiert habt, könnt ihr folgenden Code schreiben:

```javascript
import express from "express";
```

Dann könnt ihr express in eurem Code verwenden, um eine Webanwendung zu erstellen und zu starten.

Wenn das Modul mehrere Funktionen oder Objekte exportiert, könnt ihr sie mit geschweiften Klammern importieren und ihnen eigene Namen geben. Zum Beispiel:

```javascript
import { Router, json } from "express";
```

Dann könnt ihr Router und json in eurem Code verwenden, um Routen und Middleware für eure Webanwendung zu definieren.

Ihr könnt auch alle exportierten Funktionen oder Objekte eines Moduls mit einem Sternchen (*) importieren und ihnen einen gemeinsamen Namen geben. Zum Beispiel:

```javascript
import * as math from "mathjs";
```

Dann könnt ihr math in eurem Code verwenden, um mathematische Operationen auszuführen.

---
Quelle: 
(1) Identifizierung von Problemen, die durch Module von Drittanbietern in .... https://support.mozilla.org/de/kb/probleme-durch-drittanbieter-module-identifizieren Zugegriffen 14.3.2023.
(2) Importieren von Zertifizierungsstellen von Drittanbietern (CAs) in den .... https://learn.microsoft.com/de-de/troubleshoot/windows-server/windows-security/import-third-party-ca-to-enterprise-ntauth-store Zugegriffen 14.3.2023.
(3) So verwenden Sie Node.js-Module mit npm und package.json. https://www.digitalocean.com/community/tutorials/how-to-use-node-js-modules-with-npm-and-package-json-de Zugegriffen 14.3.2023.

---