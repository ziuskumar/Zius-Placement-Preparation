# 02. Object-Oriented Programming (OOP)

---

# 📖 Introduction

Object-Oriented Programming (OOP) is a programming paradigm that organizes software around **objects** instead of functions.

Every object represents a real-world entity that contains:

- Data (Attributes)
- Behavior (Methods)

LLD is built on OOP concepts.

---

# 📌 Definition

> **Object-Oriented Programming (OOP) is a programming paradigm that models software using classes and objects, allowing code to be modular, reusable, and maintainable.**

---

# ❓ Why OOP?

Imagine developing an application with thousands of lines of code.

Without OOP:

- Code duplication
- Difficult maintenance
- Poor scalability
- Hard debugging

OOP solves these problems by organizing code into reusable components.

---

# 🏗️ Basic Terminologies

## Class

A class is a blueprint for creating objects.

Example:

```java
class Car {

}
```

---

## Object

An object is an instance of a class.

```java
Car car1 = new Car();
```

---

## Attributes

Variables inside a class.

```java
class Car{

    String company;
    String model;

}
```

---

## Methods

Functions inside a class.

```java
void start(){

}
```

---

# 🌍 Real World Analogy

## Car

Class

```
Car
```

Objects

```
BMW
Audi
Tesla
Ferrari
```

Each object has different values but follows the same blueprint.

---

# 🏛️ Four Pillars of OOP

## 1. Encapsulation

Wrapping data and methods together into one unit.

```java
class Student{

    private int age;

    public void setAge(int age){
        this.age = age;
    }

}
```

Benefits

- Data Hiding
- Better Security
- Controlled Access

---

## 2. Abstraction

Showing only important information while hiding implementation details.

Example

```
ATM Machine

Visible:
Withdraw
Deposit

Hidden:
Database
Network Calls
Verification
```

Benefits

- Simplicity
- Security
- Easy Maintenance

---

## 3. Inheritance

One class acquires properties of another.

```java
class Animal{

    void eat(){}

}

class Dog extends Animal{

}
```

Benefits

- Code Reuse
- Extensibility

---

## 4. Polymorphism

One interface, multiple implementations.

Compile Time

```
Method Overloading
```

Run Time

```
Method Overriding
```

Example

```java
class Animal{

    void sound(){
        System.out.println("Animal");
    }

}

class Dog extends Animal{

    @Override
    void sound(){
        System.out.println("Bark");
    }

}
```

---

# 📊 OOP Summary

| Concept | Purpose |
|----------|----------|
| Class | Blueprint |
| Object | Instance |
| Encapsulation | Data Hiding |
| Abstraction | Hide Complexity |
| Inheritance | Code Reuse |
| Polymorphism | Multiple Behaviors |

---

# 🏗️ OOP Architecture

```text
           Class
             │
     Creates Objects
             │
             ▼
        +-----------+
        |  Object   |
        +-----------+
             │
      ┌──────┴──────┐
      ▼             ▼
 Attributes      Methods
```

---

# 🌍 Real-World Example

Instagram User

Attributes

- username
- followers
- posts

Methods

- login()
- uploadPost()
- followUser()
- likePost()

---

# 🎯 Why OOP is Important in LLD?

Almost every LLD interview question starts with designing:

- Classes
- Objects
- Relationships

Without OOP, LLD cannot be implemented effectively.

---

# 🎯 Interview Keywords

- Class
- Object
- Encapsulation
- Abstraction
- Inheritance
- Polymorphism
- Constructor
- Method
- Object Creation
- Instance Variable

---

# 🚨 Common Mistakes

❌ Confusing Class and Object.

❌ Thinking Inheritance means copying code.

❌ Ignoring Encapsulation.

❌ Using Public variables everywhere.

❌ Violating Single Responsibility Principle.

---

# 🔥 Interview Questions

### What is OOP?

Programming using classes and objects.

---

### Difference between Class and Object?

Class is a blueprint.

Object is an instance of a class.

---

### Name the four pillars of OOP.

- Encapsulation
- Abstraction
- Inheritance
- Polymorphism

---

### Why is OOP used in LLD?

Because software components are designed using classes, objects, and their relationships.

---

# 🧠 Quick Revision

- ✅ Class → Blueprint
- ✅ Object → Instance
- ✅ Encapsulation → Data Hiding
- ✅ Abstraction → Hide Complexity
- ✅ Inheritance → Code Reuse
- ✅ Polymorphism → Multiple Behaviors
- ✅ OOP is the foundation of LLD.