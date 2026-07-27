# LeetCode Pattern: Union Find (Disjoint Set Union)

## Overview

The Union Find, also known as the Disjoint Set Union (DSU), pattern is
used to efficiently manage groups of connected elements.

The main idea is to keep track of which elements belong to the same set
while supporting two fast operations:

- **Find**: determine which set an element belongs to.
- **Union**: merge two sets into one.

Instead of traversing an entire graph to determine connectivity, Union
Find maintains a forest of trees that can be updated efficiently.

This pattern is especially useful for:

- connected components;
- connectivity queries;
- cycle detection;
- graph construction;
- minimum spanning tree algorithms.

In C++, this pattern commonly uses:

- `std::vector`;
- path compression;
- union by rank or union by size.

The key skill is recognizing when the problem repeatedly asks whether two
elements belong to the same connected component.

---

## Practice Problems

Solve these problems in order. The early problems introduce the basic DSU
operations, while the later ones require more advanced applications.

### Easy

- **1971. Find if Path Exists in Graph**  
  <https://leetcode.com/problems/find-if-path-exists-in-graph/>

  Determine whether two nodes belong to the same connected component.

### Medium

- **547. Number of Provinces**  
  <https://leetcode.com/problems/number-of-provinces/>

  Count connected components using Union Find.

- **684. Redundant Connection**  
  <https://leetcode.com/problems/redundant-connection/>

  Detect the edge that creates a cycle.

- **1319. Number of Operations to Make Network Connected**  
  <https://leetcode.com/problems/number-of-operations-to-make-network-connected/>

  Merge connected components until the entire network becomes connected.

- **721. Accounts Merge**  
  <https://leetcode.com/problems/accounts-merge/>

  Merge related accounts that share common email addresses.

- **990. Satisfiability of Equality Equations**  
  <https://leetcode.com/problems/satisfiability-of-equality-equations/>

  Group equal variables and verify inequality constraints.

### Hard

- **305. Number of Islands II**  
  <https://leetcode.com/problems/number-of-islands-ii/>

  Dynamically maintain connected components as new land appears.

- **827. Making A Large Island**  
  <https://leetcode.com/problems/making-a-large-island/>

  Merge neighboring components to maximize island size.

---

## Pattern Recognition Checklist

Ask yourself:

- Do I need to determine whether two elements are connected?
- Am I repeatedly merging groups?
- Do connected components change over time?
- Do I need fast connectivity queries?
- Can each element belong to exactly one set?

If yes, Union Find is likely a strong candidate.

---

## Common Interview Keywords

Look for phrases like:

- "connected";
- "component";
- "merge";
- "union";
- "disjoint";
- "network";
- "cycle";
- "province";
- "group";
- "connectivity".

---

## Common Union Find Variations

### Basic Union Find

Maintain disjoint sets using parent pointers.

Example:

```text
Initially:

1   2   3   4

Union(1, 2)

1
|
2

3

4

Union(2, 3)

1
|
2
|
3

4
```

Typical examples:

- Number of Provinces
- Find if Path Exists in Graph

---

### Path Compression

Flatten the tree whenever `find()` is called.

Example:

```text
Before:

1
|
2
|
3
|
4

find(4)

After:

1
|\
2 3
 \
  4
```

Path compression makes future `find()` operations much faster.

---

### Union by Rank / Union by Size

Always attach the smaller tree under the larger one.

Example:

```text
Small tree

  A

Large tree

    B
   / \
  C   D

After union:

    B
   /|\
  C D A
```

This keeps trees shallow and improves performance.

---

## Complexity

With path compression and union by rank:

- Find: nearly `O(1)`
- Union: nearly `O(1)`

More precisely:

- Time complexity: `O(α(n))`

where `α(n)` is the inverse Ackermann function, which grows so slowly that
it is effectively constant for all practical input sizes.

Space complexity:

- `O(n)`

to store the parent and rank (or size) arrays.

---

## Learning Goals

After completing this pattern, you should be able to:

- implement Union Find from scratch;
- apply path compression correctly;
- implement union by rank or union by size;
- recognize connectivity problems;
- solve graph problems involving dynamic components.

---

## Progress

- [ ] 1971. Find if Path Exists in Graph
- [ ] 547. Number of Provinces
- [ ] 684. Redundant Connection
- [ ] 1319. Number of Operations to Make Network Connected
- [ ] 721. Accounts Merge
- [ ] 990. Satisfiability of Equality Equations
- [ ] 305. Number of Islands II
- [ ] 827. Making A Large Island
