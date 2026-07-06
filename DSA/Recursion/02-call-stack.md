# 📚 Call Stack in Recursion

---

# 📖 Introduction

Whenever a function is called, the computer needs to remember where the function was called from and what it was doing.

To keep track of this information, the computer uses a special memory structure called the **Call Stack**.

Every function call is stored inside the Call Stack until it finishes execution.

---

# 📌 Definition

> **A Call Stack is a stack data structure that stores information about active function calls.**

It follows the **LIFO (Last In, First Out)** principle.

---

# 🤔 Why Do We Need a Call Stack?

The Call Stack helps the computer:

- 📌 Store active function calls.
- 📌 Remember local variables.
- 📌 Store return addresses.
- 📌 Resume execution after a function finishes.

Without the Call Stack, recursion would not be possible.

---

# ⚙️ How Call Stack Works

Whenever a function is called,

✅ A new **Stack Frame** is created.

When the function finishes,

✅ That Stack Frame is removed.

This process continues until all function calls are completed.

---

# 💻 Example

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
    fun(3);

    return 0;
}
```

---

# 📥 Input

```
3
```

---

# 📤 Output

```
3
2
1
```

---

# 🧠 Step-by-Step Execution

### Step 1

```
main()
```

Call Stack

```
┌─────────┐
│ main()  │
└─────────┘
```

---

### Step 2

```
fun(3)
```

Call Stack

```
┌─────────┐
│ fun(3)  │
├─────────┤
│ main()  │
└─────────┘
```

---

### Step 3

```
fun(2)
```

Call Stack

```
┌─────────┐
│ fun(2)  │
├─────────┤
│ fun(3)  │
├─────────┤
│ main()  │
└─────────┘
```

---

### Step 4

```
fun(1)
```

Call Stack

```
┌─────────┐
│ fun(1)  │
├─────────┤
│ fun(2)  │
├─────────┤
│ fun(3)  │
├─────────┤
│ main()  │
└─────────┘
```

---

### Step 5

```
fun(0)
```

Base Case reached.

No new function call is added.

---

### Step 6

Functions start returning one by one.

```
fun(1)
↓

fun(2)

↓

fun(3)

↓

main()
```

---

# 📊 Complete Visualization

```
CALLS

main()

↓

fun(3)

↓

fun(2)

↓

fun(1)

↓

fun(0)

↓

RETURN

fun(1)

↓

fun(2)

↓

fun(3)

↓

main()
```

---

# 🧠 Stack Frame

Every function call creates a **Stack Frame**.

A Stack Frame stores:

- 📌 Function parameters
- 📌 Local variables
- 📌 Return address
- 📌 Temporary data

Example

```
┌────────────────────┐
│ Function Name      │
├────────────────────┤
│ Parameters         │
├────────────────────┤
│ Local Variables    │
├────────────────────┤
│ Return Address     │
└────────────────────┘
```

---

# 🌍 Real-world Example

Imagine a stack of books.

📚 Book 1

📚 Book 2

📚 Book 3

The last book placed on the stack is removed first.

The Call Stack works exactly the same way.

---

# ⏱ Time & Space Complexity

| 📌 Operation | Complexity |
|--------------|------------|
| Function Call | O(1) |
| Function Return | O(1) |
| Total Stack Space | O(N) |

---

# 🎯 Interview Keywords

- ✅ Call Stack
- ✅ Stack Frame
- ✅ LIFO
- ✅ Function Call
- ✅ Function Return
- ✅ Recursive Calls
- ✅ Memory Management

---

# ⚠️ Common Mistakes

❌ Thinking recursion runs all functions together.

❌ Forgetting that each function has its own local variables.

❌ Assuming memory is shared between recursive calls.

❌ Forgetting that the last called function returns first.

---

# 🔥 Interview Questions

### ❓ What is a Call Stack?

A memory structure that stores active function calls.

---

### ❓ Which principle does it follow?

✅ LIFO (Last In, First Out)

---

### ❓ What is stored in a Stack Frame?

- Parameters
- Local Variables
- Return Address

---

### ❓ Why is recursion memory expensive?

Because every recursive call creates a new Stack Frame.

---

### ❓ What happens after reaching the Base Case?

The functions start returning one by one in reverse order.

---

# 📝 Advantages

✅ Makes recursion possible.

✅ Keeps function calls organized.

✅ Automatically handles function returns.

---

# ❌ Disadvantages

❌ Uses additional memory.

❌ Too many recursive calls can cause Stack Overflow.

---

# 🧠 Quick Revision

✅ Every function call creates a Stack Frame.

✅ Stack follows LIFO.

✅ Last called function returns first.

✅ Every recursive call occupies memory.

✅ Stack Frames are removed after function execution.

---

# 🎉 Key Takeaways

⭐ Call Stack is the backbone of recursion.

⭐ Every recursive call creates a new Stack Frame.

⭐ Functions return in reverse order.

⭐ Understanding the Call Stack makes recursion much easier to debug.

⭐ One of the most frequently asked recursion interview concepts.