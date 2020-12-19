# JavaScript Fundamentals - [Part 3](https://www.theodinproject.com/courses/foundations/lessons/fundamentals-part-3) 

Check out this [MDN document](https://developer.mozilla.org/en-US/docs/Learn/JavaScript/Building_blocks/Functions) on functions and pay special attention to function scope.
```js
function myGreeting() {
  alert('hello world');
}
```

## Anonymous Functions
```js
const myButton = document.querySelector('button');

myButton.onclick = function() {
  alert('hello world');
}
```
An anonymous function won't do anything on its own and is generally used along with an event handler as shown above. You can also assign an anonymous function to be the value of the variable:
```js
const myGreeting = function() {
  alert('hello world');
}
```
This is also known as a **function expression** and unlike function declarations, function expressions are _not hoisted_. This function can be invoked by using the following and effectively gives the function name:
```js
myGreeting();
```
You can also assign the function to be the value of a variable and can be invoked by calling either, `myGreeting();` or `newGreeting();`:
```js
let newGreeting = myGreeting;
```
However, we mainly use anonymous functions to run code in response to an event.

## Function Parameters
These are values that need to be included inside the function parentheses and are sometimes called **arguments**, **properties** and **attributes**.
The browsers built-in `Math.random()` function doesn't require any parameters and returns an random number between 1 and 0.
The `replace()` function, however, requires 2 parameters: the substring to find in the main string, and the substring to replace the string:
```js
let myText = 'I am a string';
let newString = myText.replace('string', 'sausage');
```
When you need to specify multiple parameters, they are separated by commas. Some parameters are optional, and if you don't specify them, the function will adopt some kind of default behaviour. For example, the array `join()` function's parameter are optional:
```js
let myArray = ['I', 'love', 'chocolate', 'frogs'];
let madeAString = myArray.join(' ');
// returns 'I love chocolate frogs'
let madeAString = myArray.join();
// returns 'I,love,chocolate,frogs'
```
If no parameter is included to specify a joining/delimiting character, a comma is used by default.

## Function Scope & Conflicts
The top level outside all your functions is called the **global scope**. Values defined in the global scope are accessible from everywhere in the code. The variables and other things defined inside the function are inside their own separate scope.