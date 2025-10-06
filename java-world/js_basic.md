# Linking JS to HTML:
```html
<script src="script.js"></script>
```

# Loggin output for debugging:
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

# •	Arrow function (modern syntax):
```js
const greet = () => {};

const greet = (name) => 'Hello, ${name}';
console.log(greet("Polash"));
```