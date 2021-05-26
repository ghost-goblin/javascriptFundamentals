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
