# <center> COMPONENTS ?
  
A JavaScript function that returns JSX   
Same like function, but name starts with **Capital** letter

```jsx
// App.jsx
function Welcome(){ //Welcome is component, name need not same as fileName
  return(
    <div>
      <h1>Hey Buddy</h1>
    </div>
  );
}
export default Welcome;
```
You can then render this inside your main file:
```jsx
//main.jsx
import Apple from './App.jsx' //Any name but location should be correct

createRoot(document.getElementById('root')).render(
  <StrictMode>
    <Apple />   //Jo import kra whi use kro
  </StrictMode>,
)
```
## <center> TYPES
### 1. Functional Component (Modern & preferred way)
```JSX
function Welcome(props) {
  return <h1>Hello, {props.name}</h1>;
}
```
#### 1.2. Arrow Function Component
```JSX
const Welcome = ({ name }) => <h1>Hello, {name}</h1>;
```
### 2. Class Component (Older)
```jsx
class Welcome extends React.Component {
  render() {
    return <h1>Hello, {this.props.name}</h1>;
  }
}
```


## <center>Multiple Components
```jsx
function App(){
  return(
    <div>
      <h1>Hey Buddy</h1>
      <Fruit></Fruit> //other components to be exported
      <Color></Color>
    </div>
  )
}

function Fruit(){
  return (
    <h1>Apple</h1>
  )
}

function Color(){
  return (
    <h1>Red</h1>
  )
}

export default App;
```