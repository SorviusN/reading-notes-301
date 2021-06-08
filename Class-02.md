# Reading Notes 2

### Based off the diagram, what happens first, the ‘render’ or the ‘componentDidMount’?
'render' first, componentDidMount next.

### What is the very first thing to happen in the lifecycle of React?
The mounting Phase (constructor).

### Question 3 Order:
constructor, render, componentDidMount, UNSAFE_componentWillMount, React updates.

### What does componentDidMount do?
Invoked immediately after a component is mounted. It renders information right after that point (such as a console.log.).

### What types of things can you pass in the props?
They are similar to arguments in a function. Think of them as parameter - so pass in information that you'd like to render or use in your component.

### What is the big difference between props and state?
props are passed into a component while state is handled inside of the component itself. Therefore, props must be updated outside of the component while state is handled inside.

### When do we re-render our app?
When you change the state, you'll re-render the component as it is inside. If you want to change something and re-render, use the state. 
With props, however, you can change the data easily and simply as it is outside of the component itself. The component only displays the data.

### What are some examples of things that we could store in state?
We can use state inside of a form. Input, Checkbox, select must be updated and re-rendered, therefore state is best. Updating a count could also be used, as every time
we click the count we want to be able to add 1 and render the component again.

## Notes

### taken directly from State and Lifecycle - React: 

You can convert a function component like Clock to a class in five steps:
Create an ES6 class, with the same name, that extends React.Component.
Add a single empty method to it called render().
Move the body of the function into the render() method.
Replace props with this.props in the render() body.
Delete the remaining empty function declaration.
``` js
class Clock extends React.Component {
  render() {
    return (
      <div>
        <h1>Hello, world!</h1>
        <h2>It is {this.props.date.toLocaleTimeString()}.</h2>
      </div>
    );
  }
}
```
Clock is now defined as a class rather than a function.
The render method will be called each time an update happens, but as long as we render <Clock /> into the same DOM node,
only a single instance of the Clock class will be used. This lets us use additional features such as local state and lifecycle methods.

### Passing Arguments to Event Handlers
Inside a loop, it is common to want to pass an extra parameter to an event handler. For example, if id is the row ID, either of the following would work:
``` js
<button onClick={(e) => this.deleteRow(id, e)}>Delete Row</button>
<button onClick={this.deleteRow.bind(this, id)}>Delete Row</button>
```
The above two lines are equivalent, and use arrow functions and Function.prototype.bind respectively.
In both cases, the e argument representing the React event will be passed as a second argument after the ID. With an arrow function, we have to pass it explicitly, but with bind any further arguments are automatically forwarded.
