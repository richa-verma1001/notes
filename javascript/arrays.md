
### Array and prototype functions and comprehensions
Documentation source - https://developer.mozilla.org/en-US/docs/Web/JavaScript/Guide/Indexed_collections
Array APIs - https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Array


##### Static #####
* Array.from - Creates a new shallow copied array from an array like or iterable object
```
console.log(Array.from('foo'));
// expected output: Array ["f", "o", "o"]
```
* Array.isArray - Return boolean
* Array.of - Creates an array of provided value 

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

* array.copyWithin(target, startCopyIndex, endCopyIndex) // **Returns modified array**
 > ``` [1,2,3,4,5].copyWithin(0,2,4); // [3, 4, 3, 4, 5] ```
* array.fill(value, startIndex, endIndex) // Returns modified array
>```
>[1,2,3,4,5].fill(4,1,2); // [1,4,3,4,5]
>[1,2,3,4,5].fill(4,1,1); // [1,2,3,4,5]
>```
* array.push(item) // Modifies array, adds items to the top of the stack; **return length of new array**
> ```
> [1,2,3,4,5].push(90); // **Return new array length 6** 
>```
* array.pop() // Pop and **return the top element(string, number, object etc)** out of the stack
> ```
> [1,2,3,4,5].pop(); // Removes last element and return it ; 5 
> ['broccoli', 'cauliflower', 1,'tomato', {'a':1, 'b': 2}].pop(); // {'a':1, 'b': 2}
>```
* array.shift() // Remove and return item at index 0
> ```
> [1,2,3,4,5].shift(); // Removes first element and returns it : 1
>```
* array.unshift(item) // adds item to index 0 and return new array length 
> ```
> [1,2,3,4,5].unshift(190); // adds new element to beginning, returns new length of array ; 6  
>```
* array.sort(function compareFn(firstEl, secondEl){....}) 
> If nothing supplied string conversions have and sort done based UTF comparisons  
> For numbers a,b if result is > 0, b is sorted before a, if < 0, a is sorted before b, if === no change. 


* array.splice(start, deleteCount, item1, item2, ..., itemN)
> ```
> let array = [1,2,3,4,5];
> let removed = array.splice(2, 2,8,9,10);    // [3,4]
> console.log(array);   // [1,2,8,9.10,5]
>
> let array = [1,2,3,4,5];
> let removed = array.splice(2);  // [3,4,5]
> console.log(array);   // [1,2] , all elements at starting index are removed whene deletecount is omitted
> 
> let myFish = ['angel', 'clown', 'mandarin', 'sturgeon']
> let removed = myFish.splice(2, 0, 'drum', 'guitar');  // ['angel', 'clown', 'drum', 'guitar', 'mandarin', 'sturgeon']
> 
> let myFish = ['angel', 'clown', 'mandarin', 'sturgeon']
> let removed = myFish.splice(-2, 1); //['angel', 'clown', 'sturgeon']
>```
* array.reverse() // Returns reversed array, first element is last, last is first. 

###### accessor methods ######
These methods do not modify array, they return a new arrays

* array.concat(arr1, arr2, arr3, [], arr4, ..., arr5) // Returns shallow copy of all arrays 
* array.filter(function(item, i, array){}, thisArg) //returns new array with items that return true for criteria or emptry []
* array.indexOf(searchElement, fromIndex) 
>```
> [1,2,3,4,5].indexOf(2);  
> [4,3,2,5,5,7,8].indexOf(5, 3); //3 (first occurance)
> [8,3,2,1,5].indexOf(9); //-1 Not found 
>```
* array.lastIndexOf(searchElement, fromIndex) // Return first occurance when searching backwards 
* array.join() || array.join(separator) // Returns concatened **STRING** 
>```
> const elements = ['Fire', 'Air', 'Water'];
> console.log(elements.join()); // 'Fire,Air,Water
> console.log(elements.join(''); // FireAirWater
> console.log(elements.join('-'); // Fire-Air-Water
> console.log(elements.join(' ');  // Fire Air Water
>```
* array.slice(startIndex, endIndex) // return shallow copy of sliced array with end not included.
>```
> const animals = ['ant', 'bison', 'camel', 'duck', 'elephant'];
> animals.slice(-2, -1);   // 'duck' -ve index starts from the end of the array. i.e. length - sIndex
>```
* array.toString() // Returns a string representing array 
* array.toLocaleString **TBD**

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
