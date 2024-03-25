### Variables

Variables in programming are containers for storing data values. In JavaScript, variables are declared using the `let`, `const`, or `var` keyword, followed by the variable name.

```javascript
let name = "John";  //Declare a variable that can be reassigned
const age = 30;     //Declare a constant variable
var country = "USA"; //Using var (older method, avoid using it in modern JS)
```
### Variables in JavaScript: `let`, `var`, and `const`

In JavaScript, there are three main keywords used for variable declaration: `let`, `var`, and `const`. Each has its own characteristics and best practices.

#### `let`:
- `let` is a relatively new addition to JavaScript, introduced in ES6 (ECMAScript 2015).
- It allows you to declare variables that can be reassigned.
- Variables declared with `let` are block-scoped, meaning they exist only within the block they are declared in.
- It's the preferred way to declare variables in modern JavaScript for most use cases.

#### `var`:
- `var` was the original way to declare variables in JavaScript.
- Variables declared with `var` are function-scoped, or globally scoped if declared outside a function.
- Unlike `let`, variables declared with `var` can be re-declared within the same scope without raising an error.
- It's generally considered less preferable to `let` due to its lack of block-scoping and potential for variable hoisting issues.

#### `const`:
- `const` is also introduced in ES6 and stands for "constant."
- Variables declared with `const` are block-scoped like `let`, but their value cannot be reassigned once initialized.
- It's ideal for declaring variables that are meant to remain constant throughout the program.
- If the variable is an object or array, its properties or elements can still be modified, but the variable itself cannot be reassigned.

### Data-Types
JavaScript supports several primitive data types and non-primitive (reference) data types. Here's an overview of the most common data types:

#### Primitive Data Types:
1. **String**: Represents a sequence of characters, enclosed in single or double quotes.
2. **Number**: Represents numeric data, including integers and floating-point numbers.
3. **Boolean**: Represents a logical value, either `true` or `false`.
4. **Undefined**: Represents an uninitialized variable or missing property.
5. **Null**: Represents an intentional absence of any object value.
6. **Symbol**: Represents a unique identifier that's guaranteed to be unique.

#### Non-Primitive (Reference) Data Types:
1. **Object**: Represents a collection of key-value pairs, where keys are strings and values can be any data type.
2. **Array**: Represents a collection of elements, each identified by an index.
3. **Function**: Represents reusable blocks of code that can be invoked with parameters.

#### Example Usage:
```javascript
//Primitive DataTypes
let name = "John"; // String
let age = 30;      // Number
let isAdult = true;// Boolean
let job;           // Undefined
let car = null;    // Null

//Non-Primitive Data Types
let person = { name: "John", age: 30 }; // Object
let hobbies = ["reading", "painting", "coding"]; // Array
function greet(name) { return "Hello, " + name + "!"; } // Function
```