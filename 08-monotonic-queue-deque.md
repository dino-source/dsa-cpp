# LeetCode Pattern: Monotonic Queue (Deque)

## Overview

The Monotonic Queue pattern is used to efficiently maintain the maximum or
minimum value inside a moving window.

The main idea is to use a deque that keeps elements in increasing or
decreasing order while removing values that are no longer useful.

Unlike a normal queue, a monotonic queue allows:

- adding new elements;
- removing expired elements;
- retrieving the current maximum or minimum in `O(1)` time.

This pattern is especially useful for:

- sliding window maximum/minimum problems;
- maintaining the best candidate in a range;
- optimizing dynamic programming transitions.

In C++, this pattern commonly uses:

- `std::deque`
- `std::vector`

The key skill is recognizing when a problem requires the maximum or minimum
value inside a moving range.

---

## Practice Problems

Solve these problems in order. The early problems introduce the basic
monotonic deque idea, while the later ones combine it with other patterns.

### Medium

- **239. Sliding Window Maximum**  
  <https://leetcode.com/problems/sliding-window-maximum/>

  Maintain a decreasing deque to track the maximum value in each window.

- **1438. Longest Continuous Subarray With Absolute Diff <= Limit**  
  <https://leetcode.com/problems/longest-continuous-subarray-with-absolute-diff-less-than-or-equal-to-limit/>

  Use two monotonic deques to track the current minimum and maximum values.

- **862. Shortest Subarray with Sum at Least K**  
  <https://leetcode.com/problems/shortest-subarray-with-sum-at-least-k/>

  Combine prefix sums with a monotonic deque.

### Hard

- **1499. Max Value of Equation**  
  <https://leetcode.com/problems/max-value-of-equation/>

  Use a monotonic deque to maintain the best previous candidates.

- **1696. Jump Game VI**  
  <https://leetcode.com/problems/jump-game-vi/>

  Optimize dynamic programming by keeping the best values in a deque.

---

## Pattern Recognition Checklist

Ask yourself:

- Do I need the maximum or minimum value inside a sliding window?
- Does the window move from left to right?
- Can I remove elements that will never become useful again?
- Do I need `O(1)` access to the best candidate?
- Is a priority queue too slow because of repeated removals?

If yes, Monotonic Queue is likely a strong candidate.

---

## Common Interview Keywords

Look for phrases like:

- "sliding window maximum";
- "maximum in every window";
- "minimum in every window";
- "longest subarray";
- "shortest subarray";
- "moving range";
- "maximum value";
- "minimum value".

---

## Common Monotonic Queue Variations

### Decreasing Deque

The deque stores values in decreasing order.

The front always contains the current maximum.

When adding a new element:

1. Remove smaller elements from the back.
2. Add the new element.
3. Remove expired elements from the front.

Example:

```text
Window:

[4, 2, 1]

New value: 5

Remove:
1
2

Deque:

[5]
```

Typical examples:

- Sliding Window Maximum
- Jump Game VI

---

### Increasing Deque

The deque stores values in increasing order.

The front always contains the current minimum.

Typical examples:

- Longest Continuous Subarray With Absolute Diff <= Limit
- Shortest Subarray with Sum at Least K

---

## Complexity

Most Monotonic Queue solutions have:

- Time complexity: `O(n)`
- Space complexity: `O(k)`

where `k` is the size of the current window.

Each element is added and removed from the deque at most once.

---

## Learning Goals

After completing this pattern, you should be able to:

- recognize sliding window maximum/minimum problems;
- use `std::deque` to maintain candidates;
- remove useless elements efficiently;
- understand why each element is processed once;
- combine monotonic queues with other patterns.

---

## Progress

- [ ] 239. Sliding Window Maximum
- [ ] 1438. Longest Continuous Subarray With Absolute Diff <= Limit
- [ ] 862. Shortest Subarray with Sum at Least K
- [ ] 1499. Max Value of Equation
- [ ] 1696. Jump Game VI
