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

```js
if
}