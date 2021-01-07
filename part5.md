# JavaScript Fundamentals - [Part 5](https://www.theodinproject.com/courses/foundations/lessons/fundamentals-part-5)

## Array Functions

## `filter()`

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
