# JavaScript Fundamentals - [Part 2](https://www.theodinproject.com/courses/foundations/lessons/fundamentals-part-2) 

## 1. What are the eight data types of javascript?
1. `number`: integer or floating-point, integers are limited by ±(253-1)
2. `bigint` is for integer numbers of arbitrary length
3. `string` for strings. A string may have zero or more characters, there’s no separate single-character type
4. `boolean` for true/false
5. `null` for unknown values – a standalone type that has a single value null
6. `undefined` for unassigned values – a standalone type that has a single value undefined
7. `object` for more complex data structures
8. `symbol` for unique identifiers

## 2. Which data type is NOT primitive?
Data types that are known as **primitive values** in JavaScript are **numbers**, **strings**, **booleans**, **null** and **undefined**. **Objects** such as **functions** and **arrays** are referred to as **non-primitive** values. The fundamental difference between primitives and non-primitives is that _primitives are immutable_ and _non-primitives are mutable_.

## 3. What is the difference between single, double, and backtick quotes for strings?
Single quotes and double quotes behave in exactly the same way in JavaScript.
The backtick quote allows **string templating**.

## 4. Which type of quote lets you embed variables/expressions into a string?
[Template literals](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Template_literals) are string literals allowing embedded expressions.

## 5. How do you embed variables/expressions into a string?
```js
var value = 4;
var str = `text with a ${value}` // 'text with a 4'
```

## 6. How do you escape characters in a string?
To use a special character as a regular one, prepend it with a backslash: `\`.
```js
var x = 'It\'s alright.';
```
Read this [JavaScript tutorial](https://javascript.info/regexp-escaping#:~:text=As%20we%20may%20recall%2C%20regular,backslash%20is%20used%20for%20escaping.) on escaping special characters.

## 7. What is the difference between slice/substring/substr?
As in [this tutorial](https://masteringjs.io/tutorials/fundamentals/substring), the `slice()` function seems like the clear winner out of the 3 for the following reasons:
- Not considered a _"legacy function"_
- Supports negative indices
- Less name confusion: there's no `String#splice()`

## 8. What are methods?


9. What are the three logical operators and what do they stand for?
10. What are the comparison operators?
11. What is nesting?
12. What are truthy and falsy values?
13. What are the falsy values in JavaScript?
14. What is the syntax for an if/else conditional?
15. What is the syntax for a switch statement?
16. What is the syntax for a ternary operator?
17. What is the relationship between null and undefined?
18. What are conditionals?
