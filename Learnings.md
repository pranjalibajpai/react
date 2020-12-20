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
- Components [Sandbox]https://codesandbox.io/s/component-forked-s9jrf?file=/src/index.jsx)
 - custom components in pascal case to differentiate from the html elements
 ```
 function Heading(){
 return <h1>HEllo World</h1>
 }
 ...
 <Heading />
 ```
