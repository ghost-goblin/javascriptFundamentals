# JavaScript - [Objects & Object Constructors](https://www.theodinproject.com/courses/javascript/lessons/objects-and-object-constructors) 

```js
function Book(title, author, pages, read) {
	this.title = title;
  this.author = author;
  this.pages = pages;
  this.read = read;
  
  this.bookInfo = function() {
  console.log(title);
  
  };
};

const addBook = new Book('Hobbit', 'J.R.R. Tolkien', 182, true);

addBook.bookInfo();
```
