---
title: "Transpiling & Bundling"
theme: "black"
---
# Transpiling & Bundling

---

## Babel Transpiling:

-   Wandelt modernen JS-Code in ältere Version um
-   Konvertiert Module in verschiedene Formate
-   Installation mit Node.js und npm
-   Installation: "npm install --save-dev @babel/core @babel/cli"
-   Konfiguration durch .babelrc-Datei
-   Verwendung: "npx babel src --out-dir lib"
---

![Bild](https://gcdnb.pbrd.co/images/S9iY6Q09n1Kn.png?o=1)

---

## Plugins und Presets:

-   Plugins transformieren Code
-   Presets sind Sammlungen von Plugins oder konfigurierbaren .babelrc-Dateien
-   Reihenfolge von Plugins und Presets beeinflusst Ergebnis
-   .babelrc-Datei nutzt man zur Angabe von Plugins und Presets

---

## Bundling Tools:

- Wandeln Code und Ressourcen in optimierte Pakete um
-   Verbessern Ladezeit, Kompatibilität und Sicherheit
-   Beliebte Tools: Webpack, Rollup, Parcel, Browserify

---
![webpackimg.png (1349×575) (malekbenz.com)](https://malekbenz.com/images/webpack-intro/webpackimg.png)

---

## Webpack vs. Parcel:

-   Webpack anpassbar und erweiterbar, erfordert aber viel Konfiguration
-   Parcel einfach zu bedienen und erfordert fast keine Konfiguration
-   Parcel erkennt automatisch Eingabedatei und Transformationen
-   Parcel schnell mit Multicore-Verarbeitung und Caching
-   Webpack standardmäßig ein JS-File, Parcel separate Dateien für CSS, JS-Bündel, Bilder etc.

---

