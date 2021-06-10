# Reading Notes class 04

Quoted from - https://reactjs.org/docs/forms.html
## FORMS

``` 
<form> HTML
  <label>
    Name:
    <input type="text" name="name" />
  </label>
  <input type="submit" value="Submit" />
</form>

```
### What is a ‘Controlled Component’?
In HTML, form elements such as input, textarea, and select typically maintain their own state and update it based on user input. In React, mutable state is typically kept in the state property of components, and only updated with setState().
An input whose value is controlled by React in a manner that changes based on what is input.
###Should we wait to store the users responses from the form into state when they submit the form OR 
### should we update the state with their responses as soon as they enter them? Why.
Example:
``` js
class NameForm extends React.Component {
  constructor(props) {
    super(props);
    this.state = {value: ''};

    this.handleChange = this.handleChange.bind(this);
    this.handleSubmit = this.handleSubmit.bind(this);
  }

  handleChange(event) {
    this.setState({value: event.target.value});
  }

  handleSubmit(event) {
    alert('A name was submitted: ' + this.state.value);
    event.preventDefault();
  }

  render() {
    return (
      <form onSubmit={this.handleSubmit}>
        <label>
          Name:
          <input type="text" value={this.state.value} onChange={this.handleChange} /> // setting value of text to value of the class constructor. When inputting, we have onChange which updates the 
          // event.target.value
        </label>
        <input type="submit" value="Submit" />
      </form>
    );
  }
}
```
Example above shows that we are updating the state of the class when changing the text input - therefore we should update the state with their responses as soon as they enter them.
This shows that we would like more reactivity in our site - the second answer is better.

### How do we target what the user is entering if we have an event handler on an input field?
When you need to handle multiple controlled input elements, 
you can add a name attribute to each element and let the handler function choose what to do based on the value of event.target.name.

## Ternary Operators

### Why would we use a ternary operator?

### Rewrite the following statement using a ternary statement:
``` js 
if(x===y){
 console.log(true);
  } else {
 console.log(false);
  }
// REWRITTEN:

let answer = (x === y ? console.log(true) : console.log(false));
```

## Things I want to know more about

Ternary operators in real life examples as well as using controlled components in forms with real life examples.
