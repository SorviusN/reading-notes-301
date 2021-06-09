

## React Docs - lists and keys
### What does .map() return?
.map() returns a new array with the information that was manipulated inside the arrow function of the array that .map is being called under.
### If I want to loop through an array and display each value in JSX, how do I do that in React?
We can build a collection of elements and include them in JSX using curly braces. 
``` js
const nums = [1, 2, 3, 4, 5];
const listOfNums = nums.map(num => 
  <li>{num}</li>
);
//afterward, render each of the nums to the dom inside of a UL.
ReactDOM.render(
  <ul>{listOfNums}</ul>, // the list we created above from map is being displayed inside of the UL.
  document.getElementById('root')
);
```
### Each list item needs a unique KEY.
### What is the purpose of a key?
"Keys help React identify which items have changed, are added, or are removed". - quoted directly from https://reactjs.org/docs/lists-and-keys.html
## The spread Operator

### What is the spread operator?
"JavaScript, spread syntax refers to the use of an ellipsis of three dots (…) to expand an iterable object into the list of arguments". - quote from https://medium.com/coding-at-dawn/how-to-use-the-spread-operator-in-javascript-b9e4a8b06fab 
### List 4 things that the spread operator can do.
- Copy an array exactly.
- Concatenate or combine arrays
- use math functions with in the array for each individual component.
- Add to a state in react.

### Give an example of using the spread operator to combine two arrays.
``` js
const myArr = [1, 2, 3]
const yourArr = [a, b, c]
const theirArr = [...myArr...yourArr]
console.log(...theirArr) // this would be [1 2 3 a b c].
```
### Give an example of using the spread operator to add a new item to an array.
``` js
const fruits = ['🍏','🍊','🍌','🍉','🍍']
const moreFruits = [...fruits];
console.log(moreFruits) // Array(5) [ "🍏", "🍊", "🍌", "🍉", "🍍" ]
fruits[0] = '🍑'
console.log(...[...fruits,'...',...moreFruits]) //  🍑 🍊 🍌 🍉 🍍 ... 🍏 🍊 🍌 🍉 🍍### Give an example of using the spread operator to combine two objects into one.
```

### In the video, what is the first step that the developer does to pass functions between components?
Create the function inside of the parent component - which is where we will be changing the state.
### In your own words, what does the increment function do?
The increment function, in the case of the video, adds 1 to the count of whichever react component it is attached to.
``` js 
class App extends Component {
  constructor() {
    super();
    this.state = { //setting the initial state of the parent component class.
      people: [
        {name: 'Jona', count: 0},
        {name: 'Melanie', count: 0}
      ]
    }}

    render() {
      return (
        <div className="App">
          {this.state.people.map( person => { // creating the Person component and initializing all of the values to whatever we say at the initial state.
            <Person name={person.name}
            key={person.name}
            count={person.count} />
            })}
        </div>
      );
    }
  }
```
### How can you pass a method from a parent component into a child component?
Fortunately, you're able to give the child component the function that it can call to let the parent know that it was updated.
### How does the child component invoke a method that was passed to it from a parent component?
When the child is given a method to call from the parent, it is usually invoked by some sort of event listener - the child then invokes the function (without parentheses).


## Reading

### Lifting state up
Several components need to reflect the same changing data - lifting the shared state up to their closest common ancestor can be best.
## Things I want to know more about
Learning more about the functionality of Keys would be nice.
Having real life practice with the spread operator would be nice as well.


