
# Merge sort

Pseudo code:
```python
function merge_sort(list m)
    if length of m ≤ 1 then
        return m
    var left := empty list
    var right := empty list
    for each x with index i in m do
        if i is odd then
            add x to left
        else
            add x to right
    left := merge_sort(left)
    right := merge_sort(right)
    return merge(left, right)
```

---

Python:
```python
from heapq import merge
 
def merge_sort(m):
    if len(m) <= 1:
        return m
 
    middle = len(m) // 2
    left = m[:middle]
    right = m[middle:]
 
    left = merge_sort(left)
    right = merge_sort(right)
    return list(merge(left, right))

```
---
# Merge Sort - Algorithm

Conceptually, a merge sort works as follows:

1. Divide the unsorted list into n sublists, each containing 1 element (a list of 1 element is considered sorted).
2. Repeatedly merge sublists to produce new sorted sublists until there is only 1 sublist remaining. This will be the sorted list.