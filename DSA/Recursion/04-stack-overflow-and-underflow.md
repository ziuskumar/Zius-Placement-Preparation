# 💥 Stack Overflow & Stack Underflow

---

# 📖 Introduction

Whenever a function is called, it is stored inside the **Call Stack**.

If too many function calls are made without returning, the Call Stack becomes full, resulting in a **Stack Overflow**.

If we try to remove an element from an **empty stack**, it results in a **Stack Underflow**.

---

# 📌 Definition

## 💥 Stack Overflow

> **Stack Overflow occurs when the Call Stack exceeds its memory limit due to excessive function calls.**

It is one of the most common errors in recursion.

---

## 📌 Stack Underflow

> **Stack Underflow occurs when an attempt is made to remove (POP) an element from an empty stack.**

It generally occurs in stack data structures, not in recursion.

---

# 🤔 Why Does Stack Overflow Occur?

It occurs when recursion never stops.

Common reasons include:

- ❌ Missing Base Case
- ❌ Wrong Base Case
- ❌ Infinite Recursion
- ❌ Recursive call does not reduce the problem

---

# ⚙️ Stack Overflow Example

```cpp
#include<iostream>
using namespace std;

void fun()
{
    cout << "Hello" << endl;

    fun();          // Infinite recursion
}

int main()
{
    fun();

    return 0;
}
```

---

# ❌ Output

```
Hello
Hello
Hello
Hello
Hello
Hello
...

Stack Overflow
Program Crashed
```

---

# 💡 Why Did This Happen?

There is **no Base Case**.

```
fun()

↓

fun()

↓

fun()

↓

fun()

↓

fun()

↓

fun()

↓

...
```

The function keeps calling itself forever.

Eventually,

```
Call Stack Full

↓

Stack Overflow
```

---

# ✅ Correct Example

```cpp
#include<iostream>
using namespace std;

void fun(int n)
{
    if(n == 0)
        return;

    cout << n << endl;

    fun(n - 1);
}

int main()
{
    fun(5);

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
5
4
3
2
1
```

---

# 🧠 Dry Run

```
fun(5)

↓

fun(4)

↓

fun(3)

↓

fun(2)

↓

fun(1)

↓

fun(0)

↓

Base Case

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

Since a Base Case exists, recursion stops normally.

---

# 📌 Stack Underflow Example

```cpp
stack<int> st;

st.pop();
```

Since the stack is already empty,

```
Stack Underflow
```

occurs.

---

# 📊 Difference Between Stack Overflow & Stack Underflow

| 💥 Stack Overflow | 📌 Stack Underflow |
|-------------------|-------------------|
| Stack becomes full | Stack becomes empty |
| Mostly seen in Recursion | Mostly seen in Stack Data Structure |
| Caused by excessive PUSH/Function Calls | Caused by POP on an empty stack |
| Program may crash | Invalid stack operation |

---

# 📊 Visualization

## 💥 Stack Overflow

```
┌──────────────┐
│ fun()        │
├──────────────┤
│ fun()        │
├──────────────┤
│ fun()        │
├──────────────┤
│ fun()        │
├──────────────┤
│ fun()        │
├──────────────┤
│ fun()        │
├──────────────┤
│ Memory Full  │
└──────────────┘

↓

Stack Overflow
```

---

## 📌 Stack Underflow

```
┌──────────────┐
│              │
│ Empty Stack  │
│              │
└──────────────┘

↓

POP()

↓

Stack Underflow
```

---

# 🌍 Real-world Example

## 💥 Stack Overflow

Imagine stacking books on a table.

📚

📚

📚

📚

📚

📚

📚

Eventually,

There is no space left.

The books fall.

➡️ **Stack Overflow**

---

## 📌 Stack Underflow

Imagine trying to remove a book from an empty table.

```
No Books

↓

Pick One

↓

Impossible
```

➡️ **Stack Underflow**

---

# ⏱ Time & Space Complexity

| 📌 Operation | Complexity |
|--------------|------------|
| Function Call | O(1) |
| Stack Space | O(N) |

---

# 🎯 Interview Keywords

- ✅ Stack Overflow
- ✅ Stack Underflow
- ✅ Base Case
- ✅ Infinite Recursion
- ✅ Call Stack
- ✅ Stack Frame

---

# ⚠️ Common Mistakes

❌ Forgetting the Base Case.

❌ Calling the function without reducing the input.

❌ Using the wrong stopping condition.

❌ Calling `pop()` on an empty stack.

---

# 🔥 Interview Questions

### ❓ What is Stack Overflow?

It occurs when the Call Stack exceeds its memory limit.

---

### ❓ What causes Stack Overflow in recursion?

- Missing Base Case
- Infinite recursion
- Wrong recursive call

---

### ❓ What is Stack Underflow?

Removing an element from an empty stack.

---

### ❓ Does Stack Underflow occur in recursion?

❌ No.

It is mainly related to Stack Data Structures.

---

### ❓ How can Stack Overflow be prevented?

✅ Write a correct Base Case.

✅ Reduce the problem in every recursive call.

---

# 💡 Best Practices

✅ Always write the Base Case first.

✅ Ensure every recursive call moves toward the Base Case.

✅ Never call `pop()` without checking if the stack is empty.

---

# 🧠 Quick Revision

✅ Stack Overflow → Stack becomes full.

✅ Stack Underflow → Stack becomes empty.

✅ Missing Base Case causes Stack Overflow.

✅ Underflow occurs when popping from an empty stack.

---

# 🎉 Key Takeaways

⭐ Stack Overflow is one of the most common recursion errors.

⭐ A correct Base Case prevents Stack Overflow.

⭐ Stack Underflow belongs to the Stack data structure.

⭐ Understanding these concepts is essential for recursion interviews.