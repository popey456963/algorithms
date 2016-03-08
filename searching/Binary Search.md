# Binary Search - Code

Psuedo code:
```python
BinarySearch_Right(A[0..N-1], value, low, high) {
    if (high < low)
        return low
    mid = (low + high) / 2
    if (A[mid] > value)
        return BinarySearch_Right(A, value, low, mid-1)
    else
        return BinarySearch_Right(A, value, mid+1, high)
}
```

Python
```python
def binary_search(l, value):
    low = 0
    high = len(l)-1
    while low <= high: 
        mid = (low+high)//2
        if l[mid] > value: high = mid-1
        elif l[mid] < value: low = mid+1
        else: return mid
    return -1
```

# Binary Search - Algorithm

The binary search algorithm begins by comparing the target value to the value of the middle element of the sorted array. If the target value is equal to the middle element's value, then the position is returned and the search is finished. If the target value is less than the middle element's value, then the search continues on the lower half of the array; or if the target value is greater than the middle element's value, then the search continues on the upper half of the array. This process continues, eliminating half of the elements, and comparing the target value to the value of the middle element of the remaining elements - until the target value is either found (and its associated element position is returned), or until the entire array has been searched (and "not found" is returned).

