# •	Basic React Component:
```jsx (JavaScript XML) 
function App(){
    return <h1></h1>;
}
export default App;
```

## Functional Component function Greeting(){}
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

# useEffect Hook (Side Effects & API Calls) useEffect({return()},[]);
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
## Show or Hide Elements
```jsx
 function Toggle() {
  const [isVisible, setIsVisible] = useState(true);

  return (
    <div>
      <button onClick={() => setIsVisible(!isVisible)}>Toggle</button>
      {isVisible && <p>This text is visible</p>}
    </div>
  );
}
```
## in JavaScript, the && operator only evaluates the right-hand side if the left-hand side is true.
true && <p>...</p> → shows the paragraph

false && <p>...</p> → shows nothing

## Using Ternary Operator
```jsx
 
{isVisible ? <p>Visible</p> : <p>Hidden</p>}
```

# Lists & Keys
## Rendering Lists in React to display multiple elements (like a list of items), you often use .map()
###  .map()-Loops through arrays and returns JSX
### key={index}- Unique ID for React to track list items
```jsx 
function List() {
  const items = ["Apple", "Banana", "Mango"];

  return (
    <ul>
      {items.map((item, index) => <li key={index}>{item}</li>)}
    </ul>
  );
}
```


# React Router (Navigation Between Pages)
## Setting Up Routes:
```jsx
import { BrowserRouter as Router, Route, Routes, Link } from "react-router-dom";

function Home() {
  return <h1>Home Page</h1>;
}

function About() {
  return <h1>About Page</h1>;
}

function App() {
  return (
    <Router>
      <nav>
        <Link to="/">Home</Link>
        <Link to="/about">About</Link>
      </nav>
      <Routes>
        <Route path="/" element={<Home />} />
        <Route path="/about" element={<About />} />
      </Routes>
    </Router>
  );
}
```


# Context API (Global State Management Without Redux)
## Avoids prop drilling by passing data globally.
```jsx
import { createContext, useContext, useState } from "react";

const ThemeContext = createContext();

function ThemeProvider({ children }) {
  const [theme, setTheme] = useState("light");
  return (
    <ThemeContext.Provider value={{ theme, setTheme }}>
      {children}
    </ThemeContext.Provider>
  );
}

function ToggleTheme() {
  const { theme, setTheme } = useContext(ThemeContext);
  return (
    <button onClick={() => setTheme(theme === "light" ? "dark" : "light")}>
      Toggle Theme
    </button>
  );
}

function App() {
  return (
    <ThemeProvider>
      <ToggleTheme />
    </ThemeProvider>
  );
}
```


# Deploying React App
## Build App:
```bash
 npm run build

#	Deploy with Vercel:
npm install -g vercel

# Deploy with GitHub Pages:
npm install gh-pages --save-dev
```

### Add to package.json:
```json
 
"homepage": "https://yourusername.github.io/your-repo",
"scripts": {
  "predeploy": "npm run build",
  "deploy": "gh-pages -d build"
}
```

### Deploy with:
```bash
 npm run deploy
```