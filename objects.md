# JavaScript - [Objects & Object Constructors](https://www.theodinproject.com/courses/javascript/lessons/objects-and-object-constructors)

```js
function Book(title, author, pages, read) {
  this.title = title;
  this.author = author;
  this.pages = pages;
  this.read = read;
  
  this.info = function() {
  return `${title} by ${author}, ${pages} pages, read: ${read}`;  
  };
};

const theHobbit = new Book('The Hobbit', 'J.R.R. Tolkien', 182, true);

console.log(theHobbit.info());
```
> It's _always_ better to `return` things in functions!