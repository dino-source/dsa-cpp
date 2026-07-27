# LeetCode Pattern: Meet in the Middle

## Overview

The Meet in the Middle pattern is an optimization technique used for
problems where brute force enumeration is too expensive, but the input is
small enough to split into two halves.

The main idea is to divide the problem into two smaller independent
parts, solve each part separately, and then combine the results.

Instead of exploring all possibilities:

```text
n elements:

2^n possibilities
```

split the input:

```text
First half:

2^(n/2)

Second half:

2^(n/2)
```

The total work becomes approximately:

```text
2 * 2^(n/2)
```

which is dramatically faster.

Meet in the Middle is especially useful for:

- subset problems;
- combinatorial search;
- optimization problems;
- problems where `n` is too large for backtracking but too small for
  polynomial solutions.

Typical constraints:

```text
n ≈ 30 - 40
```

where normal brute force is impossible.

In C++, this pattern commonly uses:

- recursion;
- `std::vector`;
- `std::unordered_map`;
- `std::sort`;
- binary search.

The key skill is recognizing when the search space is exponential but can
be reduced by splitting the input.

---

## Practice Problems

Solve these problems in order. The early problems introduce subset
enumeration, while the later ones require combining multiple techniques.

### Medium

- **1755. Closest Subsequence Sum**  
  <https://leetcode.com/problems/closest-subsequence-sum/>

  Split the array into two halves and find the subset sum closest to a
  target.

- **2035. Partition Array Into Two Arrays to Minimize Sum Difference**  
  <https://leetcode.com/problems/partition-array-into-two-arrays-to-minimize-sum-difference/>

  Generate subset sums from both halves and combine them efficiently.

- **805. Split Array With Same Average**  
  <https://leetcode.com/problems/split-array-with-same-average/>

  Use subset enumeration and mathematical transformations.

### Hard

- **698. Partition to K Equal Sum Subsets**  
  <https://leetcode.com/problems/partition-to-k-equal-sum-subsets/>

  Apply advanced subset search techniques with pruning.

- **956. Tallest Billboard**  
  <https://leetcode.com/problems/tallest-billboard/>

  Divide possible assignments into two groups and optimize the balance.

- **1434. Number of Ways to Wear Different Hats to Each Other**  
  <https://leetcode.com/problems/number-of-ways-to-wear-different-hats-to-each-other/>

  Combine state compression with combinatorial search.

---

## Pattern Recognition Checklist

Ask yourself:

- Is brute force exploring all subsets or combinations?
- Is `2^n` too large, but `2^(n/2)` manageable?
- Is `n` around 30-40?
- Can the input be divided into two independent halves?
- Can results from both halves be combined efficiently?

If yes, Meet in the Middle is likely a strong candidate.

---

## Common Interview Keywords

Look for phrases like:

- "subset";
- "subsequence";
- "combination";
- "partition";
- "closest sum";
- "minimum difference";
- "maximum possible";
- "all possible ways".

---

## Common Meet in the Middle Variations

### Subset Sum Splitting

The most common form.

Example:

```text
Array:

[3, 8, 5, 7]

Split:

Left:

[3, 8]

Right:

[5, 7]
```

Generate all sums:

```text
Left:

0, 3, 8, 11

Right:

0, 5, 7, 12
```

Combine the two sets to find the best answer.

Typical examples:

- Closest Subsequence Sum
- Partition Array Into Two Arrays to Minimize Sum Difference

---

### Meet in the Middle + Binary Search

After generating subset sums:

1. Sort one half.
2. Search for the best matching value.

Example:

```text
Need:

left_sum + right_sum <= target
```

Find the closest:

```text
right_sum <= target - left_sum
```

Typical examples:

- Closest Subsequence Sum

---

### Meet in the Middle + Hashing

Store one half of generated states in a hash structure.

Example:

```text
unordered_map<state, count>
```

Useful when:

- exact matching is needed;
- duplicate states exist;
- counting solutions.

Typical examples:

- Split Array With Same Average

---

### Meet in the Middle + Bitmask

Represent subsets as bitmasks.

Example:

```text
00010101

Selected elements:

0, 2, 4
```

Useful when:

- `n <= 20`;
- states can be compressed.

Typical examples:

- Partition problems.

---

## Complexity

Without optimization:

```text
O(2^n)
```

With Meet in the Middle:

```text
O(2^(n/2))
```

For `n = 40`:

Brute force:

```text
2^40 ≈ 1 trillion
```

Meet in the Middle:

```text
2^20 ≈ 1 million
```

which is practical.

Typical complexity:

- Time complexity: `O(2^(n/2) log(2^(n/2)))`
- Space complexity: `O(2^(n/2))`

---

## Common Pitfalls

### Generating Too Many States

Even after splitting, storing all combinations may consume a lot of
memory.

Possible solutions:

- remove duplicates;
- sort and process incrementally;
- use pruning.

---

### Forgetting Empty Subsets

Every half must include:

```text
sum = 0
```

because selecting no elements is a valid choice.

---

### Wrong Combination Logic

The difficult part is usually not generating subsets but combining them.

Common approaches:

- binary search;
- two pointers;
- hash lookup.

---

## Learning Goals

After completing this pattern, you should be able to:

- recognize exponential search problems;
- estimate when brute force is impossible;
- split problems into independent halves;
- combine partial results efficiently;
- use binary search or hashing to merge solutions.

---

## Progress

- [ ] 1755. Closest Subsequence Sum
- [ ] 2035. Partition Array Into Two Arrays to Minimize Sum Difference
- [ ] 805. Split Array With Same Average
- [ ] 698. Partition to K Equal Sum Subsets
- [ ] 956. Tallest Billboard
- [ ] 1434. Number of Ways to Wear Different Hats to Each Other
