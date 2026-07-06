# 01. Introduction to Low-Level Design (LLD)

---

# 📖 Introduction

Low-Level Design (LLD) is the process of designing the internal structure of a software system. It focuses on **how the system is implemented**, including classes, objects, methods, relationships, and design patterns.

Unlike High-Level Design, which shows the overall architecture, LLD explains how each component works internally.

---

# 📌 Definition

> **Low-Level Design (LLD) is the detailed design of software components that describes classes, objects, methods, interfaces, and their interactions before implementation.**

---

# ❓ Why Do We Need LLD?

Imagine building a car.

- HLD decides:
  - Engine
  - Wheels
  - Seats
  - Doors

- LLD decides:
  - Engine class
  - Car class
  - Brake class
  - Wheel class
  - Methods inside each class

LLD converts ideas into actual software structure.

---

# 🎯 Objectives of LLD

- Write clean code
- Improve maintainability
- Reduce code duplication
- Increase reusability
- Make applications scalable
- Simplify testing

---

# 🏗️ What Does LLD Include?

- Classes
- Objects
- Methods
- Interfaces
- Relationships
- UML Diagrams
- SOLID Principles
- Design Patterns

---

# 🔄 HLD vs LLD

| High-Level Design (HLD) | Low-Level Design (LLD) |
|--------------------------|------------------------|
| System Architecture | Code Structure |
| Modules | Classes |
| Services | Objects |
| Databases | Methods |
| APIs | Interfaces |
| Scalability | Implementation |

---

# 🏛️ LLD Workflow

```text
Requirements
      │
      ▼
Identify Classes
      │
      ▼
Identify Objects
      │
      ▼
Define Relationships
      │
      ▼
Create UML Diagrams
      │
      ▼
Apply SOLID Principles
      │
      ▼
Implement Code
```

---

# 🌍 Real-World Example

### Library Management System

Possible Classes:

- Book
- Member
- Librarian
- Library
- Fine
- Transaction

Each class has:

Attributes

Book

- id
- title
- author

Methods

- issueBook()
- returnBook()

---

# 💻 Example

```java
class Book {

    private int id;
    private String title;

    public void issueBook() {
        System.out.println("Book Issued");
    }

    public void returnBook() {
        System.out.println("Book Returned");
    }

}
```

---

# 🎯 Interview Keywords

- Class
- Object
- Encapsulation
- Abstraction
- Inheritance
- Polymorphism
- SOLID
- UML
- Design Patterns
- Composition
- Aggregation

---

# 🚨 Common Mistakes

❌ Jumping directly into coding.

❌ Ignoring relationships.

❌ Violating SOLID principles.

❌ Creating God Classes.

❌ Tight Coupling.

---

# 🔥 Interview Questions

### What is LLD?

Designing software at the class and object level.

---

### Difference between HLD and LLD?

HLD focuses on architecture.

LLD focuses on implementation.

---

### Why is LLD important?

It improves maintainability, scalability, readability, and testability.

---

# 🧠 Quick Revision

- ✅ LLD focuses on implementation.
- ✅ Uses classes and objects.
- ✅ Uses UML diagrams.
- ✅ Uses SOLID principles.
- ✅ Uses Design Patterns.
- ✅ Makes software maintainable and reusable.