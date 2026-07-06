# 🔁 Introduction to Recursion

---

# 📖 What is Recursion?

**Recursion** is a programming technique in which a function **calls itself** repeatedly to solve a problem by breaking it into **smaller subproblems**.

Instead of using loops (`for`, `while`), recursion solves the problem until a **base case** is reached.

---

# 📌 Definition

> **Recursion is the process in which a function calls itself directly or indirectly until a stopping condition (Base Case) is met.**

---

# 🤔 Why Do We Need Recursion?

Recursion helps us solve problems that can be divided into smaller versions of the same problem.

It is widely used in:

- 🌳 Trees
- 📊 Graphs
- 📂 File System Traversal
- 🔍 Binary Search
- 🧩 Backtracking
- ⚡ Divide & Conquer Algorithms
- 📈 Dynamic Programming

---

# 🧠 How Recursion Works

Every recursive function has **two important parts**:

### ✅ 1. Base Case

The condition where recursion stops.

### ✅ 2. Recursive Case

The part where the function calls itself.

---

# 💻 Basic Syntax

```cpp
returnType functionName(parameters)
{
    // Base Case
    if(condition)
        return;

    // Recursive Case
    functionName(parameters);
}
```

---

# 💻 Example 1

Print "Hello" 5 times.

```cpp
#include<iostream>
using namespace std;

void printHello(int n)
{
    if(n == 0)
        return;

    cout << "Hello" << endl;

    printHello(n - 1);
}

int main()
{
    printHello(5);

    return 0;
}
```

---

# 📥 Input

```
5
```

---

# 📤 Output

```
Hello
Hello
Hello
Hello
Hello
```

---

# 💡 Dry Run

```
printHello(5)

↓

Hello

↓

printHello(4)

↓

Hello

↓

printHello(3)

↓

Hello

↓

printHello(2)

↓

Hello

↓

printHello(1)

↓

Hello

↓

printHello(0)

↓

Return
```

---

# 📊 ASCII Diagram

```
printHello(5)
      │
      ▼
printHello(4)
      │
      ▼
printHello(3)
      │
      ▼
printHello(2)
      │
      ▼
printHello(1)
      │
      ▼
printHello(0)
      │
      ▼
    Return
```

---

# 🌍 Real-world Example

Think of **Russian Dolls (Matryoshka Dolls)** 🪆

Each doll contains a smaller doll inside it.

You keep opening dolls until the smallest one is reached.

Then the process stops.

Recursion works in exactly the same way.

---

# ⚙️ How Function Calls Work

Each recursive function call is stored inside the **Call Stack**.

```
printHello(5)

↓

printHello(4)

↓

printHello(3)

↓

printHello(2)

↓

printHello(1)

↓

printHello(0)

↓

Return

↓

Return

↓

Return

↓

Return

↓

Return

↓

Return
```

---

# ⏱ Time Complexity

| 📌 Operation | Complexity |
|--------------|------------|
| Time | O(N) |
| Space | O(N) |

---

# 🎯 Interview Keywords

- ✅ Recursion
- ✅ Self Calling Function
- ✅ Base Case
- ✅ Recursive Case
- ✅ Call Stack
- ✅ Stack Frame
- ✅ Divide and Conquer

---

# ⚠️ Common Mistakes

❌ Forgetting the Base Case.

❌ Infinite Recursive Calls.

❌ Incorrect Recursive Call.

❌ Changing parameters incorrectly.

---

# 🔥 Interview Questions

### ❓ What is recursion?

A function calling itself until a base condition is met.

---

### ❓ Why is the Base Case important?

Without it, recursion never stops and causes a **Stack Overflow**.

---

### ❓ Can recursion replace loops?

✅ Yes.

Many looping problems can also be solved using recursion.

---

### ❓ What happens after reaching the Base Case?

The recursive calls start returning one by one in **LIFO (Last In, First Out)** order.

---

# 📝 Advantages

✅ Cleaner Code

✅ Easier to solve complex problems

✅ Useful in Trees and Graphs

✅ Natural for Divide & Conquer

---

# ❌ Disadvantages

❌ Uses extra stack memory.

❌ Slower than iteration in some cases.

❌ Can cause Stack Overflow.

---

# 🧠 Quick Revision

✅ Function calls itself.

✅ Must have a Base Case.

✅ Uses Call Stack.

✅ Stops when Base Case becomes true.

✅ Returns in reverse order.

---

# 🎉 Key Takeaways

⭐ A recursive function always calls itself.

⭐ Every recursion needs a Base Case.

⭐ Every recursive call creates a new stack frame.

⭐ Recursion is the foundation of Trees, Graphs, Backtracking and Dynamic Programming.

⭐ One of the most important topics for coding interviews.