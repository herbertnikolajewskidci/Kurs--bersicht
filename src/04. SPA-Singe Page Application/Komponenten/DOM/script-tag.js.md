Um JavaScript-Code in eine HTML-Seite einzufügen, wird der `<script>`-Tag verwendet. Der `<script>`-Tag kann entweder verwendet werden, um den JavaScript-Code direkt in die HTML-Datei einzufügen oder um eine externe JavaScript-Datei zu verknüpfen. Wenn der JavaScript-Code in einer externen Datei enthalten ist, muss diese Datei durch das Attribut "src" im `<script>`-Tag referenziert werden. Das Einfügen von JavaScript-Code in eine HTML-Datei ermöglicht es Entwicklern, interaktive Funktionen wie Formularvalidierung, Animationen und vieles mehr zu erstellen.


## Einbindung über eine externe Datei

HTML-Code:

```html
<!DOCTYPE html>
<html>
<head>
	<title>Meine Webseite</title>
	<!-- Füge eine externe JavaScript-Datei hinzu -->
	<script src="script.js"></script>
</head>
<body>
	<h1>Willkommen auf meiner Webseite!</h1>
	<p>Dies ist eine Beispiel-Seite.</p>
	<!-- Füge einen Button hinzu, der die Funktion aus der JavaScript-Datei aufruft -->
	<button onclick="meinFunction()">Klick mich!</button>
</body>
</html>
```

In diesem HTML-Code wird eine Webseite erstellt. Der `<head>`-Abschnitt enthält den Titel der Webseite und einen `<script>`-Tag, der auf eine externe JavaScript-Datei verweist (script.js). Der `<body>`-Abschnitt enthält eine Überschrift, einen Textabschnitt und einen Button, der eine JavaScript-Funktion aufruft, wenn er geklickt wird.


JavaScript-Code in externer Datei (script.js):

```js
// Definiere eine Funktion, die eine Alert-Box mit dem Text "Hallo Welt!" öffnet
function meinFunction() {
  alert("Hallo Welt!");
}
```

Dieser JavaScript-Code definiert eine Funktion namens "meinFunction()", die eine Alert-Box öffnet, die den Text "Hallo Welt!" enthält. Wenn der Button in der HTML-Datei geklickt wird, ruft er diese Funktion auf und zeigt eine Alert-Box an. Die JavaScript-Datei muss im gleichen Verzeichnis wie die HTML-Datei gespeichert sein, damit sie ordnungsgemäß geladen werden kann.

## Direkte Einbindung über den `<script>`-Tag

```html
<!DOCTYPE html>
<html>
<head>
	<title>Meine Webseite</title>
	<script>
		function meinFunction() {
			alert("Hallo Welt!");
		}
	</script>
</head>
<body>
	<h1>Willkommen auf meiner Webseite!</h1>
	<p>Dies ist eine Beispiel-Seite.</p>
	<button onclick="meinFunction()">Klick mich!</button>
</body>
</html>
```

In diesem Beispiel wird die Funktion "meinFunction()" direkt im `<script>`-Tag definiert, anstatt eine externe JavaScript-Datei zu verwenden. Der Button ruft immer noch die Funktion auf, wenn er geklickt wird.