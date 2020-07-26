
### Array and prototype functions and comprehensions
Documentation source - https://developer.mozilla.org/en-US/docs/Web/JavaScript/Guide/Indexed_collections
Array APIs - https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Array


##### Static #####
* Array.from
* Array.isArray
* Array.of

#### Initialize Arrays
* let array = [];
* let array = [1,2,3,4,5];  // [1,2,3,4,5]
* let array = new Array(5); // arraylength is 5
* let array = new Array(1,2,3,4,5);  // [1,2,3,4,5]
* let anyArray = new Array(1,2 , [3,4,5], 6, 7);  //[1, 2, Array[3], 6, 7]
* let wisenArray = Array.of(9.3) //wisenArray contains only one element 9.3

##### Instance Properties #####
* array.length

##### Instance methods #####

###### Mutator methods ######
These methods modify array

* array.copyWithin
* array.fill
* array.push
* array.pop
* array.shift
* array.unshift
* array.sort
* array.splice
* array.reverse

###### accessor methods ######
These methods do not modify array, they return a new arrays

* array.concat
* array.filter
* array.indexOf
* array.lastIndexOf
* array.join
* array.slice
* array.toString
* array.toLocaleString

##### Iterables #####
These Iterable functions can take a callback function to determine how elements are compared. They are iterables because they iterate over entire array in some fashion.

* array.entries
* array.every
* array.find
* array.findIndex
* array.forEach
* array.keys
* array.map
* array.reduce
* array.reduceRight
* array.some
* array.values


Example 'sort'
````
// numbers is a array [5,4, 2, 6, 9]
sort.numbers(() => );

````

Example 'forEach'
````
// Array colors is [red, green, blue];
colors.forEach(color => console.log(color));
// Prints, a, b and c
````


##### Spread Parameter #####
let arr1 = [1,2, 3];
let arr2 = [5, ...arr1, 6];
or
let arr2 = [...arr1];
or
let arr3 =  [...arr1, ...arr2];

#### Copying Array 
const itemsCopy = [...items];

const foo = document.querySelectorAll('.foo');
const nodes = [...foo];

##### Multi-dimensional Arrays #####

##### Buffers and views: Types array architecture #####

see MDN documentation to cover these topics
