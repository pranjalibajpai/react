>#  Day 1 - 20/12/20
- ReactDOM.render(What to Show, Where to show)
- Where To Show - HTML element div with id = root
- JSX - Plain HTML in JS File
- Babel - JS Compiler 
```
    import React from "react";
    import ReactDOM from "react-dom";
    ReactDOM.render(<h1>Hello World!</h1>, document.getElementById("root"));

```
-  render can take only single element
- ```ReactDOM.render(<div><h1>Hello World!</h1><p>Hey</p></div>, document.getElementById("root"));```
- In render, js expression (not statement) can be wrapped inside {} ``` Hello {name} ```
- ES6 template literals
  - </h1>HEllo {fname} {lname}</h1>
  - </h1>HEllo `${fname} ${lname}`</h1>
- className instead of class
- change text/javascript to text/JSX
- alt+click -multicursor
- inline styling : style = {JS Object}
```
const customStyle = { color: "blue" };
<h1 style={customStyle}> Hello World! </h1>
```
- Components [Sandbox](
https://codesandbox.io/s/component-forked-s9jrf?file=/src/index.jsx)
 - custom components in pascal case to differentiate from the html elements
 ```
 function Heading(){
 return <h1>HEllo World</h1>
 }
 ...
 <Heading />
 ```
 >#  Day 2 - 21/12/20
 - [Components Practice](https://codesandbox.io/s/react-components-practice-forked-umiw1?file=/src/components/App.jsx)
 - npx create-react-app <name>
   cd <name>
   npm start
 - [Google Keep Clone](https://uyz3m.csb.app/)
 - React Props 
    - different pieces of info on components (custom components custom properties)
```
function Card(props) {
  return (
    <div>
      <h2>{props.name}</h2>
      <img src={props.img} alt="avatar_img" />
      <p>{props.tel}</p>
      <p>{props.mail}</p>
    </div>
  );
}
```
- https://codesandbox.io/s/react-props-forked-ddg7f?file=/src/index.js 
>#  Day 3 - 22/12/20
- [Props Practice] (https://codesandbox.io/s/react-props-practice-forked-zo8ek?file=/src/components/Card.jsx)
- use export before importing
- React Developer Tools
- Map values to components
    - use of key is necessary but key is not a prop, if we want to use this key then make a new prop with same value
```
 {<array>.map(<function>)} //functional programming
 function <name>(item){
    }
```
- [Mapping Components Practice](https://codesandbox.io/s/mapping-components-practice-forked-gh6k5?file=/src/components/App.jsx) | [Emojipedia](https://gh6k5.csb.app/)
- Methods
    - map
    - filter - creates an array for values which return true
        - <array>.filter(function(item){return item>10});
    - reduce
    - find
    - findIndex
>#  Day 4 - 23/12/20 
- Anonymous function
- Arrow functions
```
let newNumbers = numbers.map(function (x) {
  return x * 2;
});
newNumbers = numbers.map((x) => {
  return x * 2;
});
newNumbers = numbers.map((x) => x * 2);
```
    
```
{emojipedia.map((emojiTerm) => (
  <Entry
    key={emojiTerm.id}
    emoji={emojiTerm.emoji}
    name={emojiTerm.name}
    description={emojiTerm.meaning}
  />
))}
```
- [Keeper App Project Part 2](https://codesandbox.io/s/keeper-app-part-2-starting-forked-y88ci)
- Conditional REndering of React Components: because we need an expression rather than statements we have to make use of ternary operators instead of simple if-else
 - [Example](https://codesandbox.io/s/conditional-rendering-forked-dldn9?file=/src/components/App.jsx)
 - && in React => Condition && Expression
    - example x>10 ? A : null is equivalent to x>10 && A 
    - rendering the componenet only when the condition is true
 - [Basic Login Flow](https://codesandbox.io/s/conditional-rendering-practice-forked-p7dlw)
 - State 
    -UI = function(State)
    - Declarative & Imperative Programming
    - React Hooks 
>#  Day 5 - 24/12/20
- React Hooks
    - In order to change the UI, we need to re-render ReactDOM
    - Hook called useState -> use inside a functional component i.e. create a function that renders a component  
    - useState(initial state, function)
    - to get value state[0]
    - now we track the state whenever it gets updated we re-render the components
    - Destructure example 
        - const [red, green, blue] = [1, 2, 3]
        - now we don't need the index to access the elements
```
import React, { useState } from "react";
function App() {
  const [count, setCount] = useState(0);
  function increase() {
    setCount(count + 1);
  }
  function decrease() {
    setCount(count - 1);
  }
  return (
    <div className="container">
      <h1>{count}</h1>
      <button onClick={increase}>+</button>
      <button onClick={decrease}>-</button>
    </div>
  );
export default App;
```
- [Hooks Example](codesandbox.io/s/usestate-hook-forked-vpcf1)
- setInterval(function, time in milliseconds)
- [Get Current Time Hooks Practice](https://codesandbox.io/s/usestate-hook-practice-forked-zei4x)
>#  Day 6 - 26/12/20
- [Event Handling](https://z06b7.csb.app/)
```
<button
style={{ backgroundColor: color }}
onMouseOver={handleOver}
onMouseOut={handleOut}>
const [color, setColor] = useState("white");

function handleOver() {
setColor("black");
}

function handleOut() {
setColor("white");
}
```
- controlled components
 - form input
```
 function handleChange(event){
    setName(event.target.value);
 }
```
 -preventDefault() - prevents default behaviour of elements, in case of button inside form elements it is refresh
 - if using form element use form onSubmit={handleClick} instead of having this on submit button
- Hooks can be used with functional components, we can't use them with class components
- 
