1.  The 'window' object 
   Das 'window'-Objekt ist das globale Objekt des Browsers und stellt das Fenster des Browsers dar, in dem die Webseite geladen wird. Es ist das oberste Objekt der Browser-Objekt-Hierarchie und bietet viele Methoden und Eigenschaften, um auf die Webseite und den Browser zuzugreifen.
    
2.  **Host-Objekte** vs. *native Objekte*: 
   Host-Objekte werden vom Browser oder der Umgebung bereitgestellt, in der der JavaScript-Code ausgeführt wird. Beispiele hierfür sind das **'window'-Objekt**, das **'document'-Objekt** oder das **'XMLHttpRequest'-Objekt**. Native Objekte sind Objekte, die in der JavaScript-Sprache definiert sind, wie z.B. das *'Array'-Objekt* oder das *'Math'-Objekt*. Im Gegensatz zu Host-Objekten sind native Objekte nicht browserabhängig und können auf allen Plattformen ausgeführt werden, die JavaScript unterstützen.

3.  window als globaler Bereich:  
   Das 'window'-Objekt ist der globale Bereich in JavaScript und alle Variablen, die im globalen Kontext definiert werden, werden automatisch als Eigenschaften des 'window'-Objekts hinzugefügt. Zum Beispiel:
```js
var myVar = "Hello World";
console.log(window.myVar); // gibt "Hello World" aus
```

**Christians Recherche hat ergeben:**

-   Mit **var** deklarierte variablen werden im window objekt gespeichert - aber so wie das aussieht aus kompatibilitätsgründen, weil das früher so gemacht wurde
-   Mit **let/const** geht das nicht mehr, sondern da muss man dann die eigenschaft direkt zum objekt hinzugefügt werden (window.myVar = "Blah")
4.  Benutzereingaben und Meldungen an das Fenster: window.prompt() und window.alert() 
   Die Methode **'window.prompt()'** wird verwendet, um dem Benutzer eine Eingabeaufforderung anzuzeigen, bei der er Text in ein Dialogfeld eingeben kann. Zum Beispiel:
```js
let name = window.prompt('Wie ist dein Name?');
console.log(name); // gibt den vom Benutzer eingegebenen Namen aus
```
Die Methode **'window.alert()'** wird verwendet, um eine Meldung an den Benutzer anzuzeigen. Zum Beispiel:
```js
window.alert('Hallo Welt!');
```
5.  Das document-Objekt
   Das 'document'-Objekt stellt das aktuelle HTML-Dokument dar, das im Browser angezeigt wird, und bietet viele Methoden und Eigenschaften, um auf das Dokument und dessen Elemente zuzugreifen. Zum Beispiel:
```js
let title = document.title; // gibt den Titel des Dokuments zurück
let element = document.getElementById('myElement'); // gibt das Element mit der ID 'myElement' zurück
```
6.  HTML DOM Dokumentation: MDN 
   Das Mozilla Developer Network (MDN) bietet eine umfassende Dokumentation der HTML-DOM-API, einschließlich des 'window'-Objekts und des 'document'-Objekts. Du kannst die Dokumentation hier finden: [https://developer.mozilla.org/de/docs/Web/API/Document_Object_Model](https://developer.mozilla.org/de/docs/Web/API/Document_Object_Model).