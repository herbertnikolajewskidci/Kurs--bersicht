### User Events (interaction)

```js
document.getElementById('button').addEventListener('click', function(){
  alert('Button clicked');
});
```

---

Die ersten Codebeispiele zeigen, wie man auf Benutzerereignisse wie Klicks reagieren kann. Hier wird das `addEventListener`-Methode verwendet, um einen Ereignislistener auf das Button-Element zu setzen. Wenn das Button-Element geklickt wird, wird die angegebene Funktion ausgeführt, die eine Benachrichtigung anzeigt.

---

### Browser Events 
```js
window.addEventListener('load', function(){
  console.log('Page loaded');
});

window.addEventListener('resize', function(){
  console.log('Window resized');
});
```

---

Die nächsten Codebeispiele zeigen, wie man auf Browserereignisse wie das Laden der Seite oder das Ändern der Fenstergröße reagieren kann. Hier wird das `window`-Objekt verwendet, um Ereignislistener auf das Laden der Seite und das Ändern der Fenstergröße zu setzen. Wenn das Ereignis ausgelöst wird, wird die angegebene Funktion ausgeführt, die eine Meldung in der Konsole ausgibt.

---

