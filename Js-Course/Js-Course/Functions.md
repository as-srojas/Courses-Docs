### Functions

In JavaScript, functions are blocks of reusable code that can be invoked (called) with specific arguments. They are fundamental building blocks for organizing and reusing code.

#### Declaring Functions:

Functions in JavaScript can be declared using the `function` keyword followed by a name, a list of parameters (enclosed in parentheses), and a block of code (enclosed in braces).

```javascript
//Example function
function greet(name) {
    return "Hello, " + name + "!";
}
```
#### Invoking Functions:

Functions are invoked using their name followed by parentheses containing any arguments needed for the function.

```javascript
//Invoking a function
let message = greet("John");
console.log(message);
```

### Anonymous Functions and Arrow Functions

Anonymous functions are functions without a name. They can be assigned to variables or passed as arguments to other functions. Arrow functions are a concise way to write anonymous functions introduced in ES6.
Anonymous Functions:

```javascript
//Anonymous function
let greet = function(name) {
    return "Hello, " + name + "!";
};
```
#### Arrow Functions:

Arrow functions provide a more concise syntax for writing functions, especially for one-liner functions.

```javascript

//Arrow function
let greet = (name) => {
    return "Hello, " + name + "!";
};
```
Arrow functions with a single expression can be further simplified by removing the curly braces and the return keyword, implicitly returning the expression.

```javascript

//Simplified arrow function
let greet = (name) => "Hello, " + name + "!";
```
Arrow functions also have a lexical this, meaning they inherit this from the surrounding code.

```javascript
function Person() {
    this.age = 0;

    setInterval(() => {
        this.age++;
    }, 1000);
}
```