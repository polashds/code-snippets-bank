# •	Basic React Component:
```jsx (JavaScript XML) 
function App(){
    return <h1></h1>;
}
export default App;
```

## Functional Component 
```jsx
function Greeting({name}) {
    return <h1>Hello {name}</h1>;
}
```
## Use a Component in App.js
```jsx
function App(){
    return <Greeting name="Polash"/>;
}
```

## Proops (passing data)
```jsx
function UserProfile({name, age}){
    return <p>{name} is {age} years old!</p>
}
<UserProfile name = "Polash" age = 38; />;
```

## State: •	State allows components to manage data.
### React re-renders the component when state updates.
### const [count, setCount] = useState();
```jsx
import {useState} from "react";
function Counter (){
    const [count, setCount] = useState();
    return (
        <div>
            <p>Count : {count}</p>
            <button onClick={() => setCount(count + 1)}>Increment</button>
        </div>
    )
}
```

## Handling Events in React
### Click Event: const handleClick = () => alert();
```jsx
function Button(){
    const handleClick = () => alert("Button clicked!);
    return <button onClick= {handleClick}>Click Me</button>
}



**React Hooks Cheat Sheet:**
```markdown
# React Hooks Quick Reference
```js
## useState
const [state, setState] = useState(initialValue);

## useEffect
useEffect(() => {
    // Side effect code
    return () => cleanup(); // Optional cleanup
}, [dependencies]); // Empty array = run once
```
## Common Patterns
- Data fetching in useEffect
- Event handlers for user interactions
- Conditional rendering
```

