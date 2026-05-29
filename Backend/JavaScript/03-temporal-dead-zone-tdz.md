# 03. Temporal Dead Zone (TDZ)

## 📌 Definition

The Temporal Dead Zone (TDZ) is the period between entering a scope and initializing a variable declared with `let` or `const`.

During this period, the variable exists in memory but cannot be accessed.

---

## Why TDZ Exists

TDZ helps prevent bugs by ensuring variables are declared before they are used.

It makes JavaScript behavior safer and more predictable.

---

## Example 1: TDZ with let

```javascript
console.log(age);

let age = 20;
```

### Output

```javascript
ReferenceError: Cannot access 'age' before initialization
```

### Explanation

The variable is hoisted but remains inside the TDZ until initialization.

---

## Example 2: TDZ with const

```javascript
console.log(PI);

const PI = 3.14;
```

### Output

```javascript
ReferenceError: Cannot access 'PI' before initialization
```

---

## Example 3: No TDZ with var

```javascript
console.log(city);

var city = "Delhi";
```

### Output

```javascript
undefined
```

### Explanation

`var` is hoisted and initialized with `undefined`.

Therefore, no TDZ exists.

---

## Memory Visualization

```text
Memory Phase
-----------------
age → uninitialized

Execution Phase
-----------------
console.log(age) ❌

let age = 20; ✅

console.log(age) → 20
```

---

## TDZ Timeline

```text
Start of Scope
      │
      ▼
TDZ Begins
      │
      ▼
let age = 20
      │
      ▼
TDZ Ends
      │
      ▼
Variable Accessible
```

---

## var vs let vs const

| Feature                      | var       | let            | const          |
| ---------------------------- | --------- | -------------- | -------------- |
| Hoisted                      | ✅         | ✅              | ✅              |
| TDZ                          | ❌         | ✅              | ✅              |
| Access Before Initialization | undefined | ReferenceError | ReferenceError |

---

## 🎯 Interview Keywords

* Temporal Dead Zone (TDZ)
* Hoisting
* Memory Creation Phase
* Execution Phase
* ReferenceError
* Block Scope

---

## 🚨 Common Interview Trap

```javascript
{
    console.log(score);

    let score = 100;
}
```

### Output

```javascript
ReferenceError
```

The variable exists in memory but is inside the TDZ.

---

## 📝 Quick Revision

* TDZ applies to `let` and `const`.
* TDZ starts when scope begins.
* TDZ ends when variable is initialized.
* Accessing a variable inside TDZ causes a `ReferenceError`.
* `var` does not have a TDZ.
* `let` and `const` are hoisted but remain uninitialized.
