# PROPS 
Props (short for properties) are read-only inputs passed from a parent component to a child component.

```jsx
// App.jsx

function App(){
  return(
      <User name="Ayush Poddar" age="22" /> 
  )
}
export default App
```

```jsx
// User.jsx
function User(param) { //As an object
    return (
        <>
            <h1>{param.name}</h1>
            <h1>{param.age}</h1>
        </>
    )
}
//OR
function User( {name, age} ) { //Directly, destructuring
    return (
        <>
            <h1>{name}</h1>
            <h1>{age}</h1>
        </>
    )
}
```

## <center>Passing pre made variable

```jsx
//App.jsx
function App()
{
  let userName = "Aditi";
  let age = 21;
  
  return(
      <User name={userName} age={age} />
  )
}
export default App
```

## <center> DEFAULT PROPS
```jsx
//DEFAULT PARAMETER
function User( {name="Ayush"}){
    return (
            <h1>Hii {name}</h1>
    )
}
```