Various Module Loaders to choose from -

1. Require JS: Seen used in combination with AMD/dojo etc. Examples: define([], ..), require(['app/hello', function(hello) { ..});

2. Common JS Format: Included and used with Node - https://webpack.github.io/docs/commonjs.html
module.exports = hello;
var hello = require(./helloworld);


3. import / export --> Now built into ES6 and the default approach
module.exports = hello;
import hello from './helloworld';

```
class Module1 {
  function1 () {

  };
  function 2 () {

  };
}
export {Module1};
```
```
import {Module1} from './module1';
let myModule = new Module1();
myModule.function1();
```

OR
```
export default function myFunc1() {

}
export function myFunc2(){

}
```

```
import myFunc1, {myFunc2} from './module2';
myFunc1();
myFunc2();
```

Note - Found React documentation at http://requirejs.org/docs very helpful in understanding available loaders and the need for AMD i.e async module definitions.
