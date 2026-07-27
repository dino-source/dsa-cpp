# LeetCode Pattern: Fast & Slow Pointer

## Overview

The Fast & Slow Pointer pattern uses two pointers that move through a
data structure at different speeds.

The most common version uses:

- a slow pointer that moves one step at a time;
- a fast pointer that moves two steps at a time.

This pattern is also known as Floyd's Cycle Detection Algorithm.

It is especially useful for:

- detecting cycles;
- finding the middle of a linked list;
- finding cycle entry points;
- analyzing repeated sequences.

In C++, this pattern is commonly used with:

- linked lists;
- iterators;
- arrays with special constraints.

The key insight is that two pointers moving at different speeds can reveal
information that is difficult to find with a single traversal.

---

## Practice Problems

Solve these problems in order. The early problems introduce the basic
fast/slow technique, while the later ones require deeper reasoning.

### Easy

- **141. Linked List Cycle**  
  <https://leetcode.com/problems/linked-list-cycle/>

  Use fast and slow pointers to detect whether a cycle exists.

- **876. Middle of the Linked List**  
  <https://leetcode.com/problems/middle-of-the-linked-list/>

  Move the fast pointer twice as fast to find the middle node.

- **202. Happy Number**  
  <https://leetcode.com/problems/happy-number/>

  Treat number transformations as a sequence and detect cycles.

### Medium

- **142. Linked List Cycle II**  
  <https://leetcode.com/problems/linked-list-cycle-ii/>

  Find the node where a cycle begins after detecting a loop.

- **287. Find the Duplicate Number**  
  <https://leetcode.com/problems/find-the-duplicate-number/>

  Model the array as a linked list and detect the cycle entry point.

---

## Pattern Recognition Checklist

Ask yourself:

- Is there a possibility of a cycle?
- Am I repeatedly applying a transformation?
- Do I need to find the middle element?
- Can I solve this without extra memory?
- Would two different pointer speeds reveal useful information?

If the answer is yes, Fast & Slow Pointer is likely a good candidate.

---

## Common Interview Keywords

Look for phrases like:

- "cycle";
- "loop";
- "middle";
- "duplicate";
- "repeated sequence";
- "without extra space";
- "linked list";
- "constant memory".

---

## Common Fast & Slow Pointer Techniques

### Cycle Detection

Move:

- slow pointer by one step;
- fast pointer by two steps.

If they meet, a cycle exists.

Example:

```text
slow:  ->  ->  ->  ->

fast:  ->  ->  ->  ->  ->  ->
```

---

### Finding the Middle Element

The fast pointer reaches the end while the slow pointer reaches the
middle.

Example:

```text
1 -> 2 -> 3 -> 4 -> 5

slow:
          ^
          3

fast:
                    ^
                    5
```

---

### Finding Cycle Entry Point

After detecting a cycle:

1. Keep one pointer at the meeting point.
2. Move both pointers one step at a time.
3. The next meeting point is the cycle entry.

---

## Complexity

Most Fast & Slow Pointer solutions have:

- Time complexity: `O(n)`
- Space complexity: `O(1)`

The main advantage is solving problems that normally require a visited set
without using additional memory.

---

## Learning Goals

After completing this pattern, you should be able to:

- recognize cycle detection problems quickly;
- apply Floyd's algorithm;
- find the middle of a linked list;
- solve repeated sequence problems with constant memory;
- explain why two different pointer speeds work.

---

## Progress

- [ ] 141. Linked List Cycle
- [ ] 876. Middle of the Linked List
- [ ] 202. Happy Number
- [ ] 142. Linked List Cycle II
- [ ] 287. Find the Duplicate Number
