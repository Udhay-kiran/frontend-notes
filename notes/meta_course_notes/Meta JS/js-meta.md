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



# Module 2- Building blocks

