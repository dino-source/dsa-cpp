# LeetCode Pattern: Monotonic Stack

## Overview

The Monotonic Stack pattern is used to efficiently solve problems where
you need to find the next or previous greater or smaller element.

The main idea is to maintain a stack where elements are always increasing
or decreasing in order.

Instead of comparing every element with all previous or following
elements, the stack stores only useful candidates.

This pattern is especially useful for:

- next greater element problems;
- next smaller element problems;
- finding ranges where an element is the minimum or maximum;
- processing elements in a single pass.

There are two main variations:

- increasing monotonic stack;
- decreasing monotonic stack.

In C++, this pattern commonly uses:

- `std::stack`
- `std::vector`

The key skill is recognizing when elements need to be compared with their
nearest greater or smaller neighbors.

---

## Practice Problems

Solve these problems in order. The early problems introduce the basic
monotonic stack idea, while the later ones require more advanced
reasoning.

### Easy

- **496. Next Greater Element I**  
  <https://leetcode.com/problems/next-greater-element-i/>

  Use a decreasing stack to find the next greater element.

- **1475. Final Prices With a Special Discount in a Shop**  
  <https://leetcode.com/problems/final-prices-with-a-special-discount-in-a-shop/>

  Find the next smaller or equal value using a monotonic stack.

### Medium

- **503. Next Greater Element II**  
  <https://leetcode.com/problems/next-greater-element-ii/>

  Apply monotonic stack logic to a circular array.

- **739. Daily Temperatures**  
  <https://leetcode.com/problems/daily-temperatures/>

  Find the next warmer day for each temperature.

- **901. Online Stock Span**  
  <https://leetcode.com/problems/online-stock-span/>

  Maintain a stack of previous prices that are still relevant.

- **84. Largest Rectangle in Histogram**  
  <https://leetcode.com/problems/largest-rectangle-in-histogram/>

  Use increasing stack logic to find maximum rectangle areas.

### Hard

- **42. Trapping Rain Water**  
  <https://leetcode.com/problems/trapping-rain-water/>

  Use stack-based processing to calculate trapped water between bars.

- **907. Sum of Subarray Minimums**  
  <https://leetcode.com/problems/sum-of-subarray-minimums/>

  Find how many subarrays each element contributes as the minimum.

---

## Pattern Recognition Checklist

Ask yourself:

- Do I need the next greater or smaller element?
- Am I comparing each element with previous elements?
- Can previous elements become irrelevant after seeing a new value?
- Do I need to find ranges where an element is the maximum or minimum?
- Can I process the array from left to right while maintaining candidates?

If yes, Monotonic Stack is likely a strong candidate.

---

## Common Interview Keywords

Look for phrases like:

- "next greater";
- "next smaller";
- "previous greater";
- "previous smaller";
- "nearest";
- "span";
- "largest rectangle";
- "temperature";
- "histogram".

---

## Common Monotonic Stack Variations

### Decreasing Stack

The stack keeps elements in decreasing order.

When a new element is larger than the stack top, smaller elements are
removed because they can no longer be useful.

Typical examples:

- Next Greater Element
- Daily Temperatures
- Online Stock Span

Example:

```text
Stack:

[8, 5, 3]

New value: 6

Remove:
3
5

Keep:
8, 6
```

---

### Increasing Stack

The stack keeps elements in increasing order.

When a new element is smaller than the stack top, larger elements are
removed.

Typical examples:

- Largest Rectangle in Histogram
- Sum of Subarray Minimums

---

## Complexity

Most Monotonic Stack solutions have:

- Time complexity: `O(n)`
- Space complexity: `O(n)`

Although elements may be pushed and popped multiple times, each element
is processed at most once.

---

## Learning Goals

After completing this pattern, you should be able to:

- recognize next greater/smaller element problems;
- choose between increasing and decreasing stacks;
- understand when elements become irrelevant;
- avoid nested loops with stack-based solutions;
- explain why the algorithm runs in linear time.

---

## Progress

- [ ] 496. Next Greater Element I
- [ ] 1475. Final Prices With a Special Discount in a Shop
- [ ] 503. Next Greater Element II
- [ ] 739. Daily Temperatures
- [ ] 901. Online Stock Span
- [ ] 84. Largest Rectangle in Histogram
- [ ] 42. Trapping Rain Water
- [ ] 907. Sum of Subarray Minimums
