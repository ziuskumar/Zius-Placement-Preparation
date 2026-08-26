# 🎯 Selection Sort

---

# 📖 Introduction

**Selection Sort** is a comparison-based sorting algorithm.

It repeatedly finds the **smallest element from the unsorted portion** and places it at the beginning of that portion.

The array is divided into:

```text
Sorted Portion | Unsorted Portion
```

---

# 📌 Definition

> **Selection Sort repeatedly selects the smallest element from the unsorted portion and swaps it with the first element of that portion.**

---

# 🧠 Basic Idea

Given:

```text
5 3 8 1 2
```

Find the smallest element:

```text
1
```

Place it at the beginning:

```text
1 3 8 5 2
```

Now ignore `1`.

Find the smallest element in:

```text
3 8 5 2
```

Smallest = `2`

Place it correctly:

```text
1 2 8 5 3
```

Continue until sorted.

---

# ⚙️ How Selection Sort Works

## 🔹 Pass 1

```text
5 3 8 1 2
```

Find minimum:

```text
1
```

Swap with first element:

```text
1 3 8 5 2
```

Now:

```text
[1] | 3 8 5 2
```

`1` is fixed ✅

---

## 🔹 Pass 2

Unsorted portion:

```text
3 8 5 2
```

Minimum:

```text
2
```

Swap with `3`:

```text
1 2 8 5 3
```

Now:

```text
[1 2] | 8 5 3
```

`2` is fixed ✅

---

## 🔹 Pass 3

Unsorted portion:

```text
8 5 3
```

Minimum:

```text
3
```

Swap with `8`:

```text
1 2 3 5 8
```

Now:

```text
[1 2 3] | 5 8
```

`3` is fixed ✅

---

## 🔹 Pass 4

Unsorted portion:

```text
5 8
```

Minimum:

```text
5
```

Already in the correct position.

```text
1 2 3 5 8
```

---

# 📊 Visualization

```text
5 3 8 1 2
↓
Find minimum = 1
↓
1 3 8 5 2

[1] | 3 8 5 2
        ↓
Find minimum = 2
        ↓
1 2 8 5 3

[1 2] | 8 5 3
          ↓
Find minimum = 3
          ↓
1 2 3 5 8

[1 2 3] | 5 8
            ↓
          Sorted
```

---

# 💻 C++ Implementation

```cpp
#include<iostream>
using namespace std;

void selectionSort(int arr[], int n)
{
    for(int i = 0; i < n - 1; i++)
    {
        int minIndex = i;

        for(int j = i + 1; j < n; j++)
        {
            if(arr[j] < arr[minIndex])
            {
                minIndex = j;
            }
        }

        swap(arr[i], arr[minIndex]);
    }
}

int main()
{
    int arr[] = {5, 3, 8, 1, 2};
    int n = 5;

    selectionSort(arr, n);

    for(int i = 0; i < n; i++)
    {
        cout << arr[i] << " ";
    }

    return 0;
}
```

---

# 🧩 Understanding the Code

## `minIndex`

```cpp
int minIndex = i;
```

Assume the first element of the unsorted portion is the minimum.

---

## Find Minimum

```cpp
for(int j = i + 1; j < n; j++)
{
    if(arr[j] < arr[minIndex])
    {
        minIndex = j;
    }
}
```

Search the remaining unsorted elements.

If a smaller element is found:

```cpp
minIndex = j;
```

---

## Swap

After finding the minimum:

```cpp
swap(arr[i], arr[minIndex]);
```

Place the smallest element at its correct position.

---

# 🎯 Example

```text
Array:

64 25 12 22 11
```

### Pass 1

Minimum = `11`

```text
11 25 12 22 64
```

### Pass 2

Minimum = `12`

```text
11 12 25 22 64
```

### Pass 3

Minimum = `22`

```text
11 12 22 25 64
```

### Pass 4

Minimum = `25`

```text
11 12 22 25 64
```

Final:

```text
11 12 22 25 64
```

---

# ⏱️ Time Complexity

Selection Sort always searches the remaining unsorted portion.

Therefore:

| Case | Complexity |
|------|------------|
| Best Case | **O(N²)** |
| Average Case | **O(N²)** |
| Worst Case | **O(N²)** |

Even if the array is already sorted, it still performs comparisons.

---

# 💾 Space Complexity

```text
O(1)
```

Selection Sort works **in-place**.

---

# 📊 Complexity Summary

| Property | Selection Sort |
|----------|----------------|
| Best | O(N²) |
| Average | O(N²) |
| Worst | O(N²) |
| Space | O(1) |
| In-place | ✅ |
| Stable | ❌ |

---

# 🧠 Important Properties

## 🔹 In-Place

Only a few variables are used:

```cpp
minIndex
i
j
```

Therefore:

```text
Space = O(1)
```

---

## 🔹 Usually Not Stable

Selection Sort can change the relative order of equal elements because of swapping.

Therefore, the standard implementation is:

```text
Not Stable ❌
```

---

# 🆚 Selection Sort vs Bubble Sort

| Feature | 🎯 Selection Sort | 🫧 Bubble Sort |
|---------|------------------|----------------|
| Best | O(N²) | O(N) optimized |
| Average | O(N²) | O(N²) |
| Worst | O(N²) | O(N²) |
| Space | O(1) | O(1) |
| In-place | ✅ | ✅ |
| Stable | ❌ | ✅ |
| Main Idea | Select minimum | Swap adjacent |

---

# 🆚 Selection Sort vs Insertion Sort

| Feature | 🎯 Selection Sort | 🃏 Insertion Sort |
|---------|------------------|-------------------|
| Best | O(N²) | O(N) |
| Average | O(N²) | O(N²) |
| Worst | O(N²) | O(N²) |
| Space | O(1) | O(1) |
| Stable | ❌ | ✅ |
| Nearly Sorted | ❌ | 🚀 Excellent |

---

# 🆚 All 4 Sorting Algorithms

| Algorithm | Best | Average | Worst | Space | Stable |
|-----------|------|---------|-------|-------|--------|
| 🫧 Bubble | O(N) | O(N²) | O(N²) | O(1) | ✅ |
| 🃏 Insertion | O(N) | O(N²) | O(N²) | O(1) | ✅ |
| 🔀 Merge | O(N log N) | O(N log N) | O(N log N) | O(N) | ✅ |
| 🎯 Selection | O(N²) | O(N²) | O(N²) | O(1) | ❌ |

---

# 🔥 Interview Questions

### ❓ What is the main idea of Selection Sort?

Find the minimum element from the unsorted portion and place it at the beginning.

---

### ❓ What is the time complexity?

```text
O(N²)
```

for best, average, and worst cases.

---

### ❓ Is Selection Sort in-place?

✅ Yes.

```text
O(1) space
```

---

### ❓ Is Selection Sort stable?

❌ Standard Selection Sort is not stable.

---

### ❓ Why is the best case still O(N²)?

Because the algorithm still scans the remaining unsorted elements to find the minimum.

---

### ❓ How many major passes are required?

Approximately:

```text
N - 1
```

passes.

---

# 🧠 Quick Revision

```text
Start
  ↓
Assume current element is minimum
  ↓
Search remaining array
  ↓
Find actual minimum
  ↓
Swap
  ↓
Move boundary
  ↓
Repeat
```

### Remember:

```text
Selection Sort
      ↓
Find Minimum
      ↓
Swap with Current
      ↓
Sorted Portion Grows
```

---

# 🎯 Interview Cheat Sheet

```text
Algorithm      → Selection Sort

Technique      → Comparison

Main Operation → Find Minimum + Swap

Best Case      → O(N²)

Average Case   → O(N²)

Worst Case     → O(N²)

Space          → O(1)

In-place       → Yes

Stable         → No
```

---

# 🎉 Key Takeaways

⭐ Selection Sort repeatedly finds the minimum element.

⭐ The minimum is placed at the beginning of the unsorted portion.

⭐ The sorted portion grows from left to right.

⭐ Time Complexity → **O(N²)** in all cases.

⭐ Space Complexity → **O(1)**.

⭐ Standard Selection Sort is **in-place but not stable**.

⭐ It performs fewer swaps than Bubble Sort, but still requires O(N²) comparisons.