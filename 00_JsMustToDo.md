# Js Essentials

```js
var arr = [1,2,3,4]
var arr2 = arr; //gets copied by reference

console.log(arr);  //[ 1, 2, 3, 4 ]
console.log(arr2); //[ 1, 2, 3, 4 ]

arr2.pop(); //If changes made to new

console.log(arr);  //[ 1, 2, 3 ] //old gets changed too
console.log(arr2); //[ 1, 2, 3 ]
```

### <center>SPREAD OPERATOR
```js
var state = [1,2,3,4];
state.pop(); //Not allowed in react
//Dont change previous value rather assign new value

var state = [1,2,3,4];
var copy = [...state]; //SPREAD OPERATOR used to copy

copy.pop(); //changes made

console.log(state); //[ 1, 2, 3, 4 ] //unaffected
console.log(copy); //[ 1, 2, 3 ]
```
Real life example
```js
var state = {name: "Ayush", age: 21}
var copy = {...state}

copy.name = "Aditi"; 
state = copy;

console.log(state); //{ name:'Aditi', age:21 }
```

## <center> DESTRUCTURING

```js
var obj = {name: "Ayush", age: 21}

// Rather than using obj.age 'n' times
const {age} = obj; //as a alias of obj.age

console.log(age); //21
```

```js
var obj = {
    name: "String",
    social: {
        facebook: {
            first: "Ayush",
            second: "Aditi"
        }
    }
}
//obj.social.facebook.second RATHER
const {second} = obj.social.facebook;
console.log(second); //Aditi
```
Let's take array example
```js
var arr = [12, function(){}, 13]
const [f, ,s] = arr;
console.log(f,s); //12 13
```

## <center> IMPORT EXPORT
Alag Alag components ko export krkr main file me import

navbar - export  
sidebar - export  
cart - export  
main - import navbar, sidebar, cart

```js
export function ABC()
{
}
//OR
function ABC(){}
default export ABC()

//Where we are importing
import {ABC} from Src
```

## <center>ARROW FUNCTIONS
```js
const ABC = () => {
    //Code
}

//Parameter
const ABC = (a) => {
    console.log(a);
}
const ABC = a => {
    console.log(a);
}

//Implicit return
const ABCD = () => 12;
//This auto returns 12

//What if we need to return object
const ABCD = () => (
    {name: "Ayush"}
);
```

## <center>ARRAY FILTER
Both returns a new array
