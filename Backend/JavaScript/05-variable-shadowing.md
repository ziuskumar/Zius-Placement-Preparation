# 05. Variable Shadowing

## 📌 Definition

Variable Shadowing occurs when a variable declared inside a local scope has the same name as a variable in an outer scope.

The inner variable hides (or shadows) the outer variable within that scope.

---

## Why Variable Shadowing Happens

JavaScript always searches for variables from the current scope outward.

If it finds a variable in the current scope, it stops searching further.

---

## Example 1: Basic Shadowing

```javascript
let company = "Cognizant";

function employee() {
    let company = "Google";

    console.log(company);
}

employee();
```

### Output

```javascript
Google
```

### Explanation

JavaScript finds `company` inside the function.

Therefore it does not use the global variable.

---

## Example 2: Accessing Global Variable Outside Function

```javascript
let company = "Cognizant";

function employee() {
    let company = "Google";

    console.log(company);
}

employee();

console.log(company);
```

### Output

```javascript
Google
Cognizant
```

### Explanation

The local variable exists only inside the function.

Outside the function, the global variable is used.

---

## Scope Visualization

```text
Global Scope
│
├── company = "Cognizant"
│
└── employee()
     │
     └── company = "Google"
```

The inner variable shadows the outer variable.

---

## Example 3: Block Scope Shadowing

```javascript
let city = "Delhi";

{
    let city = "Mumbai";

    console.log(city);
}

console.log(city);
```

### Output

```javascript
Mumbai
Delhi
```

---

## Illegal Shadowing

### ❌ Not Allowed

```javascript
let name = "Lucky";

{
    var name = "Kumar";
}
```

### Output

```javascript
SyntaxError
```

### Why?

`var` is function-scoped and tries to redeclare a `let` variable in the same scope.

JavaScript does not allow this.

---

## Legal Shadowing

### ✅ Allowed

```javascript
var name = "Lucky";

{
    let name = "Kumar";
}

console.log(name);
```

### Output

```javascript
Lucky
```

---

## Shadowing vs Scope Chain

| Variable Shadowing       | Scope Chain             |
| ------------------------ | ----------------------- |
| Hides outer variable     | Finds variables         |
| Same variable name       | Variable lookup process |
| Stops search immediately | Searches outward        |

---

## 🎯 Interview Keywords

* Variable Shadowing
* Lexical Scope
* Scope Chain
* Local Scope
* Global Scope
* Block Scope
* Illegal Shadowing

---

## 🚨 Common Interview Trap

```javascript
let a = 10;

function test() {
    let a = 20;

    console.log(a);
}

test();
```

### Output

```javascript
20
```

Many developers expect `10`.

But JavaScript always prefers the nearest variable.

---

## Real Interview Rule

```text
Nearest Variable Wins
```

Whenever JavaScript finds a variable in the current scope, it stops searching.

---

## 📝 Quick Revision

* Variable Shadowing occurs when inner and outer variables have the same name.
* Inner variable hides the outer variable.
* JavaScript always prefers the nearest variable.
* Shadowing is based on Scope Chain.
* Block scope and function scope can both create shadowing.
* Illegal shadowing causes a SyntaxError.
