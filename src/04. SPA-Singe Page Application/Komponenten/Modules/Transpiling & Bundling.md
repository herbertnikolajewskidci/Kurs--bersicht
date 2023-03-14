# Transpiling & Bundling

## Transpilling mit Babel

Nicht alle Browser unterstützen die neuesten Funktionen und Standards von JavaScript, wie zum Beispiel ES6 oder ES2015. Um diese Kompatibilitätsprobleme zu lösen, können wir einen Transpiler wie Babel verwenden. Babel ist ein Werkzeug, das modernen JavaScript-Code in eine Version umwandelt, die von älteren Browsern verstanden werden kann. Babel kann auch JavaScript-Module in verschiedene Formate konvertieren, um sie mit verschiedenen Modulsystemen zu verwenden.

### Babel intallieren

Um Babel zu installieren, benötigst du zunächst Node.js und npm auf deinem Computer. Node.js ist eine JavaScript-Laufzeitumgebung, die es dir ermöglicht, JavaScript außerhalb des Browsers auszuführen. npm ist ein Paketmanager, mit dem du JavaScript-Module herunterladen und verwalten kannst. Du kannst Node.js und npm von der offiziellen Website herunterladen¹.

Nachdem du Node.js und npm installiert hast, kannst du Babel mit dem folgenden Befehl in deinem Terminal oder der Eingabeaufforderung installieren:

`npm install --save-dev @babel/core @babel/cli`

Dieser Befehl installiert zwei wichtige Pakete: @babel/core und @babel/cli. Das erste Paket ist das Herzstück von Babel, das den Transpilierungsprozess koordiniert. Das zweite Paket ist eine Kommandozeilenschnittstelle, die es dir ermöglicht, Babel-Befehle auszuführen².

Du kannst auch weitere Pakete installieren, um Babel anzupassen und zu erweitern. Zum Beispiel kannst du das @babel/preset-env Paket installieren, um die neuesten JavaScript-Funktionen zu transpilieren:

`npm install --save-dev @babel/preset-env`

Du musst auch eine Datei namens .babelrc in deinem Projektordner erstellen, um Babel zu konfigurieren. In dieser Datei kannst du deine gewünschten Plugins und Presets angeben. Zum Beispiel kannst du folgendes schreiben:

```json
{
  "presets": ["@babel/preset-env"]
}
```

Dies teilt Babel mit, dass es das @babel/preset-env Preset verwenden soll, um deinen Code zu transpilieren.

Nachdem du Babel installiert und konfiguriert hast, kannst du es verwenden, um deine JavaScript-Dateien zu transpilieren. Zum Beispiel kannst du den folgenden Befehl ausführen:

`npx babel src --out-dir lib`

Dieser Befehl nimmt alle Dateien im src-Ordner und transpiliert sie in den lib-Ordner².

Das ist eine kurze Einführung in die Installation von Babel. Du kannst mehr über Babel auf der offiziellen Website² oder in anderen Online-Ressourcen³ erfahren.

---
Quelle: 
(1) ‎Babbel - Language Learning im App Store. https://apps.apple.com/de/app/babbel-language-learning/id829587759 Zugegriffen 14.3.2023.
(2) Babel. https://babeljs.io/setup Zugegriffen 14.3.2023.
(3) Babbel - Download | NETZWELT. https://www.netzwelt.de/download/23881-babbel-kostenlos.html Zugegriffen 14.3.2023.

---

### Plugins und Presets

Plugins und Presets sind zwei Arten von Erweiterungen für Babel, die es dir ermöglichen, verschiedene Funktionen und Anpassungen zu deinem Transpilierungsprozess hinzuzufügen.

Plugins sind einzelne Module, die eine bestimmte Transformation an deinem Code durchführen. Zum Beispiel gibt es Plugins, die ES6-Klassen in ES5-Funktionen umwandeln, oder Plugins, die JSX-Syntax in JavaScript umwandeln. Du kannst Plugins einzeln oder in Kombination verwenden, um deinen Code nach deinen Wünschen zu transpilieren¹.

Presets sind Sammlungen von Plugins oder konfigurierbare .babelrc-Dateien, die du mit anderen teilen kannst. Presets erleichtern es dir, eine Reihe von Plugins zu verwenden, ohne sie alle einzeln auflisten zu müssen. Zum Beispiel gibt es Presets, die alle neuesten JavaScript-Funktionen transpilieren, oder Presets, die speziell für TypeScript oder React entwickelt wurden. Du kannst Presets verwenden, um eine Standardkonfiguration für dein Projekt zu erstellen oder zu übernehmen².

Die Reihenfolge der Plugins und Presets ist wichtig für das Endergebnis der Transpilierung. Plugins werden vor Presets ausgeführt. Die Reihenfolge der Plugins ist von vorne nach hinten. Die Reihenfolge der Presets ist umgekehrt (von hinten nach vorne)¹. Du kannst die Reihenfolge deiner Plugins und Presets in deiner .babelrc-Datei angeben.

Du kannst mehr über Plugins und Presets auf der offiziellen Babel-Website¹² oder in anderen Online-Ressourcen³ erfahren.

---
Quelle: 
(1) Presets · Babel. https://babeljs.io/docs/presets Zugegriffen 14.3.2023.
(2) Plugins · Babel. https://babeljs.io/docs/plugins/ Zugegriffen 14.3.2023.
(3) Difference between plugins and presets in .babelrc. https://stackoverflow.com/questions/45943889/difference-between-plugins-and-presets-in-babelrc Zugegriffen 14.3.2023.

---

## Bundling Tools

Wenn du eine moderne Webanwendung mit JavaScript entwickelst, wirst du wahrscheinlich viele verschiedene Dateien, Module, Bibliotheken und Abhängigkeiten haben, die deinen Code ausmachen. All diese Ressourcen müssen jedoch vom Browser geladen und verstanden werden, was zu Problemen wie langen Ladezeiten, Kompatibilitätsproblemen oder Sicherheitslücken führen kann. Um diese Probleme zu vermeiden, kannst du ein Bündelungswerkzeug verwenden.

Ein Bündelungswerkzeug ist ein Werkzeug, das deinen gesamten Code und alle damit verbundenen Ressourcen nimmt und sie in eine oder mehrere optimierte Dateien oder Pakete umwandelt. Diese Pakete sind kleiner, schneller und sicherer als deine ursprünglichen Dateien und können vom Browser leichter geladen und ausgeführt werden. Ein Bündelungswerkzeug kann auch andere Aufgaben ausführen, wie z.B. das Transpilieren von modernem JavaScript in älteres JavaScript, das Minifizieren oder Komprimieren von Code, das Hinzufügen von Präfixen für die Browser-Kompatibilität oder das Erstellen von Quellkarten für die Fehlerbehebung¹.

Es gibt viele verschiedene Bündelungswerkzeuge zur Auswahl, je nach deinen Anforderungen und Vorlieben. Einige der beliebtesten sind **Webpack,** Rollup, Parcel und Browserify. Jedes dieser Werkzeuge hat seine eigenen Stärken, Schwächen und Besonderheiten, die du kennen solltest, bevor du dich für eines entscheidest².


---
Quelle:
(1) Übersicht-SPA. https://herbertnikolajewskidci.github.io/kurs-uebersicht/04.-spa-singe-page-application/%C3%BCbersicht-spa.html Zugegriffen 14.3.2023.
(2) BMAS - Publikationen. https://www.bmas.de/DE/Service/Publikationen/publikationen.html Zugegriffen 14.3.2023.

---

### Webpack vs. Parcel

Webpack und Parcel sind zwei beliebte Bündelungswerkzeuge, die einige Gemeinsamkeiten und Unterschiede haben.

Beide Werkzeuge können deinen JavaScript-Code und alle damit verbundenen Ressourcen wie CSS, Bilder, Schriftarten usw. in optimierte Pakete umwandeln, die vom Browser geladen werden können. Beide Werkzeuge können auch andere Aufgaben ausführen, wie z.B. das Transpilieren von modernem JavaScript mit Babel, das Minifizieren oder Komprimieren von Code, das Hinzufügen von Präfixen für die Browser-Kompatibilität oder das Erstellen von Quellkarten für die Fehlerbehebung¹.

Der Hauptunterschied zwischen Webpack und Parcel liegt in der Konfiguration und der Benutzerfreundlichkeit. Webpack ist sehr anpassbar und erweiterbar mit vielen Plugins und Loadern, aber es erfordert auch viel manuelle Konfiguration und Einrichtung. Du musst eine webpack.config.js-Datei erstellen und verschiedene Optionen für deine Eingabe-, Ausgabe-, Modul- und Plugin-Einstellungen angeben. Du musst auch viele Abhängigkeiten installieren und verwalten, um Webpack zu verwenden².

Parcel hingegen ist sehr einfach zu bedienen und erfordert fast keine Konfiguration. Du kannst Parcel mit einem einzigen Befehl installieren und ausführen, ohne eine Konfigurationsdatei zu erstellen. Parcel erkennt automatisch deine Eingabedatei und wendet die entsprechenden Transformationen an. Parcel bietet auch eine schnelle Leistung mit Multicore-Verarbeitung und Dateisystem-Caching³.

Ein weiterer Unterschied zwischen Webpack und Parcel ist die Struktur der Ausgabedateien. Webpack fügt standardmäßig alles in eine einzige JavaScript-Datei ein (obwohl es konfiguriert werden kann), während Parcel separate Dateien für CSS, JavaScript-Bündel, Bilder usw. erstellt.

Du kannst mehr über Webpack auf der offiziellen Website² oder in anderen Online-Ressourcen erfahren.

Du kannst mehr über Parcel auf der offiziellen Website³ oder in anderen Online-Ressourcen erfahren.

---
Quelle: 
(1) Benchmarking bundlers 2020: Rollup vs. Parcel vs. webpack. https://blog.logrocket.com/benchmarking-bundlers-2020-rollup-parcel-webpack/ Zugegriffen 14.3.2023.
(2) Switching to Parcel from webpack - LogRocket Blog. https://blog.logrocket.com/switching-to-parcel-from-webpack/ Zugegriffen 14.3.2023.
(3) Parcel vs webpack | blog.jakoblind.no. https://blog.jakoblind.no/parcel-webpack/ Zugegriffen 14.3.2023.

---