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

#### Javascript Variables and Global Scope

It is important to try not to declare variables or functions in global scope. To avoid conflicts with other global functions, it is recommended that all your functions are scoped inside your JS classes. With ES6, `var` declaration has been improved with a new keyword `let` that lets developers declare variables for the block scope. This means a variable declared with 'let' inside a if block, will not be available outside the 'if' block where as before es6, the variables declaration 'var' only provided function(global) scope.

#### Javascript Hoisting
What is the purpose?

### Data type conversion
Javascript is a dynamic language and does not require `type` to be defined at the time of variable declaration. Example -
`
  var a = 32;
  a = 'Hello';  // No error
`
