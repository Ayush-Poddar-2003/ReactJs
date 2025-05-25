# JSX
JSX is syntax extension of Js, JavaScriptXML  
Let us write html in js

```jsx
function Welcome(){
    const user = "Ayush";
    return(
        <>
            <h3>I am {user}</h3>
            <h3>Sum of 10+20={10+20}</h3>
            
            <button onClick = {()=>alert("Clicked")}>CLick Me</button>
        </>
    )
}
export default Welcome
```
React can work without JSX too but complexity raises

```jsx
import { createElement, Fragment } from "react";

function Welcome() {
  const user = "Ayush";

  return createElement(
    Fragment,
    null,
    createElement("h3", null, `I am ${user}`),
    createElement("h3", null, `Sum of 10+20=${10 + 20}`),
    createElement(
      "button",
      { onClick: () => alert("Clicked") },
      "Click Me"
    )
  );
}

export default Welcome;
```

## <center> CURLY BRACES

```jsx
function App() {
  const name = "Ayush";
  function callFun(a,b){
    return "Sum is "+(a+b)
  }
  const fruit = (name) =>{
    alert(name)
  }
  const obj={
    name: "Ayush",
    age: 21
  }

  return (
    <>
      <h3>Variable used : {name}</h3>

      Function used : {callFun(60,9)}
      
      <button onClick = {()=>fruit("Apple")}>Click Here</button>

      Object used : {obj.name} {obj.age}
    </>
  )
}

export default App

```