# JavaScript Fundamentals - [Dom Manipulation](https://www.theodinproject.com/courses/foundations/lessons/dom-manipulation)
## What is DOM in relation to a webpage?
The **Document Object Model** is a tree-like representation of the contents of a webpage - a tree of “nodes” with different relationships depending on how they’re arranged in the HTML document.

![Document Object Model](https://www.w3schools.com/js/pic_htmltree.gif)

## What's the difference between a "node" and an "element"?
Elements are just HTML elements, such as a div, span, or body tag. Generally when you are working with the DOM you will be working with elements since most often you want to interact with HTML elements. Nodes are the more generic version of an element. A node could be an HTML element, but it could also be anything else in an HTML document, such as text or comments. 

## How do you target nodes with "selectors"?
When traversing the DOM sometimes you will get returned a collection of elements/nodes (querySelector, children). This will either be an HTMLCollection or a NodeList.
Things like forEach, map, and reduce are not available on an HTMLCollection.
## What are the basic methods for finding/adding/removing and altering DOM nodes?
```html
<div id="container">              <!-- Parent -->
  <div class="display"></div>     <!-- Children & Siblings -->
  <div class="controls"></div>
</div>
```
#### Tageting Nodes with Selectors
The following selectors to refer to `<div class="display"></div>` through a combination of CSS-style selectors and relationship properties:
* div.display
* .display
* #container > .display
* div#container > div.display

#### Relational Selectors
```js
const container = document.querySelector('#container'); //Select the #container div
console.dir(container.firstElementChild);               //Select the first child of #container (.display)
const controls = document.querySelector('.controls');   //Select the .controls div
console.dir(controls.previousElementSibling);           //Selectes the prior sibling (.display)
```

## What is the difference between a "nodelist" and an "array of nodes"?
A NodeList on the other hand can contain any type of node including elements. NodeLists are also similar to arrays, but they again lack most higher order functions. The only higher order function on a NodeList is the forEach function. Some examples of methods that return NodeLists are querySelectorAll and childNodes.

## How do "events" and "listeners" work? What are three ways to use events in your code?
```js
// method 1
<button onclick="alert('Hello World')">Click Me</button>

//method 2
const btn = document.querySelector('#btn');
btn.onclick = () => alert("Hello World");

//method 3
const btn = document.querySelector('#btn');
btn.addEventListener('click', () => {
  alert("Hello World");
});
```

## How does "bubbling" work?
[RIP Tutorial](https://riptutorial.com/dom/example/1344/event-bubbling-and-capturing)
