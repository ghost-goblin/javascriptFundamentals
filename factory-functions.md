# JavaScript - [Factory Functions & the Module Pattern](https://www.theodinproject.com/paths/full-stack-javascript/courses/javascript/lessons/factory-functions-and-the-module-pattern)

## Describe common bugs you might run into using constructors
Constructors were introduced into JavaScript to give the _appearance_ of popular, class-based, object-oriented languanges. run contrary to the prototypal, functional, object-based nature from which JavaScript draws its strength

The lack of encapsulation may create security problems. When using factory functions, only the methods we expose are public, everything else is encapsulated.
`this` losing context problems are still there when using class. There are no such problems when using a factory function, as it doesn’t use `this` at all.


Write a factory method that returns an object.
Explain how scope works in JavaScript (bonus points if you can point out what ES6 changed!).
Explain what Closure is and how it impacts private functions & variables.
Describe how private functions & variables are useful.
Use inheritance in objects using the factory pattern.
Explain the module pattern.
Describe IIFE. What does it stand for?
Briefly explain namespacing and how it’s useful.
