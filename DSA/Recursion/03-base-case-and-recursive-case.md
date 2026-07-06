# 🎯 Base Case & Recursive Case

---

# 📖 Introduction

Every recursive function consists of **two essential parts**:

1. ✅ Base Case
2. 🔁 Recursive Case

Without these two components, recursion cannot work correctly.

Think of them as the **heart of recursion**.

---

# 📌 Definition

## ✅ Base Case

The **Base Case** is the stopping condition of recursion.

When the Base Case becomes true, the function stops calling itself and starts returning.

---

## 🔁 Recursive Case

The **Recursive Case** is the part where the function calls itself with a smaller or modified input.

It keeps reducing the problem until the Base Case is reached.

---

# 🤔 Why Do We Need Them?

### ✅ Base Case

- Stops infinite recursion.
- Prevents Stack Overflow.
- Gives the final answer.

### 🔁 Recursive Case

- Breaks a large problem into smaller problems.
- Continues recursion.
- Moves towards the Base Case.

---

# ⚙️ General Structure

```cpp
void function(int n)
{
    // Base Case
    if(n == 0)
        return;

    // Recursive Case
    function(n - 1);
}
```

---

# 💻 Example

```cpp
#include<iostream>
using namespace std;

void print(int n)
{
    // Base Case
    if(n == 0)
        return;

    cout << n << endl;

    // Recursive Case
    print(n - 1);
}

int main()
{
    print(5);

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

### Function Call

```
print(5)
```

↓

```
Base Case?

5 == 0 ❌

Recursive Case

print(4)
```

↓

```
Base Case?

4 == 0 ❌

Recursive Case

print(3)
```

↓

```
Base Case?

3 == 0 ❌

Recursive Case

print(2)
```

↓

```
print(1)
```

↓

```
print(0)
```

↓

```
Base Case

0 == 0 ✅

Return
```

---

# 📊 Visualization

```
print(5)

↓

print(4)

↓

print(3)

↓

print(2)

↓

print(1)

↓

print(0)

──────────────
Base Case Hit
──────────────

↑

Return

↑

Return

↑

Return

↑

Return

↑

Return
```

---

# 🌍 Real-world Example

Imagine climbing down a staircase.

```
Step 5

↓

Step 4

↓

Step 3

↓

Step 2

↓

Step 1

↓

Ground Floor ✅
```

The **Ground Floor** is the **Base Case**.

Every step downward is the **Recursive Case**.

---

# 📊 Difference Between Base Case & Recursive Case

| ✅ Base Case | 🔁 Recursive Case |
|--------------|-------------------|
| Stops recursion | Continues recursion |
| Executes only once | Executes multiple times |
| Prevents infinite calls | Reduces problem size |
| Starts returning | Keeps calling itself |

---

# ⏱ Time & Space Complexity

| 📌 Operation | Complexity |
|--------------|------------|
| Time | O(N) |
| Space | O(N) |

---

# 🎯 Interview Keywords

- ✅ Base Case
- ✅ Recursive Case
- ✅ Recursive Function
- ✅ Stack Frame
- ✅ Function Call
- ✅ Function Return

---

# ⚠️ Common Mistakes

❌ Forgetting the Base Case.

❌ Writing the Base Case after the recursive call.

❌ Not reducing the input.

❌ Infinite recursion.

❌ Wrong stopping condition.

---

# 🔥 Interview Questions

### ❓ What is a Base Case?

The stopping condition of recursion.

---

### ❓ What is a Recursive Case?

The part where the function calls itself.

---

### ❓ What happens if there is no Base Case?

The recursion never stops and eventually causes **Stack Overflow**.

---

### ❓ Why should the Recursive Case reduce the problem?

So that the recursion eventually reaches the Base Case.

---

# 💡 Best Practices

✅ Always write the Base Case first.

✅ Make sure each recursive call moves closer to the Base Case.

✅ Test the Base Case separately.

✅ Keep recursive calls simple.

---

# 🧠 Quick Revision

✅ Every recursive function has two parts.

✅ Base Case stops recursion.

✅ Recursive Case continues recursion.

✅ Recursive calls must reduce the problem.

✅ Base Case is checked before making another recursive call.

---

# 🎉 Key Takeaways

⭐ Base Case is the stopping condition.

⭐ Recursive Case keeps solving smaller subproblems.

⭐ Both are mandatory for recursion.

⭐ Missing the Base Case causes Stack Overflow.

⭐ This is one of the most frequently asked recursion interview concepts.