---
tags: ["Algorithm", "Programming", "Python"]
metaDescription: Learn how to work with modular arithmetic in Python for wrapping values around a range, like hours and letters.
---

In modular arithmetic, we work within a set range, and when we perform operations like addition or subtraction,
the values "wrap around" within that range.

For instance, let's consider a function that takes an hour as one input and an increment (a positive integer) as another.
The hour can range from 0 to 23, and we want the function to return an hour within this range after incrementing.

The solution is straightforward: we use the modulo operator to get the result. Here's the code:

```python
def increment_hour(hour, increment):
    return (hour + increment) % 24
```

However, things get a bit more interesting when the starting point of our range isn't 0.
Consider a function that takes a lowercase English character as the first argument and an increment as the second.
This increment shifts the character to the right and wraps around.
For example, if we start with "z" and increment it by 2, the result should be "b".

We can see that "a" has an integer representation of `ord("a")` = 97, and "z" is `ord("z")` = 122.
Now, when we increase "z" by 2, it becomes 124. But how can we transform 124 into 98, which represents "b"?

If we attempt to calculate 124 modulo 26, we'll get 20, which isn't what we need. And adding 20 to 97 won't yield 98 either. 
Something's missing.

Actually 20 would be the correct answer if we were starting from 0.
To illustrate, let's consider cycles:

- 0 to 25
- 26 to 51
- 52 to 77
- 78 to 103
- 104 to 129

In the last cycle, we can see that 124 is in the 6th position from the last value, just like 20.

The solution is to determine the difference between the shifted number and the starting number,
effectively resetting the starting point to 0.
We then calculate this number modulo the total number of alphabets, which is 26.
At this stage, the result represents the position as if "a" had started at 0. To get it back to where we want, we add 97.

```python
def right_shift_letter(letter, increment):
    return chr((ord(letter) + increment - ord("a")) % 26 + ord("a"))
```
