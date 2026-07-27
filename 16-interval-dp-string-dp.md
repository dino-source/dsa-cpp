# LeetCode Pattern: Interval DP / String DP

## Overview

Interval DP and advanced String DP are specialized forms of Dynamic
Programming where the state is defined over a range or a pair of string
indices.

Although both belong to the broader Dynamic Programming family, they are
worth studying separately because their state transitions differ
significantly from standard 2D DP.

### Interval DP

Interval DP solves problems involving contiguous ranges.

Instead of asking, "What is the answer up to index `i`?", Interval DP asks:

```text
What is the best answer for the interval [left, right]?
```

Typical applications include:

- merging intervals;
- removing elements;
- optimal game strategies;
- palindrome problems.

### String DP

Advanced String DP compares prefixes or suffixes of strings and often
requires more sophisticated state transitions than basic sequence DP.

Typical applications include:

- palindrome detection;
- string transformations;
- regular expression matching;
- subsequences.

In C++, this pattern commonly uses:

- `std::vector<std::vector<int>>`;
- recursion with memoization;
- bottom-up DP tables.

The key skill is recognizing when a solution depends on a substring or an
interval rather than a single position.

---

## Practice Problems

Solve these problems in order. The early problems introduce palindrome
DP, while the later ones require interval optimization.

### Medium

- **5. Longest Palindromic Substring**  
  <https://leetcode.com/problems/longest-palindromic-substring/>

  Determine whether every substring is a palindrome.

- **516. Longest Palindromic Subsequence**  
  <https://leetcode.com/problems/longest-palindromic-subsequence/>

  Build solutions for larger substrings from smaller ones.

- **647. Palindromic Substrings**  
  <https://leetcode.com/problems/palindromic-substrings/>

  Count all palindromic substrings using DP.

- **131. Palindrome Partitioning**  
  <https://leetcode.com/problems/palindrome-partitioning/>

  Combine backtracking with palindrome DP.

- **132. Palindrome Partitioning II**  
  <https://leetcode.com/problems/palindrome-partitioning-ii/>

  Minimize the number of cuts using precomputed palindrome states.

### Hard

- **312. Burst Balloons**  
  <https://leetcode.com/problems/burst-balloons/>

  Solve an interval DP problem by choosing the last balloon to burst.

- **664. Strange Printer**  
  <https://leetcode.com/problems/strange-printer/>

  Optimize printing operations over string intervals.

- **730. Count Different Palindromic Subsequences**  
  <https://leetcode.com/problems/count-different-palindromic-subsequences/>

  Combine interval DP with careful state transitions.

- **87. Scramble String**  
  <https://leetcode.com/problems/scramble-string/>

  Compare recursively partitioned substrings using DP.

---

## Pattern Recognition Checklist

Ask yourself:

- Does the state naturally represent a substring?
- Does the answer depend on an interval `[left, right]`?
- Am I repeatedly solving the same substring problem?
- Can larger intervals be built from smaller intervals?
- Do I need to compare two substrings?

If yes, Interval DP or advanced String DP is likely a strong candidate.

---

## Common Interview Keywords

Look for phrases like:

- "substring";
- "subsequence";
- "palindrome";
- "partition";
- "interval";
- "split";
- "merge";
- "range";
- "transform".

---

## Common Interval DP Variations

### Palindrome DP

Each state represents a substring.

Example:

```text
dp[left][right]

true if s[left...right] is a palindrome
```

Typical examples:

- Longest Palindromic Substring
- Palindromic Substrings

---

### Interval Optimization

Choose the best splitting point inside an interval.

Example:

```text
dp[left][right]

Try every possible split:

[left ... k]

[k + 1 ... right]
```

Typical examples:

- Burst Balloons
- Strange Printer

---

### String Partition DP

Split a string into optimal pieces.

Example:

```text
dp[i]

Minimum cuts for:

s[0...i]
```

Often combined with a palindrome table.

Typical examples:

- Palindrome Partitioning II

---

## Complexity

Most Interval DP problems have:

- Time complexity: `O(n³)`

because every interval may consider every possible split.

Simple palindrome DP often has:

- Time complexity: `O(n²)`
- Space complexity: `O(n²)`

Space complexity is usually:

- `O(n²)`

for storing interval states.

---

## Learning Goals

After completing this pattern, you should be able to:

- recognize interval-based DP problems;
- define states using substring boundaries;
- build larger intervals from smaller ones;
- optimize palindrome-related problems;
- distinguish interval DP from standard 2D DP.

---

## Progress

- [ ] 5. Longest Palindromic Substring
- [ ] 516. Longest Palindromic Subsequence
- [ ] 647. Palindromic Substrings
- [ ] 131. Palindrome Partitioning
- [ ] 132. Palindrome Partitioning II
- [ ] 312. Burst Balloons
- [ ] 664. Strange Printer
- [ ] 730. Count Different Palindromic Subsequences
- [ ] 87. Scramble String
