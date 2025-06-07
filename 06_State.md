# STATE

Why State ?
```jsx
function App() {

  let Fruit = "Apple";
  const changeFruit = () => {
    Fruit = "Banana";
  }

  return (
    <>
      <h3>State in Reactjs</h3>
      <h3>{Fruit}</h3>

      <button onClick={changeFruit}>Change Fruit Name</button>
    </>
  )
}

export default App
```

This will change fruit in backend but won't reflect   
As reacts reflects changes only on re rendring   
React don't give a shit to variable, it needs state

STATE ?  
Container to store data just like variable  
Mutable and dynamic  
We have to import if want to use  
Re renders component automatically unlike variable 

HOOKS ?
Speacial feature for functional component, lets us use react features  
Usually starts from use