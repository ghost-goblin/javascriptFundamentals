# JavaScript Fundamentals - [Part 5](https://www.theodinproject.com/courses/foundations/lessons/fundamentals-part-5)

## Array Functions

# `map()`
The `map()` method is used for creating a new array from an existing one, applying a function to each one of the elements of the first array.
```js
const numbers = [1,2,3,4];
const doubled = numbers.map(num => num * 2);
console.log(doubled);
```
In the callback, only the array element is required. Usually some action is performed on the value and then a new value is returned.
### Syntax
```js
var new_array = arr.map(function callback(element, index, array) {
    // Return value for new_array
}[, thisArg])
````

# `filter()`
The `filter()` method takes each element in an array and applies a conditional statement against it. If the condition returns `true`, the element gets pushed to the output array.
```js
const numbers = [1,2,3,4];
const evenNumbers = numbers.filter((num) => {
  if (num % 2 === 0) return num;
});
console.log(evenNumbers);

// or a simpler way to do it is:
const numbers = [1,2,3,4];
const evenNumbers = numbers.filter(num => num % 2 === 0);
console.log(evenNumbers);
```
### Syntax
The `filter()` method takes a **callback function** with the following parameters: `element`, `index` and `array`
```js
var new_array = arr.filter(function callback(element, index, array) {
    // Return true or false
}[, thisArg])
```

# `reduce()`
The `reduce()` method reduces an array of values down to just one value. To get the output value, it runs a reducer function on each element of the array.
### Syntax
```js
arr.reduce(callback[, initialValue])
```
