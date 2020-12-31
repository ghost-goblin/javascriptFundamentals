# JavaScript Fundamentals - [Part 4](https://www.theodinproject.com/courses/foundations/lessons/fundamentals-part-4)

## Arrays
JavaScript arrays are used to store multiple values in a single variable. Arrays are objects and the `typeof` operator returns "object".

## Array Methods
[W3schools](https://www.w3schools.com/js/js_array_methods.asp) covers some of the most useful built-in array methods.
- The `splice()` method can be used to add new items to an array.
```js
var fruits = ["Banana", "Orange", "Apple", "Mango"];
fruits.splice(2, 0, "Lemon", "Kiwi");
// or
fruits.splice(0, 1);        // Removes the first element of fruits
```
- The `slice()` method creates a new array. It does not remove any elements from the source array.

## The Arguments Object
[Arguments](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Functions/arguments) is an Array-like object accessible inside functions that contains the values of the arguments passed to that function. The arguments object is a local variable available within all non-arrow functions. You can refer to a function's arguments inside that function by using its arguments object. It has entries for each argument the function was called with, with the first entry's index at 0.

As you can do with any Array-like object, you can use ES2015's Array.from() method or spread syntax to convert arguments to a real Array:
```js
let args = Array.from(arguments);
// or
let args = [...arguments];
```

## Rest Parameters
The [rest parameter](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Functions/rest_parameters) syntax allows us to represent an indefinite number of arguments as an array.
```js
function sum(...theArgs) {
  return theArgs.reduce((previous, current) => {
    return previous + current;
  });
}

console.log(sum(1, 2, 3));
// expected output: 6

console.log(sum(1, 2, 3, 4));
// expected output: 10
```

## forEach Method
```js
var removeFromArray = function(...args) {
    let newArr = [];
    const array = args[0];
    
    // array.forEach(func) – func is executed by forEach for every array item.    
    array.forEach((item) => {
        if (!args.includes(item)) {
             newArr.push(item);
             };
             });
             return newArr;
             };

console.log(removeFromArray([1, 2, 3, 4, 5, 7, 8], 1, 4, 8));
```
