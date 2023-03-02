`index.html`:
```html
<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="UTF-8">
  <title>JS Promises Examples</title>
</head>
<body>
  <h1>JS Promises Examples</h1>

  <h2>The request response cycle</h2>
  <p>Sorry, no example available for this topic.</p>

  <h2>Client perspective</h2>
  <p>Sorry, no example available for this topic.</p>

  <h2>Blocking vs. Non-Blocking code: A brief example</h2>
  <button id="block-button">Block for 3 seconds</button>
  <button id="non-block-button">Non-Block for 3 seconds</button>

  <h2>Race conditions: Reading non blocking code</h2>
  <p>Sorry, no example available for this topic.</p>

  <h2>Promises</h2>
  <button id="promise-button">Promise Example</button>

  <h2>Promisifying: Converting `setTimeout()` to a promise</h2>
  <button id="promisifying-button">Promisifying Example</button>

  <h2>Breaking Promises</h2>
  <button id="breaking-button">Breaking Promise Example</button>

  <script src="script.js"></script>
</body>
</html>
```

`script.js`:

```js
// Blocking vs. Non-Blocking code example
document.querySelector('#block-button').addEventListener('click', function() {
  console.log('Start blocking');
  const start = Date.now();
  while (Date.now() - start < 3000) {
    // Wait for 3 seconds
  }
  console.log('End blocking');
});

document.querySelector('#non-block-button').addEventListener('click', function() {
  console.log('Start non-blocking');
  setTimeout(function() {
    console.log('End non-blocking');
  }, 3000);
});

// Promises example
document.querySelector('#promise-button').addEventListener('click', function() {
  console.log('Start Promise Example');
  const promise = new Promise(function(resolve, reject) {
    setTimeout(function() {
      resolve('Promise Resolved!');
    }, 3000);
  });

  promise.then(function(result) {
    console.log(result);
  }).catch(function(error) {
    console.log(error);
  }).finally(function() {
    console.log('Promise Completed!');
  });
});

// Promisifying example
function delay(ms) {
  return new Promise(function(resolve) {
    setTimeout(resolve, ms);
  });
}

document.querySelector('#promisifying-button').addEventListener('click', function() {
  console.log('Start Promisifying Example');
  delay(3000).then(function() {
    console.log('Promise Resolved!');
  });
});

// Breaking Promises example
document.querySelector('#breaking-button').addEventListener('click', function() {
  console.log('Start Breaking Promise Example');
  const promise = new Promise(function(resolve, reject) {
    reject('Promise Rejected!');
  });

  promise.catch(function(error) {
    console.log(error);
  }).finally(function() {
    console.log('Promise Completed!');
  });
});
```