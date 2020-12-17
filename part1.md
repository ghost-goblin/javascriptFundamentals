# JavaScript Fundamentals - [Part 1](https://www.theodinproject.com/courses/foundations/lessons/fundamentals-part-1) 

## 1. How do you declare a variable?
A _variable_ is a storage container for data.

```js
let message;
message = 'Hello'; //store the string
// or
let message = 'Hello';
```

## 2. What are three different ways to declare a variable?
- `var`
- `let`
- `const`

## 3. Which one should you use when?
- `var`is **global-scoped** / **function-scoped** and declartions are processed when the _function or script starts_. This is called **hoisting**.
JavaScript **hoists** the variable declarion to the top of the function block.
- `let`provides **block-scoping**.
- `const`is immutable and will throw an error if an attempt is made to change its value after it has been declared.

Here is a link to [Hacker Noon](https://medium.com/hackernoon/why-you-shouldnt-use-var-anymore-f109a58b9b70) on why we shouldn't use var anymore.

## 4. What are the rules for naming variables?
- ⚠️ Declaring a variable twice triggers an error
- The name must contain only letters, digits, or the symbols `$` and `_`
- The first character must not be a digit
- Case matters!
- `let`, `class`, `return`, and `function` are reserved and cannot be used as variable names
- When the name contains multiple words, **camelCase** is commonly used

`"use strict";` defines that JavaScript code should be executed in "strict mode". Strict mode changes previously accepted _"bad syntax"_ into real errors.

```js
"use strict";
x = 3;       // This will cause an error because x is not declared
```

## 5. What are operators, operands, and operations?
Check out this [guide on MDN web docs](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Guide/Expressions_and_Operators) on expressions and operators.
A **binary** operator requires two operands, one before the operator and one after the operator:
`operand1` `operator` `operand2` e.g. `3 + 4` or `x * y`.
A **unary** operator requires a single operand, either before or after the operator:
`operator` `operand` OR `operand` `operator` e.g. `x++` or `++x`.


## 6. What is concatenation and what happens when you add numbers and strings together?
Concatenation is the process of appending one string to the end of another string. You can check out this [tutorial](https://masteringjs.io/tutorials/fundamentals/string-concat) on the 3 ways to concatenate strings in JavaScript.
Adding two numbers, will return the sum, but adding a number and a string will return a string.

## 7. What are the different types of operators in JavaScript?
1. Arithmetic
2. Comparison
3. Assignment
4. Logical

## 8. What is the difference between == and ===?
`==` in JavaScript is used for comparing two variables, but it ignores the datatype of variable. `===` is used for comparing two variables, but this operator also checks datatype and compares two values.

## 9. What are operator precedence values?

## 10. What are the increment/decrement operators?
The increment and decrement operators in JavaScript will add one (+1) or subtract one (-1), respectively, to their operand, and then return a value. This [Codeburst lesson](https://codeburst.io/javascript-increment-and-decrement-8c223858d5ed) explains that using `++` or `--` prior to our variable, the operation executes and adds/subtracts 1 prior to returning.

## 11. What is the difference between prefixing and post-fixing them?
Another useful post on [Hacker Noon](https://hackernoon.com/javascript-back-to-basics-prefix-vs-postfix-8da5256223d2) about prefix vs. postfix

## 12. What are assignment operators?
Assignment operators assign values to JavaScript variables. [W3Schools](https://www.w3schools.com/js/js_assignment.asp) provides a list of the various assignment operator that can be used.

## 13. What is the **Unary +** Operator?
The unary plus operator precedes its operand and evaluates to its operand but attempts to convert it into a number, if it isn't already. Check out the [MDN web docs](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Operators/Unary_plus) for more information.
