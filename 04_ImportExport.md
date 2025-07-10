# IMPORT EXPORT ✅

We can't make every component in a single file, like everything in app.jsx    
We can, but not feasible and professional, imagine 1000s of lines of code.

Let's Make a Custom component and learn exporting, importing
```jsx
//CustomComponent.jsx

//Method 1 to export
function Custom(){
    return(
        <div>
            <h1>Customised Component exporting to App.jsx</h1>
        </div>
    )
}
export default Custom; 
```
```JSX
//Method 2 direct: { } While importing
export function Custom2(){
    return(
        <div>
            <h1>Customised Component 2</h1>
        </div>
    )
}
```

```jsx
//App.jsx, Importing custom components here
import Custom, {Custom2} from "./CustomComponent";

function App() {
  return(
    <div>
      <h1>Hey Importing in this App.jsx file</h1>
      <Custom/>
      <Custom2/>
    </div>
  )
}

export default App;
```

```jsx
// main.jsx
import App from './App.jsx'

createRoot(document.getElementById('root')).render(
  <StrictMode>
    <App />
  </StrictMode>,
)
```
