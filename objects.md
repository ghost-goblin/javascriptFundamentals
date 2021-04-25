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
```
## Constructor Functions
```js
function Witch(name, colour) {
    this.name = name
    this.colour = colour
}

let witch = new Witch('Abby', 'Green');
console.log(witch); // Witch {name: "Abby", colour: "Green"}
```
## ES6 Classes
```js
class Goblin {
    constructor(name, colour) {
        this.name = name
        this.colour = colour
    }
    fight() {
        console.log('...fighting the goblin!');
    }
}

let goblin = new Goblin('Elliot', 'Pink');
console.log(goblin); // Goblin {name: "Elliot", colour: "Pink"}
goblin.fight(); // ...fighting the goblin!
```
## Object Properties
`Object.getOwnPropertyDescriptor()`

```js
const cat = {
    name: 'Salem',
    colour: 'Black'
}

console.log(Object.getOwnPropertyDescriptor(cat, 'name'));
// {value: "Salem", writable: true, enumerable: true, configurable: true}
```
## Change the Property Attributes using the `Object.defineProperty()` Method
```js
const cat = {  // object literal
    name: 'Salem',
    colour: 'Black'
}


Object.defineProperty(cat, 'name', { writable: false });
console.log(Object.getOwnPropertyDescriptor(cat, 'name'));
```
> You can change the following at the writable attribute is just a pointer
```js
let cat = {  // object literal
    name: { first: 'Salem', last: 'Spellman' },
    colour: 'Black'
}


Object.defineProperty(cat, 'name', { writable: false });
cat.name.first = 'Scratchy';
console.log(cat.name);
```
> You can prevent the Object being changed by the using `Object.freeze(cat.name)`

## Looping through Properties in Objects
```js
let cat = {  // object literal
    name: { first: 'Salem', last: 'Spellman' },
    colour: 'Black'
}

// The for ... in Loop
for (let propertyName in cat) {
  console.log(propertyName + ': ' + cat[propertyName])
}
// "name: [object Object]"
// "colour: Black"
```
Setting enumerable to false, `Object.defineProperty(cat, 'name', {enumerable: false})` also prevents the properties from showing up in the object keys.
Prevents JSON serialisation of the Object `JSON.stringify(cat)`.
```js
let cat = {  // object literal
    name: { first: 'Salem', last: 'Spellman' },
    colour: 'Black'
}

Object.defineProperty(cat, 'name', { enumerable: false })
// The FOR ... IN Loop
for (let propertyName in cat) {
  console.log(propertyName + ': ' + cat[propertyName])
}
console.log(Object.keys(cat));
// [object Array] (1)
// ["colour"]
```

## Getters & Setters
Attributes on a property that allow you to specify the return value of a property using a function.
```js
let cat = {  // object literal
    name: { first: 'Salem', last: 'Spellman' },
    colour: 'Black'
}

// To create Getters & Setters the have to use the define property
Object.defineProperty(cat, 'fullName',
                     {
  get: function() {
    return this.name.first + ' ' + this.name.last;
  }
})

console.log(cat.fullName); // "Salem Spellman"
```
Let create a setter to spilt the name up again ...
```js
let cat = {  // object literal
    name: { first: 'Salem', last: 'Spellman' },
    colour: 'Black'
}

// To create Getters & Setters the have to use the define property
Object.defineProperty(cat, 'fullName',
                     {
  get: function() {
    return this.name.first + ' ' + this.name.last;
  },
  set: function(value) {
    let nameSplit = value.split(' ');
    this.name.first = nameSplit[0];
    this.name.last = nameSplit[1];
  }
})

cat.fullName = 'Tulip Flower'
console.log(cat.fullName); // "Tulip Flower"
console.log(cat.name.first); // "Tulip"
```
## Prototypes
```js
let arr = ['red', 'blue', 'green']

Object.defineProperty(arr, 'last', { get: function() {
  return this[this.length-1]
}});

let last = arr.last
console.log(last); // green
```
## Creating a Prototype
An Array Object is just a function that is meant to be used as a constructor function
```js
let arr = ['red', 'blue', 'green']

Object.defineProperty(Array.prototype, 'last', { get: function() {
  return this[this.length-1]
}});

let last = arr.last
let arr2 = ['one', 'two', 'three']
console.log(arr2.last); // green
```
## What is a Prototype?
```js
let myFunc = function()  {
  return console.log(myFunc.prototype);
}
myFunc(); // {}
```
