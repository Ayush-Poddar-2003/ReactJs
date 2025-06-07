# <center> COMPONENTS ?

Components allow to break down complex UI into smaller manageable pieces.
A React component is a JavaScript function that returns JSX   
Components let you reuse UI.  
Same like function, but name starts with **Capital** letter

---
Single Component
```jsx
// App.jsx
function Welcome(){
  return(
    <div>
      <h1>Hey Buddy</h1>
    </div>
  );
}
export default Welcome;

// You can then render this inside your main file:

//main.jsx
import { StrictMode } from 'react'
import { createRoot } from 'react-dom/client'
import './index.css'
import App from './App.jsx' 

createRoot(document.getElementById('root')).render(
  <StrictMode>
    <App />
  </StrictMode>,
)
```

Multiple Components
```jsx
function App(){
  return(
    <div>
      <h1>Hey Buddy</h1>
      <Fruit></Fruit>
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