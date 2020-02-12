

Helpful review of Javascript OOP how it was done in ES5 and ES6
* https://www.youtube.com/watch?v=vDJpGenyHaA&list=PLillGF-RfqbbnEGy3ROiLWk7JMCuSyQtX&index=10


Javascript has functions and Objects.

Example of a Object
var book = {
  name: 'CookBook',
  author: 'Ms. Richa Verma',
  published: '1999'
}

Example of function

var createBook = function(name, author, published) {
  this.name = name;
  this.author = author;
  this.published = published;
}

In ES5, classes were defined with the help of functions

Example
