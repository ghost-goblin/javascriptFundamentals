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

## Explain what Closure is and how it impacts private functions & variables
## Describe how private functions & variables are useful
## Use inheritance in objects using the factory pattern
## Explain the module pattern
## Describe IIFE. What does it stand for?
## Briefly explain namespacing and how it’s useful
