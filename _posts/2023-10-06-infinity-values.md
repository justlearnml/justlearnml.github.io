---
tags: ["Javascript", "Programming", "Python"]
metaDescription: Learn how to use infinity and negative infinity in Python and JavaScript to set range boundaries.
---

We can use infinity and negative infinity to represent the upper bound and lower bound of a range.

In Python, they are `float("inf")` and `float("-inf")`.
Here's an example code to find the minimum value from a list without using a built-in function in Python.

```python
    def find_min(arr):
        min = float("inf")
        for num in arr:
            if num < min:
                min = num
        return min
```

In Javascript, they are `Number.POSITIVE_INFINITY` and `Number.NEGATIVE_INFINITY`.
Here's the code.

```javascript
    function findMin(arr) {
        let min = Number.POSITIVE_INFINITY;
        for (let num of arr) {
            if (num < min) {
                min = num;
            }
        }
        return min;
    }
```
