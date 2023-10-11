### Literals vs. Objects
Example String literals, String objects

### Accessing object properties
Object properties can be accessed in two ways

```obj.property  // return value  ; as-is, not computed like square brackets

obj[property]  // also returns value ; [] provide for computed property
```

##### Cloning objects via: Object.assign(dest, [src1, src2, ...,srcN]);

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

##### Example complex object
How to access properties of a complex Object

```
const ourStorage = {
  "desk": {
    "drawer": "stapler"
  },
  "cabinet": {
    "top drawer": {
      "folder1": "a file",
      "folder2": "secrets"
    },
    "bottomdrawer": {
        "folder1" : "empty"
    }
  }
};
```

```
ourStorage.desk or ourStorage['desk']    // Gives back same result obj{}
ourStorage.cabinet['top drawer'].folder1  // "a file";
ourStorage.cabinet.top drawer.folder1   // Syntax Error
ourStorage.cabinet.'top drawer'.folder1  // Syntax Error
ourStorage.cabinet.bottomdrawer.folder1  // "empty"
```
'top drawer' cannot be used in . notation because of the space and must be addressed with bracket notation


#### Destructuring
Use destructing to
 * extract values from objects,
 * assign variables from objects,
 * assign variables from nested objects,
 * assign variables from arrays,
 * use it with rest parameter to reassign array elemnts,
 * in place destructuring when object is passed into a function

Revise this under ES6 https://www.freecodecamp.org/learn/javascript-algorithms-and-data-structures/#es6

Revise these -
https://www.freecodecamp.org/learn/javascript-algorithms-and-data-structures/es6/use-destructuring-assignment-to-assign-variables-from-nested-objects

```
const obj = {
  name: 'richa',
  height: 5.5,
  children: {
    name: 'mansi'
  }
}
const {name, height} = obj;  // name = richa; height = 5.5
const {children: {name: firstChild}} = obj; // firstChild = mansi

const [a, b,,, c] = [1, 2, 3, 4, 5, 6];
console.log(a, b, c);  // 1,2,5

let a = 8, b = 6;
[a, b] = [b, a];  // a=6, b=8
```

```
const [a, b, ...arr] = [1, 2, 3, 4, 5, 7]; // rest param only works well as last element in the list
console.log(a, b);   // 1, 2
console.log(arr);  // [3,4,5,7]

let arr = [1,2,3,4,5,7];
let result = arr.slice(2);  //[3,4,5,7];slice(start, end)

// arr : [1,2,3,4,5,7], result: [3,4,5,7]
```

##### Write Concise Object Literal Declarations Using Object Property Shorthand

```
const getMousePosition = (x, y) => ({
  x: x,
  y: y
});

can be rewritten as
const getMousePosition = (x, y) => ({ x, y });
```

Also lookup spread operator

##### Iterating over a object

```for(let key in obj) {
  console.log(`key: 4{key} value: ${obj[key]}`);
}
````

##### instanceof
The instanceof operator tests to see if the prototype property of a constructor appears anywhere in the prototype chain of an object. The return value is a boolean value

```
function Car(make, model, year) {
  this.make = make;
  this.model = model;
  this.year = year;
}
const auto = new Car('Honda', 'Accord', 1998);

console.log(auto instanceof Car);
```
