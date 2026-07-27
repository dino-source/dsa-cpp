# LeetCode Pattern: Breadth-First Search (BFS)

## Overview

The Breadth-First Search (BFS) pattern is used to explore data structures
level by level.

The main idea is to process all nodes at the current distance before
moving to nodes that are farther away.

BFS is especially useful for:

- finding the shortest path in an unweighted graph;
- level-order tree traversal;
- exploring layers of a graph;
- finding minimum number of steps.

Unlike DFS, which goes deep first, BFS expands outward from the starting
point.

In C++, this pattern commonly uses:

- `std::queue`;
- `std::vector`;
- `std::unordered_set`;
- `std::unordered_map`.

The key skill is recognizing when the distance from a starting point or
the order of exploration matters.

---

## Practice Problems

Solve these problems in order. The early problems introduce basic BFS
traversal, while the later ones require shortest path reasoning.

### Easy

- **102. Binary Tree Level Order Traversal**  
  <https://leetcode.com/problems/binary-tree-level-order-traversal/>

  Traverse a binary tree level by level using a queue.

- **111. Minimum Depth of Binary Tree**  
  <https://leetcode.com/problems/minimum-depth-of-binary-tree/>

  Use BFS to find the first level containing a leaf node.

- **637. Average of Levels in Binary Tree**  
  <https://leetcode.com/problems/average-of-levels-in-binary-tree/>

  Process each tree level separately and calculate averages.

### Medium

- **994. Rotting Oranges**  
  <https://leetcode.com/problems/rotting-oranges/>

  Use multi-source BFS to simulate the spread over time.

- **127. Word Ladder**  
  <https://leetcode.com/problems/word-ladder/>

  Find the shortest transformation sequence using BFS.

- **1091. Shortest Path in Binary Matrix**  
  <https://leetcode.com/problems/shortest-path-in-binary-matrix/>

  Find the shortest path through a grid using BFS.

- **130. Surrounded Regions**  
  <https://leetcode.com/problems/surrounded-regions/>

  Use BFS to identify connected regions that should not be changed.

### Hard

- **126. Word Ladder II**  
  <https://leetcode.com/problems/word-ladder-ii/>

  Combine BFS with path reconstruction to find all shortest sequences.

- **847. Shortest Path Visiting All Nodes**  
  <https://leetcode.com/problems/shortest-path-visiting-all-nodes/>

  Use BFS with state tracking to solve a complex shortest path problem.

---

## Pattern Recognition Checklist

Ask yourself:

- Do I need the shortest path in an unweighted graph?
- Does the problem ask for minimum number of steps?
- Do I need to process nodes by distance or level?
- Can multiple starting points spread simultaneously?
- Does every move have the same cost?

If yes, BFS is likely a strong candidate.

---

## Common Interview Keywords

Look for phrases like:

- "shortest path";
- "minimum steps";
- "nearest";
- "level order";
- "distance";
- "number of moves";
- "transform";
- "spread";
- "minimum time".

---

## Common BFS Variations

### Standard BFS

Start from one node and explore neighbors level by level.

Example:

```text
Start:

        A

Level 0:
        A

Level 1:
      B   C

Level 2:
    D E   F
```

Typical examples:

- Binary Tree Level Order Traversal
- Shortest Path in Binary Matrix

---

### Multi-Source BFS

Start BFS from multiple nodes at the same time.

Example:

```text
Initial sources:

A       B

Expand together:

A -> X <- B
```

Typical examples:

- Rotting Oranges
- Walls and Gates

---

### BFS With State

Track additional information together with each node.

Example:

```text
(queue item)

(node, distance, state)
```

Typical examples:

- Word Ladder
- Shortest Path Visiting All Nodes

---

## Complexity

Most BFS solutions have:

- Time complexity: `O(V + E)`

where:

- `V` is the number of vertices;
- `E` is the number of edges.

Space complexity:

- `O(V)`

because the queue and visited structure may contain many nodes.

For grid problems:

- Time complexity: `O(rows * columns)`
- Space complexity: `O(rows * columns)`

---

## Learning Goals

After completing this pattern, you should be able to:

- recognize shortest path problems;
- implement queue-based traversal;
- understand level-by-level exploration;
- apply multi-source BFS;
- track additional state during traversal.

---

## Progress

- [ ] 102. Binary Tree Level Order Traversal
- [ ] 111. Minimum Depth of Binary Tree
- [ ] 637. Average of Levels in Binary Tree
- [ ] 994. Rotting Oranges
- [ ] 127. Word Ladder
- [ ] 1091. Shortest Path in Binary Matrix
- [ ] 130. Surrounded Regions
- [ ] 126. Word Ladder II
- [ ] 847. Shortest Path Visiting All Nodes
