# JavaScript: var vs let vs const

## 📌 Introduction

In JavaScript, `var`, `let`, and `const` are used to declare variables.

ES6 introduced `let` and `const` to solve problems related to scope and accidental reassignment.

---

# 1️⃣ var

## Definition

`var` declares a variable with **function scope**.

It can be:

* Re-declared
* Re-assigned

## Example

```javascript
var city = "Delhi";

var city = "Mumbai"; // Allowed

city = "Chandigarh"; // Allowed

console.log(city);
```

### Output

```javascript
Chandigarh
```

---

## Scope Example

```javascript
if (true) {
    var name = "Lucky";
}

console.log(name);
```

### Output

```javascript
Lucky
```

### Why?

Because `var` ignores block scope and is function scoped.

---

## Hoisting

```javascript
console.log(a);

var a = 10;
```

### Output

```javascript
undefined
```

### Explanation

JavaScript hoists:

```javascript
var a;

console.log(a);

a = 10;
```

---

# 2️⃣ let

## Definition

`let` declares a variable with **block scope**.

It can be:

* Re-assigned ✅
* Re-declared ❌

---

## Example

```javascript
let age = 20;

age = 21;

console.log(age);
```

### Output

```javascript
21
```

---

## Re-declaration Error

```javascript
let age = 20;

let age = 21;
```

### Output

```javascript
SyntaxError
```

---

## Block Scope

```javascript
if (true) {
    let marks = 90;
}

console.log(marks);
```

### Output

```javascript
ReferenceError
```

### Why?

`marks` exists only inside the block.

---

## Hoisting & TDZ

```javascript
console.log(score);

let score = 100;
```

### Output

```javascript
ReferenceError
```

### Why?

`let` is hoisted but stays inside the **Temporal Dead Zone (TDZ)** until initialization.

---

# 3️⃣ const

## Definition

`const` creates a block-scoped variable whose reference cannot be reassigned.

It:

* Cannot be re-declared ❌
* Cannot be re-assigned ❌

---

## Example

```javascript
const PI = 3.14;

console.log(PI);
```

### Output

```javascript
3.14
```

---

## Re-assignment Error

```javascript
const PI = 3.14;

PI = 3.14159;
```

### Output

```javascript
TypeError
```

---

## Objects with const

```javascript
const person = {
    name: "Lucky"
};

person.name = "Karan";

console.log(person.name);
```

### Output

```javascript
Karan
```

### Why?

The object contents can change.

Only the reference cannot change.

---

# 🔥 var vs let vs const

| Feature         | var      | let   | const |
| --------------- | -------- | ----- | ----- |
| Scope           | Function | Block | Block |
| Re-declare      | ✅        | ❌     | ❌     |
| Re-assign       | ✅        | ✅     | ❌     |
| Hoisted         | ✅        | ✅     | ✅     |
| TDZ             | ❌        | ✅     | ✅     |
| Preferred Today | ❌        | ✅     | ✅     |

---

# 🎯 Interview Keywords

### "Block Scope"

Think:

* let
* const

### "Function Scope"

Think:

* var

### "Temporal Dead Zone (TDZ)"

Think:

* let
* const

### "Hoisting"

Think:

* var → undefined
* let/const → ReferenceError

---

# 🚨 Common Interview Trap

```javascript
for (var i = 0; i < 3; i++) {
    setTimeout(() => console.log(i), 0);
}
```

Output:

```javascript
3
3
3
```

Because all callbacks share the same `i`.

---

```javascript
for (let i = 0; i < 3; i++) {
    setTimeout(() => console.log(i), 0);
}
```

Output:

```javascript
0
1
2
```

Because `let` creates a new binding for every iteration.

---

# 📝 Quick Revision

* Use `const` by default.
* Use `let` when value changes.
* Avoid `var` in modern JavaScript.
* `var` → function scope.
* `let` & `const` → block scope.
* `let` & `const` have TDZ.
* `const` prevents reassignment, not object mutation.
