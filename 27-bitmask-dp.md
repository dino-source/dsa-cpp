# LeetCode Pattern: Bitmask Dynamic Programming

## Overview

Bitmask Dynamic Programming is an advanced Dynamic Programming technique
that combines DP with bit manipulation.

The main idea is to use a bitmask to represent a state.

Each bit represents whether an element has been selected, visited, or
completed.

Example:

```text
Elements:

A B C D

Bitmask:

0101

Means:

A and C are selected.
```

Instead of storing a large state object:

```text
visited = {A, C}
```

we encode the same information as an integer:

```cpp
mask = 0101
```

This allows efficient state transitions.

Bitmask DP is especially useful for:

- subsets;
- permutations;
- assigning resources;
- visiting all nodes;
- scheduling problems;
- problems with small `n`.

Typical constraints:

```text
n <= 20
```

because the number of states is:

```text
2^n
```

In C++, this pattern commonly uses:

- bit operators;
- `std::vector`;
- memoization;
- recursion;
- iterative DP tables.

The key skill is recognizing when the complete state of a problem can be
represented by a set of selected items.

---

## Practice Problems

Solve these problems in order. The early problems introduce basic state
compression, while the later ones require more advanced transitions.

### Medium

- **698. Partition to K Equal Sum Subsets**  
  <https://leetcode.com/problems/partition-to-k-equal-sum-subsets/>

  Use bitmasks to track which elements have already been assigned.

- **464. Can I Win**  
  <https://leetcode.com/problems/can-i-win/>

  Represent used numbers as a bitmask and memoize game states.

- **526. Beautiful Arrangement**  
  <https://leetcode.com/problems/beautiful-arrangement/>

  Count valid permutations using visited-state DP.

### Hard

- **847. Shortest Path Visiting All Nodes**  
  <https://leetcode.com/problems/shortest-path-visiting-all-nodes/>

  Combine BFS with bitmask states to track visited nodes.

- **943. Find the Shortest Superstring**  
  <https://leetcode.com/problems/find-the-shortest-superstring/>

  Use DP over subsets and last chosen string.

- **1125. Smallest Sufficient Team**  
  <https://leetcode.com/problems/smallest-sufficient-team/>

  Represent required skills as bitmasks and optimize team selection.

- **1349. Maximum Students Taking Exam**  
  <https://leetcode.com/problems/maximum-students-taking-exam/>

  Use row-by-row bitmask DP to maximize valid placements.

- **1595. Minimum Cost to Connect Two Groups of Points**  
  <https://leetcode.com/problems/minimum-cost-to-connect-two-groups-of-points/>

  Apply subset DP to track connected points.

---

## Pattern Recognition Checklist

Ask yourself:

- Is `n` small enough that `2^n` states are possible?
- Does the problem involve choosing subsets?
- Do I need to remember which elements were already used?
- Can a set of objects be represented by bits?
- Are recursive states repeating?

If yes, Bitmask DP is likely a strong candidate.

---

## Common Interview Keywords

Look for phrases like:

- "subset";
- "choose";
- "assign";
- "visit all";
- "minimum team";
- "maximum arrangement";
- "remaining";
- "used elements";
- "state compression".

---

## Common Bitmask DP Variations

### Subset State DP

The simplest form.

State:

```text
dp[mask]
```

where:

```text
mask = current selected elements
```

Example:

```text
mask = 1010

Elements 1 and 3 are selected.
```

Typical examples:

- Can I Win
- Smallest Sufficient Team

---

### Subset + Position DP

Track both:

- selected elements;
- current position.

State:

```text
dp[mask][position]
```

Example:

```text
Which items are used?

Who is being assigned next?
```

Typical examples:

- Beautiful Arrangement
- Find the Shortest Superstring

---

### Traveling Salesman Style DP

Classic formulation:

```text
dp[mask][node]
```

Meaning:

```text
Minimum cost to visit nodes in mask
and finish at node.
```

Typical examples:

- Shortest Path Visiting All Nodes
- Shortest Superstring

---

### Bitmask as a Set

Common operations:

Check if bit is set:

```cpp
(mask & (1 << i))
```

Add an element:

```cpp
mask |= (1 << i)
```

Remove an element:

```cpp
mask &= ~(1 << i)
```

Toggle an element:

```cpp
mask ^= (1 << i)
```

---

## Complexity

The number of possible masks is:

```text
2^n
```

For each state, we may try all elements:

```text
O(n * 2^n)
```

Typical complexity:

- Time complexity: `O(n * 2^n)`
- Space complexity: `O(2^n)`

For:

```text
n = 20
```

we have:

```text
2^20 ≈ 1 million states
```

which is practical.

---

## Common Pitfalls

### Using Bitmask DP for Too Large n

The number of states grows exponentially.

Usually:

```text
n <= 20
```

is required.

---

### Incorrect State Definition

The most important part is deciding what the mask represents.

Examples:

Good:

```text
mask = already visited nodes
```

Bad:

```text
mask = random collection of information
```

The state must contain exactly the information needed for future decisions.

---

### Forgetting Memoization

Many Bitmask DP solutions are exponential without caching.

Example:

```cpp
unordered_map<int, int> memo;
```

or:

```cpp
vector<int> dp(1 << n);
```

---

## Learning Goals

After completing this pattern, you should be able to:

- represent sets using bitmasks;
- design DP states with subsets;
- optimize exponential search;
- combine recursion with memoization;
- recognize when `2^n` solutions are acceptable.

---

## Progress

- [ ] 698. Partition to K Equal Sum Subsets
- [ ] 464. Can I Win
- [ ] 526. Beautiful Arrangement
- [ ] 847. Shortest Path Visiting All Nodes
- [ ] 943. Find the Shortest Superstring
- [ ] 1125. Smallest Sufficient Team
- [ ] 1349. Maximum Students Taking Exam
- [ ] 1595. Minimum Cost to Connect Two Groups of Points
