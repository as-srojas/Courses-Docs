# JavaScript Loops

Loops are used in JavaScript to execute a block of code repeatedly as long as a specified condition is true.

## `for` Loop

The `for` loop is commonly used when you know how many times you want to execute the loop.

```javascript
//Example 
for (let i = 0; i < 5; i++) {
    console.log(i);
}
```

## While Loop

The while loop repeats a block of code as long as a specified condition evaluates to true.

```javascript
//Example
let i = 0;
while (i < 5) {
    console.log(i);
    i++;
}
```

## Do While Loop

The do...while loop is similar to the while loop, but it always executes the block of code at least once before checking the condition.

```javascript
//Example
let i = 0;
do {
    console.log(i);
    i++;
} while (i < 5);
```

## Loop Control

JavaScript provides several loop control statements to manipulate loop execution:

- break: Terminates the loop immediately.

- continue: Skips the current iteration of the loop and continues with the next iteration.

- return: Exits the loop and the enclosing function.

```javascript
// Example
for (let i = 0; i < 10; i++) {
    if (i === 5) {
        break; //Terminate the loop
    }
    if (i % 2 === 0) {
        continue; //Skip even numbers
    }
}
```
