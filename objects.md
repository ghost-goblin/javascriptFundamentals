# JavaScript - [Objects & Object Constructors](https://www.theodinproject.com/courses/javascript/lessons/objects-and-object-constructors)

```js
function Book(title, author, pages, read) {
  this.title = title;
  this.author = author;
  this.pages = pages;
  this.read = read;
  
  this.info = function() {
  return `${title} by ${author}, ${pages} pages, read: ${read}`;  
  };
};

const theHobbit = new Book('The Hobbit', 'J.R.R. Tolkien', 182, true);

console.log(theHobbit.info());
```
> It's _always_ better to `return` things in functions!
> 

## Object Literals
```js
'use strict';

let witch = { name: 'Abby', colour: 'Green' }
witch.fly = () => { console.log('The witch is flying!') };
witch.fly(); // run the fly fun function

//OR

let witch = { name: 'Abby',
              colour: 'Green',
              fly: () => { console.log('The witch is flying!') }
            }

witch.fly();
```
## `this` Keyword
Refers to an object that is executing the current bit of code, by default that is the global object.
In a web browser this is the window object. The `new` keyword creates a emoty JavaScript object, set the context of `this` to the new object and then calls the witch function.

```js
function Witch() {
    this.name = 'Abby'
    this.colour = 'Green'
}

let witch = new Witch();
console.log(witch); // Witch {name: "Abby", colour: "Green"}

//OR

'use strict';

function Witch(name, colour) {
    this.name = name
    this.colour = colour
}

let witch = new Witch('Abby', 'Green');
console.log(witch); // Witch {name: "Abby", colour: "Green"}
```
