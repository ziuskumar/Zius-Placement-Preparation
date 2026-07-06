# ➕ Sum of First N Numbers Using Recursion

---

# 📖 Introduction

One of the most fundamental recursion problems is finding the **sum of the first N natural numbers**.

Instead of using loops, recursion repeatedly adds the current number to the sum of the remaining numbers until it reaches the Base Case.

This problem helps us understand:

- 🔁 Recursive Thinking
- 🎯 Base Case
- 📚 Recursive Formula
- ⚡ Returning Values

---

# 📌 Problem Statement

Given a number **N**, calculate the sum of all natural numbers from **1 to N** using recursion.

---

# 💡 Mathematical Formula

```
Sum(N) = N + Sum(N - 1)
```

Base Case

```
Sum(0) = 0
```

---

# 🧠 Recursive Relation

```
Sum(5)

= 5 + Sum(4)

= 5 + 4 + Sum(3)

= 5 + 4 + 3 + Sum(2)

= 5 + 4 + 3 + 2 + Sum(1)

= 5 + 4 + 3 + 2 + 1 + Sum(0)

= 15
```

---

# 💻 C++ Code

```cpp
#include<iostream>
using namespace std;

int sum(int n)
{
    if(n == 0)
        return 0;

    return n + sum(n - 1);
}

int main()
{
    int n = 5;

    cout << sum(n);

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
15
```

---

# 💡 Dry Run

```
sum(5)

↓

5 + sum(4)

↓

5 + 4 + sum(3)

↓

5 + 4 + 3 + sum(2)

↓

5 + 4 + 3 + 2 + sum(1)

↓

5 + 4 + 3 + 2 + 1 + sum(0)

↓

5 + 4 + 3 + 2 + 1 + 0

↓

15
```

---

# 📊 Call Stack Visualization

```
sum(5)
   │
   ▼
sum(4)
   │
   ▼
sum(3)
   │
   ▼
sum(2)
   │
   ▼
sum(1)
   │
   ▼
sum(0)

────────────

Return 0

↓

Return 1

↓

Return 3

↓

Return 6

↓

Return 10

↓

Return 15
```

---

# 🌍 Real-world Example

Imagine saving money every day.

```
Day 5 → ₹5

↓

Day 4 → ₹4

↓

Day 3 → ₹3

↓

Day 2 → ₹2

↓

Day 1 → ₹1

Total = ₹15
```

Each day contributes its value to the final total.

---

# ⏱ Time & Space Complexity

| 📌 Operation | Complexity |
|--------------|------------|
| Time | O(N) |
| Space | O(N) |

---

# 🎯 Interview Keywords

- ✅ Recursion
- ✅ Base Case
- ✅ Recursive Relation
- ✅ Function Return
- ✅ Call Stack

---

# ⚠️ Common Mistakes

❌ Returning `1` instead of `0` in the Base Case.

❌ Forgetting to return the recursive call.

❌ Writing

```cpp
sum(n);
```

instead of

```cpp
return n + sum(n - 1);
```

❌ Missing the Base Case.

---

# 🔥 Interview Questions

### ❓ Why is the Base Case `return 0`?

Because the sum of zero numbers is **0**, making it the correct stopping condition.

---

### ❓ Why do we use `return`?

Each recursive call returns its partial sum to the previous function call.

---

### ❓ Can this be solved iteratively?

✅ Yes.

Using a loop from **1 to N**.

---

### ❓ Which is more efficient?

- Iteration → O(1) Space
- Recursion → O(N) Space

---

# 💡 Best Practices

✅ Always define the Base Case first.

✅ Return the recursive result.

✅ Ensure the recursive call reduces the problem size.

---

# 🧠 Quick Revision

✅ Base Case → `n == 0`

✅ Recursive Relation

```cpp
return n + sum(n - 1);
```

✅ Time Complexity → O(N)

✅ Space Complexity → O(N)

---

# 🎉 Key Takeaways

⭐ One of the easiest recursion problems.

⭐ Introduces recursive return values.

⭐ Builds the foundation for Factorial and Fibonacci.

⭐ Frequently asked in coding interviews.