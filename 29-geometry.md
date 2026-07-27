# LeetCode Pattern: Geometry / Computational Geometry

## Overview

The Geometry pattern focuses on solving problems involving points, lines,
distances, angles, and spatial relationships.

Unlike many algorithmic patterns, geometry problems often require strong
mathematical reasoning rather than complex data structures.

The main idea is to transform geometric concepts into mathematical
operations.

Common techniques include:

- coordinate manipulation;
- distance calculations;
- vector operations;
- line equations;
- cross products;
- orientation tests;
- sorting points.

Geometry is especially useful for:

- points on a plane;
- detecting intersections;
- finding maximum collinear points;
- constructing convex hulls;
- calculating areas.

In C++, this pattern commonly uses:

- `std::vector`;
- `std::pair`;
- sorting algorithms;
- custom comparison functions;
- floating-point arithmetic.

The key skill is recognizing when a problem is fundamentally about spatial
relationships rather than graph traversal or dynamic programming.

---

## Practice Problems

Solve these problems in order. The early problems introduce coordinate
operations, while the later ones require more advanced geometry concepts.

### Easy

- **1979. Find Greatest Common Divisor of Array**  
  <https://leetcode.com/problems/find-greatest-common-divisor-of-array/>

  Practice mathematical thinking and coordinate-independent reasoning.

- **1232. Check If It Is a Straight Line**  
  <https://leetcode.com/problems/check-if-it-is-a-straight-line/>

  Determine whether points lie on the same line.

### Medium

- **149. Max Points on a Line**  
  <https://leetcode.com/problems/max-points-on-a-line/>

  Group points by slope to find the maximum number of collinear points.

- **973. K Closest Points to Origin**  
  <https://leetcode.com/problems/k-closest-points-to-origin/>

  Use distance calculations with sorting or a heap.

- **587. Erect the Fence**  
  <https://leetcode.com/problems/erect-the-fence/>

  Construct the convex hull of a set of points.

- **1401. Circle and Rectangle Overlapping**  
  <https://leetcode.com/problems/circle-and-rectangle-overlapping/>

  Apply geometric distance reasoning.

### Hard

- **218. The Skyline Problem**  
  <https://leetcode.com/problems/the-skyline-problem/>

  Combine geometry with sweep line techniques.

- **391. Perfect Rectangle**  
  <https://leetcode.com/problems/perfect-rectangle/>

  Verify whether rectangles form one perfect rectangle.

- **850. Rectangle Area II**  
  <https://leetcode.com/problems/rectangle-area-ii/>

  Combine geometry with coordinate compression and sweep line.

---

## Pattern Recognition Checklist

Ask yourself:

- Are the inputs points, lines, circles, or rectangles?
- Does the problem involve coordinates?
- Am I calculating distances or slopes?
- Do I need to determine intersections?
- Is the problem asking about spatial relationships?

If yes, Geometry is likely a strong candidate.

---

## Common Interview Keywords

Look for phrases like:

- "point";
- "coordinate";
- "line";
- "rectangle";
- "circle";
- "distance";
- "intersection";
- "overlap";
- "closest";
- "convex hull";
- "collinear".

---

## Common Geometry Techniques

### Distance Formula

For two points:

```text
(x1, y1)

(x2, y2)
```

Euclidean distance:

```text
sqrt(
    (x2 - x1)^2 +
    (y2 - y1)^2
)
```

Usually compare squared distances instead:

```text
(x2 - x1)^2 + (y2 - y1)^2
```

because square root is unnecessary.

Typical examples:

- K Closest Points to Origin
- Circle and Rectangle Overlapping

---

### Slope Calculation

To determine whether points are on the same line:

```text
slope = (y2 - y1) / (x2 - x1)
```

Avoid floating-point precision problems.

Instead normalize:

```text
dy / dx
```

using greatest common divisor.

Typical example:

- Max Points on a Line

---

### Cross Product

The cross product determines the orientation of three points.

Given:

```text
A(x1, y1)

B(x2, y2)

C(x3, y3)
```

Calculate:

```text
(B - A) × (C - A)
```

Result:

```text
> 0

counterclockwise


< 0

clockwise


= 0

collinear
```

Used for:

- convex hull;
- intersection tests;
- ordering points.

Typical example:

- Erect the Fence

---

### Convex Hull

Find the smallest polygon containing all points.

Common algorithm:

```text
Monotonic Chain

or

Graham Scan
```

Basic idea:

1. Sort points.
2. Build lower hull.
3. Build upper hull.
4. Combine results.

Typical example:

- Erect the Fence

---

### Coordinate Compression

Large coordinates are mapped to smaller indexes.

Example:

```text
Original:

100
500000
1000000


Compressed:

0
1
2
```

Used when geometry problems involve large ranges.

Typical examples:

- Rectangle Area II
- Perfect Rectangle

---

## Complexity

Geometry problems vary significantly.

Typical examples:

### Checking points

```text
O(n)
```

Example:

- Straight Line

---

### Sorting points

```text
O(n log n)
```

Example:

- K Closest Points
- Convex Hull

---

### Comparing all point pairs

```text
O(n^2)
```

Example:

- Max Points on a Line

---

### Advanced geometry

May require:

- sweep line;
- segment trees;
- coordinate compression.

Complexity depends on the supporting data structures.

---

## Common Pitfalls

### Floating Point Precision

Avoid:

```cpp
double slope;
```

when exact comparison is possible.

Prefer:

```cpp
dy / gcd(dy, dx)
```

---

### Overflow

Coordinates can be large.

Avoid:

```cpp
int
```

for calculations involving multiplication.

Prefer:

```cpp
long long
```

---

### Vertical Lines

Vertical lines have:

```text
dx = 0
```

Handle them separately.

---

### Duplicate Points

Two identical points:

```text
(x, y)

(x, y)
```

require special handling in many problems.

---

## Learning Goals

After completing this pattern, you should be able to:

- work with coordinate systems;
- calculate distances safely;
- compare slopes correctly;
- use cross products;
- solve basic computational geometry problems;
- recognize when geometry techniques are required.

---

## Progress

- [ ] 1232. Check If It Is a Straight Line
- [ ] 973. K Closest Points to Origin
- [ ] 149. Max Points on a Line
- [ ] 1401. Circle and Rectangle Overlapping
- [ ] 587. Erect the Fence
- [ ] 218. The Skyline Problem
- [ ] 391. Perfect Rectangle
- [ ] 850. Rectangle Area II
