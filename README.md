# node-http-debug

``` sh
npm install github https://github.com/jmervine/node-http-debug.git
```

Usage:

``` javascript
var http = require('node-debug').http;
// var https = require('node-debug').https;

http.debug = 2;

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

Sample Output:
``` sh
# on stderr

HTTP REQUEST:
{ ... http request data ... }
HTTP REQUEST: END CALLED
{ ... request end data if any ... }
HTTP REQUEST: SOCKET EVENT
{ ... request socket event data ... }

```

# Development

Please contribute. I built this quickly for my own needs.

``` sh
git clone https://github.com/jmervine/node-http-debug.git
cd node-http-debug
npm install
npm test
```

No pull requests will be accepted unless tests are (added if need be and) passing.

