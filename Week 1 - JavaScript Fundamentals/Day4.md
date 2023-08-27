## Objects & Object Oriented Programming

> Object-oriented programming (OOP) is a programming paradigm that revolves around the concept of "objects." In object-oriented programming, code is organized into reusable and self-contained units called objects, which can represent real-world entities, concepts, or abstract data structures. JavaScript is a versatile programming language that supports object-oriented programming.

### 1. Objects

An object in JavaScript is a complex data type that bundles properties (data) and methods (functions) together. Properties are variables that hold data, and methods are functions that define actions the object can perform. Objects in JavaScript can be thought of as containers that group related data and behavior.

### 2. Creating an object in javascript

There are multiple ways to create objects in JavaScript:

#### **(i) Object Literals:** 

The simplest way to create an object in javascript is using `object literals`. An object literal is defined by enclosing comma-separated key-value pairs within curly braces `{}`.

**Example :**

```javascript
const person = {
    firstName: 'John',
    lastName: 'Doe',
    age: 30,
    sayHello: function() {
        console.log(`Hello, my name is ${this.firstName} ${this.lastName}`);
    }
};
```

#### **(ii) Constructor Functions:** 

Constructor functions are used to create multiple instances of objects with the same structure. They act as blueprints for creating objects. You define a constructor function and use the `'new'` keyword to create instances.

**Example :**

```javascript
function Person(firstName, lastName, age) {
    this.firstName = firstName;
    this.lastName = lastName;
    this.age = age;
    this.sayHello = function() {
        console.log(`Hello, my name is ${this.firstName} ${this.lastName}`);
    };
}

const person1 = new Person('John', 'Doe', 30);
const person2 = new Person('Jane', 'Smith', 25);
```

#### **(iii) Prototypes and Prototype Chain:**

In JavaScript, objects can have prototypes, which are objects from which they inherit properties and methods. The prototype chain allows objects to inherit properties and methods from their prototypes. This forms the basis of inheritance in JavaScript.

**Example :**

```javascript
// Adding a method to the prototype of Person
Person.prototype.introduce = function() {
    console.log(`Hi, I'm ${this.firstName} and I'm ${this.age} years old.`);
};

person1.introduce(); // "Hi, I'm John and I'm 30 years old."
```

#### **(iv) ES6 Classes:**

ES6 introduced class syntax to JavaScript, making it more similar to traditional class-based OOP languages. Classes provide a clear and structured way to define objects and their behavior.

**Example :**

```javascript
class Person {
    constructor(firstName, lastName, age) {
        this.firstName = firstName;
        this.lastName = lastName;
        this.age = age;
    }

    sayHello() {
        console.log(`Hello, my name is ${this.firstName} ${this.lastName}`);
    }
}

const person = new Person('John', 'Doe', 30);
```

#### **(v) Encapsulation, Inheritance, Polymorphism:**

These are the three main principles of OOP.

(a) Encapsulation: The concept of bundling data and methods that operate on the data into a single unit (object), while also restricting access to certain parts of the object.

(b) Inheritance: The ability of objects to inherit properties and methods from other objects, creating a hierarchical relationship. This promotes code reuse and extensibility.

(c) Polymorphism: The ability to present the same interface (method or property) for different data types. It allows objects of different classes to be treated as instances of a common superclass.

JavaScript, being a dynamic language, supports these OOP principles, but in a flexible and sometimes unconventional manner compared to strictly class-based languages.


