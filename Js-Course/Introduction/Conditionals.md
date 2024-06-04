### Conditionals and Complex Conditionals

Conditional statements are used in JavaScript to execute different code blocks based on different conditions. Complex conditionals involve combining multiple conditions using logical operators such as AND (`&&`) and OR (`||`).

#### Simple Conditionals:

```javascript
let age = 20;
if (age >= 18) {
    console.log("You are an adult.");
} else {
    console.log("You are a minor.");
}
```
### Complex Conditionals

```javascript
let student = {
    name: "Alice",
    age: 20,
    grade: "A",
    attendance: true
};

if (student.age >= 18 && student.grade === "A" && student.attendance) {
    console.log(student.name + " is eligible for a scholarship.");
} else if (student.age >= 18 && student.grade === "B" && student.attendance) {
    console.log(student.name + " is eligible for a partial scholarship.");
} else if (student.age >= 18 && student.attendance) {
    console.log(student.name + " is eligible to apply for financial aid.");
} else {
    console.log(student.name + " is not eligible for any financial assistance.");
}
```
### Boolean Rules

|   A   |   B   | AND (A && B) | OR (A \|\| B) | NOT (!A) |
|-------|-------|--------------|--------------|----------|
| true  | true  | true         | true         | false    |
| true  | false | false        | true         | false    |
| false | true  | false        | true         | true     |
| false | false | false        | false        | true     |

