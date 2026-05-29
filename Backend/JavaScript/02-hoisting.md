# JavaScript: Hoisting

## 📌 Definition

Hoisting is JavaScript's behavior of moving declarations to the top of their scope before code execution.

This does NOT mean values are moved—only declarations.

---

# Why Hoisting Exists

JavaScript executes code in two phases:

### 1. Memory Creation Phase

* Variables are allocated memory.
* Function declarations are stored completely.

### 2. Execution Phase

* Values are assigned.
* Code runs line by line.

---

# Example 1: var Hoisting

```javascript
console.log(a);

var a = 10;
```

### Output

```javascript
undefined
```

### What JavaScript Sees

```javascript
var a;

console.log(a);

a = 10;
```

---

# Example 2: let Hoisting

```javascript
console.log(age);

let age = 20;
```

### Output

```javascript
ReferenceError
```

---

# Example 3: const Hoisting

```javascript
console.log(PI);

const PI = 3.14;
```

### Output

```javascript
ReferenceError
```

---

# Temporal Dead Zone (TDZ)

The TDZ is the time between:

```javascript
Variable Declaration
        ↓
Variable Initialization
```

During this period, accessing the variable causes an error.

Example:

```javascript
console.log(score);

let score = 100;
```

The variable exists in memory but cannot be accessed yet.

---

# Function Hoisting

Function declarations are fully hoisted.

```javascript
greet();

function greet() {
    console.log("Hello");
}
```

### Output

```javascript
Hello
```

---

# Function Expression Hoisting

```javascript
greet();

var greet = function () {
    console.log("Hello");
};
```

### Output

```javascript
TypeError
```

### Why?

```javascript
var greet;

greet(); // undefined()

greet = function () {};
```

The variable is hoisted, not the function body.

---

# Arrow Function Hoisting

```javascript
sayHi();

const sayHi = () => {
    console.log("Hi");
};
```

### Output

```javascript
ReferenceError
```

---

# Interview Keywords

🔑 "Memory Creation Phase"

🔑 "Execution Phase"

🔑 "Temporal Dead Zone"

🔑 "Function Declaration"

🔑 "Function Expression"

🔑 "ReferenceError"

---

# Common Mistakes

### Mistake 1

Thinking let and const are not hoisted.

❌ Wrong

They are hoisted but remain inside TDZ.

---

### Mistake 2

Thinking hoisting moves values.

❌ Wrong

Only declarations are hoisted.

---

# Interview Trap

```javascript
var x = 5;

function test() {
    console.log(x);

    var x = 10;
}

test();
```

### Output

```javascript
undefined
```

### Why?

JavaScript sees:

```javascript
function test() {
    var x;

    console.log(x);

    x = 10;
}
```

The local variable shadows the global variable.

---

# Quick Revision

✅ JavaScript runs in two phases

✅ var is hoisted and initialized with undefined

✅ let and const are hoisted but stay in TDZ

✅ Function declarations are fully hoisted

✅ Function expressions are not fully hoisted

✅ Hoisting moves declarations, not values
