# 🔢 Print 1 to N and N to 1 Using Recursion

---

# 📖 Introduction

Printing numbers is one of the easiest and most important recursion problems.

It helps us understand:

- 🔁 Recursive Calls
- 📚 Call Stack
- 🎯 Base Case
- 🔄 Backtracking

This problem is usually the first coding question asked while learning recursion.

---

# 📌 Problem Statement

There are two common problems:

1. ✅ Print numbers from **1 to N**
2. ✅ Print numbers from **N to 1**

Although both problems look similar, the position of the `cout` statement changes the output.

---

# 🧠 Concept

## 🔽 Print N to 1

Print the current number **before** making the recursive call.

```
Work

↓

Recursive Call
```

---

## 🔼 Print 1 to N

Make the recursive call **first**, then print the number.

```
Recursive Call

↓

Work
```

---

# 💻 Program 1 : Print N to 1

```cpp
#include<iostream>
using namespace std;

void print(int n)
{
    if(n == 0)
        return;

    cout << n << " ";

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
5 4 3 2 1
```

---

# 🧠 Dry Run

```
print(5)

Print 5

↓

print(4)

Print 4

↓

print(3)

Print 3

↓

print(2)

Print 2

↓

print(1)

Print 1

↓

print(0)

Return
```

---

# 📊 Visualization

```
print(5)
   │
Print 5
   │
   ▼
print(4)
   │
Print 4
   │
   ▼
print(3)
   │
Print 3
   │
   ▼
print(2)
   │
Print 2
   │
   ▼
print(1)
   │
Print 1
   │
   ▼
print(0)

Return
```

---

# 💻 Program 2 : Print 1 to N

```cpp
#include<iostream>
using namespace std;

void print(int n)
{
    if(n == 0)
        return;

    print(n - 1);

    cout << n << " ";
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
1 2 3 4 5
```

---

# 🧠 Dry Run

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

↓

Return

Print 1

↓

Print 2

↓

Print 3

↓

Print 4

↓

Print 5
```

---

# 📊 Visualization

```
Calls

print(5)
   │
print(4)
   │
print(3)
   │
print(2)
   │
print(1)
   │
print(0)

────────────

Returns

Print 1

↓

Print 2

↓

Print 3

↓

Print 4

↓

Print 5
```

---

# 📊 Difference Between Both Approaches

| 🔽 Print N to 1 | 🔼 Print 1 to N |
|-----------------|-----------------|
| Print first | Recursive call first |
| Output while going down | Output while returning |
| Uses Forward Recursion | Uses Backtracking |
| Easy to understand | Slightly tricky |

---

# 🌍 Real-world Example

Imagine walking down a staircase.

### N to 1

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
```

You announce every step while going down.

---

### 1 to N

You stay silent while going down.

When coming back,

```
Step 1

↓

Step 2

↓

Step 3

↓

Step 4

↓

Step 5
```

You announce every step while climbing back.

---

# ⏱ Time & Space Complexity

| 📌 Operation | Complexity |
|--------------|------------|
| Time | O(N) |
| Space | O(N) |

---

# 🎯 Interview Keywords

- ✅ Forward Recursion
- ✅ Backtracking
- ✅ Base Case
- ✅ Recursive Call
- ✅ Call Stack

---

# ⚠️ Common Mistakes

❌ Printing before recursion in both programs.

❌ Forgetting the Base Case.

❌ Using `n < 0` instead of `n == 0`.

❌ Confusing the order of execution.

---

# 🔥 Interview Questions

### ❓ Why does `cout` after recursion print 1 to N?

Because the function prints while returning from the recursive calls (Backtracking).

---

### ❓ Why does `cout` before recursion print N to 1?

Because the current value is printed before making the next recursive call.

---

### ❓ Which concept is used while printing 1 to N?

✅ Backtracking.

---

### ❓ Which concept is used while printing N to 1?

✅ Forward Recursion.

---

# 💡 Best Practices

✅ Always write the Base Case first.

✅ Understand whether work is done before or after the recursive call.

✅ Practice dry runs to understand the Call Stack.

---

# 🧠 Quick Revision

✅ `cout` before recursion → N to 1.

✅ `cout` after recursion → 1 to N.

✅ Base Case → `if(n == 0) return;`

✅ Both solutions use recursion.

---

# 🎉 Key Takeaways

⭐ The position of `cout` changes the output completely.

⭐ Printing before recursion gives **N to 1**.

⭐ Printing after recursion gives **1 to N**.

⭐ This introduces the concept of **Backtracking**, which is used in advanced recursion problems like Subsets, Permutations, N-Queens, and Sudoku Solver.