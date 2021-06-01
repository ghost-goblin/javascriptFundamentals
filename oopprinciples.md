# JavaScript - [OOP Principles](https://www.theodinproject.com/paths/full-stack-javascript/courses/javascript/lessons/oop-principles)

## Explain the *Single Responsibility Principle*
A class or object or module should only have _one_ responsibility. 
## Briefly explain the additional SOLID principles
**SOLID** is a _mnemonic_ acronym referring to a collection of design principles. JavaScript is a prototype-based, dynamically typed language, blending concepts from object-oriented and functional programming paradigms.
### The Single Responsibility Principle

> “Do one thing and do it well”

Every function that you write should do exactly *one* thing and have a clearly defined goal.

### The Open/Closed Principle
JavaScript modules should be open to extension but closed to modification. If you want to extend a modules behaviour, you don't need to modify the existing code.
There is one easy test to follow, if you have to open up your JS module and make a modification in order to extend it, you have failed the test.

### The Liskov Substitution Principle
Sometimes something that sounds right in natural language doesn't quite work in code. For example, in mathematics, a `square` is a `rectangle`, and makes you want to model this based on inheritance. However, in your code, if you are deriving your square from your rectangle, using the `setHeight` and `setWidth` properties, the reference point of `rectangle` doesn't make any sense.

### The Interface Segregation Principle
Do not create bloated interfaces ... meaning whenever you expose a module for outside use, make sure only the bare essentials are required and the rest are optional.

### The Dependency Inversion Principle

## Explain what “tightly coupled” objects are and why we want to avoid them
