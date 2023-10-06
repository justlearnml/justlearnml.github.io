---
tags: ["Programming", "Python"]
metaDescription: Simplicity of Python List Comprehensions
---

As someone who worked extensively in frontend development,
I view Python's list comprehensions as the equivalent of JavaScript's `Array.prototype.map()` and `Array.prototype.filter()`. 
Personally I find this syntax more appealing because it keeps things simple with the usual syntax, no extra bits.

The basic syntax of a list comprehension is as follows:

```python
    new_list = [expression for item in iterable if condition]
```

To square all the numbers in a list
```python
    numbers = [1, 2, 3, 4, 5]
    squares = [x**2 for x in numbers]
    # squares is [1, 4, 9, 16, 25]
```

To filter even numbers from a list
```python
    numbers = [1, 2, 3, 4, 5, 6]
    evens = [x for x in numbers if x % 2 == 0]
    # evens is [2, 4, 6]
```
