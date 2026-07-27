# LeetCode Pattern: Shortest Path

## Overview

The Shortest Path pattern is used to find the minimum cost, distance, or
number of steps needed to travel from one node to another.

Unlike BFS, which only works for unweighted graphs (or graphs where every
edge has the same cost), shortest path algorithms handle weighted graphs.

The most common algorithms are:

- Breadth-First Search (BFS) for unweighted graphs;
- Dijkstra's Algorithm for non-negative edge weights;
- Bellman-Ford for graphs with negative edge weights;
- Floyd-Warshall for all-pairs shortest paths.

In coding interviews, **Dijkstra's Algorithm** is by far the most common.

This pattern is especially useful for:

- weighted graphs;
- minimum travel cost;
- minimum travel time;
- routing problems;
- path planning.

In C++, this pattern commonly uses:

- `std::priority_queue`;
- `std::vector`;
- adjacency lists;
- distance arrays.

The key skill is recognizing whether the graph is weighted and choosing
the appropriate shortest path algorithm.

---

## Practice Problems

Solve these problems in order. The early problems introduce Dijkstra's
Algorithm, while the later ones require more advanced graph techniques.

### Medium

- **743. Network Delay Time**  
  <https://leetcode.com/problems/network-delay-time/>

  Use Dijkstra's Algorithm to determine how long a signal takes to reach
  every node.

- **1514. Path with Maximum Probability**  
  <https://leetcode.com/problems/path-with-maximum-probability/>

  Modify Dijkstra's Algorithm to maximize probabilities instead of
  minimizing distances.

- **1631. Path With Minimum Effort**  
  <https://leetcode.com/problems/path-with-minimum-effort/>

  Minimize the maximum edge weight along a path.

- **787. Cheapest Flights Within K Stops**  
  <https://leetcode.com/problems/cheapest-flights-within-k-stops/>

  Combine shortest path techniques with an additional stop constraint.

- **1976. Number of Ways to Arrive at Destination**  
  <https://leetcode.com/problems/number-of-ways-to-arrive-at-destination/>

  Count the number of shortest paths while computing distances.

### Hard

- **778. Swim in Rising Water**  
  <https://leetcode.com/problems/swim-in-rising-water/>

  Use Dijkstra's Algorithm where the path cost is the maximum elevation.

- **882. Reachable Nodes In Subdivided Graph**  
  <https://leetcode.com/problems/reachable-nodes-in-subdivided-graph/>

  Compute shortest paths while accounting for subdivided edges.

- **1928. Minimum Cost to Reach Destination in Time**  
  <https://leetcode.com/problems/minimum-cost-to-reach-destination-in-time/>

  Optimize two constraints simultaneously: travel cost and travel time.

---

## Pattern Recognition Checklist

Ask yourself:

- Is the graph weighted?
- Am I looking for the minimum cost or distance?
- Are all edge weights non-negative?
- Can the problem be represented as nodes connected by weighted edges?
- Do I need the shortest path from one source?

If yes, a Shortest Path algorithm is likely a strong candidate.

---

## Common Interview Keywords

Look for phrases like:

- "minimum distance";
- "minimum cost";
- "minimum time";
- "shortest path";
- "weighted graph";
- "travel";
- "route";
- "network";
- "road";
- "flight".

---

## Common Shortest Path Variations

### BFS (Unweighted Graph)

If every edge has the same cost, BFS naturally finds the shortest path.

Example:

```text
Distance:

A -> B -> C

Every edge costs 1.
```

Typical examples:

- Word Ladder
- Shortest Path in Binary Matrix

---

### Dijkstra's Algorithm

Always process the unvisited node with the smallest known distance.

Algorithm:

```text
1. Set all distances to infinity.
2. Set the source distance to 0.
3. Push the source into a min-heap.
4. Pop the closest node.
5. Relax all outgoing edges.
6. Repeat until the heap is empty.
```

Typical examples:

- Network Delay Time
- Path With Minimum Effort
- Cheapest Flights Within K Stops

---

### Bellman-Ford

Relax every edge repeatedly.

Unlike Dijkstra's Algorithm, Bellman-Ford supports negative edge weights.

Typical examples:

- Problems involving negative costs
- Detecting negative cycles

Bellman-Ford is much less common in coding interviews.

---

### Floyd-Warshall

Compute the shortest distance between every pair of nodes.

Typical examples:

- All-pairs shortest path problems

This algorithm is uncommon in interviews because of its `O(n³)` time
complexity.

---

## Complexity

### BFS Complexity

- Time complexity: `O(V + E)`
- Space complexity: `O(V)`

### Dijkstra's Algorithm Complexity

Using a binary heap:

- Time complexity: `O((V + E) log V)`
- Space complexity: `O(V + E)`

### Bellman-Ford Complexity

- Time complexity: `O(V × E)`
- Space complexity: `O(V)`

### Floyd-Warshall Complexity

- Time complexity: `O(V³)`
- Space complexity: `O(V²)`

---

## Learning Goals

After completing this pattern, you should be able to:

- distinguish between weighted and unweighted graphs;
- choose the correct shortest path algorithm;
- implement Dijkstra's Algorithm using a priority queue;
- understand edge relaxation;
- recognize when Bellman-Ford or Floyd-Warshall is required.

---

## Progress

- [ ] 743. Network Delay Time
- [ ] 1514. Path with Maximum Probability
- [ ] 1631. Path With Minimum Effort
- [ ] 787. Cheapest Flights Within K Stops
- [ ] 1976. Number of Ways to Arrive at Destination
- [ ] 778. Swim in Rising Water
- [ ] 882. Reachable Nodes In Subdivided Graph
- [ ] 1928. Minimum Cost to Reach Destination in Time
