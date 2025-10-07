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

JavaScript operators are grouped by purpose: **Arithmetic**, **Assignment**, **Comparison**, **Logical**, **String**, and **Others**.

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

## Logical Operators

Used to combine or invert Boolean expressions.

| Operator | Description | Example | Output |
|-----------|--------------|----------|--------|
| `&&` | Logical AND (true only if both are true) | `(5 > 3 && 8 > 6)` | `true` |
| `||` | Logical OR (true if at least one is true) | `(5 > 10 || 3 < 8)` | `true` |
| `!` | Logical NOT (reverses the value) | `!(5 > 3)` | `false` |

---

## String Operator

- The `+` operator can also **concatenate (join)** strings.

```js
let first = "Hello";
let last = "World";
console.log(first + " " + last); // "Hello World"
```