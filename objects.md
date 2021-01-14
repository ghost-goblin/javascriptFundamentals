# JavaScript - [Objects & Object Constructors](https://www.theodinproject.com/courses/javascript/lessons/objects-and-object-constructors) 

```js
function Book(title, author, pages, read) {
  this.title = title;
  this.author = author;
  this.pages = pages;
  this.read = read;
  
  this.info = function() {
  console.log(title);
  
  };
};

const theHobbit = new Book('Hobbit', 'J.R.R. Tolkien', 182, true);

theHobbit.info();
```
