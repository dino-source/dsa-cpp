# LeetCode Pattern: Binary Search

## Overview

The Binary Search pattern is used to efficiently search for an element or
a valid answer in a sorted search space.

The main idea is to repeatedly divide the search space in half and remove
the part that cannot contain the answer.

Instead of checking every element:

```text
Brute force:
Check every element one by one.
Time complexity: O(n)

Binary search:
Eliminate half of the search space each step.
Time complexity: O(log n)
```

Binary Search is commonly used for:

- searching in sorted arrays;
- finding boundaries;
- finding the first or last occurrence;
- searching over possible answers.

In C++, this pattern commonly uses:

- `std::vector`
- `std::lower_bound`
- `std::upper_bound`

The key skill is recognizing when the search space is ordered or when the
answer can be found by repeatedly narrowing possible solutions.

---

## Practice Problems

Solve these problems in order. The early problems introduce classic binary
search, while the later ones require searching over an answer space.

### Easy

- **704. Binary Search**  
  <https://leetcode.com/problems/binary-search/>

  Implement classic binary search on a sorted array.

- **35. Search Insert Position**  
  <https://leetcode.com/problems/search-insert-position/>

  Find the position where a target should be inserted.

- **69. Sqrt(x)**  
  <https://leetcode.com/problems/sqrtx/>

  Use binary search to find the integer square root.

- **374. Guess Number Higher or Lower**  
  <https://leetcode.com/problems/guess-number-higher-or-lower/>

  Use feedback to decide which half of the search space to discard.

### Medium

- **33. Search in Rotated Sorted Array**  
  <https://leetcode.com/problems/search-in-rotated-sorted-array/>

  Identify the sorted portion and decide which side to search.

- **153. Find Minimum in Rotated Sorted Array**  
  <https://leetcode.com/problems/find-minimum-in-rotated-sorted-array/>

  Use ordering information to locate the minimum element.

- **162. Find Peak Element**  
  <https://leetcode.com/problems/find-peak-element/>

  Move toward the side where a peak must exist.

- **34. Find First and Last Position of Element in Sorted Array**  
  <https://leetcode.com/problems/find-first-and-last-position-of-element-in-sorted-array/>

  Find the left and right boundaries of a target value.

### Hard

- **4. Median of Two Sorted Arrays**  
  <https://leetcode.com/problems/median-of-two-sorted-arrays/>

  Use binary search to partition two sorted arrays efficiently.

---

## Pattern Recognition Checklist

Ask yourself:

- Is the input sorted?
- Can I eliminate half of the search space each step?
- Am I looking for a boundary or position?
- Is there a monotonic relationship between input and output?
- Can I search over possible answers instead of actual values?

If yes, Binary Search is likely a strong candidate.

---

## Common Interview Keywords

Look for phrases like:

- "sorted array";
- "find position";
- "first occurrence";
- "last occurrence";
- "minimum possible";
- "maximum possible";
- "search space";
- "find the smallest value that works".

---

## Common Binary Search Variations

### Classic Binary Search

Search for an exact value in a sorted collection.

Example:

```text
Array:

[1, 3, 5, 7, 9]

Search: 7

1. Check the middle element.
2. Eliminate the wrong half.
3. Repeat.
```

Typical examples:

- Binary Search
- Search Insert Position

---

### Boundary Search

Find the first or last position where a condition is true.

Typical examples:

- Find First and Last Position of Element
- Lower Bound
- Upper Bound

The goal is not always finding a value, but finding a boundary.

---

### Binary Search on Answer

Search through possible answers instead of array elements.

Example:

```text
Find the minimum capacity that satisfies all requirements.
```

Typical examples:

- Koko Eating Bananas
- Capacity To Ship Packages Within D Days
- Split Array Largest Sum

---

## Complexity

Most Binary Search solutions have:

- Time complexity: `O(log n)`
- Space complexity: `O(1)`

Recursive implementations may use:

- Space complexity: `O(log n)`

because of the recursion stack.

---

## Learning Goals

After completing this pattern, you should be able to:

- recognize binary search opportunities quickly;
- implement boundary searches correctly;
- avoid common off-by-one errors;
- search over an answer space;
- explain why the solution runs in logarithmic time.

---

## Progress

- [ ] 704. Binary Search
- [ ] 35. Search Insert Position
- [ ] 69. Sqrt(x)
- [ ] 374. Guess Number Higher or Lower
- [ ] 33. Search in Rotated Sorted Array
- [ ] 153. Find Minimum in Rotated Sorted Array
- [ ] 162. Find Peak Element
- [ ] 34. Find First and Last Position of Element in Sorted Array
- [ ] 4. Median of Two Sorted Arrays
