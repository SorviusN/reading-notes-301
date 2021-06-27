# Reading Notes 10

## Understanding the JS Call Stack

### What is a ‘call’?
At the most basic level, a call stack is a data structure that uses the Last In, First Out (LIFO) principle to temporarily store and manage function invocation (call)
### How many ‘calls’ can happen at once?
only one call may happen at any given time in a single-threaded program.
### What does LIFO mean?
"Last in, First out"
### Draw an example of a call stack and the functions that would need to be invoked to generate that call stack.
/Users/sorviusn/Downloads/QgR2uIk7tW0YNz0Xm8g0jAPeRFI0e4sCejsv.png
### What causes a Stack Overflow?
A stack overflow occurs when there is a recursive function present that does not have an exit point.


## JS error messages

### What is a ‘refrence error’?
This is as simple as when you try to use a variable that is not yet declared you get this type os errors.
``` js
console.log(foo) // Uncaught ReferenceError: foo is not defined
```
### What is a ‘syntax error’?
this occurs when you have something that cannot be parsed in terms of syntax, like when you try to parse an invalid object using JSON.parse.
``` js
JSON.parse( {'foo': 'bar'} ) // Uncaught SyntaxError: Unexpected token o in JSON at position 1
```
### What is a ‘range error’?
Try to manipulate an object with some kind of length and give it an invalid length and this kind of errors will show up
``` js
var foo= []
foo.length = foo.length -1 // Uncaught RangeError: Invalid array length
```
### What is a ‘type error’?
this types of errors show up when the types (number, string and so on) you are trying to use or access are incompatible, like accessing a property in an undefined type of variable.
``` js
var foo = {}
foo.bar // undefined
foo.bar.baz // Uncaught TypeError: Cannot read property 'baz' of undefined
```
### What is a breakpoint?
A place to stop the code for debugging.
### What does the word ‘debugger’ do in your code?
it creates a breakpoint in the code.

### Resource: https://www.freecodecamp.org/news/understanding-the-javascript-call-stack-861e41ae61d4/
### https://codeburst.io/javascript-error-messages-debugging-d23f84f0ae7c
