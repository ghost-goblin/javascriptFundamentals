# JavaScript Fundamentals - [Dom Manipulation](https://www.theodinproject.com/courses/foundations/lessons/dom-manipulation)
The **Document Object Model** is a tree-like representation of the contents of a webpage - a tree of “nodes” with different relationships depending on how they’re arranged in the HTML document.

![Document Object Model](https://www.w3schools.com/js/pic_htmltree.gif)

```html
<div id="container">              <!-- Parent -->
  <div class="display"></div>     <!-- Children & Siblings -->
  <div class="controls"></div>
</div>
```
## Tageting Nodes with Selectors
The following selectors to refer to `<div class="display"></div>` through a combination of CSS-style selectors and relationship properties:
* div.display
* .display
* #container > .display
* div#container > div.display

## Relational Selectors
```js
const container = document.querySelector('#container'); //Select the #container div
console.dir(container.firstElementChild);               //Select the first child of #container (.display)
const controls = document.querySelector('.controls');   //Select the .controls div
console.dir(controls.previousElementSibling);           //Selectes the prior sibling (.display)
```

## What is DOM in relation to a webpage?
## What's the difference between a "node" and an "element"?
## How do you target nodes with "selectors"?
## What are the basic methods for finding/adding/removing and altering DOM nodes?
## What is the difference between a "nodelist" and an "array of nodes"?
## How do "events" and "listeners" work? What are three ways to use events in your code?
## How does "bubbling" work?
