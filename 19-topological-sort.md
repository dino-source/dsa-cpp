# LeetCode Pattern: Topological Sort

## Overview

The Topological Sort pattern is used to determine a valid ordering of
tasks that have dependency relationships.

The main idea is that a node can only be processed after all of its
prerequisites have been completed.

Topological Sort applies only to **Directed Acyclic Graphs (DAGs)**.

This pattern is especially useful for:

- scheduling tasks;
- resolving dependencies;
- determining build order;
- detecting cycles in directed graphs;
- processing prerequisite relationships.

There are two common algorithms:

- Kahn's Algorithm (BFS);
- DFS-based Topological Sort.

In C++, this pattern commonly uses:

- `std::vector`;
- `std::queue`;
- recursion;
- adjacency lists;
- indegree arrays.

The key skill is recognizing when the problem asks for a valid ordering
that satisfies dependency constraints.

---

## Practice Problems

Solve these problems in order. The early problems introduce dependency
graphs, while the later ones require more advanced graph reasoning.

### Medium

- **207. Course Schedule**  
  <https://leetcode.com/problems/course-schedule/>

  Detect whether all courses can be completed.

- **210. Course Schedule II**  
  <https://leetcode.com/problems/course-schedule-ii/>

  Produce one valid ordering of all courses.

- **1462. Course Schedule IV**  
  <https://leetcode.com/problems/course-schedule-iv/>

  Answer prerequisite queries efficiently.

- **2115. Find All Possible Recipes from Given Supplies**  
  <https://leetcode.com/problems/find-all-possible-recipes-from-given-supplies/>

  Build recipes by satisfying ingredient dependencies.

- **1203. Sort Items by Groups Respecting Dependencies**  
  <https://leetcode.com/problems/sort-items-by-groups-respecting-dependencies/>

  Perform topological sorting on both groups and items.

### Hard

- **269. Alien Dictionary**  
  <https://leetcode.com/problems/alien-dictionary/>

  Infer the order of characters from a sorted dictionary.

- **2392. Build a Matrix With Conditions**  
  <https://leetcode.com/problems/build-a-matrix-with-conditions/>

  Use two independent topological sorts to satisfy row and column
  constraints.

---

## Pattern Recognition Checklist

Ask yourself:

- Do some tasks depend on others?
- Does the problem ask for a valid ordering?
- Are prerequisites explicitly given?
- Can the problem be modeled as a directed graph?
- Do I need to detect a cycle?

If yes, Topological Sort is likely a strong candidate.

---

## Common Interview Keywords

Look for phrases like:

- "prerequisite";
- "dependency";
- "before";
- "after";
- "order";
- "schedule";
- "build";
- "compile";
- "workflow";
- "directed graph".

---

## Common Topological Sort Variations

### Kahn's Algorithm (BFS)

Repeatedly process nodes with zero incoming edges.

Algorithm:

```text
1. Compute indegree for every node.
2. Push all nodes with indegree 0 into a queue.
3. Remove a node from the queue.
4. Reduce the indegree of its neighbors.
5. Push newly unlocked nodes into the queue.
6. Repeat until the queue becomes empty.
```

Typical examples:

- Course Schedule
- Course Schedule II
- Find All Possible Recipes from Given Supplies

---

### DFS-Based Topological Sort

Visit every node using DFS.

After exploring all neighbors, place the current node into the result.

Example:

```text
DFS(node)

Visit neighbors

Append node

Reverse the final order
```

Typical examples:

- Alien Dictionary
- Course Schedule

---

### Cycle Detection

A valid topological ordering exists **only if the graph has no cycles**.

During DFS, each node has one of three states:

```text
0 = unvisited

1 = visiting

2 = visited
```

Encountering a node in the **visiting** state means a cycle exists.

Typical examples:

- Course Schedule
- Alien Dictionary

---

## Complexity

Both Kahn's Algorithm and DFS-based Topological Sort have:

- Time complexity: `O(V + E)`

where:

- `V` is the number of vertices;
- `E` is the number of edges.

Space complexity:

- `O(V + E)`

for the adjacency list, queue (or recursion stack), and auxiliary data
structures.

---

## Learning Goals

After completing this pattern, you should be able to:

- recognize dependency graph problems;
- implement Kahn's Algorithm;
- implement DFS-based Topological Sort;
- detect cycles in directed graphs;
- explain why topological sorting only works on DAGs.

---

## Progress

- [ ] 207. Course Schedule
- [ ] 210. Course Schedule II
- [ ] 1462. Course Schedule IV
- [ ] 2115. Find All Possible Recipes from Given Supplies
- [ ] 1203. Sort Items by Groups Respecting Dependencies
- [ ] 269. Alien Dictionary
- [ ] 2392. Build a Matrix With Conditions
