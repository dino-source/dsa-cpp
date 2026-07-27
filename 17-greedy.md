# LeetCode Pattern: Greedy

## Overview

The Greedy pattern is used to solve optimization problems by making the
best local decision at each step.

The main idea is that a sequence of locally optimal choices leads to a
globally optimal solution.

Unlike Dynamic Programming, Greedy algorithms do not reconsider previous
decisions.

Instead of exploring multiple possibilities:

```text
Dynamic Programming:
Evaluate many possible states.

Greedy:
Always choose the best available option.
```

Greedy algorithms are commonly used for:

- interval scheduling;
- resource allocation;
- minimizing or maximizing values;
- sorting-based optimization;
- making locally optimal decisions.

In C++, this pattern commonly uses:

- sorting (`std::sort`);
- `std::priority_queue`;
- `std::vector`.

The key skill is recognizing when making the best immediate choice cannot
prevent reaching the optimal overall solution.

---

## Practice Problems

Solve these problems in order. The early problems introduce simple greedy
choices, while the later ones require proving that the greedy strategy is
correct.

### Easy

- **455. Assign Cookies**  
  <https://leetcode.com/problems/assign-cookies/>

  Match the smallest suitable cookie to each child.

- **605. Can Place Flowers**  
  <https://leetcode.com/problems/can-place-flowers/>

  Make the earliest valid planting decision at each position.

### Medium

- **55. Jump Game**  
  <https://leetcode.com/problems/jump-game/>

  Track the farthest position that can currently be reached.

- **45. Jump Game II**  
  <https://leetcode.com/problems/jump-game-ii/>

  Greedily choose jumps that maximize future reach.

- **134. Gas Station**  
  <https://leetcode.com/problems/gas-station/>

  Find the unique starting position using greedy reasoning.

- **435. Non-overlapping Intervals**  
  <https://leetcode.com/problems/non-overlapping-intervals/>

  Remove the minimum number of overlapping intervals.

- **763. Partition Labels**  
  <https://leetcode.com/problems/partition-labels/>

  Build the largest possible partitions without overlapping characters.

### Hard

- **135. Candy**  
  <https://leetcode.com/problems/candy/>

  Satisfy local constraints while minimizing the total number of candies.

- **871. Minimum Number of Refueling Stops**  
  <https://leetcode.com/problems/minimum-number-of-refueling-stops/>

  Combine greedy decisions with a priority queue.

---

## Pattern Recognition Checklist

Ask yourself:

- Am I trying to maximize or minimize something?
- Can I always make the best local decision?
- Is there no benefit to revisiting previous choices?
- Can sorting simplify the problem?
- Can I prove that a locally optimal choice leads to a globally optimal
  solution?

If yes, Greedy is likely a strong candidate.

---

## Common Interview Keywords

Look for phrases like:

- "minimum number";
- "maximum number";
- "earliest";
- "latest";
- "largest possible";
- "smallest possible";
- "choose";
- "schedule";
- "interval";
- "optimize".

---

## Common Greedy Variations

### Sort Then Process

Sort the input first, then make greedy decisions.

Example:

```text
Sort intervals by end time.

Process them from left to right.

Always keep the interval that finishes first.
```

Typical examples:

- Assign Cookies
- Non-overlapping Intervals

---

### Reachability Greedy

Maintain the best position that can currently be reached.

Example:

```text
Current index:

i

Reach:

max(reach, i + nums[i])
```

Typical examples:

- Jump Game
- Jump Game II

---

### Greedy + Heap

Always choose the best available option using a priority queue.

Example:

```text
Reach all available choices.

Select the best one.

Continue.
```

Typical examples:

- Minimum Number of Refueling Stops

---

## Complexity

Greedy algorithms often require sorting.

Typical complexities:

- Time complexity: `O(n log n)`
- Space complexity: `O(1)` or `O(n)`

Problems that only scan the input once often have:

- Time complexity: `O(n)`

---

## Learning Goals

After completing this pattern, you should be able to:

- recognize greedy optimization problems;
- identify when sorting enables a greedy solution;
- distinguish Greedy from Dynamic Programming;
- justify why a greedy strategy is correct;
- combine greedy algorithms with heaps when necessary.

---

## Progress

- [ ] 455. Assign Cookies
- [ ] 605. Can Place Flowers
- [ ] 55. Jump Game
- [ ] 45. Jump Game II
- [ ] 134. Gas Station
- [ ] 435. Non-overlapping Intervals
- [ ] 763. Partition Labels
- [ ] 135. Candy
- [ ] 871. Minimum Number of Refueling Stops
