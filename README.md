# node-http-debug

```
npm install github https://github.com/jmervine/node-http-debug.git
```

Usage:

```

var http = require('node-debug').http;
// var https = require('node-debug').https;

http.debug = true;

/****
 * debug states
 * - false : off
 * - 0     : off
 * - true  : on (request, write, end)
 * - 1     : on
 * - 2     : verbose (on + error and socket event reporting)
 ****/
 
// Make http requests as usual.
http.get('http://mervine.net/', function (err, res) {
   if (err) console.trace(err);
   console.log(res.statusCode);
});

```

# Development

Please contribute. I built this quickly for my own needs.

```
git clone <repo>
cd <repo>
npm install
npm test
```

