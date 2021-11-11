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
What is the purpose?

### Data type conversion
Javascript is a dynamic language and does not require `type` to be defined at the time of variable declaration. Example -
`
  var a = 32;
  a = 'Hello';  // No error
`
### Integers
Integers can be expressed in decimal (base 10), hexadecimal (base 16), octal (base 8) and binary (base 2).

### Literals vs. Objects
Example String literals, String objects

### Accessing object properties
Object properties can be accessed in two ways

```obj.property  // return value

obj[property]  // also returns value
```

Use the second approach when you need to use a variable for the property as that will be eval'ed runtime.

Example:

```var myObj = { a: "1", b: "2", c: 24 };
myObj.a    // "1"

var x = 'c';
myObj['c']   //24
myObj[x]     //24
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

Quick cheatsheet when revisiting https://websitesetup.org/javascript-cheat-sheet/
Overview of all JS topics https://www.youtube.com/watch?v=gSnbnYffz7k
