# 🌀 Fibonacci Number Using Recursion

---

# 📖 Introduction

The **Fibonacci Series** is one of the most famous recursion problems.

Each number in the series is obtained by adding the previous two numbers.

It is widely used to understand:

- 🔁 Multiple Recursive Calls
- 📚 Recursion Tree
- ⚡ Overlapping Subproblems
- 🧠 Dynamic Programming (Later)

---

# 📌 What is a Fibonacci Number?

The Fibonacci sequence starts with:

```
0 1 1 2 3 5 8 13 21 34 ...
```

Rule:

```
F(n) = F(n-1) + F(n-2)
```

Base Cases

```
F(0) = 0

F(1) = 1
```

---

# 🤔 Why Learn Fibonacci?

This problem teaches us:

- ✅ Multiple recursive calls
- ✅ Recursion Tree
- ✅ Exponential Time Complexity
- ✅ Why Dynamic Programming is needed

It is one of the most frequently asked recursion interview questions.

---

# 🧠 Recursive Formula

```
F(n) = F(n-1) + F(n-2)
```

Example

```
F(5)

= F(4) + F(3)

= (F(3)+F(2)) + (F(2)+F(1))

= 5
```

---

# 💻 C++ Code

```cpp
#include<iostream>
using namespace std;

int fibonacci(int n)
{
    if(n == 0)
        return 0;

    if(n == 1)
        return 1;

    return fibonacci(n - 1) + fibonacci(n - 2);
}

int main()
{
    int n = 6;

    cout << fibonacci(n);

    return 0;
}
```

---

# 📥 Input

```
6
```

---

# 📤 Output

```
8
```

---

# 💡 Dry Run

```
fibonacci(6)

=

fibonacci(5)

+

fibonacci(4)

↓

fibonacci(4)

+

fibonacci(3)

+

fibonacci(3)

+

fibonacci(2)

↓

...

↓

8
```

---

# 🌳 Recursion Tree

```
                     F(5)
                   /      \
               F(4)        F(3)
              /   \       /   \
           F(3)  F(2)   F(2)  F(1)
          /   \   / \    / \
       F(2) F(1)F(1)F(0)F(1)F(0)
       / \
    F(1) F(0)
```

Notice that

```
F(3)

F(2)

F(1)
```

are calculated **multiple times**.

This is called **Overlapping Subproblems**.

---

# 🌍 Real-world Example

Imagine a rabbit population.

- 🐇 First month → 1 pair
- 🐇 Second month → 1 pair
- 🐇 Third month → 2 pairs
- 🐇 Fourth month → 3 pairs
- 🐇 Fifth month → 5 pairs

Every month's population depends on the previous two months.

---

# ⏱ Time & Space Complexity

| 📌 Operation | Complexity |
|--------------|------------|
| Time | O(2ⁿ) |
| Space | O(N) |

---

# 🎯 Interview Keywords

- ✅ Fibonacci
- ✅ Recursion Tree
- ✅ Multiple Recursive Calls
- ✅ Overlapping Subproblems
- ✅ Dynamic Programming
- ✅ Memoization

---

# ⚠️ Common Mistakes

❌ Forgetting the second Base Case.

```cpp
if(n == 1)
```

❌ Returning incorrect values for

```
F(0)

F(1)
```

❌ Thinking recursion is efficient for Fibonacci.

❌ Forgetting that the same subproblem is solved multiple times.

---

# 🔥 Interview Questions

### ❓ Why is Fibonacci recursion slow?

Because the same recursive calls are repeated many times.

---

### ❓ Why is the time complexity O(2ⁿ)?

Each function makes **two recursive calls**, creating an exponential recursion tree.

---

### ❓ How can Fibonacci be optimized?

✅ Memoization

✅ Tabulation

✅ Dynamic Programming

---

### ❓ Is recursion the best solution?

❌ No.

Recursion is used for learning.

Dynamic Programming is the preferred approach for large values of **N**.

---

# 💡 Best Practices

✅ Learn recursion first.

✅ Then learn Memoization.

✅ Finally learn Dynamic Programming optimization.

---

# 🧠 Quick Revision

✅ Base Cases

```cpp
if(n==0) return 0;

if(n==1) return 1;
```

✅ Recursive Formula

```cpp
return fibonacci(n-1)+fibonacci(n-2);
```

✅ Time Complexity → **O(2ⁿ)**

✅ Space Complexity → **O(N)**

---

# 🎉 Key Takeaways

⭐ Fibonacci is the first recursion problem with **multiple recursive calls**.

⭐ It introduces the concept of **Overlapping Subproblems**.

⭐ It forms the foundation of **Dynamic Programming**.

⭐ One of the most important recursion interview questions.
