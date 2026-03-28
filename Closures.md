# Closures in JavaScript Presentation

---

## 1. Closure

A closure is a function that remembers variables from its outer scope.  
Even after the outer function has finished execution.

It allows inner functions to access variables of the parent function.  
Closures are created every time a function is defined.

Simple definition:  
Closure = function + its lexical environment

---

## 2. Lexical Scope

Lexical scope means variables are determined by where they are written in code.

Inner functions can access:
- Their own variables
- Parent function variables
- Global variables

Closures depend on lexical scope to work.

### Example:

~~~javascript
function outer() {
    let name = "Akshat";

    function inner() {
        console.log("Name:", name);
    }

    inner();
}

outer();
~~~

---

## 3. Basic Closure Example

A function returning another function creates a closure.

### Example:

~~~javascript
function outer() {
    let count = 0;

    return function inner() {
        count++;
        console.log("Count:", count);
    };
}

const counter = outer();

counter(); // 1
counter(); // 2
counter(); // 3
~~~

Here, `count` is preserved even after `outer()` finishes.

---

## 4. How Closures Work

When a function is returned:
- It keeps access to its original scope
- Variables are not destroyed
- They stay in memory

### Example:

~~~javascript
function outer() {
    let message = "Hello Closure";

    return function inner() {
        console.log(message);
    };
}

const fn = outer();
fn(); // Hello Closure
~~~

---

## 5. Data Encapsulation

Closures help in hiding data.

Variables cannot be accessed directly from outside.

### Example:

~~~javascript
function secret() {
    let password = "12345";

    return function() {
        console.log("Accessing password:", password);
    };
}

const getPassword = secret();
getPassword();
~~~

---

## 6. Function Factory

Closures allow creating dynamic functions.

### Example:

~~~javascript
function multiplier(x) {
    return function(y) {
        return x * y;
    };
}

const double = multiplier(2);
const triple = multiplier(3);

console.log(double(5)); // 10
console.log(triple(5)); // 15
~~~

---

## 7. Closures in Callbacks

Closures are widely used in asynchronous operations.

### Example:

~~~javascript
function greet(name) {
    setTimeout(function () {
        console.log("Hello " + name);
    }, 1000);
}

greet("Akshat");
~~~

---

## 8. Solution Using Closure

Using `let` fixes the issue.

### Example:

~~~javascript
for (let i = 0; i < 3; i++) {
    setTimeout(() => console.log(i), 1000);
}
~~~

### Output:

0 1 2

---

## 9. Advantages

Closures provide several benefits.

- Data hiding and encapsulation
- State preservation
- Reusable functions
- Cleaner and modular code

---

## 10. Disadvantages

Closures also have some drawbacks.

- Higher memory usage
- Variables are not garbage collected easily
- Can cause memory leaks if misused

---

## 11. Summary

Closure → function with memory of outer variables

Used for:
- Data privacy
- Callbacks
- Function factories

Closures are a core concept in JavaScript.  
Important for interviews and real-world development.

---

---
