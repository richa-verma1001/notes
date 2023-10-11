# About ES6

## Lets get started
+ Your primary source to ES6 documentation - https://developer.mozilla.org/en-US/docs/Web/JavaScript/
+ Checkout codepen or scrimba to run JS exercises or snippets.
+ Add enough comments and its still done via // or /* this \*/


## Get your basics right

+ Bytes and bits - 1 byte is 8 bits (Yes, very basic revision)
+ ASCII - Has 128 characters with values 0 thru 127. Its a 8 BIT CHARACTER SET where all characters can be represented within 8 bits. http://www.asciitable.com/
+ UTF-16: A 2 byte or 16 bit character set proposed by unicode to account of multiple language characters. The character set has short comings and evolved into more widely used UTF-8 character set.
+ UTF-8: A 4 bytle (32 bit) character set, can be expanded to upto 6 bytes if needed. Widely used today. The first bit marks how many bytes the character uses and therefore ASCII which can be denoted in a single bytle does not need to take 4 bytes unecessarily - https://www.youtube.com/watch?v=-oYfv794R9s and https://www.youtube.com/watch?v=vLBtrd9Ar28


### Datatypes
> undefined, null, boolean, string, symbol, number, object

### Types of variables aka Variable declaration
> const, let, var
+ const - read only, blocked scoped, not hoisted, must be initialized when declared
+ let - blocked scope, optional initialization to a value, not hoisted
+ var - has function scope, and is hoisted  // e.g. \_numOfApples
    + A variable that is not initialized has value undefined

```
    a = a + 5; >> a += 5;
    b = b - 1; >> b -= 1;
    a = a * 5; >> a \*= 5;
    b = b / 4; >> b /= 4;
```

#### Hoisting
Variables and Functions are hoisted in javascript which means that all function declarations are hoisted up and therefore function invocations can happen before we actually see the declaration in JS file. Hoisting obviously happens at runtime. In ES6 `let` isn't hoisted.

#### Functions
ES6 uses arrow function. They use the arrow syntax obviously. There are 2 reason for using them
1. A more concise syntax
2. ** 'this' keyword is redefined to be the scope in which the function is called. **

````
function sum(a,b) {
  return a+b;
}  

Can be rewritten as

let sum = (a,b) => a+b;

Using arrow assumes you are defining function and can therefore skip the funciton key word. Anything after the arrow is assumed is the return value.

````

##### Default Parameters
```
const sum = (a, b=1) => a + b; // when not provided, b has a default value of 1
```

#### IIFE
Immediately invoked function expression - Done for scoping i.e. to isolate all variables and functions so that there is no conflict.
````
(function () {
  console.log('Welcome to the Internet. Please follow me.');
}());
````
