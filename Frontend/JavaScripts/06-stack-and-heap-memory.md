# 06. Stack and Heap Memory

## 📌 Introduction

JavaScript uses two types of memory allocation:

1. Stack Memory
2. Heap Memory

Both are used differently depending on the type of data.

---

# Stack Memory

## Definition

Stack memory is used for:

* Primitive data types
* Function execution
* Static memory allocation

---

## Primitive Data Types

* Number
* String
* Boolean
* null
* undefined
* BigInt
* Symbol

---

## Stack Characteristics

* Fast access
* Fixed size
* Stores copy of values
* Automatically managed

---

## Example 1: Primitive Values

```javascript id="hzg4r4"
let a = 10;

let b = a;

b = 20;

console.log(a);
console.log(b);
```

### Output

```javascript id="9s4m6f"
10
20
```

---

## Explanation

`b` gets a copy of `a`.

Changing `b` does not affect `a`.

---

## Stack Visualization

```text id="7xqjlwm"
Stack Memory

a → 10
b → 20
```

Both variables store separate copies.

---

# Heap Memory

## Definition

Heap memory is used for:

* Objects
* Arrays
* Functions

Heap stores data dynamically.

---

## Heap Characteristics

* Dynamic size
* Slower than stack
* Stores reference values
* Shared memory location

---

## Example 2: Objects

```javascript id="f1m0rx"
let user1 = {
    name: "Lucky"
};

let user2 = user1;

user2.name = "Kumar";

console.log(user1.name);
console.log(user2.name);
```

### Output

```javascript id="g71wsk"
Kumar
Kumar
```

---

## Explanation

Objects are stored in heap memory.

Variables store references to the same object.

Changing one reference affects both.

---

## Heap Visualization

```text id="4jg6m8"
Stack Memory
----------------
user1 ──┐
        │
user2 ──┘

Heap Memory
----------------
{name: "Kumar"}
```

Both variables point to the same object.

---

# Stack vs Heap

| Feature     | Stack            | Heap             |
| ----------- | ---------------- | ---------------- |
| Stores      | Primitive Values | Objects & Arrays |
| Allocation  | Static           | Dynamic          |
| Speed       | Faster           | Slower           |
| Access      | Direct           | Reference Based  |
| Memory Size | Fixed            | Flexible         |

---

# Example 3: Arrays in Heap

```javascript id="s6dl2p"
let arr1 = [1, 2, 3];

let arr2 = arr1;

arr2.push(4);

console.log(arr1);
console.log(arr2);
```

### Output

```javascript id="2q34ha"
[1, 2, 3, 4]
[1, 2, 3, 4]
```

---

## Why?

Arrays are reference types stored in heap memory.

Both variables point to the same array.

---

# Real Interview Concept

## Primitive → Copy

```javascript id="y5m0hm"
let a = 10;
let b = a;
```

---

## Non-Primitive → Reference

```javascript id="a22fyz"
let obj2 = obj1;
```

---

# Common Interview Trap

```javascript id="k90d3y"
let user1 = {
    name: "Lucky"
};

let user2 = {
    name: "Lucky"
};

console.log(user1 === user2);
```

### Output

```javascript id="q3yih9"
false
```

---

## Why?

Both objects have different memory references.

Objects are compared by reference, not value.

---

# 🎯 Interview Keywords

* Stack Memory
* Heap Memory
* Primitive Types
* Reference Types
* Memory Allocation
* Dynamic Memory
* Pass by Value
* Pass by Reference

---

# 📝 Quick Revision

* Primitive values use stack memory.
* Objects and arrays use heap memory.
* Stack stores copies.
* Heap stores references.
* Primitive changes do not affect original values.
* Object changes affect all references.
* Stack is faster than heap.
