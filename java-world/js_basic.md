# Linking JS to HTML:
```html
<script src="script.js"></script>
```

# Logging output for debugging:
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