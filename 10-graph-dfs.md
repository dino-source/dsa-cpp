# LeetCode Pattern: Graph DFS

## Overview

The Graph DFS pattern is used to explore graphs by recursively visiting
connected nodes and tracking which nodes have already been processed.

The main idea is to start from a node, explore as far as possible, and
continue until all reachable nodes have been visited.

Graph DFS is commonly used for:

- finding connected components;
- detecting cycles;
- exploring paths;
- solving graph traversal problems;
- processing grid-based graphs.

In C++, this pattern commonly uses:

- recursion;
- `std::vector`;
- `std::unordered_set`;
- `std::unordered_map`;
- `std::stack`.

The key skill is recognizing when a problem can be represented as a graph
and solved by exploring neighboring nodes.

---

## Practice Problems

Solve these problems in order. The early problems introduce basic graph
traversal, while the later ones require cycle detection and more advanced
reasoning.

### Easy

- **733. Flood Fill**  
  <https://leetcode.com/problems/flood-fill/>

  Explore connected cells and change their values using DFS.

- **1971. Find if Path Exists in Graph**  
  <https://leetcode.com/problems/find-if-path-exists-in-graph/>

  Determine whether two nodes are connected.

### Medium

- **200. Number of Islands**  
  <https://leetcode.com/problems/number-of-islands/>

  Count connected components in a grid using DFS.

- **695. Max Area of Island**  
  <https://leetcode.com/problems/max-area-of-island/>

  Calculate the size of connected regions.

- **133. Clone Graph**  
  <https://leetcode.com/problems/clone-graph/>

  Create a copy of a graph while avoiding repeated visits.

- **207. Course Schedule**  
  <https://leetcode.com/problems/course-schedule/>

  Detect cycles in a directed graph using DFS states.

- **210. Course Schedule II**  
  <https://leetcode.com/problems/course-schedule-ii/>

  Use DFS to produce a valid ordering of courses.

### Hard

- **329. Longest Increasing Path in a Matrix**  
  <https://leetcode.com/problems/longest-increasing-path-in-a-matrix/>

  Combine DFS with memoization to avoid repeated exploration.

- **332. Reconstruct Itinerary**  
  <https://leetcode.com/problems/reconstruct-itinerary/>

  Use graph traversal to build a valid path.

---

## Pattern Recognition Checklist

Ask yourself:

- Is the input a graph, grid, or network of connected objects?
- Do I need to visit all reachable nodes?
- Do I need to find connected components?
- Do I need to detect cycles?
- Can I mark nodes as visited to avoid repeated work?

If yes, Graph DFS is likely a strong candidate.

---

## Common Interview Keywords

Look for phrases like:

- "graph";
- "connected";
- "reachable";
- "path";
- "cycle";
- "component";
- "network";
- "dependency";
- "neighbors";
- "visit all nodes".

---

## Common Graph DFS Variations

### Undirected Graph DFS

Nodes are connected in both directions.

Example:

```text
A --- B --- C

Start:
A

Visit:
A -> B -> C
```

Typical examples:

- Number of Islands
- Clone Graph
- Find if Path Exists in Graph

---

### Directed Graph DFS

Edges have a direction.

Example:

```text
A -> B -> C
```

DFS is commonly used to detect cycles by tracking node states:

```text
0 = unvisited
1 = visiting
2 = completed
```

Typical examples:

- Course Schedule
- Course Schedule II

---

### DFS + Memoization

Store results for already processed nodes.

Typical examples:

- Longest Increasing Path in a Matrix

This avoids repeating expensive calculations.

---

## Complexity

Most Graph DFS solutions have:

- Time complexity: `O(V + E)`

where:

- `V` is the number of vertices;
- `E` is the number of edges.

Space complexity:

- `O(V)`

because of:

- visited tracking;
- recursion stack;
- auxiliary data structures.

---

## Learning Goals

After completing this pattern, you should be able to:

- represent problems as graphs;
- implement DFS traversal correctly;
- track visited nodes;
- detect cycles in directed graphs;
- solve connected component problems;
- combine DFS with memoization.

---

## Progress

- [ ] 733. Flood Fill
- [ ] 1971. Find if Path Exists in Graph
- [ ] 200. Number of Islands
- [ ] 695. Max Area of Island
- [ ] 133. Clone Graph
- [ ] 207. Course Schedule
- [ ] 210. Course Schedule II
- [ ] 329. Longest Increasing Path in a Matrix
- [ ] 332. Reconstruct Itinerary
