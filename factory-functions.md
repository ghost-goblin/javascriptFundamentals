# JavaScript - [Factory Functions & the Module Pattern](https://www.theodinproject.com/paths/full-stack-javascript/courses/javascript/lessons/factory-functions-and-the-module-pattern)

## Describe common bugs you might run into using constructors
Constructors were introduced into JavaScript to give the _appearance_ of popular, class-based, object-oriented languanges but goes against the prototypal, functional, object-based nature from which JavaScript draws its powers.
`this` losing context problems are still there when using class. There are no such problems when using a **factory function**, as it doesn’t use `this` at all.
 The `prototype` property isn’t used, so there will be no `instanceof` link between the function and the objects it creates. It is simply a function that happens to create objects.

## Write a factory method that returns an object
```js
const ghostGoblinFactory = (name, age) => {
  const fightSpell = () => console.log('Fight!')
  return { name, age, fightSpell };
};

const ghost1 = ghostGoblinFactory('Fred', 31);
console.log(ghost1.name);
ghost1.fightSpell();
```
## Explain how scope works in JavaScript (bonus points if you can point out what ES6 changed!)
With constructor functions, the lack of encapsulation may create security problems. When using factory functions, only the methods we expose are **public**, everything else is encapsulated. Because of the concept of scope, functions created inside factory functions cannot not be accessed outside the function itself. The only way to use either of those fuctions is to `return` them in the object.
```js
const factoryFunction = string => {
  const privateFunction = () => string.toUpperCase();
  const publicFunction = () => console.log(`----${privateFunction()}----`);
  return { publicFunction };
};

const taco = factoryFunction('taco');

printString(); // ERROR!!
publicString(); // ERROR!!
taco.privateFunction(); // ERROR!!
console.log(taco.publicFunction()); // this prints "----TACO----"
```
ES6 adds more weapons in it’s arsenal when it comes to scope. It has a well defined scoping system which gives flexibility to the developer over hoisting. ES6 introduces the `let` keyword to declare the variables in a block scope. It also ensures variable is not valid if declaring order is upside down.

## Explain what Closure is and how it impacts private functions & variables
Closure is that even though we can’t access the `privateFunction()` function, `publicFunction()` can be accessed. Functions retain their scope even if they are passed around and called outside of that scope. `publicFunction()` has access to everything inside of FactoryFunction, even if it gets called outside of that function.
In the context of factory functions, **closures** allow us to create private variables and functions. **Private functions** are functions that are used in the workings of our objects that are not intended to be used elsewhere in our program.

## Describe how private functions & variables are useful
> For every bit of functionality that you need for your program, there are likely to be several supporting functions that do NOT need to be used in your program as a whole. Tucking these away and making them inaccessible makes your code easier to refactor, easier to test, and easier to reason about for you and anyone else that wants to use your objects.

## Use inheritance in objects using the factory pattern
Factories are simply plain old JavaScript functions that return objects for us to use in our code and you can pick and choose which functions you want to include in your new object. The `Object.assign()` method copies all enumerable own properties from one or more source objects to a target object and returns the target object.
```js
const Nerd = (name) => {
  const prototype = Person(name)
  const doSomethingNerdy = () => console.log('nerd stuff')
  return Object.assign({}, prototype, {doSomethingNerdy}) // lump it together
}
```

## Explain the Module Pattern
The Module Pattern is one of the most common design patterns used in JavaScript and are actually very similar to factory functions.

## Describe IIFE. What does it stand for?
**Immediately Invoked Function Expression**, the function is evaluated then immediately invoked.  Write a function, wrap it in parentheses, and then immediately call the function by adding `();` the end of it. The module pattern creates **encapsulation** of our code and is great for services and testing / TDD.
```js
(function() {
  'use strict'; // good practice to run your modules in strict mode
  // Your code here
  // All function and variables are scoped to this function
})();
```
Exporting a module and creating a public method for the module to call. To expose this method to code outside our module we `return` an Object with the methods defined.
```js
const myModule = (function() {
  'use strict';

  return {
    publicMethod: function() {
      console.log('Hello World!');
    }
  };
})();

myModule.publicMethod(); // outputs 'Hello World'
```

## Briefly explain namespacing and how it’s useful
Namespacing is a technique that is used to avoid naming collisions in our programs.
