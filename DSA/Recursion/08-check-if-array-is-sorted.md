# ✅ Check if Array is Sorted Using Recursion

---

# 📖 Introduction

Checking whether an array is sorted is one of the most common beginner recursion problems.

Instead of comparing all elements using a loop, recursion compares one pair of adjacent elements at a time and then recursively checks the remaining array.

This problem helps us understand:

- 🔁 Recursive Calls
- 🎯 Base Case
- 📚 Array Traversal
- ⚡ Returning Boolean Values

---

# 📌 Problem Statement

Given an array, determine whether it is sorted in **ascending order** using recursion.

Return:

- ✅ `true` if the array is sorted.
- ❌ `false` otherwise.

---

# 💡 Logic

For an array to be sorted,

```
arr[i] <= arr[i+1]
```

must be true for every index.

If any adjacent pair violates this condition,

```
arr[i] > arr[i+1]
```

the array is **not sorted**.

---

# 🧠 Recursive Relation

```
isSorted(arr, i)

↓

Check

arr[i] <= arr[i+1]

↓

True ?

↓

Check remaining array

↓

isSorted(arr, i+1)
```

---

# 💻 C++ Code

```cpp
#include<iostream>
using namespace std;

bool isSorted(int arr[], int n, int i)
{
    if(i == n - 1)
        return true;

    if(arr[i] > arr[i + 1])
        return false;

    return isSorted(arr, n, i + 1);
}

int main()
{
    int arr[] = {1,2,3,4,5};
    int n = 5;

    if(isSorted(arr, n, 0))
        cout << "Sorted";
    else
        cout << "Not Sorted";

    return 0;
}
```

---

# 📥 Input

```
1 2 3 4 5
```

---

# 📤 Output

```
Sorted
```

---

# 💡 Dry Run

```
isSorted(0)

↓

1 <= 2 ✅

↓

isSorted(1)

↓

2 <= 3 ✅

↓

isSorted(2)

↓

3 <= 4 ✅

↓

isSorted(3)

↓

4 <= 5 ✅

↓

isSorted(4)

↓

Base Case

↓

true
```

---

# 📊 Recursion Flow

```
isSorted(0)
      │
      ▼
isSorted(1)
      │
      ▼
isSorted(2)
      │
      ▼
isSorted(3)
      │
      ▼
isSorted(4)

Base Case

↓

true

↓

true

↓

true

↓

true

↓

true
```

---

# ❌ Example (Not Sorted)

Input

```
1 4 3 5 6
```

Execution

```
1 <= 4 ✅

↓

4 <= 3 ❌

↓

Return false
```

Output

```
Not Sorted
```

---

# 🌍 Real-world Example

Imagine checking exam marks arranged in ascending order.

```
40

↓

55

↓

72

↓

89

↓

95
```

Every next mark should be greater than or equal to the previous one.

If any mark is smaller than the previous one,

the sequence is **not sorted**.

---

# ⏱ Time & Space Complexity

| 📌 Operation | Complexity |
|--------------|------------|
| Time | O(N) |
| Space | O(N) |

---

# 🎯 Interview Keywords

- ✅ Recursion
- ✅ Array Traversal
- ✅ Base Case
- ✅ Boolean Function
- ✅ Adjacent Comparison

---

# ⚠️ Common Mistakes

❌ Using

```cpp
i == n
```

instead of

```cpp
i == n - 1
```

❌ Forgetting to return the recursive call.

❌ Comparing the wrong indices.

❌ Missing the Base Case.

---

# 🔥 Interview Questions

### ❓ Why is the Base Case `i == n - 1`?

Because the last element has no next element to compare.

---

### ❓ Why return `false` immediately?

Once one pair is out of order, the entire array is not sorted.

---

### ❓ Can this be solved iteratively?

✅ Yes.

Using a simple loop.

---

### ❓ Why use recursion then?

To understand recursive traversal and recursive return values.

---

# 💡 Best Practices

✅ Check the Base Case first.

✅ Compare only adjacent elements.

✅ Return immediately when an unsorted pair is found.

---

# 🧠 Quick Revision

✅ Compare

```cpp
arr[i] <= arr[i+1]
```

✅ Base Case

```cpp
i == n - 1
```

✅ If one comparison fails

```
Return false
```

✅ Time Complexity → **O(N)**

✅ Space Complexity → **O(N)**

---

# 🎉 Key Takeaways

⭐ One of the easiest recursion problems on arrays.

⭐ Introduces recursive traversal of arrays.

⭐ Uses Boolean return values.

⭐ Frequently asked in coding interviews.