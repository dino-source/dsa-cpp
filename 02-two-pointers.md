# LeetCode Pattern: Two Pointers

## Overview

The Two Pointers pattern uses two indices to traverse an array or a
string efficiently.

Instead of checking every possible pair with nested loops, two pointers
allow you to reduce many `O(n²)` solutions to `O(n)` by carefully moving
through the data.

This pattern is especially useful for:

- sorted arrays;
- comparing elements from opposite directions;
- removing duplicates;
- modifying arrays in-place;
- finding pairs that satisfy certain conditions.

In C++, this pattern commonly uses:

- `std::vector`
- `std::string`
- iterators

The key skill is understanding when pointer movement can eliminate
unnecessary comparisons.

---

## Practice Problems

Solve these problems in order. The early problems introduce basic pointer
movement, while the later ones require more advanced reasoning.

### Easy

- **125. Valid Palindrome**  
  <https://leetcode.com/problems/valid-palindrome/>

  Compare characters from both ends while moving pointers toward the center.

- **344. Reverse String**  
  <https://leetcode.com/problems/reverse-string/>

  Swap characters using left and right pointers.

- **26. Remove Duplicates from Sorted Array**  
  <https://leetcode.com/problems/remove-duplicates-from-sorted-array/>

  Use a slow pointer to track the next position for unique values.

- **27. Remove Element**  
  <https://leetcode.com/problems/remove-element/>

  Filter unwanted values while modifying the array in-place.

- **88. Merge Sorted Array**  
  <https://leetcode.com/problems/merge-sorted-array/>

  Merge two sorted arrays by processing elements from the end.

- **283. Move Zeroes**  
  <https://leetcode.com/problems/move-zeroes/>

  Move non-zero elements forward while preserving their relative order.

### Medium

- **167. Two Sum II - Input Array Is Sorted**  
  <https://leetcode.com/problems/two-sum-ii-input-array-is-sorted/>

  Use left and right pointers because the array is sorted.

- **11. Container With Most Water**  
  <https://leetcode.com/problems/container-with-most-water/>

  Move the pointer with the smaller height to search for a better result.

### Hard

- **42. Trapping Rain Water**  
  <https://leetcode.com/problems/trapping-rain-water/>

  Track maximum boundaries while moving pointers inward.

---

## Pattern Recognition Checklist

Ask yourself:

- Is the input sorted?
- Can I avoid checking every possible pair?
- Do I need to compare values from both ends?
- Can I solve the problem with a single pass?
- Can I modify the data structure in-place?
- Can pointer movement maintain a useful invariant?

If the answer is yes, Two Pointers is likely a strong candidate.

---

## Common Interview Keywords

Look for phrases like:

- "sorted array";
- "find a pair";
- "remove duplicates";
- "in-place";
- "reverse";
- "merge";
- "compare from both ends";
- "closest pair";
- "partition".

---

## Two Pointer Variations

### Opposite Direction Pointers

Two pointers start at opposite ends and move toward each other.

Typical examples:

- Valid Palindrome
- Two Sum II
- Container With Most Water

Example:

```text
left  --->        <---  right
```

---

### Same Direction Pointers

Both pointers move in the same direction, usually at different speeds.

Typical examples:

- Remove Duplicates from Sorted Array
- Remove Element
- Move Zeroes

Example:

```text
slow --->

fast -------->
```

---

## Complexity

Most Two Pointers solutions have:

- Time complexity: `O(n)`
- Space complexity: `O(1)`

The main advantage is replacing nested loops with a single linear scan.

---

## Learning Goals

After completing this pattern, you should be able to:

- recognize when two pointers can replace brute force;
- choose the correct pointer movement strategy;
- solve in-place array problems;
- explain the invariant behind your solution;
- analyze time and space complexity.

---

## Progress

- [ ] 125. Valid Palindrome
- [ ] 344. Reverse String
- [ ] 26. Remove Duplicates from Sorted Array
- [ ] 27. Remove Element
- [ ] 88. Merge Sorted Array
- [ ] 283. Move Zeroes
- [ ] 167. Two Sum II - Input Array Is Sorted
- [ ] 11. Container With Most Water
- [ ] 42. Trapping Rain Water
