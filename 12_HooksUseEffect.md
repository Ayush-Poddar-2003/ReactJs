# HOOKS
In old React version, we were using class-based components.
Now class-based components are not much used in React.
So to achieve state, lifecycle, other features in functional components, we use hooks.

Hooks were introduced to replace class components with functional components using special functions.

1. useState
2. useEffect

# <CENTER> USE EFFECT
- Remove side effect inside component
- Use to fetch data
- as life cycle methods
- controls side affects of use state

SYNTAX

```jsx
import { useState } from "react";

function App()
{
  const [counter, setCounter] = useState(0);

  function callOnce(){
      alert("callOnce Function Called")
  }
  callOnce();

  return(
      <button onClick = {() => setCounter(counter+1) }> Counter {counter} </button>
  )
  // Everytime setcounter is updated 
  // callOnce function is run 
  // Bcoz state is change, hence rerenders
  // But if we want to execute it only once?
}

export default App;
```
Let say we have 2 buttons, we want everytime function run with only one button not with other
```jsx
import { useEffect, useState } from "react";

function App()
{
  const [counter, setCounter] = useState(0);
  const [data, setData] = useState(0);
 
  useEffect(()=>{
    callOnce(); 
  }, [counter] )  //Bs counter update hone pr chalega

  function callOnce(){
    alert("callOnce Function Called")
  }

  return(
    <div>
      <button onClick = {() => setCounter(counter+1)}> Counter {counter} </button>

      <button onClick = {() => setData(data+1)}> Data {data} </button>
    </div>
  )
}
export default App;
```

# HANDLING PROPS SIDE EFFECTS
