# Linking JS to HTML:
```html
<script src="script.js"></script>
```

# Logging output for debugging: console.log() similar to print() in python
```js
console.log("hello, js");
```

# Varialbes
```js
let name = "Polash"; // Can be reassigned
const name = 38; // Cannot be reassigned
var city = "Dhaka"; // Older way (avoid using var)
```

# Data Types & Operators
## Primitive Types: string, number, boolean, null, undefined, symbol, bigint
### Operators:
o	Arithmetic: +, -, *, /, %, **
o	Comparison: ==, ===, !=, !==, >, <, >=, <=
o	Logical: &&, ||, !

```js
let x = 5;
let y = "5";
console.log(x==y); // true (loose comparision)
console.log(x===y) // false (strict comparison)
```

# Function
```js
function greet() {
    return 
};

// regular funciton
function greet(name) {
    return "Hello" + name;
};
console.log(greet("Polash"));
```

# Arrow function (modern syntax):
```js
const greet = () => {};

const greet = (name) => 'Hello, ${name}';
console.log(greet("Polash"));
```


# Control flow (Loops & Conditions)

## if statement
```js
let age = 25;
if () {

} else {    

}

e.g 
let age = 20;
if (age >= 18) {
    console.log("You are an adult");
} else {
    console.log("You are minor");
}
```

## Loops
### for loops
```js
for () {

}

e.g 
for (let i=1; i <= 5; i++) {
    console.log(i);
}
```

### while loop
```js
while (){

}

e.g 
let i =1;
while (i<=5;){
    console.log(i);
    i++;
}
```

# Arrays (Lists of data)
```js
let fruits = ["Apple", "Banana", "Mango"];
console.log(fruits[1]);
```

## Array methods
```js
fruits.push("Orange"); // Add at the end
fruits.pop("Orange"); // Remove last item
fruits.unshift("Orange") // add at the beginning
fruits.shift("Orange") // Remove first item
```

# Objects (Key-Value Pairs) like dict in python
```js
let person = {
    name : "Polash",
    age : 40,
    city : "Dhaka",
};
console.log(person.name); // "Polash"
```


# DOM Manipulation (Interacting with HTML)
```js
//Selecting elements:
let heading = document.querySelector("h1");
console.log(heading.innerText);

//Changing text:
heading.innerText = "New Title";

//Changing styles:
heading.style.color = "blue";

//Handling events:
document.querySelector("button").addEventListener("click", () => {
  alert("Button clicked!");
});
```



# Error Handling (Try-Catch Block- Handling errors gracefully)
```js
try{

} catch (){

}

e.g. 
try {
    let result = 10/0;
    console.log(result);
} catch (error){
    console.log("An error occoured:" error);
}
```


# Asynchronous JavaScript (Promises & Fetch API)
## Timeout Example:
```js
setTimeout (() => {
    console.log("Execute after 2 seconds");
}, 2000); 

```

##  Fetching Data (API Calls) fetch().then().then().catch()
```js
fetch("https://jsonplaceholder.typicode.com/posts/1")
  .then(response => response.json())
  .then(data => console.log(data))
  .catch(error => console.error("Error:", error));
```


## Async/Await (Modern Syntax) async function fetchData(){try{respone, data}catch{}}fetchData();
```js
async function fetchData() {
  try {
    let response = await fetch("https://jsonplaceholder.typicode.com/posts/1");
    let data = await response.json();
    console.log(data);
  } catch (error) {
    console.error("Error:", error);
  }
}
fetchData();
```


