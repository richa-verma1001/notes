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
