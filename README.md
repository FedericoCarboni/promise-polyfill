Promise [![Build Status](https://travis-ci.org/taylorhakes/promise-polyfill.png?branch=master)](https://travis-ci.org/taylorhakes/promise-polyfill)
=============

Light weight promise polyfill for the browser and node. A+ Compliant. It is a perfect polyfill IE, Firefox or any other browser that does not support native promises.

This implementation is based on [then/promise](https://github.com/then/promise). It has been changed to use the prototype for performance and memory reasons.

For API information about Promises, please check out this article [HTML5Rocks article](http://www.html5rocks.com/en/tutorials/es6/promises/).

It is extremely light weight. ***< 1kb Gzipped***

## Downloads

- [Promise](https://raw.github.com/taylorhakes/promise-polyfill/master/Promise.js)
- [Promise-min](https://raw.github.com/taylorhakes/promise-polyfill/master/Promise.min.js)

### Node
```
npm install promise-polyfill
```

## Simple use
```
var prom = new Promise(function(resolve, reject) {
  // do a thing, possibly async, then…

  if (/* everything turned out fine */) {
    resolve("Stuff worked!");
  }
  else {
    reject(new Error("It broke"));
  }
});

// Do something when async done
prom.then(function() {
  ...
});
```

## Testing
```
npm install
npm test
```

## License
MIT
