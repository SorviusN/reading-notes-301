#Reading-Notes 301

## Component based architecture

### What is a component?
A modular, portable, replaceable and reusable set of well-defined functionalities
that encapsulates its implementation and exporting it as a higher-level interface.

### What are the characteristics of a componenet?
- Reusability
- Replaceable
- Not context specific
- Extensible
- Encapsulated
- Independent: Components are designed to have minimal dependencies on differing components.

### What are the advantages of using componenet based architecture?
We are ble to break our software system into reusable, cohesive component units that interact with each other.

## What is Props and how to use it in react

### What is props short for?/How are they use?
Properties, being used for passing data from one component to another.

### What is the flow of props?
Being passed in uni-directional flow (parent to child).

## Hello World

smallest React example:
``` js
ReactDOM.render(
  <h1>Hello, world!</h1>,
  document.getElementById('root')
);
```

