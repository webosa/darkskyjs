Pull Requests welcome, if you have used this script in a project let me know, I'd like to start a directory. Have fun. 

darksky.net-javascript-api
==========================

darksky.net JavaScript API

## Getting Started
PHP is required for proxy to work. This is a cross domain policy workaround.

darksky.net.js is configured to work with both [AMD](https://en.wikipedia.org/wiki/Asynchronous_module_definition) and [CJS](https://en.wikipedia.org/wiki/CommonJS) applications. When the module is loaded it will return a constructor that, once run, will provide the necessary interface functions, namely:

* `getCurrentConditions`
* `getForecastToday`
* `getForecastWeek`

Use of the above is demonstrated within index.html. 

If you're using [Require.JS](http://requirejs.org/) use the example configuration in index.html as a reference. 

If you're using [Webpack](http://webpack.github.io/), [Browserify](http://browserify.org/) or some other CJS module loader simply require the module like so

`var Darksky = require('darksky.net');`

and use the `Darksky` constructor as per the demo on the index page.

## Location data

Forecast.io.js can handle multiple location requests. Any request _must_ be supplied as an array of objects as per the example in index.html. 

## Dependencies

Forecast.io.js uses [moment.js](http://momentjs.com/) to handle date/time data and an [ES6 Promises Polyfill](https://github.com/jakearchibald/es6-promise) to handle the requests via promises.

If you're using Require.JS be sure to load include these two libraries somewhere in your application.

If you're using a CJS module loader be sure to install these two libraries using npm:

`npm install moment`

Ref: [https://www.npmjs.com/package/moment](https://www.npmjs.com/package/moment)

`npm install es6-promise`

Ref: [https://www.npmjs.com/package/es6-promise](https://www.npmjs.com/package/es6-promise)
    
There are also more returns which will be added into the plain Javascript in due course. 
