# JavaScript Notes

Helps add interactivity, logic and dynamic behaviour to HTML pages. (Determines webpage behaviour)

Example:

```html
<!DOCTYPE html>
<html>
  <head><title>My First JS</title></head>
  <body>
    <h1>Hello JavaScript!</h1>
    <script>
      console.log("Hello, World!");
      alert("Welcome to JavaScript!");
    </script>
  </body>
</html>
```

(Keep `<script>` tag at the end of `<body>` so HTML loads first)


## Different ways to add Javascript to HTML

1. Inline Script

```html
<button onclick="alert('Button clicked!')">Click me</button>
```

2. Internal Script

Inside the same HTML file within <script>.....</script>

3. External Script

```html
<script src="script.js"></script>
```

(Note that `script.js` should be placed in the same folder)


## Syntax rules

1. Case sensitive
2. Each statement ends with ; (optional)
3. Indentation for readability
4. // for single line comment and /*....*/ for multi line comment.


## Variables and Constants

```js
let age = 25;       // changeable
const pi = 3.1416;  // constant
var city = "Berlin"; // old way (avoid in modern JS)
```

`let`- for values that change

`const`- values that never change

`var`- Used in old JS and avoided.

## Data Tyoes

| Type      | Example                 | Description         |
| --------- | ----------------------- | ------------------- |
| String    | `"Hello"`               | Text                |
| Number    | `42`, `3.14`            | Integers/floats     |
| Boolean   | `true`, `false`         | Logic values        |
| Undefined | declared but no value   | `let a;`            |
| Null      | intentional empty       | `let b = null;`     |
| Object    | `{name:"Alex", age:22}` | key-value pair      |
| Array     | `[1,2,3]`               | List-like structure |

To check a variable's type:

```js
let name= "Udhay";
console.log(typeof name); //string - is the output
```

## Console and Alerts

| Command         | Purpose                              |
| --------------- | ------------------------------------ |
| `console.log()` | Prints messages to browser console   |
| `alert()`       | Popup message on screen              |
| `prompt()`      | Takes user input                     |
| `confirm()`     | OK/Cancel popup returning true/false |

Example:

```js
let user = prompt("Enter your name:");
console.log("Hello, " + user);
alert("Welcome " + user + "!");
```
