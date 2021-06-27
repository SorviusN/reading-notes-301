# Reading Notes 9

## Functional Programming Concepts

### What is functional programming?
- Functional programming is a way of thinking about software construction by creating pure functions. It avoids shared state/mutable data observed in OOP.

### What is a pure function and how do we know if something is a pure function?
A pure function is "well defined", meaning that it it will return the same output every time.

### What are the benefits of a pure function?
It produces not side effects and gives consistent results. Additionally, they are very independent and do not rely on outside state(s) and as such, they are immune to a lot of bugs that shared immutable states have.

### What is immutability?
An immutable value is one that can never change over time. While you cannot change the value, you can perform functions with it and return new values.

### What is Referential transparency?
Referential transparency means that a function call can be replaced by its value or another referentially transparent call with the same result
### Reference Article - https://medium.com/javascript-scene/master-the-javascript-interview-what-is-a-pure-function-d1c076bec976

## Node JS Tutorial for Beginners #6

### What is a module?
A module is a way to organize our Node JS code by separating each function that the app redirects to. Think:

``` js
let bookHandlers = require('./bookHandlers'); //creating a variable that has the route of bookHandlers in your directory.

app.get('/', bookHandlers.getBook); // calling a specific module within the bookHandlers directory.
```
### What does the word ‘require’ do?
require is very similar to "import" on the front end. It lets your current file access the data inside of 'require'.

### How do we bring another module into the file the we are working in?
See the js example above for how to import modules into another file.

### What do we have to do to make a module available?
We need to explicitly say what part of the module we want other programs to see (privacy in files).

``` js
module.exports = getBook; // this would allow our server.js file to access the getBook function of the module.
```
