---
title: "InsertionSort: Sorting"
date: "2025-03-12"
tags:
  - "Sorting"
  - "InsertionSort"
---

**Time Complexity ->** O(N²)
**Space Complexity ->** O(1)
**When to use :**
>Small data 
>Nearly sorted array 

**How to ?**
- Start with the second element (assuming the first element is already sorted).
- Compare the current element with the elements before it.
- Shift larger elements to the right to make space for the current element.
- Insert the current element into its correct position.
- Repeat for each element until the entire array is sorted.

```
for (int i = 1; i < n; i++) {  
    int key = arr[i];  
    int j = i - 1;  
  
    while (j >= 0 && arr[j] > key) {  
        arr[j + 1] = arr[j];  
        j = j - 1;  
    }  
    arr[j + 1] = key;  
}
```