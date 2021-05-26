# JavaScript - [Classes](https://www.theodinproject.com/paths/full-stack-javascript/courses/javascript/lessons/classes)

Often, we need to create many objects of the same kind i.e. users. The syntax for a class is as follows:
```js
class MyClass {
  // class methods
  constructor() { ... }
  method1() { ... }
  method2() { ... }
  method3() { ... }
  ...
}
```
What class User {...} construct really does is:

1. Creates a **function** named `User`, that becomes the result of the class declaration. The function code is taken from the constructor method __(assumed empty if we don’t write such method)__
2. Stores class methods, such as `sayHi`, in `User.prototype`
3. We can the use `new MyClass()` to create a new object with all the listed methods.

## The `constructor()` Method
The `constructor()` method is called automatically by `new`, this is how we initialise the object.
```js
class User {

  constructor(name) {
    this.name = name;
  }

  sayHi() {
    console.log("Hi " + this.name);
  }

}

// Usage:
let user = new User("John");
user.sayHi();
```
So what happens when the `new User()` is called?
1. A **new object** is created
2. The constructor runs with the given argument and assigns it to `this.name`
3. After `new User` object is created, when we call its method, which is taken from the **prototype**, so the object has access to class methods

## Syntactic Sugar?!
Technically, we could do the same without creating a class but there are still a few important differences to note:
1. A function created by a class has a special internal property, `[[isClassConstructor]]: true`. Javascript checks for that property in a variety of places and unlike a regular function, must be called with the `new` keyword
2. A string representation of a class constructor in most JavaScript engines starts with the “class…”
3. Class methods are _non-enumerable_. A class definition sets enumerable flag to `false` for all **methods** in the "prototype" which is handy as when we create a `for...in` loop, we don't want to loop over the methods
4. Classes always `use strict`. All code inside the class construct is automatically in **strict mode**

## Class Expressions
Just like functions, classes can be defined inside another expression, passed around, returned, assigned, etc.
```js
let User = class MyClass {
  sayHi() {
    console.log(MyClass); // MyClass name is visible only inside the class
  }
};

new User().sayHi(); // works, shows MyClass definition
console.log(MyClass); // error, MyClass name isn't visible outside of the class
```
