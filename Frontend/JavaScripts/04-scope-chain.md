# 04. Scope Chain

## 📌 Definition

A Scope Chain is the mechanism JavaScript uses to find variables.

When a variable is not found in the current scope, JavaScript searches the parent scope, then the grandparent scope, until it reaches the global scope.

---

## Why Scope Chain Exists

Scope Chain allows inner functions to access variables declared in outer functions.

This enables data sharing between nested scopes.

---

## Scope Hierarchy

```text
Global Scope
    │
    ▼
Function Scope
    │
    ▼
Block Scope
```

JavaScript searches from the innermost scope outward.

---

## Example 1: Accessing Global Variable

```javascript
let company = "Cognizant";

function employee() {
    console.log(company);
}

employee();
```

### Output

```javascript
Cognizant
```

### Explanation

JavaScript looks for `company` inside `employee()`.

Not found.

Moves to global scope.

Finds `company`.

---

## Example 2: Nested Functions

```javascript
let company = "Cognizant";

function department() {

    let team = "Java";

    function employee() {
        console.log(company);
        console.log(team);
    }

    employee();
}

department();
```

### Output

```javascript
Cognizant
Java
```

### Explanation

`employee()` can access:

* Its own scope
* Parent scope
* Global scope

This is Scope Chain.

---

## Example 3: Variable Not Found

```javascript
function test() {
    console.log(city);
}

test();
```

### Output

```javascript
ReferenceError
```

### Explanation

JavaScript searches:

```text
Current Scope ❌
Parent Scope ❌
Global Scope ❌
```

Variable not found.

---

## Scope Chain Visualization

```text
employee()
    │
    ▼
department()
    │
    ▼
Global Scope
```

JavaScript searches upward.

Never downward.

---

## Important Rule

JavaScript searches:

```text
Inside → Outside
```

Never:

```text
Outside → Inside
```

---

## Interview Trap

```javascript
let company = "Cognizant";

function department() {

    let company = "Google";

    function employee() {
        console.log(company);
    }

    employee();
}

department();
```

### Output

```javascript
Google
```

### Why?

JavaScript always picks the nearest variable first.

This is called Variable Shadowing.

---

## Scope Chain vs Hoisting

| Scope Chain              | Hoisting                     |
| ------------------------ | ---------------------------- |
| Finds variables          | Creates variables in memory  |
| Happens during execution | Happens before execution     |
| Searches parent scopes   | Moves declarations to memory |

---

## 🎯 Interview Keywords

* Lexical Scope
* Scope Chain
* Global Scope
* Function Scope
* Block Scope
* Variable Shadowing
* Parent Scope
* Nested Functions

---

## Common Mistakes

### Mistake 1

Thinking child scopes can be accessed from parent scopes.

❌ Wrong

Parent cannot access child variables.

---

### Mistake 2

Thinking JavaScript searches downward.

❌ Wrong

JavaScript always searches upward.

---

## 🚨 Common Interview Question

```javascript
let a = 10;

function outer() {

    let b = 20;

    function inner() {
        let c = 30;

        console.log(a);
        console.log(b);
        console.log(c);
    }

    inner();
}

outer();
```

### Output

```javascript
10
20
30
```

Because `inner()` can access its complete scope chain.

---

## 📝 Quick Revision

* Scope Chain helps JavaScript find variables.
* Search starts from current scope.
* JavaScript searches upward only.
* Inner functions can access outer variables.
* Parent functions cannot access child variables.
* Nearest variable wins (Variable Shadowing).
* Scope Chain is based on Lexical Scope.
