# •	Basic React Component:
```jsx (JavaScript XML) 
function App(){
    return <h1></h1>;
}
export default App;
```

## Functional Component function Greeting({}){}
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
<UserProfile name = "Polash" age = {38}; />;
```

## State: State allows components to manage data.
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
```
## Form Handling:
```jsx
 
function Form() {
  const [name, setName] = useState("");

  const handleSubmit = (e) => {
    e.preventDefault();
    alert(`Hello, ${name}!`);
  };

  return (
    <form onSubmit={handleSubmit}>
      <input type="text" onChange={(e) => setName(e.target.value)} />
      <button type="submit">Submit</button>
    </form>
  );
}
```

# useEffect Hook (Side Effects & API Calls)
## Runs after component renders
```jsx
 
import { useState, useEffect } from "react";

function FetchData() {
  const [data, setData] = useState([]);

  useEffect(() => {
    fetch("https://jsonplaceholder.typicode.com/posts")
      .then(response => response.json())
      .then(data => setData(data));
  }, []);

  return (
    <ul>
      {data.slice(0, 5).map(post => <li key={post.id}>{post.title}</li>)}
    </ul>
  );
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
```
- Data fetching in useEffect
- Event handlers for user interactions
- Conditional rendering
```

# Conditional Rendering
•	Show or Hide Elements
jsx
 
function Toggle() {
  const [isVisible, setIsVisible] = useState(true);

  return (
    <div>
      <button onClick={() => setIsVisible(!isVisible)}>Toggle</button>
      {isVisible && <p>This text is visible</p>}
    </div>
  );
}
•	Using Ternary Operator
jsx
 
{isVisible ? <p>Visible</p> : <p>Hidden</p>}
