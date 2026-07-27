# LeetCode Pattern: Segment Tree / Fenwick Tree

## Overview

The Segment Tree and Fenwick Tree (also known as the Binary Indexed Tree,
or BIT) are data structures designed for efficiently answering repeated
range queries while supporting updates.

Without these data structures, a typical solution looks like this:

```text
Update: O(1)
Query:  O(n)
```

With a Segment Tree or Fenwick Tree:

```text
Update: O(log n)
Query:  O(log n)
```

These structures are especially useful when an array changes over time and
range queries must be answered repeatedly.

Typical applications include:

- range sum queries;
- range minimum/maximum queries;
- frequency counting;
- inversion counting;
- order statistics.

### Fenwick Tree (Binary Indexed Tree)

A Fenwick Tree is simpler to implement and is ideal for prefix-based
operations such as sums and frequencies.

### Segment Tree

A Segment Tree is more flexible and supports a wider variety of range
queries and updates.

In C++, these structures commonly use:

- `std::vector`;
- iterative or recursive implementations;
- index arithmetic.

The key skill is recognizing when repeated updates and range queries make
recomputing results too expensive.

---

## Practice Problems

Solve these problems in order. The early problems introduce mutable range
queries, while the later ones require more advanced applications.

### Medium

- **307. Range Sum Query – Mutable**  
  <https://leetcode.com/problems/range-sum-query-mutable/>

  Implement efficient updates and range sum queries.

- **303. Range Sum Query – Immutable**  
  <https://leetcode.com/problems/range-sum-query-immutable/>

  Learn why prefix sums work for immutable arrays and why mutable arrays
  require more advanced data structures.

- **729. My Calendar I**  
  <https://leetcode.com/problems/my-calendar-i/>

  A common introduction to interval data structures. While many solutions
  use ordered maps, Segment Trees are also applicable.

### Hard

- **315. Count of Smaller Numbers After Self**  
  <https://leetcode.com/problems/count-of-smaller-numbers-after-self/>

  Use a Fenwick Tree or Segment Tree for efficient frequency queries.

- **327. Count of Range Sum**  
  <https://leetcode.com/problems/count-of-range-sum/>

  Combine prefix sums with a Fenwick Tree or Segment Tree.

- **493. Reverse Pairs**  
  <https://leetcode.com/problems/reverse-pairs/>

  Count special inversion pairs efficiently.

- **699. Falling Squares**  
  <https://leetcode.com/problems/falling-squares/>

  Use a Segment Tree with coordinate compression.

---

## Pattern Recognition Checklist

Ask yourself:

- Do I need many range queries?
- Does the underlying array change over time?
- Is recomputing every query too slow?
- Can each update affect many future queries?
- Is `O(n)` per query unacceptable?

If yes, a Segment Tree or Fenwick Tree is likely a strong candidate.

---

## Common Interview Keywords

Look for phrases like:

- "range sum";
- "range minimum";
- "range maximum";
- "mutable array";
- "many updates";
- "many queries";
- "prefix sum";
- "frequency";
- "inversions".

---

## Common Segment Tree / Fenwick Tree Variations

### Fenwick Tree Examples

Store prefix information compactly.

Typical operations:

```text
update(index, delta)

query(prefix)
```

Range queries are computed as:

```text
sum(left, right)

=

prefix(right)

-

prefix(left - 1)
```

Typical examples:

- Range Sum Query – Mutable
- Count of Smaller Numbers After Self

---

### Segment Tree Examples

Each node represents an interval.

Example:

```text
                [0, 7]
               /      \
          [0, 3]      [4, 7]
          /    \      /    \
      [0,1] [2,3] [4,5] [6,7]
```

Each node stores information about its interval, such as:

- sum;
- minimum;
- maximum;
- greatest common divisor.

Typical examples:

- Falling Squares
- Range Sum Query – Mutable

---

### Coordinate Compression

Compress large coordinate values into a compact index range before
building the tree.

Example:

```text
Original:

1
100
1,000,000

Compressed:

0
1
2
```

Typical examples:

- Falling Squares
- Reverse Pairs

---

## Complexity

### Fenwick Tree Complexity

- Update: `O(log n)`
- Prefix query: `O(log n)`
- Range query: `O(log n)`

Space complexity:

- `O(n)`

---

### Segment Tree Complexity

- Update: `O(log n)`
- Range query: `O(log n)`
- Build: `O(n)`

Space complexity:

- `O(n)`

A Segment Tree typically requires about `4n` nodes for a recursive
implementation.

---

## Choosing Between Them

Use a **Fenwick Tree** when:

- only prefix-based operations are needed;
- the operation is reversible (such as addition);
- simplicity and memory efficiency are important.

Use a **Segment Tree** when:

- arbitrary range queries are required;
- multiple query types are needed;
- lazy propagation or advanced interval operations are required.

---

## Learning Goals

After completing this pattern, you should be able to:

- recognize range query problems;
- implement a Fenwick Tree from scratch;
- implement a Segment Tree from scratch;
- understand coordinate compression;
- choose the appropriate data structure for mutable arrays.

---

## Progress

- [ ] 303. Range Sum Query – Immutable
- [ ] 307. Range Sum Query – Mutable
- [ ] 729. My Calendar I
- [ ] 315. Count of Smaller Numbers After Self
- [ ] 327. Count of Range Sum
- [ ] 493. Reverse Pairs
- [ ] 699. Falling Squares
