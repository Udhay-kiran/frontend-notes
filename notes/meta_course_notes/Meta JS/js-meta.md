# Module 1- Intro

## Comments in JavaScript

1. Single line comment - `//this is a comment!`
2. Multi-line comment -`/*multi line comment*/`

%c- to add css styling to a console output within the same line in different " "

## Variables 

Named container that stores value in memory.

| Keyword | Description                        | Example               |
| ------- | ---------------------------------- | --------------------- |
| `let`   | used for values that can change    | `let score = 10;`     |
| `const` | used for values that stay constant | `const pi = 3.1416;`  |
| `var`   | old way (avoid using in modern JS) | `var name = "Udhay";` |

```js
let username = "Udhay";
const birthYear = 2000;
let age = 2025 - birthYear;

console.log("Name:", username);
console.log("Age:", age);
```

**Note** that variables are case-sensitive, cannot start with a number, try to make them descriptive to avoid confusion.

## Data Types (Primitive)

There are **7 primitive data types**

`String`, `Number`, `Boolean`, `Null`, `Undefined`, `BigInt` and `symbol`.

### Primitive Data Types in JavaScript

| No. | Data Type | Definition | Syntax / Example | Common Use Cases |
|-----|------------|-------------|------------------|------------------|
| **1** | **String** | Used to store text values. | `"Hello"`, `'World'`, `` `Welcome!` `` | Titles, names, messages, or any text data. |
| **2** | **Number** | Represents numeric values (integers or decimals). | `42`, `3.14`, `-100` | Prices, quantities, ages, scores, calculations. |
| **3** | **Boolean** | Represents logical values — either `true` or `false`. | `true`, `false` | Conditions, comparisons, control flow. |
| **4** | **Null** | Represents an intentional absence of any value. | `let user = null;` | Used to clear or reset variable values. |
| **5** | **Undefined** | A variable that has been declared but not assigned a value. | `let x; // undefined` | To check if a variable is initialized. |
| **6** | **BigInt** | Used for integers that are too large for the Number type. | `1234567890123456789n` | For precise calculations with huge numbers. |
| **7** | **Symbol** | A unique and immutable data type, mainly used as identifiers. | `Symbol("id")` | For creating unique object property keys. |

---

### Key Takeaways

- Primitive values are **immutable** (cannot be changed directly).  
- Use the **`typeof`** operator to check a variable’s type:

```js
typeof "Hello";     // "string"
typeof 42;          // "number"
typeof true;        // "boolean"
typeof null;        // "object"  <-- known JS quirk
typeof undefined;   // "undefined"
typeof 123n;        // "bigint"
typeof Symbol();    // "symbol"
```

## JavaScript Operators

### Overview

> **Operators** are special symbols used to perform operations on values and variables.  
They help JavaScript calculate, compare, and make logical decisions.

JavaScript operators are grouped by purpose: **Arithmetic**, **Assignment**, **Comparison**, **Logical (Boolean) **, **String**, and **Others**.

---

## Arithmetic Operators

Used to perform basic mathematical calculations.

| Operator | Description | Example | Output |
|-----------|--------------|----------|--------|
| `+` | Addition | `5 + 2` | `7` |
| `-` | Subtraction | `5 - 2` | `3` |
| `*` | Multiplication | `5 * 2` | `10` |
| `/` | Division | `10 / 2` | `5` |
| `%` | Modulus (remainder) | `10 % 3` | `1` |
| `**` | Exponentiation | `2 ** 3` | `8` |
| `++` | Increment by 1 | `let a=5; a++;` | `6` |
| `--` | Decrement by 1 | `let a=5; a--;` | `4` |

---

## Assignment Operators

Used to assign or update values of variables.

| Operator | Description | Example | Equivalent To |
|-----------|--------------|----------|---------------|
| `=` | Assign value | `x = 10` | – |
| `+=` | Add and assign | `x += 5` | `x = x + 5` |
| `-=` | Subtract and assign | `x -= 3` | `x = x - 3` |
| `*=` | Multiply and assign | `x *= 2` | `x = x * 2` |
| `/=` | Divide and assign | `x /= 2` | `x = x / 2` |
| `%=` | Modulus and assign | `x %= 3` | `x = x % 3` |
| `**=` | Power and assign | `x **= 2` | `x = x ** 2` |

---

## Comparison Operators

Used to compare two values. The result is always a **Boolean** (`true` or `false`).

| Operator | Description | Example | Output |
|-----------|--------------|----------|--------|
| `==` | Equal to (loose comparison) | `5 == "5"` | `true` |
| `===` | Strict equal to (checks value **and** type) | `5 === "5"` | `false` |
| `!=` | Not equal to (loose) | `5 != "5"` | `false` |
| `!==` | Strict not equal to | `5 !== "5"` | `true` |
| `>` | Greater than | `10 > 5` | `true` |
| `<` | Less than | `10 < 5` | `false` |
| `>=` | Greater than or equal to | `10 >= 10` | `true` |
| `<=` | Less than or equal to | `8 <= 10` | `true` |

---

## Logical (Boolean) Operators

Used to combine or invert Boolean expressions.

| Operator | Description | Example | Output |
|-----------|--------------|----------|--------|
| `&&` | Logical AND (true only if both are true) | `(5 > 3 && 8 > 6)` | `true` |
| `\|\|` | Logical OR (true if at least one is true) | `(5 > 10 \|\| 3 < 8)` | `true` |
| `!` | Logical NOT (reverses the value) | `!(5 > 3)` | `false` |

### Truth Table

| A | B | `A && B` | `A \|\| B` | `!A` |
|:-:|:-:|:---------:|:-----------:|:----:|
| true | true | true | true | false |
| true | false | false | true | false |
| false | true | false | true | true |
| false | false | false | false | true |

---

## String Operator

- The `+` operator can also **concatenate (join)** strings.

```js
let first = "Hello";
let last = "World";
console.log(first + " " + last); // "Hello World"
```

## Writing statements and Conditional Statements in JavaScript

### Overview

> JavaScript programs are made up of **statements** — each statement performs an action.  
> Conditional statements control *which* statements run, based on whether conditions are true or false.

### Writing Statements

| Concept | Description | Example |
|----------|--------------|----------|
| **Statement** | A single line of code that performs an action. | `let x = 10;` |
| **Block** | A group of statements inside `{}` braces. | `{ let y = 5; console.log(y); }` |
| **Semicolon (;)** | Marks the end of a statement (optional but recommended). | `console.log("Hello");` |

Each statement executes **in order** unless changed by control flow (like `if`, `for`, or `while`).

---

### Conditional Statements

Conditional statements let JavaScript **decide which code to run** depending on a condition.

---

#### a) The `if` Statement

Runs a block of code **only if** a condition is true.

```js
let age = 20;

if (age >= 18) {
  console.log("You are an adult.");
}
```

---

#### b) The `if...else` statement

Adds an alternative block that runs if the condition is false. 

```js
let isLoggedIn = false;

if (isLoggedIn) {
  console.log("Welcome back!");
} else {
  console.log("Please log in.");
}
```

#### c) The `if...else if...else chain`

Used to check multiple conditions

```js
let score = 75;

if (score >= 90) {
  console.log("Grade: A");
} else if (score >= 75) {
  console.log("Grade: B");
} else if (score >= 50) {
  console.log("Grade: C");
} else {
  console.log("Grade: F");
}
```

Javascript checks each condition from top to bottom and stops once its true.

#### d) The `switch` statement

Used when you want to test one variable against multiple possible values.

```js
let day = "Monday";

switch (day) {
  case "Monday":
    console.log("Start of the week!");
    break;
  case "Friday":
    console.log("Weekend is near!");
    break;
  case "Saturday":
  case "Sunday":
    console.log("It's the weekend!");
    break;
  default:
    console.log("Just another day.");
}
```

`break` stops the execution after a match;
`default` runs if no case matches.

#### e) The `break` Statement


> The **`break`** statement is used to **immediately exit** a loop or a `switch` statement.  
> When JavaScript encounters `break`, it stops executing the current block and jumps to the next line of code **after** the loop or switch.

---

##### Using `break` in Loops

| Purpose | Example Code | Explanation |
|----------|---------------|--------------|
| Exit a loop early when a condition is met | ```js let i = 0; while (i < 10) { if (i === 5) break; console.log(i); i++; } console.log("Loop stopped at", i); ``` | The loop stops when `i` becomes 5. Numbers 0–4 are printed, then the loop exits. |

`break` is useful when you’ve **found what you’re looking for** and don’t need to continue looping.

---

##### Using `break` in `for` Loops

```js
for (let num = 1; num <= 10; num++) {
  if (num === 4) {
    break; // exit the loop when num = 4
  }
  console.log("Number:", num);
}
```

#### f) Nested `if` statements

An `if` can be placed inside another for more complex logic:

```js
let age = 25;
let hasID = true;

if (age >= 18) {
  if (hasID) {
    console.log("Access granted.");
  } else {
    console.log("ID required.");
  }
} else {
  console.log("Access denied.");
}
```

### Looping Constructs

**Loops** let you repeat a block of code automatically until a condition is **false**. They help avoid writing the same statement multiple times. 


#### a) The `for` loop

It is used when **you know how many times** the loop should run.

**Syntax and Example:**

```js

for (initialization; condition; increment) {
  // code to execute each iteration
}

Example:

for (let i = 1; i <= 5; i++) {
  console.log("Iteration:", i);
}
```


| Part           | Meaning                              | Example     |
| -------------- | ------------------------------------ | ----------- |
| Initialization | Runs once before loop starts         | `let i = 1` |
| Condition      | Checked before each iteration        | `i <= 5`    |
| Increment      | Updates counter after each iteration | `i++`       |

#### b) The `while` loop:

Used when **you dont know beforehand** how many times to repeat, but you know the stopping condition.

**Syntax and Example:**

while (condition) {
  // code to execute
}

```js
while (condition) {
  // code to execute
}

Example:

let count = 1;

while (count <= 3) {
  console.log("Count is:", count);
  count++;
}
```
Runs **as long as** the condition is true. If the condition is false at the start, the loop doesn't run at all.

---

# Module 2- Building blocks

## Functions

A **function** is a reusable block of code designed to perform a specific task.

**Syntax:**

```js
function functionName(parameters) {
  // code to execute
}

**Example:**

function greet() {
  console.log("Hello, world!");
}
greet(); // function call
```

### Function parameters and arguments

| Term          | Description                             | Example                        |
| ------------- | --------------------------------------- | ------------------------------ |
| **Parameter** | Placeholder in the function definition. | `function greet(name) { ... }` |
| **Argument**  | Actual value passed to the function.    | `greet("Alice");`              |

```js
function add(a, b) {
  console.log(a + b);
}
add(3, 4); // Output: 7
```

### Return statement in a function

Used to **send a result back** from a function.

```js
function multiply(x, y) {
  return x * y;
}
let result = multiply(4, 5);
console.log(result); // 20
```

**Note:** Without `return` a function gives `undefined`.

### Function Expression

Storing a function inside a variable is possible.

```js
const greet = function(name) {
  return `Hello, ${name}`;
};
console.log(greet("Udhay"));
```

## Storing data in arrays

An array stores multiple values in a single variable.

```js
let fruits = ["apple", "banana", "cherry"];
console.log(fruits[0]); // apple
console.log(fruits.length); // 3
```

### **Common array methods**

| Method        | Description            | Example                    | Result                                |
| ------------- | ---------------------- | -------------------------- | ------------------------------------- |
| `.push()`     | Adds to end            | `fruits.push("mango")`     | `["apple","banana","cherry","mango"]` |
| `.pop()`      | Removes last item      | `fruits.pop()`             | `["apple","banana"]`                  |
| `.shift()`    | Removes first item     | `fruits.shift()`           | `["banana","cherry"]`                 |
| `.unshift()`  | Adds to start          | `fruits.unshift("grape")`  | `["grape","apple","banana"]`          |
| `.indexOf()`  | Finds index of value   | `fruits.indexOf("banana")` | `1`                                   |
| `.includes()` | Checks if value exists | `fruits.includes("apple")` | `true`                                |


## Intro to Objects

An **object** groups related data and behaviour (properties and methods).

**Syntax:**

```js
let person = { //person- name of the object
  name: "Alice", // name - property key; "Alice"- property value
  age: 25,
  greet: function() {
    console.log("Hello!");
  }
};
```

**Properties:** Variables inside objects. 
**Methods:** functions inside objects.

### Object literals and Dot Notations

| Syntax              | Description                     | Example                   |
| ------------------- | ------------------------------- | ------------------------- |
| **Dot Notation**    | Access property using a dot `.` | `person.name` → `"Alice"` |
| **Add Property**    | `person.city = "Berlin";`       | Adds new property         |
| **Modify Property** | `person.age = 30;`              | Updates existing property |

**Example:**

```js
let car = { brand: "Tesla", model: "Model 3" }; // Car is the object and brand and model are its traits
console.log(car.brand); // Tesla
car.year = 2023;
console.log(car.year); // 2023
```

### Object literals and Bracket Notation

Bracket notation is used when the property name has spaces or it is stored in a variable.

```js
let student = {
  "full name": "John Doe",
  grade: "A"
};

console.log(student["full name"]); // John Doe

let key = "grade";
console.log(student[key]); // A
```

**Note:** Use bracket Notation when keys are dynamic or not valid identifiers.

### Arrays are objects

In javascript, arrays are a special kind of object with numeric indexes.

```js
let colors = ["red", "green", "blue"];
console.log(typeof colors); // "object"
```

Arrays can also hold mixed data types:

```js
let mix = ["Hello", 42, true, null];
```

**Note:** You can access elements like object properties. `colors[0]` -> `"red"`

One of the most commonly used built-in methods on arrays are the `push()` and the `pop()` methods.

To add new items to an array, I can use the `push()` method:

```js
var fruits = [];
fruits.push("apple"); // ['apple']
fruits.push('pear'); // ['apple', 'pear']
```

To remove the last item from an array, use `pop()`

```js
fruits.pop();
console.log(fruits); // ['apple']
```

**Example tying up arrays and objects:**

We can now build a function that takes all its arguments and pushes them into an array:

```js
function arrayBuilder(one, two, three) {
    var arr = [];
    arr.push(one);
    arr.push(two);
    arr.push(three);
    console.log(arr);
}

// Now call the array builder function, like for ex:

arrayBuilder('apple', 'pear', 'plum'); // ['apple', 'pear', 'plum']

// I do not necessarily have to console log the new array. Instead, a return keyword can send the array back to wherever the function was called. So the function can provide the result and you can decide what to do with it in your code.

function arrayBuilder(one, two, three) {
    var arr = [];
    arr.push(one);
    arr.push(two);
    arr.push(three);
    return arr; // The array is returned to the calling code.
}

// Now when the function is called 

var myArray = arrayBuilder('apple', 'pear', 'plum');

// The return keyword allows the function to hand the built array back to the variable my Array. You can use it to pass it to another function, print it or manipulate it further. Additionally, I can save this function call to a variable. 

console.log(myArray); // ['apple','pear','plum']
```

### A closer look at Strings

**Strings are Iterable**, meaning you can loop through each character using `for...of`. Strings also act like arrays (you can access characters by index) but are **immutable** (cannot be changed directly).

```js
//Iterating Over Strings

let word = "JS";
for (let ch of word) {
  console.log(ch);
}
// Output: J  S
```

#### String like behaviour

| Operation       | Example                  | Result                  |
| --------------- | ------------------------ | ----------------------- |
| Access by index | `"Hi"[0]`                | `"H"`                   |
| Length          | `"Hi".length`            | `2`                     |
| Loop            | `for (let c of "Hi") {}` | Iterates over each char |

#### Concatenation

```js
let a = "Front";
let b = "End";
console.log(a + b);        // FrontEnd
console.log(`${a}-${b}`);  // Front-End
```

#### Common string methods

| Method           | Example                   | Output   |
| ---------------- | ------------------------- | -------- |
| `.toUpperCase()` | `"js".toUpperCase()`      | `"JS"`   |
| `.toLowerCase()` | `"JS".toLowerCase()`      | `"js"`   |
| `.includes("a")` | `"Java".includes("a")`    | `true`   |
| `.slice(0,4)`    | `"JavaScript".slice(0,4)` | `"Java"` |

### Math Object

The Math Object provides built-in mathematical methods and constants. 

| Method / Property | Description              | Example           | Output       |
| ----------------- | ------------------------ | ----------------- | ------------ |
| `Math.PI`         | π constant               | `Math.PI`         | `3.14159...` |
| `Math.round(x)`   | Round to nearest integer | `Math.round(4.7)` | `5`          |
| `Math.floor(x)`   | Round down               | `Math.floor(4.7)` | `4`          |
| `Math.ceil(x)`    | Round up                 | `Math.ceil(4.1)`  | `5`          |
| `Math.pow(a,b)`   | Power                    | `Math.pow(2,3)`   | `8`          |
| `Math.sqrt(x)`    | Square root              | `Math.sqrt(9)`    | `3`          |
| `Math.random()`   | Random number (0–1)      | `Math.random()`   | e.g. `0.57`  |
| `Math.abs(x)` | Returns the absolute (positive) value | `Math.abs(-7.5)` | `7.5` |
| `Math.sign(x)` | Returns sign: `1` (positive), `0`, or `-1` | `Math.sign(-10)` | `-1` |
| `Math.trunc(x)` | Removes fractional part | `Math.trunc(4.9)` | `4` |

### `typeof` operator 

The `typeof` operator checks the data type of a value or variable. 

**Syntax**

```js
typeof value;
```

| Example               | Output                        |
| --------------------- | ----------------------------- |
| `typeof "Hello"`      | `"string"`                    |
| `typeof 42`           | `"number"`                    |
| `typeof true`         | `"boolean"`                   |
| `typeof undefined`    | `"undefined"`                 |
| `typeof null`         | `"object"` *(known JS quirk)* |
| `typeof [1,2,3]`      | `"object"`                    |
| `typeof function(){}` | `"function"`                  |

Used for **type checking** before performing operations.

## Errors and common types of errors in JS

An error can be defined as a faulty piece of code that prevents the program from further execution, an error gets thrown and the program stops.

| Type                | Description                             | Example                               |
| ------------------- | --------------------------------------- | ------------------------------------- |
| **Syntax Error**    | Code written incorrectly                | `console.log("Hi"` → missing `)`      |
| **Reference Error** | Using an undefined variable             | `console.log(x)` when `x` not defined |
| **Type Error**      | Performing invalid operation on a value | `123.toUpperCase()`                   |
| **Logical Error**   | Code runs but produces wrong result     | Using `+` instead of `*`              |


### The `try...catch` block

Handles error such that the program doesn't crash

```js
try {
  // code that might throw an error
} catch (error) {
  console.log("An error occurred:", error.message);
}

//example:

try {
  let result = 10 / 0;
  console.log(result);
  nonExistentFunction(); // throws error
} catch (e) {
  console.log("Error caught:", e.message);
}


//output:

Infinity
Error caught: nonExistentFunction is not defined

```

### `throw` keyword

Manually generate (throw) an error when something goes wrong

```js
function divide(a, b) {
  if (b === 0) throw new Error("Division by zero!");
  return a / b;
}

try {
  console.log(divide(10, 0));
} catch (e) {
  console.log(e.message);
}

// output: `Division by zero`
```
Note that you can use a throw keyword outside of a try block, but you won't be able to catch it.

| Keyword   | Purpose                               |
| --------- | ------------------------------------- |
| `try`     | Code to test for errors               |
| `catch`   | Runs if an error occurs               |
| `throw`   | Manually trigger an error             |
| `finally` | Runs regardless of success or failure |

**Example:**

```js
try {
  console.log("Start");
  throw new Error("Oops!");
} catch (e) {
  console.log("Caught error");
} finally {
  console.log("Always runs");
}
/*Output
Start
Caught error
Always runs*/
```

| Value       | Meaning                   | Example                               |
| ----------- | ------------------------- | ------------------------------------- |
| `undefined` | Declared but not assigned | `let a; console.log(a); // undefined` |
| `null`      | Intentional empty value   | `let b = null;`                       |
| `""`        | Empty string              | `let c = "";`                         |

Use `===` to distinguish `null` and `undefined`.

**Example:**

```js
function printName(name) {
  if (typeof name !== "string" || name === "") {
    console.log("Invalid name");
    return;
  }
  console.log("Name:", name);
}

/*Output:
Name: Udhay
Invalid name
*/
```




# Module 3: Programming Paradigms

## Intro to Functional programming

Functional programming is a **programming style** focused on writing reusable, pure functions that avoid side effects and make code predictable.

**Example:**

```js
function add(a, b) {
  return a + b;
}
console.log(add(3, 5)); // 8
```

### Return values from Functions

| Concept       | Description                                           | Example         |
| ------------- | ----------------------------------------------------- | --------------- |
| **Return**    | Sends a result back to where the function was called. | `return a + b;` |
| **No Return** | Functions without `return` give `undefined`.          | `console.log()` |

```js
// Function to double a number
function doubleIt(num) {
    return num * 2;
}

// Function to create an object with a 'prop' key
function objectMaker(val) {
    return { prop: val };
}

// Chaining functions and returning values
let result = objectMaker(doubleIt(5));
console.log(result); // { prop: 10 }
```

### Function calling and Recursion

A function can call itself. This is called **recursion.**

```js
function factorial(n) {
  if (n === 1) return 1;
  return n * factorial(n - 1);
}
console.log(factorial(5)); // 120
```

#### Base and Recursive cases:

**Base case:** The base case is the condition in a recursive function that stops the recursion. It represents the simplest, where the anawer is already known and can be returned without making further recursive calls. 

**Example:** For fibonacci, the base cases are:

fib(0)=0 :  When n=0, the Fibonacci number is 0.

fib(1)=1 :  When n=1, the Fibonacci number is 1.


**Recursive Case:** The recursive case is the part of the function that defines how the problem is broken down into smaller, similar sub-problems. It involves the function calling itself with a smaller or reduced output, moving closer to the base case with each call. This ensures the problem is eventually solved though a series of smaller, manageable steps. 

**Example:** For fibonacci, the recursive case follows the formula:

fib(n)  =  fib(n-1)  + fib(n-2)

This means to calculate fib(n),  you need the sum of the two previous Fibonacci numbers (fib(n−1) and fib(n−2)).

```js
function fib(n) {
    if (n === 0) return 0;
    if (n === 1) return 1;

    return fib(n-1)+fib(n-2) //Recursive case
    
}

console.log(fib(5)); //5
console.log(fib(10)); //55
```

### Scope

Scope defines where variables are accessible.

| Type                 | Description                                         | Example                       |
| -------------------- | --------------------------------------------------- | ----------------------------- |
| **Global**           | Declared outside functions — accessible everywhere. | `let name = "Alex";`          |
| **Local (Function)** | Declared inside a function — used only there.       | `function show(){ let x=5; }` |
| **Block**            | Declared with `let` or `const` inside `{}`.         | `{ let y = 10; }`             |

**Example:**

```js
let x = 10; //global
function test() {
  let y = 5;  //local to the function
  console.log(x); // accessible
  console.log(y); // accessible
}
console.log(y); // Error (not defined)
```

### Functional Programming Paradigm

There are actually several styles of coding, also known as **paradigm**s. A common style is called **functional programming**, or FP for short.

In functional programming, we use functions extensively and often work with immutable values. Immutability is a key principle, meaning variables are not modified after their initial assignment.

| Concept                   | Meaning                                                     | Example              |
| ------------------------- | ----------------------------------------------------------- | -------------------- |
| **Pure Function**         | Always returns same result for same input, no side effects. | `Math.max(2, 5)`     |
| **Immutability**          | Data cannot be modified — use copies.                       | `[...arr, newValue]` |
| **Higher-Order Function** | Takes another function as input or returns one.             | `arr.map(x => x*2)`  |

#### Scoping with  `var`, `let`, and `const`

**Scope** defines where a variable is accessible in the program 

| Keyword | Scope | Redeclarable | Reassignable | Hoisted | Notes |
|----------|--------|--------------|--------------|----------|-------|
| `var` | Function | Yes | Yes | Yes (initialized as undefined) | Legacy JS variable type |
| `let` | Block | No | Yes | No | Preferred for changing values |
| `const` | Block | No | No | No | Use for fixed values |

**Example:**

```js
if(true){
   var x = 10; // function scoped
  let y = 20; // block scoped
  const z = 30; // block scoped
}

console.log(x); // Works
console.log(y); // ReferenceError
console.log(z); // ReferenceError
```

##### Refactoring `var` to `let` and `const`

Replacing `var` with `let` or `const` helps prevent scope leakage and accidental overwriting.. 

```js
// Old code
var counter = 0;
for (var i = 0; i < 5; i++) {
  counter += i;
}

// Improved version
let counter = 0;
for (let i = 0; i < 5; i++) {
  counter += i;
}
```

`let` confines `i` inside the loop; it doesn't leak into global scope.

## Introduction to Object-Oriented Programming (OOP)

OOP organizes code into objects that contain both data (properties) and actions (methods).

**Example:**

```js
let car = {
  brand: "Tesla",
  start: function() {
    console.log("Car started");
  }
};
car.start(); // Car started
```

Use `this` keyword to refer to the object within the object body.

### More on OOP principles 

Fundamental principles of OOP are **inheritance, encapsulation, abstraction and polymorphism**. 


**Inheritance:**  Works like this:

1. There is a base class of a "thing".
2. There are one or more sub-classes of "things" that inherit the properties of the base class (sometimes also referred to as the "super-class")
3. There might be some other sub-sub-classes of "things" that inherit from those classes in point 2.

**Example:**

```js
class Animal { /* ...class code here... */ };
class Mammal extends Animal { /* ...class code here... */ };
class Elephant extends Mammal { /* ...class code here... */ };
```

**Encapsulation:**

Encapsulation has to do with making a code implementation "hidden" from other users, in the sense that they don't have to know how my code works in order to "consume" the code.

**Abstraction:**

Abstraction is about writing code in a way that will make it more generalized. It is about extracting the concept of what you're trying to do, rather than dealing with a specific manifestation of that concept.

**Polymorphism:** It is "something that can take on many forms" 

**Example:**

```js
const bicycle = {
    bell: function() {
        return "Ring, ring! Watch out, please!";
    }
}
const door = {
    bell: function() {
        return "Ring, ring! Come here, please!";
    }
}
//access the bell() method on each object like this:

bicycle.bell(); // "Ring, ring! Watch out, please!"
door.bell();    // "Ring, ring! Come here, please!"

function ringTheBell(thing) {
    console.log(thing.bell());    // This function declaration makes the code truly polymorphic. It accepts a thing parameter- that I expect to be an object, namely, either a bicycle object or the door object
}

//invoking ringTheBell()
ringTheBell(bicycle); // Ring, ring! Watch out, please!

ringTheBell(door); // "Ring, ring! Come here, please!"
```

Polymorphism is useful because it allows developers to build objects that can share functionality but override it as needed.

**Another example of Polymorphism using classes in JavaScript:**

```js
class Bird {
    useWings() {
        console.log("Flying!");
    }
}
class Eagle extends Bird {
    useWings() {
        super.useWings();
        console.log("Barely flapping!");
    }
}
class Penguin extends Bird {
    useWings() {
        console.log("Diving!");
    }
}
var baldEagle = new Eagle();
var kingPenguin = new Penguin();
baldEagle.useWings(); // "Flying! Barely flapping!"
kingPenguin.useWings(); // "Diving!"
```

### Constructors

JavaScript has a number of built-in object types, such as:

 `Math`, `Date`, `Object`, `Function`, `Boolean`, `Symbol`, `Array`, `Map`, `Set`, `Promise`, `JSON`, and many more.

These objects are commonly known as "native objects."

Constructor functions, commonly referred to as just "constructors", are special functions that allow us to build instances of these built-in native objects. All the constructor functions are capitalized. To use a constructor function, I must prepend it with the operator `new`.

#### Custom Constructor Functions

```js
function Icecream(flavor) {
    this.flavor = flavor;
    this.meltIt = function() {
        console.log(`The ${this.flavor} icecream has melted`);
    }
}

let kiwiIcecream = new Icecream("kiwi");
let appleIcecream = new Icecream("apple");
kiwiIcecream; // --> Icecream {flavor: 'kiwi', meltIt: ƒ}
appleIcecream; // --> Icecream {flavor: 'apple', meltIt: ƒ}
```

There are now two instance objects of `Icecream` type
The most common use case of `new` is to use it with one of the built-in object types. 


| Concept | Example | Type Returned | Performance | Comparison Result | Best Practice |
|----------|----------|---------------|--------------|-------------------|----------------|
| **Primitive value** | `"apple"` | `string` |  Fast, lightweight | `"apple" === "apple"` →  `true` |  Use this (preferred) |
| **Object via constructor** | `new String("apple")` | `object` |  Slower, more memory | `new String("apple") === new String("apple")` →  `false` |  Avoid for primitives |
| **Why false?** | Each `new String()` makes a **different object** in memory | – | – | Objects compare by **reference**, not value | – |
| **Same applies to:** | `new Number(5)`, `new Boolean(true)` | `object` |  Less efficient | – | Avoid |
| **Recommended literals:** | `5`, `true`, `"text"` | Primitive types |  Fast, clean | Compare by value |  Always use |

**Note:**  

Use **literals** (like `"hello"`, `42`, `true`) instead of constructors (`new String()`, `new Number()`, `new Boolean()`),  
because constructors create **objects**, not primitives — which are **slower and not equal by value**.

#### Alternative Patterns and Literals

Better ways to create objects (in-short)

| Type     | Constructor       | Literal (Preferred) | Notes                                         |
| -------- | ----------------- | ------------------- | --------------------------------------------- |
| Object   | `new Object()`    | `{}`                | Literal is simpler and faster                 |
| Array    | `new Array()`     | `[]`                | Avoid `new Array()` — can behave unexpectedly |
| Function | `new Function()`  | `function() {}`     | Literal is clearer                            |
| RegExp   | `new RegExp("a")` | `/a/`               | Literal is more readable                      |

Best practice: Use `{}`, `[]`, `function() {}`, and `/pattern/` — not `new Object()`, `new Array()`, etc.

#### Built-in Constructors that are easy to use

| Constructor               | Purpose                                  | Example                            |
| ------------------------- | ---------------------------------------- | ---------------------------------- |
| `Date()`                  | Create date/time objects                 | `new Date()`                       |
| `Error()`                 | Represent errors                         | `new Error("Something broke!")`    |
| `Map()`                   | Key-value pairs with any type as keys    | `new Map()`                        |
| `Set()`                   | Stores unique values                     | `new Set([1,2,3])`                 |
| `WeakMap()` / `WeakSet()` | Similar to Map/Set but garbage-collected | `new WeakMap()`                    |
| `Promise()`               | Handle asynchronous code                 | `new Promise((res, rej) => {...})` |

These are meant to be used with `new`.

### Inheritance

**Inheritance** allows one class (child) to use properties and methods of another class (parent).

| Term | Meaning | Example |
|------|----------|----------|
| **Parent Class** | Base class with shared properties/methods | `class Animal {...}` |
| **Child Class** | Extends parent, can add/override methods | `class Dog extends Animal {...}` |
| **`super()`** | Calls the parent constructor or method | `super(name);` |

**Example:**

```js
class Animal {
  constructor(name) { this.name = name; }
  speak() { console.log(`${this.name} makes a sound`); }
}

class Dog extends Animal {
  speak() { console.log(`${this.name} barks`); } // override
}

const d = new Dog("Rex");
d.speak(); // Rex barks
```

**Note:** Child class inherits all parent properties and methods. Overriding lets you change behaviour in the subclass. 

### Classes and their creation

A **Class** is a blueprint for creating objects.

**Syntax:**

```js
class Car {
  constructor(brand, color) {
    this.brand = brand;
    this.color = color;
  }
  start() {    //the keyword function is not necessary here. Just the name of the method is enough.
    console.log(`${this.brand} started!`);
  }
}

const myCar = new Car("Tesla", "red");
myCar.start(); // Tesla started!
```

| Feature         | Description                          |
| --------------- | ------------------------------------ |
| `constructor()` | Initializes object data              |
| `this`          | Refers to the created object         |
| Methods         | Added automatically to the prototype |
| `new`           | Creates an instance from the class   |


#### Default parameters

Functions can have default values for parameters, used if no argument is passed.

**Example:**

```js
function greet(name = "User") {
  console.log(`Hello, ${name}!`);
}

greet("Alex"); // Hello, Alex!
greet();       // Hello, User!
                                            //Works in both functions and constructors. 
//(or)

class Product {
  constructor(name = "Unknown", price = 0) {
    this.name = name;
    this.price = price;
  }
}
```

#### Prototype

In JavaScript, **every object** has a hidden property called `[[Prototype]]`, which acts as a link to another object - known as its prototype. It can be thought of as backup reference.

**Example (Without Classes)**

```js
function Car(brand) {
  this.brand = brand;
}
Car.prototype.drive = function() {
  console.log(`${this.brand} is driving`);
};

const c1 = new Car("Tesla");
c1.drive(); // Tesla is driving
```

**Here:**

`Car` is a constructor function.
`Car.prototype` is an object where shared methods live.
`c1` has access to those methods via its prototype chain.

So when you call `c1.drive()`, JS looks for `drive`:
Inside `c1` — not found.
In `Car.prototype` — found.
Executes it.

**Example (In classes- Modern Syntax)**

```js
class Car {
  constructor(brand) {
    this.brand = brand;
  }
  drive() {
    console.log(`${this.brand} is driving`);
  }
}

//under the hood:

Car.prototype.drive = function() { ... }
```

So methods inside a class are stored on the prototype, not inside each object- which saves memory and keeps all instances efficient. The `constructor()` runs once per instance (unique data). And the methods go on `prototype` (shared behaviour).


In simple terms - **A prototype is where JavaScript stores shared behavior for all objects created from a class or constructor.**

**Example: (Designing an OOP)**

```js

class Animal{
  constructor (color= "yellow", energy= 100){
    this.color=color;
    this.energy=energy;
  }
  isActive(){
    if(this.energy>0){
      this.energy= this.energy-20;
      console.log("Value of energy decreasing", this.energy);
   }else if(this.energy==0){
      this.sleep();
    }
  }
    sleep(){
      this.energy +=20;
      console.log("Value of energy increasing", this.sleep)
    }
  getColor(){
    console.log(this.color);
  }
  }

  class Cat extends Animal {
    constructor (sound= "purr", canJumpHigh= true, canClimbTrees= true, color, energy){
      super (color,energy)
      this.sound=sound;
      this.canJumpHigh= canJumpHigh;
      this.canClimbTrees= canClimbTrees;
    }
  makeSound(){
    console.log(this.sound);
  }
  }

  class Bird extends Animal{
    constructor (canFly= true, color, energy){
      super (color, energy)
    this.canFly=canFly;
    this.sound=sound;

    }
    makeSound(){
      console.log(this.sound);
    }
  }

class HouseCat extends Cat {
  constructor (houseCatSound= "Meow", sound, canJumpHigh, canClimbTrees, color, energy){
    super (sound, canJumpHigh, canClimbTrees)
    super (color, energy)
    this.houseCatSound= houseCatSound;
  }
  makeSound(option){
    if (option){
      super.makeSound();
    }
      console.log(this.houseCatSound);
    }
  }

  class Tiger extends cat {
    constructor(tigerSound= "Roar", sound, canJumpHigh, canClimbTrees, color, energy){
      super (sound, canJumpHigh, canClimbTrees)
      super (color, energy)
      this.tigerSound=tigerSound;
    }
  makeSound (option){
    if (option){
          super.makeSound();
    }
    console.log(this.tigerSound);
  }
  }

class Parrot extends Bird{
  constructor (canTalk= true , canFly, color, energy){
  super (canFly)
  super (color, energy)
  this.canTalk=canTalk;
}
makesound(option){
  if (option){
    super.makeSound();

  }
  if (this.canTalk){
    console.log("This is a talking parrot");
  }
}
}

var fiji = new Parrot(false); // we're passing `false` to the constructor so that fiji can't talk
var polly = new Parrot(true); // we're passing `true` to the constructor so that polly can talk

fiji.makeSound(); // undefined
fiji.makeSound(true); // chirp

polly.makeSound(); // I'm a talking parrot!
polly.makeSound(true); // chirp, I'm a talking parrot!

polly.color; // yellow
polly.energy; // 100

polly.isActive(); // Energy is decreasing, currently at: 80

var penguin = new Bird("shriek", false, "black and white", 200); // setting all the custom properties
penguin; // Bird {color: 'black and white', energy: 200, sound: 'shriek', canFly: false }

penguin.sound; // 'shriek'
penguin.canFly; // false
penguin.color; // 'black and white'
penguin.energy; // 200
penguin.isActive(); // Energy is decreasing, currently at: 180

var leo = new HouseCat();

// leo, no purring please:
leo.makeSound(false); // meow
// leo, both purr and meow now:
leo.makeSound(true); // purr, meow

var cuddles = new Tiger();
cuddles.makeSound(false); // Roar!
cuddles.makeSound(true); // purr, Roar!
```

## De-structuring arrays and objects

Destructuring lets you **unpack** values from arrays or objects into separate variables.

### Array De-structuring:

```js
const colors = ["red", "green", "blue"];
const [first, second] = colors;
console.log(first); // red
```

| Feature       | Example                          | Result                      |
| ------------- | -------------------------------- | --------------------------- |
| Skip elements | `[ , , last] = colors`           | `"blue"`                    |
| Default value | `[x, y = "yellow"] = ["orange"]` | `"yellow"`                  |
| Swap values   | `[a, b] = [b, a]`                | Exchanges variable contents |


### Object Destructuring 

```js
const user = { name: "Alex", age: 25 };
const { name, age } = user;
console.log(name); // Alex
```

| Feature         | Example                      | Result              |
| --------------- | ---------------------------- | ------------------- |
| Rename variable | `{ name: username } = user`  | `username = "Alex"` |
| Default value   | `{ city = "Berlin" } = user` | `"Berlin"`          |

## `for...of` loops and objects

Use `for of` loops to loop over iterable data types (arrays, strings, sets, maps).

```js
const fruits = ["apple", "banana", "cherry"];
for (let fruit of fruits) console.log(fruit); // apple banana cherry
```

It is simpler than traditional `for (let i = 0; i < arr.length; i++)`

Works only with `iterables`, not plain objects. **Example:**

```js
const car = {
    speed: 100,
    color: "blue"
}

for(prop of car) {
    console.log(prop)
}           // the code will throw a "Uncaught typeError: Car is not iterable"
```

You can use the fact that a `for of` loop can be run on arrays to loop over objects. But the use of following built-in methods need to be known to convert an object into an iterable form (like an array), then `for...of` loop can be used to iterate over it.

### The `Object.keys()` method

The `Object.keys()` method receives an object as its parameter. Remember, this object is **the object you want to loop over.**

**Example:**

```js
const car2 = {
    speed: 200,
    color: "red"
}
console.log(Object.keys(car2)); // ['speed','color'] 
```

So when I run `object.keys` and pass it the `car2` object, **the returned value is an array of strings**, where each string is a property key of the properties contained in the `car2` object. 


### The `Object.values()` method

```js
const car3 = {
    speed: 300,
    color: "yellow"
}
console.log(Object.values(car3)); // [300, 'yellow']
```

Similar to `Object.keys()`, this method returns an array of strings where each string is a property value of the properties contained in the `car3` object.

### The `Object.entries()` method:

Another useful method, `Object.entries()`, which returns an array listing both the keys and the values. 

```js
const car4 = {
    speed: 400,
    color: 'magenta'
}
console.log(Object.entries(car4)); //[ ['speed', 400], ['color', 'magenta'] ]
```

Now with the help of the above built-in methods, one can **loop over any object's own property keys and values**

**Example:**

```js
var clothingItem = {
    price: 50,
    color: 'beige',
    material: 'cotton',
    season: 'autumn'
}

for( const key of Object.keys(clothingItem) ) {
    console.log(key, ":", clothingItem[key])
}
```

This code demonstrates how to access an object's member using the brackets notation. We are trying to access the value of a property by its key name using the Object.keys() function on the clothingItem object. 
Another example below:

```js
function testBracketsDynamicAccess() {
  var dynamicKey;
  if(Math.random() > 0.5) {
    dynamicKey = "speed";
   }else{
     dynamicKey = "color";
   }

    var drone = {
      speed: 15,
      color: "orange"
    }

    console.log(drone[dynamicKey]);
}
testBracketsDynamicAccess();
```

Here, we are accessing the **value** of a property by its key name, chosen dynamically at runtime. 



## `for...in` loops and objects

The `for...in` loop iterates over the keys (or property names) of an object. It's used to loop through the properties of an object, not the values. 

```js
const person = { name: "Bob", age: 30 };
for (let key in person) console.log(key, person[key]);
```

Use for **objects**, not arrays (as order isn't guaranteed).


**The difference:** 

The `for...in` loop iterates over **all enumerable properties** of an object, including those inherited from its **prototype**.
In contrast, the `for...of` loop (used with `Object.keys()`) iterates only over the **object’s own properties**, making it more reliable for object iteration.

```js
let car = { engine: "V8" };
let sportsCar = Object.create(car);
sportsCar.speed = "fast";

console.log("🧠 for...in loop:");
for (let prop in sportsCar) {
  console.log("🤔", prop); // includes prototype properties
}

console.log("\n🎯 for...of loop:");
for (let prop of Object.keys(sportsCar)) {
  console.log("🎯", prop); // only own properties
}

/*🧠 for...in loop:
🤔 speed
🤔 engine

🎯 for...of loop:
🎯 speed
*/
```

### Template literals

Template literals are an alternative way of working with strings. There are several ways in which a template string is different from a regular string. 

#### It allows for **variable interpolation**

```js
let greet = "Hello";
let place = "World";
console.log(`${greet} ${place} !`) //display both variables using template literals.
//outputs Hello World! 
```

#### Template strings can span multiple lines. 

**Example:**

```js
const message = `
Dear Alex,

Your order has been shipped successfully!
It will arrive in 3-5 business days.

Thank you for shopping with us.
- The Store Team
`;

console.log(message);

//Output will be exactly the same, which can't be done using String literals.
```

#### The syntax actually allows for **Expression evaluation**

//it's possible to perform arithmetic operation inside a template literal expression

```js
console.log(`${1 + 1 + 1 + 1 + 1} stars!`);
// 5 stars!
```

## Data Structures

JavaScript includes built-in data structures for efficient data storage. 

| Structure             | Description                                              | Example                      |
| --------------------- | -------------------------------------------------------- | ---------------------------- |
| **Array**             | Ordered collection                                       | `[1,2,3]`                    |
| **Object**            | Key-value pairs                                          | `{name:"Alice"}`             |
| **Map**               | Key-value pairs (any type as key)                        | `new Map([["a",1]])`         |
| **Set**               | Collection of unique values                              | `new Set([1,2,2])` → `{1,2}` |
| **WeakMap / WeakSet** | Like Map/Set, but keys are objects and garbage-collected | –                            |

**Some built in methods that are available on arrays:**

### The `forEach()` method

Arrays in JavaScript come with a handy method that allows you to loop over each of their members.

```js
const fruits = ['kiwi','mango','apple','pear'];
function appendIndex(fruit, index) {
    console.log(`${index}. ${fruit}`)
}
fruits.forEach(appendIndex);
/*0. kiwi
1. mango
2. apple
3. pear*/
```
the `forEach()` method accepts **a function that will work on each array item**. That function's first parameter is the current array item itself, and the second (optional) parameter is the index.


### The `filter()` method

Another very useful method on the array is the `filter()` method. It filters your arrays **based on a specific test**. Those array items that pass the test are returned.

```js
const nums = [0,10,20,30,40,50];
nums.filter( function(num) {
    return num > 20;
    console.log(result);
})
//[30,40,50]
```

### The Map method

The `map()` method is used to map each array item over to another array's item, based on whatever work is performed inside the function that is passed-in to the map as a parameter.

```js
[0,10,20,30,40,50].map( function(num) {
    return num / 10
})
//[0,1,2,3,4,5]
```

### Working with Objects in Javascript

**Example:** Convert an object to an array

```js
const result=[];
const drone = {
  speed: 100,
  color: "yellow"
}

const droneKeys= object.keys(drone){
  droneKeys.forEach(function(key)){
    result.push(key,drone[key])
  }
}
console.log(result)

//['speed',100,'color','yellow']
```

### Working with Maps in JavaScript

To make a new Map, you can use the `Map()` constructor.
However, it doesn't have inheritance. No prototypes! This makes it useful as a data storage. 

**Example:**

```js
let bestBoxers = new Map();
bestBoxers.set(1, "The Champion");
bestBoxers.set(2, "The Runner-up");
bestBoxers.set(3, "The third place");

console.log(bestBoxers);
//Map(3) {1 => 'The Champion', 2 => 'The Runner-up', 3 => 'The third place'}
```

### Working with sets in JavaScript

A set is a collection of unique values. To build a new set, you can use the `Set()` constructor.

This constructor can, for example, accept an array. We can use it to quickly filter an array for unique numbers. 

```js
const repetitiveFruits = ['apple','pear','apple','pear','plum', 'apple'];
const uniqueFruits = new Set(repetitiveFruits);
console.log(uniqueFruits);
//{'apple', 'pear', 'plum'}
```

### Spread Operator (...)

Expands arrays, objects or strings into individual elements or properties. Used for concatenation, copying or passing arguments. 

#### Joining arrays and objects using the spread operator.

Its easy to concatenate objects and arrays using the spread operator.

```js
const fruits = ['apple', 'pear', 'plum'];
const berries = ['blueberry', 'strawberry'];
const fruitsAndBerries = [...fruits, ...berries]; // concatenate
console.log(fruitsAndBerries); // outputs a single array
//['apple', 'pear', 'plum', 'blueberry', 'strawberry']
```

Joining objects:

```js
const flying = { wings: 2 };
const car = { wheels: 4 };
const flyingCar = {...flying, ...car};
console.log(flyingCar); // {wings: 2, wheels: 4}
```

#### Add new members to arrays without using the `push()` method:

```js
let veggies = ['onion', 'parsley'];
veggies = [...veggies, 'carrot', 'beetroot'];
console.log(veggies);
//['onion', 'parsley', 'carrot', 'beetroot'];
```

#### Convert a string to an array using the spread operator

Given a string, it's easy to spread it out into separate array items:

```js
const anyString= "JavaScript"
const arrayOfChars = [...anyString];
console.log(arrayOfChars);
//["J", "a", "v", "a", "S", "c", "r", ...]
```

#### Copy either an object or an array into a seperate one.

**Object for Example:**

```js
const car1 = {
    speed: 200,
    color: 'yellow'
}
const car2 = {...car1};

car1.speed = 201;

console.log(car1.speed, car2.speed);
// 201,200
```

**Array for Example:**

```js
const fruits1 = ['apples', 'pears'];
const fruits2 = [...fruits1];
fruits1.pop();
console.log(fruits1, "not", fruits2);
//['apples'] 'not' ['apples','pears'];
```

### Rest Operator (...)

Collects multiple arguments into a single array.

**Example:**

```js
function sum(...nums) {
  return nums.reduce((a,b)=>a+b);
}
console.log(sum(1,2,3)); // 6
```

Spread **expands**, rest **collects**

## JavaScript Interactivity and DOM Manipulation

### JavaScript DOM Manipulation

The **DOM (Document Object Model)** represents the structure of a web page as a tree of elements that JavaScript can read and modify.

1. Every HTML element (like `<p>`, `<div>`, `<img>`) is represented as a **node** in this tree.
2. Using JavaScript, you can **find**, **change, add** or **remove** elements dynamically.

**Example:**

```html
<p id="demo">Hello!</p>
<script>
document.getElementById("demo").innerHTML = "Hello, JavaScript!";
</script>
```

Changes the content of the paragraph dynamically.

| Common DOM Methods             | Description                                         |
| ------------------------------ | --------------------------------------------------- |
| `getElementById(id)`           | Finds an element by its ID                          |
| `getElementsByClassName(name)` | Returns all elements with a given class             |
| `getElementsByTagName(name)`   | Returns all elements with a given tag               |
| `querySelector(selector)`      | Finds the first element that matches a CSS selector |
| `querySelectorAll(selector)`   | Finds *all* matching elements                       |

### JavaScript Interactivity

JS makes webpages interactive- responding to clicks, typing, mouse movement etc.

**Examples of Interactivity:**

1. Change text or color when a button is clicked.
2. Show/hide elements dynamically.
3. Display alerts or messages.

```html
<button onclick="changeText()">Click Me</button>
<p id="text">Original Text</p>

<script>
function changeText() {
  document.getElementById("text").innerText = "You clicked the button!";
}
</script>
```

### JavaScript Selectors

| Selector                   | Example                                  | Description                            |
| -------------------------- | ---------------------------------------- | -------------------------------------- |
| `getElementById()`         | `document.getElementById("title")`       | Selects by ID                          |
| `getElementsByClassName()` | `document.getElementsByClassName("btn")` | Selects by class (returns list)        |
| `querySelector()`          | `document.querySelector("p.intro")`      | Selects first match using CSS selector |
| `querySelectorAll()`       | `document.querySelectorAll("div > p")`   | Selects all matching elements          |


### Event Handling

Events are actions that occur on a webpage (clicking, typing, scrolling, etc.), and event handlers are JavaScript functions that respond to them.

| Event         | Triggered When…           | Example                      |
| ------------- | ------------------------- | ---------------------------- |
| `onclick`     | User clicks an element    | `button.onclick = func`      |
| `onmouseover` | Mouse hovers over element | Change color or show tooltip |
| `onchange`    | Input value changes       | Validate input               |
| `onload`      | Page finishes loading     | Initialize app               |


## JSON (JavaScript Object Notation)

### What is JSON?

- A lightweight **data exchange format**
- Based on **JavaScript object syntax**
- Used to send/receive data between client and server

**Example:**

```json
{
  "name": "Alex",
  "age": 25,
  "isStudent": false
}
```

#### JSON vs Javascript Object

| Feature           | JSON                         | JavaScript Object |
| ----------------- | ---------------------------- | ----------------- |
| Keys              | Must be in **double quotes** | Quotes optional   |
| Data types        | Limited                      | More flexible     |
| Functions allowed | No                           | Yes             |
| Purpose           | Data transfer                | Logic + data      |

#### JSON methods in Javascript

**Convert object to JSON:**

```js
const user = { name: "Alex", age: 25 };
const jsonStr = JSON.stringify(user);
```

**Convert JSON to object:**

```js
const obj = JSON.parse(jsonStr);
```

## Testing and JavaScript Environments

JavaScript is not limited to the browser.  
It can also run on the **server** using **Node.js**.

### Node.js

- A runtime that allows JavaScript to run outside the browser
- Used for backend development, APIs, tools

### Testing

Confirming that software works as specified in the software's requirements.
Testing ensures your code: Conciseness, Clarity and Repeatability

- Works correctly
- Handles edge cases
- Doesn’t break when updated


**Why testing matters:**

- Reduces bugs
- Improves reliability
- Helps maintain large projects

#### Types of Testing

| Type                    | Description                                   |
| ----------------------- | --------------------------------------------- |
| **Unit Testing**        | Test individual functions/components          |
| **Integration Testing** | Test how multiple parts work together         |
| **End-to-End (E2E)**    | Test full application flow (user perspective) |

Unit is the smallest piece of code that you can test seperately from the rest of the app. 

#### Red-Green Refractor Cycle

**Refactoring:** Updating code without affecting the results it produces.

1. **Red:** Write a test that **fails**. No implementation yet.
2. **Green:** Write the **minimum code** to pass the test.
3. **Refactor:** Improve code (clean, optimize). Ensure tests still pass without changing results.


#### Manual vs Automated Testing

| Type | Description | Example |
|------|-------------|----------|
| **Manual Testing** | Humans test the app manually | Clicking buttons, filling forms |
| **Automated Testing** | Code tests the app | Jest test cases |

### JEST

- A **JavaScript testing framework**
- Used to write and run **automated tests**
- Works well with **React / Node / Frontend apps**

**Basic Example:**

```js
function add(a, b) {
  return a + b;
}

test("adds two numbers", () => {
  expect(add(2, 3)).toBe(5);
});
```

#### Key Functions

| Function   | Purpose               |
| ---------- | --------------------- |
| `test()`   | Defines a test case   |
| `expect()` | Value to test         |
| `.toBe()`  | Checks exact equality |

#### Common Matches

| Matcher        | Description                            | Example                      |
| -------------- | -------------------------------------- | ---------------------------- |
| `toBe()`       | Exact value match                      | `expect(2+2).toBe(4)`        |
| `toEqual()`    | Deep equality (objects/arrays)         | `expect(obj).toEqual({...})` |
| `toBeTruthy()` | Checks truthy value                    | `expect(val).toBeTruthy()`   |
| `toBeFalsy()`  | Checks falsy value                     | `expect(val).toBeFalsy()`    |
| `toContain()`  | Checks if value exists in array/string | `expect(arr).toContain(3)`   |

#### Unit testing with JEST

Testing small, individual functions

```js
function isEven(num) {
  return num % 2 === 0;
}

test("checks even numbers", () => {
  expect(isEven(4)).toBe(true);
});
```

### Mocking in JEST

Mocking replaces real functions or modules with fake versions. Used when: API calls, Database access, External dependencies.

**Example: Mock Function**

```js
const mockFn = jest.fn();

mockFn();
mockFn();

expect(mockFn).toHaveBeenCalledTimes(2);
```

**Example: Mocking API**

```js
global.fetch = jest.fn(() =>
  Promise.resolve({
    json: () => Promise.resolve({ data: "test" })
  })
);

test("fetches data", async () => {
  const res = await fetch();
  const data = await res.json();

  expect(data.data).toBe("test");
});
```

#### Snapshot Testing

- Saves a snapshot of UI output
- Compares future output with saved version
- Detects unexpected changes.


### Test File Structure in Jest

- Tests are usually written in separate files
- Common naming:
  - `add.js` → main code
  - `add.test.js` → test file

**Example:**

```js
// add.js
export function add(a, b) {
  return a + b;
}

// add.test.js
import { add } from "./add";

test("adds two numbers", () => {
  expect(add(2, 3)).toBe(5);
});
```

Test-Driven Development is a process where you:

👉 **Write tests BEFORE writing the actual code**

Instead of:
- Write code → then test

You do:
- Write test → then write code

---

### TDD Cycle (Red → Green → Refactor)

#### Red (Failing Test)

- Write a test for functionality
- The test **fails** (because code doesn't exist yet)

```js
test("adds 2 numbers", () => {
  expect(add(2, 3)).toBe(5);
});
```

#### Green (Make it pass)

```js
function add(a, b) {
  return a + b;
}
```


#### Refractor (Improve Code)

- Clean and optimize code
- Ensure tests still pass

// Same logic, cleaner structure if needed.

