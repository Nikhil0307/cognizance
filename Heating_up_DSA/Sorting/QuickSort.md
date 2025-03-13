---
title: "QuickSort: Sorting"
date: "2025-03-12"
tags:
  - "Sorting"
  - "QuickSort"
---

**Time Complexity ->** O(N log N)
**Space Complexity ->** O(log N)
**When to use :**
>Large Data sets 

**How to ?**
- **Choose a Pivot**: Select a pivot element from the array. This can be the first element, the last element, the middle element, or chosen randomly.
- **Partition**: Rearrange the array so that elements less than the pivot are on its left, and elements greater than the pivot are on its right. The pivot is now in its correct position.
- **Recursively Sort**: Apply the same process to the left and right sub-arrays.
- **Combine**: Since the partition step sorts around the pivot, combining is simply the concatenation of the left sub-array, pivot, and right sub-array.