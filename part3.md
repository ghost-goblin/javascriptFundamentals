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
