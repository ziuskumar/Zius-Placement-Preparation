# 🔀 Merge Sort

---

# 📖 Introduction

**Merge Sort** is a comparison-based sorting algorithm based on the **Divide and Conquer** technique.

Instead of sorting the entire array at once, it:

1. ✂️ Divides the array into smaller parts.
2. 🔁 Recursively sorts those parts.
3. 🧩 Merges the sorted parts together.

---

# 📌 Definition

> **Merge Sort divides an array into smaller subarrays, recursively sorts them, and then merges the sorted subarrays to produce the final sorted array.**

---

# 🧠 Core Idea

```text
Divide
   ↓
Recursively Sort
   ↓
Merge
   ↓
Sorted Array
```

---

# 🎯 Example

Given:

```text
5 3 8 1 2 7 4 6
```

First divide:

```text
5 3 8 1 | 2 7 4 6
```

Divide again:

```text
5 3 | 8 1 | 2 7 | 4 6
```

Again:

```text
5 | 3 | 8 | 1 | 2 | 7 | 4 | 6
```

Now start merging:

```text
3 5
1 8
2 7
4 6
```

Then:

```text
1 3 5 8
2 4 6 7
```

Finally:

```text
1 2 3 4 5 6 7 8
```

---

# ⚙️ Divide and Conquer

Merge Sort follows three steps.

## 1️⃣ Divide

Split the array into two halves.

```text
[5 3 8 1 2 7 4 6]

        ↓

[5 3 8 1] [2 7 4 6]
```

---

## 2️⃣ Conquer

Recursively divide and sort each half.

```text
[5 3] [8 1] [2 7] [4 6]
```

Continue until each subarray contains one element.

```text
[5] [3] [8] [1] [2] [7] [4] [6]
```

A single element is already sorted.

---

## 3️⃣ Combine

Merge the sorted pieces.

```text
[5] [3]
 ↓
[3 5]
```

```text
[8] [1]
 ↓
[1 8]
```

Continue until the entire array is sorted.

---

# 🌳 Recursion Tree

For:

```text
5 3 8 1
```

The recursion tree looks like:

```text
             [5 3 8 1]
              /      \
          [5 3]      [8 1]
          /  \       /  \
        [5] [3]    [8] [1]
```

Then merging happens:

```text
[5] + [3]
   ↓
 [3 5]

[8] + [1]
   ↓
 [1 8]

[3 5] + [1 8]
       ↓
 [1 3 5 8]
```

---

# 💻 C++ Implementation

```cpp
#include<iostream>
using namespace std;

void merge(int arr[], int left, int mid, int right)
{
    int n1 = mid - left + 1;
    int n2 = right - mid;

    int* L = new int[n1];
    int* R = new int[n2];

    for(int i = 0; i < n1; i++)
        L[i] = arr[left + i];

    for(int j = 0; j < n2; j++)
        R[j] = arr[mid + 1 + j];

    int i = 0;
    int j = 0;
    int k = left;

    while(i < n1 && j < n2)
    {
        if(L[i] <= R[j])
        {
            arr[k] = L[i];
            i++;
        }
        else
        {
            arr[k] = R[j];
            j++;
        }

        k++;
    }

    while(i < n1)
    {
        arr[k] = L[i];
        i++;
        k++;
    }

    while(j < n2)
    {
        arr[k] = R[j];
        j++;
        k++;
    }

    delete[] L;
    delete[] R;
}

void mergeSort(int arr[], int left, int right)
{
    if(left >= right)
        return;

    int mid = left + (right - left) / 2;

    mergeSort(arr, left, mid);

    mergeSort(arr, mid + 1, right);

    merge(arr, left, mid, right);
}

int main()
{
    int arr[] = {5, 3, 8, 1, 2, 7, 4, 6};
    int n = 8;

    mergeSort(arr, 0, n - 1);

    for(int i = 0; i < n; i++)
    {
        cout << arr[i] << " ";
    }

    return 0;
}
```

---

# 📥 Input

```text
5 3 8 1 2 7 4 6
```

---

# 📤 Output

```text
1 2 3 4 5 6 7 8
```

---

# 🧩 Understanding `merge()`

Suppose we have two sorted arrays:

```text
Left  → 1 4 7
Right → 2 3 8
```

Compare the first elements:

```text
1 < 2
```

Take `1`.

```text
1
```

Then:

```text
4 > 2
```

Take `2`.

```text
1 2
```

Then:

```text
4 > 3
```

Take `3`.

```text
1 2 3
```

Continue until both arrays are merged.

Final:

```text
1 2 3 4 7 8
```

---

# 🧠 Why `mid` is Calculated This Way?

```cpp
int mid = left + (right - left) / 2;
```

Instead of:

```cpp
int mid = (left + right) / 2;
```

The first version avoids potential integer overflow when `left` and `right` are very large.

---

# ⏱️ Time Complexity

Merge Sort divides the array into approximately `log N` levels.

At every level, merging takes:

```text
O(N)
```

Therefore:

```text
O(N) × O(log N)
```

### Final Complexity

```text
O(N log N)
```

for:

- ✅ Best Case
- ✅ Average Case
- ✅ Worst Case

---

# 💾 Space Complexity

Standard Merge Sort requires temporary arrays during merging.

```text
O(N)
```

Additional recursive stack space is:

```text
O(log N)
```

Overall auxiliary space:

```text
O(N)
```

---

# 📊 Complexity Summary

| Property | Merge Sort |
|----------|------------|
| Best | O(N log N) |
| Average | O(N log N) |
| Worst | O(N log N) |
| Space | O(N) |
| In-place | ❌ |
| Stable | ✅ |

---

# 🔹 Stable Sorting

Merge Sort can be **stable**.

Notice:

```cpp
if(L[i] <= R[j])
```

The `<=` ensures that when two values are equal, the element from the left side is chosen first.

This helps preserve the relative order of equal elements.

---

# ⚠️ Common Mistakes

❌ Forgetting the Base Case.

```cpp
if(left >= right)
    return;
```

❌ Incorrect midpoint.

❌ Incorrect merge boundaries.

❌ Forgetting to copy remaining elements.

❌ Forgetting to free dynamically allocated memory.

❌ Mixing up `mid` and `mid + 1`.

---

# 🔥 Interview Questions

### ❓ What technique does Merge Sort use?

✅ Divide and Conquer.

---

### ❓ What is the time complexity?

```text
O(N log N)
```

for all three cases.

---

### ❓ Why is Merge Sort O(N log N)?

Because:

```text
Log N levels
×
O(N) work per level
=
O(N log N)
```

---

### ❓ Is Merge Sort stable?

✅ Yes, with the standard stable merge implementation.

---

### ❓ Is Merge Sort in-place?

❌ Standard Merge Sort requires extra memory for merging.

---

### ❓ What is the major advantage over Bubble/Insertion Sort?

For large datasets:

```text
O(N log N)
```

is significantly better than:

```text
O(N²)
```

---

# 🆚 Merge Sort vs Bubble Sort

| Feature | 🔀 Merge Sort | 🫧 Bubble Sort |
|---------|---------------|---------------|
| Technique | Divide & Conquer | Comparison |
| Best | O(N log N) | O(N) optimized |
| Average | O(N log N) | O(N²) |
| Worst | O(N log N) | O(N²) |
| Space | O(N) | O(1) |
| Stable | ✅ | ✅ |
| Large Data | 🚀 Better | ❌ Poor |

---

# 🆚 Merge Sort vs Insertion Sort

| Feature | 🔀 Merge Sort | 🃏 Insertion Sort |
|---------|---------------|-------------------|
| Best | O(N log N) | O(N) |
| Average | O(N log N) | O(N²) |
| Worst | O(N log N) | O(N²) |
| Space | O(N) | O(1) |
| Stable | ✅ | ✅ |
| Nearly Sorted | Good | 🚀 Excellent |

---

# 🧠 Quick Revision

```text
Merge Sort
     ↓
Divide
     ↓
Divide
     ↓
Single Elements
     ↓
Merge
     ↓
Sorted Halves
     ↓
Final Sorted Array
```

### Remember:

```text
Divide → Recursion → Merge
```

---

# 🎯 Interview Cheat Sheet

```text
Algorithm      → Merge Sort

Technique      → Divide & Conquer

Best Case      → O(N log N)

Average Case   → O(N log N)

Worst Case     → O(N log N)

Space          → O(N)

In-place       → No

Stable         → Yes
```

---

# 🎉 Key Takeaways

⭐ Merge Sort uses **Divide and Conquer**.

⭐ The array is repeatedly divided into smaller pieces.

⭐ Single-element arrays are already sorted.

⭐ Sorted pieces are merged together.

⭐ Time Complexity → **O(N log N)** in all cases.

⭐ Standard implementation requires **O(N)** extra space.

⭐ Merge Sort is an important foundation for advanced algorithms and interview problems.