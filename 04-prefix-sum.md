# LeetCode Pattern: Prefix Sum

## Overview

The Prefix Sum pattern helps solve problems involving cumulative values,
ranges, and subarrays.

The main idea is to store information about previous elements so that
future calculations can be performed efficiently.

Instead of repeatedly calculating the same ranges:

```text
Brute force:
Calculate each range separately.
Time complexity: O(n²)

Prefix sum:
Precompute cumulative values once.
Time complexity: O(n)
```

A prefix sum stores the total value from the beginning of the input up to
each position.

Example:

```text
Array:
[2, 4, 6, 8]

Prefix sum:
[2, 6, 12, 20]
```

In C++, this pattern commonly uses:

- `std::vector`
- `std::unordered_map`

The key skill is recognizing when previously calculated information can
help answer future queries faster.

---

## Practice Problems

Solve these problems in order. The early problems introduce basic prefix
sum calculations, while the later ones combine prefix sums with hashing.

### Easy

- **1480. Running Sum of 1d Array**  
  <https://leetcode.com/problems/running-sum-of-1d-array/>

  Build a running total while iterating through the array.

- **724. Find Pivot Index**  
  <https://leetcode.com/problems/find-pivot-index/>

  Compare the sum of elements on the left and right side of each index.

- **303. Range Sum Query - Immutable**  
  <https://leetcode.com/problems/range-sum-query-immutable/>

  Precompute prefix sums to answer range sum queries efficiently.

### Medium

- **560. Subarray Sum Equals K**  
  <https://leetcode.com/problems/subarray-sum-equals-k/>

  Combine prefix sums with a hash map to count matching subarrays.

- **525. Contiguous Array**  
  <https://leetcode.com/problems/contiguous-array/>

  Use prefix sums to track the balance between two values.

- **974. Subarray Sums Divisible by K**  
  <https://leetcode.com/problems/subarray-sums-divisible-by-k/>

  Use prefix sums and modular arithmetic to find valid subarrays.

---

## Pattern Recognition Checklist

Ask yourself:

- Do I need to calculate sums of ranges repeatedly?
- Am I working with subarrays or contiguous segments?
- Can previous elements help answer future queries?
- Can I avoid recalculating the same information?
- Do I need to find a subarray with a specific property?

If yes, Prefix Sum is likely a strong candidate.

---

## Common Interview Keywords

Look for phrases like:

- "range sum";
- "subarray";
- "contiguous";
- "running total";
- "cumulative";
- "sum equals";
- "number of subarrays";
- "between indices".

---

## Common Prefix Sum Variations

### Basic Prefix Sum

Store cumulative values while scanning the array.

Example:

```text
Array:
[3, 5, 2, 7]

Prefix sum:
[3, 8, 10, 17]
```

This allows range sums to be calculated without iterating through the
entire range again.

---

### Prefix Sum + Hash Map

Combine prefix sums with a hash map when you need to count or find
subarrays.

Typical examples:

- Subarray Sum Equals K
- Contiguous Array
- Subarray Sums Divisible by K

The hash map stores prefix states that have already been seen.

---

### Prefix Sum + Difference

Sometimes you only need to track the difference between values rather
than the actual sum.

Typical example:

- Contiguous Array

This transforms the problem into finding repeated prefix states.

---

## Complexity

Most Prefix Sum solutions have:

- Time complexity: `O(n)`
- Space complexity: `O(n)`

The additional space is usually used to store prefix information.

Some problems can be optimized to:

- Time complexity: `O(n)`
- Space complexity: `O(1)`

by storing only the required running values.

---

## Learning Goals

After completing this pattern, you should be able to:

- recognize range and subarray problems;
- build prefix sums quickly;
- combine prefix sums with hash maps;
- avoid repeated calculations;
- explain the complexity improvement clearly.

---

## Progress

- [ ] 1480. Running Sum of 1d Array
- [ ] 724. Find Pivot Index
- [ ] 303. Range Sum Query - Immutable
- [ ] 560. Subarray Sum Equals K
- [ ] 525. Contiguous Array
- [ ] 974. Subarray Sums Divisible by K
