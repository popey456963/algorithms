# Bubble Sort - Code

Pseudo code:
```python
def bubbleSort(alist):
    for passnum in range(len(alist)-1,0,-1):
        for i in range(passnum):
            if alist[i]>alist[i+1]:
                temp = alist[i]
                alist[i] = alist[i+1]
                alist[i+1] = temp

alist = [54,26,93,17,77,31,44,55,20]
bubbleSort(alist)
print(alist)
```

Python:
```python
func bubblesort( var a as array )
    for i from 1 to N
        for j from 0 to N - 1
           if a[j] > a[j + 1]
              swap( a[j], a[j + 1] )
end func
```
---
# Bubble Sort - Algorithm

The bubble sort works by passing sequentially over a list, comparing each value to the one immediately after it. If the first value is greater than the second, their positions are switched. Over a number of passes, at most equal to the number of elements in the list, all of the values drift into their correct positions (large values "bubble" rapidly toward the end, pushing others down around them). Because each pass finds the maximum item and puts it at the end, the portion of the list to be sorted can be reduced at each pass. A boolean variable is used to track whether any changes have been made in the current pass; when a pass completes without changing anything, the algorithm exits.
