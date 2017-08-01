Various Module Loaders to choose from -

1. Require JS: Seen used in combination with AMD/dojo etc. Examples: define([], ..), require(['app/hello', function(hello) { ..});

2. Common JS Format: Included and used with Node - https://webpack.github.io/docs/commonjs.html
module.exports = hello;
var hello = require(./helloworld);


3. ES6 import / export
module.exports = hello;
import hello from './helloworld';

Note - Found React documentation at http://requirejs.org/docs very helpful in understanding available loaders and the need for AMD i.e async module definitions.
