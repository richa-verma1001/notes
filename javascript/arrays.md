
### Array and prototype functions and comprehensions

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
These Iterable functions can take a callback function to determine how elements are compared
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

##### Multi-dimensional Arrays #####
