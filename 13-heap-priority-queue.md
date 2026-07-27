# LeetCode Pattern: Heap / Priority Queue

## Overview

The Heap / Priority Queue pattern is used to efficiently retrieve the
largest or smallest element from a collection.

The main idea is to maintain a data structure where the most important
element is always available at the top.

A heap is commonly used for:

- finding the k largest or smallest elements;
- maintaining the best candidates;
- merging sorted data;
- scheduling tasks;
- solving greedy problems.

There are two common types of heaps:

- min-heap: the smallest element is always on top;
- max-heap: the largest element is always on top.

In C++, this pattern commonly uses:

- `std::priority_queue`;
- `std::vector`.

The key skill is recognizing when you do not need to fully sort data and
only need quick access to the current best element.

---

## Practice Problems

Solve these problems in order. The early problems introduce basic heap
usage, while the later ones require combining heaps with other techniques.

### Easy

- **1046. Last Stone Weight**  
  <https://leetcode.com/problems/last-stone-weight/>

  Use a max-heap to repeatedly select the two largest elements.

- **703. Kth Largest Element in a Stream**  
  <https://leetcode.com/problems/kth-largest-element-in-a-stream/>

  Maintain a min-heap of the k largest elements seen so far.

### Medium

- **215. Kth Largest Element in an Array**  
  <https://leetcode.com/problems/kth-largest-element-in-an-array/>

  Use a heap to find the kth largest element efficiently.

- **347. Top K Frequent Elements**  
  <https://leetcode.com/problems/top-k-frequent-elements/>

  Combine frequency counting with a heap to find the most common elements.

- **973. K Closest Points to Origin**  
  <https://leetcode.com/problems/k-closest-points-to-origin/>

  Maintain the closest candidates using a heap.

- **295. Find Median from Data Stream**  
  <https://leetcode.com/problems/find-median-from-data-stream/>

  Use two heaps to maintain the lower and upper halves of the data.

- **621. Task Scheduler**  
  <https://leetcode.com/problems/task-scheduler/>

  Use a priority queue to schedule tasks with the highest frequency first.

### Hard

- **23. Merge k Sorted Lists**  
  <https://leetcode.com/problems/merge-k-sorted-lists/>

  Use a min-heap to efficiently merge multiple sorted linked lists.

- **502. IPO**  
  <https://leetcode.com/problems/ipo/>

  Combine sorting and heaps to always select the best available project.

---

## Pattern Recognition Checklist

Ask yourself:

- Do I repeatedly need the largest or smallest element?
- Do I need the top `k` elements?
- Would sorting everything be unnecessary?
- Do I need to maintain the best candidates while processing data?
- Am I merging multiple sorted sequences?

If yes, Heap / Priority Queue is likely a strong candidate.

---

## Common Interview Keywords

Look for phrases like:

- "k largest";
- "k smallest";
- "top k";
- "minimum cost";
- "maximum profit";
- "merge sorted";
- "closest";
- "stream";
- "schedule";
- "highest priority".

---

## Common Heap Variations

### Min-Heap

The smallest element is always available at the top.

Typical uses:

- k smallest elements;
- merging sorted structures;
- shortest processing time.

Example:

```text
Min-heap:

        2
       / \
      5   8
     /
    10
```

The top element is always the smallest.

Typical examples:

- Merge k Sorted Lists
- K Closest Points to Origin

---

### Max-Heap

The largest element is always available at the top.

Typical uses:

- k largest elements;
- selecting maximum values;
- greedy decisions.

Example:

```text
Max-heap:

        10
       /  \
      8    5
     /
    2
```

The top element is always the largest.

Typical examples:

- Last Stone Weight
- Kth Largest Element in an Array

---

### Two Heaps

Use two heaps to divide data into two groups.

Common approach:

- max-heap stores the smaller half;
- min-heap stores the larger half.

Typical examples:

- Find Median from Data Stream

---

## Complexity

Most Heap / Priority Queue solutions have:

- Insert: `O(log n)`
- Remove top element: `O(log n)`
- Access top element: `O(1)`

Overall complexity depends on the number of heap operations.

Common patterns:

- Top `k` elements: `O(n log k)`
- Merge `k` sorted lists: `O(n log k)`

Space complexity:

- `O(k)`

where `k` is the number of elements stored in the heap.

---

## Learning Goals

After completing this pattern, you should be able to:

- recognize when a heap is better than sorting;
- choose between min-heap and max-heap;
- solve top-k problems efficiently;
- use multiple heaps together;
- explain heap operation complexity.

---

## Progress

- [ ] 1046. Last Stone Weight
- [ ] 703. Kth Largest Element in a Stream
- [ ] 215. Kth Largest Element in an Array
- [ ] 347. Top K Frequent Elements
- [ ] 973. K Closest Points to Origin
- [ ] 295. Find Median from Data Stream
- [ ] 621. Task Scheduler
- [ ] 23. Merge k Sorted Lists
- [ ] 502. IPO
