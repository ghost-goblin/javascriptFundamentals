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

Here is a link to the [Hacker Noon](https://medium.com/hackernoon/why-you-shouldnt-use-var-anymore-f109a58b9b70) on why we shouldn't use var anymore.

## 4. What are the rules for naming variables?
- ⚠️ Declaring a variable twice triggers an error
- The name must contain only letters, digits, or the symbols `$` and `_`
- The first character must not be a digit
- Case matters!
- `let`, `class`, `return`, and `function` are reserved and cannot be used as variable names

5. What are operators, operands, and operations?

6. What is concatenation and what happens when you add numbers and strings together?

7. What are the different types of operators in JavaScript?

8. What is the difference between == and ===?

9. What are operator precedence values?

10. What are the increment/decrement operators?

11. What is the difference between prefixing and post-fixing them?

12. What are assignment operators?

13. What is the **Unary +** Operator?
