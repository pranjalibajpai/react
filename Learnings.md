## Day 1 20/12/20
- REACTDOM.render(What to Show, Where to show)
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
- 
