## Functions in JavaScript:

> A function in JavaScript is a block of reusable code that can be defined and executed whenever needed. Functions help in organizing code, making it more modular and maintainable. They allow you to group statements together and give them a name, so you can call that name to execute the code inside the function.

### 1. Function Syntax:

Here's the basic syntax of defining a function in JavaScript:

```javascript 
function functionName(parameters) {
  // Code to be executed
}
```

(i) `functionName`: This is the name you give to your function.

(ii) `parameters`: These are placeholders for values that you can pass to the function when calling it.

(iii) Code inside the curly braces `{}` is the body of the function.

### 2. Function Example :

```javascript
function greet(name) {
  console.log(`Hello, ${name}!`);
}
```

In this example, greet is the function name, and name is a parameter. When you call this function with a name, it will print a greeting with that name.

### 3. Function Calling:

To call a function, you use its name followed by parentheses:

```javascript
greet("Avinash"); // This will print: Hello, Avinash!
```

## Scopes in JavaScript:

> A scope in JavaScript defines the context in which variables, functions, and other identifiers are accessible. 

JavaScript has two main types of scopes: global scope and local scope.

### 1. Global Scope:

Variables and functions defined outside of any function or block have global scope. They are accessible from anywhere in your code, both within functions and in the global context.

### 2. Local Scope:

Variables declared within a function are scoped locally. They are only accessible within that function, and not from outside. Each function creates its own local scope.

### **Example:**

The following example shows the accessibility of local and global variables in different scopes.

```javascript
let globalVar = "I'm global";

function exampleFunction() {
  let localVar = "I'm local";
  console.log(globalVar); // Accessible
  console.log(localVar);  // Accessible

  // Nested function

  function nestedFunction() {
    let nestedVar = "I'm nested";
    console.log(globalVar); // Accessible
    console.log(localVar);  // Accessible
    console.log(nestedVar); // Accessible
  }

  nestedFunction();
}

console.log(globalVar); // Accessible
console.log(localVar);  // Not accessible
console.log(nestedVar); // Not accessible
```

### **Scope Chain:**

JavaScript follows a scope chain to resolve variable and function references. When you reference a variable, JavaScript searches for it in the local scope first, then goes up the chain to look in enclosing scopes until it reaches the global scope.

### **Closures:**

Closures are a powerful concept in JavaScript. A closure is created when a function is defined within another function, allowing the inner function to access variables from the outer (enclosing) function even after the outer function has finished executing.

> Actually, a closure is a function that remembers the variables from the outer scope in which it was created, even if that outer scope's execution has completed. In other words, a closure "closes over" the variables it needs, allowing those variables to be accessed even after the outer function has finished executing.

### Example of a Closure:

Consider a scenario where you want to create a counter function that returns a new count each time it's called. We can achieve this using closures.

```javascript
function createCounter() {
  let count = 0; // This variable is in the local scope of createCounter

  function increment() {
    count++; // The increment function has access to the count variable
    console.log(count);
  }

  return increment; // Return the increment function (a closure)
}

const counter1 = createCounter(); // Creates a new counter
const counter2 = createCounter(); // Creates another new counter

counter1(); // Output: 1
counter1(); // Output: 2

counter2(); // Output: 1 (independent of counter1)
counter2(); // Output: 2
```

### **Explanation:**

In the example above, the createCounter function defines a count variable and an inner function named increment. The inner function increment is returned from createCounter.

When we call createCounter(), it returns the increment function. This returned function still has access to the count variable even though the createCounter function has finished executing. This is the essence of a closure.

So, when we create two counters using counter1 and counter2, each counter maintains its own separate count variable within its respective closure. Calling the counter functions increments their respective counts independently.