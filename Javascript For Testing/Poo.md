# Classes and Objects in JavaScript

In JavaScript, an object is a collection of key-value pairs, where keys are strings (or Symbols) and values can be of any data type, including other objects or functions.

```javascript
const person = {
    name: 'John',
    age: 30,
    greet() {
        console.log(`Hello, my name is ${this.name} and I'm ${this.age} years old.`);
    }
};

//Accessing properties
console.log(person.name);

//Calling methods
person.greet(); 
```

## Classes in JavaScript

Classes in JavaScript are a template for creating objects. They provide a convenient way to define the structure and behavior of similar objects.

```javascript
class Person {
    constructor(name, age) {
        this.name = name;
        this.age = age;
    }

    //Method
    greet() {
        console.log(`Hello, my name is ${this.name} and I'm ${this.age} years old.`);
    }
}

//Creating objects
const person = new Person('Bob', 35);

//Accessing properties
console.log(person.name); 

//Calling methods
person.greet(); 
```

### Constructor Method

The constructor method is a special method that gets called when a new object is created using the class. It's used to initialize object properties.

#### Class Methods

Methods defined within a class are added to the prototype of the class. Instances of the class share these methods.
Inheritance

### Inheritance

```javascript
//Subclass
class Student extends Person {
    constructor(name, age, grade) {
        super(name, age); //Superconstructor
        this.grade = grade;
    }

    greet() {
        console.log(`Hello, my name is ${this.name}, I'm ${this.age} years old, and I'm in grade ${this.grade}.`);
    }
}

const student = new Student('Emma', 20, 12);
console.log(student.name);
```
### Objects And Method Tests

Examples With Jest

```javascript
// person.test.js
const person = {
    name: 'John',
    age: 30,
    greet() {
        return `Hello, my name is ${this.name} and I'm ${this.age} years old.`;
    }
};

test('person name should be John', () => {
    expect(person.name).toBe('John');
});

test('person age should be 30', () => {
    expect(person.age).toBe(30);
});

test('greet method should return correct greeting', () => {
    expect(person.greet()).toBe("Hello, my name is John and I'm 30 years old.");
});
```

#### Class Test

```javascript
// personClass.test.js
class Person {
    constructor(name, age) {
        this.name = name;
        this.age = age;
    }

    greet() {
        return `Hello, my name is ${this.name} and I'm ${this.age} years old.`;
    }
}

test('Person name should be Bob', () => {
    const person = new Person('Bob', 35);
    expect(person.name).toBe('Bob');
});

test('Person age should be 35', () => {
    const person = new Person('Bob', 35);
    expect(person.age).toBe(35);
});

test('greet method should return correct greeting', () => {
    const person = new Person('Bob', 35);
    expect(person.greet()).toBe("Hello, my name is Bob and I'm 35 years old.");
});
```

#### Inheritance Test

```javascript
// studentClass.test.js
class Person {
    constructor(name, age) {
        this.name = name;
        this.age = age;
    }

    greet() {
        return `Hello, my name is ${this.name} and I'm ${this.age} years old.`;
    }
}

class Student extends Person {
    constructor(name, age, grade) {
        super(name, age);
        this.grade = grade;
    }

    greet() {
        return `Hello, my name is ${this.name}, I'm ${this.age} years old, and I'm in grade ${this.grade}.`;
    }
}

test('Student name should be Emma', () => {
    const student = new Student('Emma', 20, 12);
    expect(student.name).toBe('Emma');
});

test('Student age should be 20', () => {
    const student = new Student('Emma', 20, 12);
    expect(student.age).toBe(20);
});

test('Student grade should be 12', () => {
    const student = new Student('Emma', 20, 12);
    expect(student.grade).toBe(12);
});

test('greet method should return correct greeting', () => {
    const student = new Student('Emma', 20, 12);
    expect(student.greet()).toBe("Hello, my name is Emma, I'm 20 years old, and I'm in grade 12.");
});
```
