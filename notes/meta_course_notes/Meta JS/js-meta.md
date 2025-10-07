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


