
### for...of
#### Iterating over a Map

````const iterable = new Map([['a', 1], ['b', 2], ['c', 3]]);

for (const entry of iterable) {
  console.log(entry);
}
// ['a', 1]
// ['b', 2]
// ['c', 3]

for (const [key, value] of iterable) {
  console.log(value);
}
// 1
// 2
// 3
````

### Strings

````
const a = 'John Smith';
a.charAt(3); // n
a[3]; // n

````
ES6 only. Strings can be accessed like array like objects in this case. 
