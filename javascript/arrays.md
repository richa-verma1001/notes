
### Array and prototype functions and comprehensions
Documentation source - https://developer.mozilla.org/en-US/docs/Web/JavaScript/Guide/Indexed_collections

#### Initialize Arrays
* let array = [];
* let array = [1,2,3,4,5];  // [1,2,3,4,5]
* let array = new Array(5); // arraylength is 5
* let array = new Array(1,2,3,4,5);  // [1,2,3,4,5]
* let anyArray = new Array(1,2 , [3,4,5], 6, 7);  //[1, 2, Array[3], 6, 7]
* let wisenArray = Array.of(9.3) //wisenArray contains only one element 9.3



##### Functions available #####
* array.length
* array.push
* array.pop
* array.indexOf
* array.splice
* array.slice
* array.indexOf
* array.concat
* array.join
* array.find
* array.reverse


##### Iterables #####
These Iterable functions can take a callback function to determine how elements are compared. They are iterables because they iterate over entire array in some fashion.

* array.sort
* array.forEach
* array.map
* array.filter
* array.every
* array.some
* array.reduce
* array.reduceRight

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

##### Static #####
* Array.from
* Array.isArray

##### Spread Parameter #####
let arr1 = [1,2, 3];
let arr2 = [5, ...arr1, 6];
or
let arr2 = [...arr1];
or
let arr3 =  [...arr1, ...arr2];

##### Multi-dimensional Arrays #####

##### Buffers and views: Types array architecture #####

see MDN documentation to cover these topics
