---
title: "npm workflow"
theme: "black"
---

# npm workflow

---

## 1.  Einführung in npm und Module

-   npm: Online-Repository für Open-Source-Node.js-Pakete
-   Module: Pakete von Code, die von anderen Entwicklern veröffentlicht wurden
-   Modul hinzufügen: `npm install <Modulname>`

---

## 2.  Module hinzufügen mit `npm install`

-   `npm install <Modulname>`: Modul und Abhängigkeiten im `node_modules`-Ordner installieren
-   Mehrere Module gleichzeitig installieren: Namen mit Leerzeichen trennen
-   Entwicklungszwecke: `-D` oder `--save-dev` verwenden

---

## 3.  Verwaltung von Abhängigkeiten mit `package.json`

-   "dependencies" (Produktion) und "devDependencies" (Entwicklung) in `package.json` auflisten
-   Modul als "dependency" oder "devDependency" hinzufügen: `--save-prod` oder `--save-dev`
-   `npm install` ohne Parameter installiert dependencies und devDependencies

---

## 4.  Importieren von Modulen von Drittanbietern

-   Modul mit `import`-Anweisung importieren: `import <namespace> from <dependency-space>;`
-   `<namespace>`: Name des Moduls in Ihrem Code, `<dependency-space>`: Name in `package.json`
-   Funktionen/Objekte einzeln mit geschweiften Klammern oder alle auf einmal mit `*` und gemeinsamem Namen importieren
---