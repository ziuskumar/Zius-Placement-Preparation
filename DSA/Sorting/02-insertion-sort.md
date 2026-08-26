# 🃏 Insertion Sort

---

# 📖 Introduction

**Insertion Sort** is a comparison-based sorting algorithm that builds the sorted array **one element at a time**.

It takes an element from the unsorted portion and inserts it into its correct position in the sorted portion.

Think of arranging playing cards in your hand 🃏.

---

# 📌 Definition

> **Insertion Sort repeatedly takes an element from the unsorted portion and inserts it into its correct position in the sorted portion.**

---

# 🧠 Basic Idea

The array is divided conceptually into:

```text
Sorted Portion | Unsorted Portion
```

Initially:

```text
[5] | 3 8 1 2
```

Take `3` and insert it:

```text
[3 5] | 8 1 2
```

Take `8`:

```text
[3 5 8] | 1 2
```

Take `1`:

```text
[1 3 5 8] | 2
```

Take `2`:

```text
[1 2 3 5 8]
```

---

# 🎯 Example

Given:

```text
5 3 8 1 2
```

Expected:

```text
1 2 3 5 8
```

---

# ⚙️ How It Works

## 🔹 Step 1

First element is considered sorted:

```text
[5] | 3 8 1 2
```

---

## 🔹 Step 2

Take `3`.

Compare it with `5`:

```text
5 > 3
```

Shift `5` right:

```text
_ 5
```

Insert `3`:

```text
3 5 | 8 1 2
```

---

## 🔹 Step 3

Take `8`.

```text
8 > 5
```

No shifting is required.

```text
3 5 8 | 1 2
```

---

## 🔹 Step 4

Take `1`.

Compare:

```text
8 > 1 → Shift
5 > 1 → Shift
3 > 1 → Shift
```

Then insert `1`:

```text
1 3 5 8 | 2
```

---

## 🔹 Step 5

Take `2`.

```text
8 > 2 → Shift
5 > 2 → Shift
3 > 2 → Shift
```

Insert `2`:

```text
1 2 3 5 8
```

---

# 💻 C++ Implementation

```cpp
#include<iostream>
using namespace std;

void insertionSort(int arr[], int n)
{
    for(int i = 1; i < n; i++)
    {
        int key = arr[i];
        int j = i - 1;

        while(j >= 0 && arr[j] > key)
        {
            arr[j + 1] = arr[j];
            j--;
        }

        arr[j + 1] = key;
    }
}

int main()
{
    int arr[] = {5, 3, 8, 1, 2};
    int n = 5;

    insertionSort(arr, n);

    for(int i = 0; i < n; i++)
    {
        cout << arr[i] << " ";
    }

    return 0;
}
```

---

# 🧩 Understanding the Code

### `key`

```cpp
int key = arr[i];
```

The current element that we want to insert into the sorted portion.

---

### `j`

```cpp
int j = i - 1;
```

Starts from the last element of the sorted portion.

---

### Shift Elements

```cpp
while(j >= 0 && arr[j] > key)
{
    arr[j + 1] = arr[j];
    j--;
}
```

Elements greater than `key` are shifted one position to the right.

---

### Insert Key

```cpp
arr[j + 1] = key;
```

After finding the correct position, insert the `key`.

---

# 📊 Visualization

```text
5 3 8 1 2

↓
5 | 3 8 1 2

Take 3

↓
3 5 | 8 1 2

Take 8

↓
3 5 8 | 1 2

Take 1

↓
1 3 5 8 | 2

Take 2

↓
1 2 3 5 8
```

---

# 🌍 Real-World Example

Imagine holding playing cards 🃏.

You receive cards one by one.

If you receive:

```text
5
```

Your hand:

```text
5
```

Receive `3`:

```text
3 5
```

Receive `8`:

```text
3 5 8
```

Receive `1`:

```text
1 3 5 8
```

You continuously insert each new card into its correct position.

That's exactly how **Insertion Sort** works.

---

# ⏱️ Time Complexity

| Case | Complexity |
|------|------------|
| Best Case | **O(N)** 🚀 |
| Average Case | **O(N²)** |
| Worst Case | **O(N²)** |

---

# 💾 Space Complexity

```text
O(1)
```

Insertion Sort works **in-place**.

No additional array is required.

---

# 📊 Complexity Summary

| Property | Insertion Sort |
|----------|----------------|
| Best | O(N) |
| Average | O(N²) |
| Worst | O(N²) |
| Space | O(1) |
| In-place | ✅ |
| Stable | ✅ |

---

# 🚀 Best Case

Already sorted array:

```text
1 2 3 4 5
```

Very few shifts are required.

Therefore:

```text
O(N)
```

---

# 💥 Worst Case

Reverse sorted array:

```text
5 4 3 2 1
```

Almost every element must be shifted.

Therefore:

```text
O(N²)
```

---

# 🧠 Important Properties

### 🔹 In-Place

```text
Extra Space = O(1)
```

---

### 🔹 Stable

Equal elements maintain their relative order.

```text
(3,A) (3,B)
```

remains:

```text
(3,A) (3,B)
```

---

### 🔹 Adaptive

Insertion Sort performs well when the array is **already sorted or nearly sorted**.

---

# ⚠️ Common Mistakes

❌ Starting from `i = 0`.

Correct:

```cpp
i = 1
```

❌ Forgetting to save the current element:

```cpp
int key = arr[i];
```

❌ Using swapping unnecessarily instead of shifting.

❌ Forgetting:

```cpp
arr[j + 1] = key;
```

---

# 🔥 Interview Questions

### ❓ Why does Insertion Sort start from index 1?

Because the first element alone is already considered sorted.

---

### ❓ What is the best-case complexity?

```text
O(N)
```

when the array is already sorted.

---

### ❓ What is the worst-case complexity?

```text
O(N²)
```

when the array is reverse sorted.

---

### ❓ Is Insertion Sort stable?

✅ Yes.

---

### ❓ Is Insertion Sort in-place?

✅ Yes.

Space:

```text
O(1)
```

---

### ❓ When is Insertion Sort useful?

It is useful for:

- ✅ Small arrays
- ✅ Nearly sorted arrays
- ✅ Online insertion scenarios
- ✅ Learning sorting fundamentals

---

# 🧠 Quick Revision

```text
Take element
     ↓
Compare with sorted portion
     ↓
Shift larger elements
     ↓
Find correct position
     ↓
Insert element
     ↓
Repeat
```

### Remember:

```text
Insertion Sort
      ↓
Sorted Portion + Unsorted Portion
      ↓
Take Key
      ↓
Shift Larger Elements
      ↓
Insert Key
```

---

# 🎯 Interview Cheat Sheet

```text
Algorithm      → Insertion Sort

Technique      → Comparison

Best Case      → O(N)

Average Case   → O(N²)

Worst Case     → O(N²)

Space          → O(1)

In-place       → Yes

Stable         → Yes

Good For       → Small / Nearly Sorted Arrays
```

---

# 🎉 Key Takeaways

⭐ Insertion Sort builds the sorted portion one element at a time.

⭐ The current element is called the **key**.

⭐ Larger elements are shifted to the right.

⭐ The key is inserted into its correct position.

⭐ It is **in-place** and **stable**.

⭐ Best Case → **O(N)**.

⭐ Average/Worst → **O(N²)**.

⭐ It performs especially well on **small or nearly sorted arrays**.    