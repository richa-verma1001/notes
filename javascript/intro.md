## Basics
JavaScript borrows most of its syntax from Java, but is also influenced by Awk, Perl and Python.

JavaScript is case-sensitive and uses the Unicode character set

### Javascript Types
* Number
* Boolean
* String
* Function
* Object: Array, Date, RegExp, Math
* Symbol (ES6 only)
* undefined
* null

### Javascript Global Functions
* decodeURI(), decodeURICompnent(), encodeURI(), encodeURIComponent(), escape(), eval(), isFinite(), isNan(), parseInt(), parseFloat(), unescape(), uneval()

### Javascript Variables and Global Scope

It is important to try not to declare variables or functions in global scope. To avoid conflicts with other global functions, it is recommended that a function or set of functions are scoped inside your Closures. With ES6, `var` declaration has been improved with a new keyword `let` that lets developers declare variables for the block scope. This means a variable declared with 'let' inside a if block, will not be available outside the 'if' block where as before es6, the variables declaration 'var' only provided function(global) scope.

### Javascript Hoisting
Means your declarations are hoisted i.e. are available at the onset of JS execution. This applies to 'var' but does not apply to 'let' and 'const' types

### Data type conversion
Javascript is a dynamic language and does not require `type` to be defined at the time of variable declaration. Example -
`
  var a = 32;
  a = 'Hello';  // No error
`
### Integers
Integers can be expressed in decimal (base 10), hexadecimal (base 16), octal (base 8) and binary (base 2).

### Numbers
Represented as primitives or objects.

```
typeof 3; // number
typeof new Number(3); // object
```
Number type in JS includes both integers and floating point values
```
12
23.45
5e3 i.e 5x10^3
234e-5  i.e. 0.00234
```

https://www.youtube.com/watch?v=Xzi4-26vdOM
```
let num = '5';
Number.parseInt(11,2); // 3; assumed base2, From binary to decimal conversion
Number.parseInt(11,16); // 17; assumed base 16, from hex conversion to decimal
Number(11).toString(2); //1101 ; convert to binary

```


### Literals vs. Objects
Example String literals, String objects

### Accessing object properties
Object properties can be accessed in two ways

```obj.property  // return value  ; as-is, not computed like square brackets

obj[property]  // also returns value ; [] provide for computed property
```

Cloning objects via: Object.assign(dest, [src1, src2, ...,srcN]);

Use the second approach when you need to use a variable for the property as that will be eval'ed runtime.

Example:

```var myObj = { a: "1", b: "2", c: 24 };
myObj.a    // "1"

var x = 'c';
myObj['c']   //24
myObj[x]     //24
```

```
delete myObj.a;  // delete a property
```

Object property names can be any string, including the empty string. If the property name would not be a valid JavaScript identifier or number, it must be enclosed in quotes.

```
var unusualPropertyNames = {
  "": "An empty string",
  "!": "Bang!"
}
console.log(unusualPropertyNames."");   // SyntaxError: Unexpected string
console.log(unusualPropertyNames[""]);  // An empty string
console.log(unusualPropertyNames.!);    // SyntaxError: Unexpected token !
console.log(unusualPropertyNames["!"]); // Bang!
```


### Resources
Overview of all JS topics https://www.youtube.com/watch?v=gSnbnYffz7k
Structured walkthru and good for revision - https://javascript.info/
JS Objects - https://www.youtube.com/watch?v=wKBu_dEaF9E
W3Schools - https://www.w3schools.com/jsref/default.asp
Complete Tutorial - https://javascript.info/
Documentation Reference - https://developer.mozilla.org/en-US/docs/Web/JavaScript

#### Cheatsheets
* https://websitesetup.org/javascript-cheat-sheet/
* https://quickref.me/javascript
* https://devhints.io/js-array
* https://devhints.io/es6
* https://devhints.io/jsdoc

### TIPS:
* Try to press Shift+Enter to input multiple lines in the debug inspector
* CMD+SHIFT+DEL - clear browser cache
* JS Equality comparison: https://developer.mozilla.org/en-US/docs/Web/JavaScript/Equality_comparisons_and_sameness#same-value-zero_equality
