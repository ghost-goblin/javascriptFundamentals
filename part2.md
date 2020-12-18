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
A method is a function which is a **property** of an object. A JavaScript **property** is a characteristic of an object, often describing attributes associated with a data structure. There are two kind of methods: **Instance Methods** which are built-in tasks performed by an object instance, or **Static Methods** which are tasks that are called directly on an object constructor.

## 9. What are the three logical operators and what do they stand for?
There are three logical operators in JavaScript: `||` (OR), `&&` (AND), `!` (NOT). Go through [this tutorial](https://javascript.info/logical-operators#:~:text=There%20are%20three%20logical%20operators,also%20be%20of%20any%20type.) to read more about logical operators.

## 10. What are the comparison operators?
[Comparison operators](https://www.w3schools.com/js/js_comparisons.asp) are used in logical statements to determine equality or difference between variables or values.

## 11. What is nesting?
When we refer to nesting in JavaScript, we are referring to the ability to create a function within a function.

## 12. What are truthy and falsy values?
In JavaScript, a truthy value is a value that is considered true when encountered in a Boolean context. All values are truthy unless they are defined as falsy (i.e., except for false, 0, -0, 0n, "", null, undefined, and NaN). A falsy value is a value that is considered false when encountered in a Boolean context.

## 13. What are the falsy values in JavaScript?
1. `false` - The keyword false
2. `0`	The number zero
3. `-0`	The number negative zero
4. `0n`	BigInt, when used as a boolean, follows the same rule as a Number.
5. `""`	Empty string value
6. `null` - the absence of any value
7. `undefined` - the primitive value
8. `NaN` - not a number

14. What is the syntax for an if/else conditional?
15. What is the syntax for a switch statement?
16. What is the syntax for a ternary operator?
17. What is the relationship between null and undefined?
18. What are conditionals?
