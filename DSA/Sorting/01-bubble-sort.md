# 🫧 Bubble Sort

---

# 📖 Introduction

**Bubble Sort** is a simple comparison-based sorting algorithm.

It repeatedly compares **adjacent elements** and swaps them if they are in the wrong order.

After every complete pass, the largest unsorted element moves to its correct position at the end.

This is why it is called **Bubble Sort** 🫧 — larger elements "bubble" toward the end.

---

# 📌 Definition

> Bubble Sort repeatedly compares adjacent elements and swaps them when they are in the wrong order.

---

# 🎯 Example

Given:

```text
5 3 8 1 2
```

We want ascending order:

```text
1 2 3 5 8
```

---

# ⚙️ How Bubble Sort Works

## 🔄 Pass 1

Compare adjacent elements:

```text
5 3 8 1 2
↑ ↑
```

5 > 3 → Swap

```text
3 5 8 1 2
```

Next:

```text
3 5 8 1 2
  ↑ ↑
```

5 < 8 → No swap

Next:

```text
3 5 8 1 2
    ↑ ↑
```

8 > 1 → Swap

```text
3 5 1 8 2
```

Next:

```text
3 5 1 8 2
      ↑ ↑
```

8 > 2 → Swap

```text
3 5 1 2 8
```

🎯 Largest element `8` is now at its correct position.

---

# 🔄 Pass 2

```text
3 5 1 2 8
```

Compare:

```text
3 5 → No Swap
5 1 → Swap
5 2 → Swap
```

Result:

```text
3 1 2 5 8
```

Now `5` is also in its correct position.

---

# 🔄 Pass 3

```text
3 1 2 5 8
```

Compare:

```text
3 1 → Swap

1 2 → No Swap

2 5 → No Swap
```

Result:

```text
1 3 2 5 8
```

---

# 🔄 Pass 4

```text
1 3 2 5 8
```

Compare:

```text
1 3 → No Swap

3 2 → Swap
```

Result:

```text
1 2 3 5 8
```

---

# ✅ Final Result

```text
1 2 3 5 8
```

---

# 💻 C++ Implementation

```cpp
#include<iostream>
using namespace std;

void bubbleSort(int arr[], int n)
{
    for(int i = 0; i < n - 1; i++)
    {
        for(int j = 0; j < n - i - 1; j++)
        {
            if(arr[j] > arr[j + 1])
            {
                swap(arr[j], arr[j + 1]);
            }
        }
    }
}

int main()
{
    int arr[] = {5, 3, 8, 1, 2};
    int n = 5;

    bubbleSort(arr, n);

    for(int i = 0; i < n; i++)
    {
        cout << arr[i] << " ";
    }

    return 0;
}
```

---

# 🧠 Understanding the Loops

```cpp
for(int i = 0; i < n - 1; i++)
```

This controls the number of **passes**.

---

```cpp
for(int j = 0; j < n - i - 1; j++)
```

This compares adjacent elements in the **unsorted portion**.

Why `n - i - 1`?

Because after every pass, one largest element reaches its final position.

```text
Pass 1 → 8 fixed

Pass 2 → 5 fixed

Pass 3 → 3 fixed

Pass 4 → 2 fixed
```

So we don't need to compare the already sorted portion.

---

# 📊 Visualization

```text
Initial

5 3 8 1 2
        ↓
3 5 1 2 8
          ↑
        8 fixed


3 5 1 2 | 8
        ↓
3 1 2 5 | 8
        ↑
        5 fixed


3 1 2 | 5 8
      ↓
1 3 2 | 5 8


1 3 2 | 5 8
  ↓
1 2 3 | 5 8
```

Final:

```text
1 2 3 5 8
```

---

# 🚀 Optimized Bubble Sort

The normal implementation keeps making passes even if the array is already sorted.

We can optimize it using a `swapped` flag.

```cpp
void bubbleSort(int arr[], int n)
{
    for(int i = 0; i < n - 1; i++)
    {
        bool swapped = false;

        for(int j = 0; j < n - i - 1; j++)
        {
            if(arr[j] > arr[j + 1])
            {
                swap(arr[j], arr[j + 1]);
                swapped = true;
            }
        }

        if(!swapped)
            break;
    }
}
```

---

# 💡 Why `swapped`?

Suppose:

```text
1 2 3 4 5
```

The array is already sorted.

During the first pass:

```text
No swaps
```

Therefore:

```cpp
swapped == false
```

We can immediately stop.

This improves the best-case performance.

---

# ⏱️ Time Complexity

| Case | Complexity |
|------|------------|
| Best Case | **O(N)** 🚀 |
| Average Case | **O(N²)** |
| Worst Case | **O(N²)** |

### Without Optimization

Best case:

```text
O(N²)
```

### With `swapped` Optimization

Best case:

```text
O(N)
```

---

# 💾 Space Complexity

```text
O(1)
```

Bubble Sort sorts the array **in-place**.

It does not require another array.

---

# 📊 Complexity Summary

| Property | Bubble Sort |
|----------|-------------|
| Best | O(N) |
| Average | O(N²) |
| Worst | O(N²) |
| Space | O(1) |
| In-place | ✅ |
| Stable | ✅ |

---

# 🧠 Important Properties

### 🔹 In-Place

Bubble Sort modifies the original array.

```text
Extra Space = O(1)
```

---

### 🔹 Stable

Equal elements maintain their relative order.

Example:

```text
(5,A) (3) (5,B)
```

After sorting:

```text
(3) (5,A) (5,B)
```

`5,A` remains before `5,B`.

---

# ⚠️ Common Mistakes

❌ Comparing non-adjacent elements.

❌ Forgetting to swap when:

```cpp
arr[j] > arr[j + 1]
```

❌ Using the wrong inner-loop boundary.

❌ Forgetting `n - i - 1`.

❌ Thinking Bubble Sort is efficient for large datasets.

---

# 🔥 Interview Questions

### ❓ Why is it called Bubble Sort?

Because larger elements gradually **bubble toward the end** of the array.

---

### ❓ What is the worst-case complexity?

```text
O(N²)
```

---

### ❓ What is the best-case complexity of optimized Bubble Sort?

```text
O(N)
```

when the array is already sorted.

---

### ❓ Is Bubble Sort in-place?

✅ Yes.

Space complexity:

```text
O(1)
```

---

### ❓ Is Bubble Sort stable?

✅ Yes.

---

### ❓ When does Bubble Sort perform best?

When the array is already sorted or nearly sorted, especially with the `swapped` optimization.

---

# 🧠 Quick Revision

```text
Compare adjacent elements
        ↓
Swap if wrong order
        ↓
Largest element reaches end
        ↓
Repeat
        ↓
Sorted ✅
```

### Remember:

```text
Bubble Sort
↓
Adjacent Comparison
↓
Swap
↓
Largest → End
```

---

# 🎯 Interview Cheat Sheet

```text
Algorithm      → Bubble Sort

Technique      → Comparison

Comparison     → Adjacent Elements

Best Case      → O(N)      [Optimized]

Average Case   → O(N²)

Worst Case     → O(N²)

Space          → O(1)

In-place       → Yes

Stable         → Yes
```

---

# 🎉 Key Takeaways

⭐ Bubble Sort compares adjacent elements.

⭐ Wrongly ordered elements are swapped.

⭐ After every pass, the largest unsorted element reaches the end.

⭐ It is an **in-place** algorithm.

⭐ It is **stable**.

⭐ Basic version → O(N²) best case.

⭐ Optimized version → O(N) best case.

⭐ Average/Worst → O(N²).

⭐ Mainly useful for learning sorting fundamentals, not large-scale performance.