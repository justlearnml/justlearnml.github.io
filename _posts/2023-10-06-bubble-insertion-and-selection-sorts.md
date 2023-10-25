---
title: "Bubble, Insertion, and Selection Sorts"
tags: ["Algorithm", "Programming", "Sorting"]
metaDescription: Discover the Basics of Bubble, Insertion, and Selection Sorting Algorithms and How They Work
---

Bubble, Insertion, and Selection sorts are three of the most basic sorting algorithms I've recently revisited. Here's what I understand about them.

## Bubble Sort
Bubble Sort works by repeatedly swapping nearby elements until the biggest one ends up on the far right.

1) We start with the leftmost number, compare it to the next number on its right. If the left one is bigger, we swap them.

2) Next we move our focus to the 2nd number on the left, no matter if we swapped the numbers before or not.
Repeat this until reaching the end of the list. And this will place the biggest number at the very right.

3) Keep doing 1) and 2) until we don't have to swap anything anymore in one round. This means everything is sorted.
We can do a little optimization. Instead of reaching the rightmost number on the 2nd round, we only need to reach the 2nd rightmost number on the 2nd round,
and so forth on the subsequent rounds.

## Insertion Sort
Think of it like picking a card from a main deck and arranging them within our hand.

1) Start with the leftmost number, envision it as drawing this number into our hand.

2) Compare this number to our sorted numbers in our hand.
  - If our hand is empty at the moment, there's nothing to do.
  - If we have some numbers, compare this number with each of them one by one, starting from the rightmost one until we can find a position to insert this number.

3) Keep doing 1) and 2) until the deck is empty. At that point, all numbers are then sorted within our hand.

## Selection Sort
In my view, selection sort is the simplest sorting algorithm and is often the one we use mentally when sorting items in real-life situations.
Check each number, pick out the smallest one, and repeat the process.

## Additional Resources
Here are some informative articles explaining Bubble, Insertion, and Selection Sorts in greater detail.
- [Bubble Sort](https://www.geeksforgeeks.org/bubble-sort/)
- [Insertion Sort](https://www.geeksforgeeks.org/insertion-sort/)
- [Selection Sort](https://www.geeksforgeeks.org/selection-sort/)
