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
We can the use `new MyClass()` to create a new object with all the listed methods.

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
1. A new object is created.
The constructor runs with the given argument and assigns it to this.name.
