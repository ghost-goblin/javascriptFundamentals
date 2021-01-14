# JavaScript - [Objects & Object Constructors](https://www.theodinproject.com/courses/javascript/lessons/objects-and-object-constructors) 

```js
function Book(title, author, pages, read) {
  this.title = title;
  this.author = author;
  this.pages = pages;
  this.read = read;
  
  this.info = function() {
  console.log(`${title} by ${author}, ${pages} pages, read: ${read}`);
  
  };
};

const theHobbit = new Book('The Hobbit', 'J.R.R. Tolkien', 295, true);

theHobbit.info();
```
