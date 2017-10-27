---
title: Selection Sort
---
## Selection Sort

Selection Sort is a sorting algorithm that closely mimics how a person would sort a list of items.

It scans the entire list of items looking for the smallest item and puts that in position 1. It then scans the entire list again looking for the next smallest item and puts that in position 2. It continues this process over and over until the entire list is sorted.

## Example in Python

```py
def selection_sort(arr):
    """
    In-place sort using Selection Sort.
    Space Complexity: O(1)
    Time Complexity: O(n^2)
    Stable: No

    :param arr: list of values
    :return: None
    """
    if arr is None or len(arr) < 2:
        return arr

    for i in range(len(arr) - 1):
        min_index = i
        for j in range(i+1, len(arr)):
            if arr[j] < arr[min_index]:
                min_index = j
        arr[min_index], arr[i] = arr[i], arr[min_index]
```

## Properties:
* Space Complexity: O(1)
* Time Complexity: O(n^2)
* Stable: Can be, but more complex.

### More Information:

- <a href='https://en.wikipedia.org/wiki/Selection_sort' target='_blank' rel='nofollow'>Wikipedia</a>
