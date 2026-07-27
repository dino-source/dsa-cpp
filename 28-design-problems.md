# LeetCode Pattern: Design Problems

## Overview

The Design Problems pattern focuses on building custom data structures and
systems that support multiple operations efficiently.

Unlike typical algorithm problems, these tasks do not ask for a single
algorithm. Instead, they test whether you can design the right combination
of data structures to satisfy strict performance requirements.

The main idea is:

- identify required operations;
- analyze their time complexity requirements;
- choose data structures that work well together;
- maintain consistency between multiple structures.

Design problems often combine:

- hash tables;
- linked lists;
- heaps;
- queues;
- stacks;
- trees;
- custom classes.

The most common challenge is achieving operations such as:

```text
Insert: O(1)

Delete: O(1)

Lookup: O(1)

Get maximum/minimum: O(1) or O(log n)
```

In C++, these problems commonly use:

- `std::unordered_map`;
- `std::list`;
- `std::vector`;
- `std::priority_queue`;
- custom classes and structs.

The key skill is recognizing that no single data structure is enough, and
multiple structures must work together.

---

## Practice Problems

Solve these problems in order. The early problems introduce combining
basic data structures, while the later ones require more complex designs.

### Medium

- **155. Min Stack**  
  <https://leetcode.com/problems/min-stack/>

  Design a stack that supports retrieving the minimum element in constant
  time.

- **146. LRU Cache**  
  <https://leetcode.com/problems/lru-cache/>

  Combine a hash map and a doubly linked list to support O(1) get and put
  operations.

- **208. Implement Trie (Prefix Tree)**  
  <https://leetcode.com/problems/implement-trie-prefix-tree/>

  Design a specialized data structure for string storage and lookup.

- **380. Insert Delete GetRandom O(1)**  
  <https://leetcode.com/problems/insert-delete-getrandom-o1/>

  Combine an array and hash map to support constant-time operations.

- **641. Design Circular Deque**  
  <https://leetcode.com/problems/design-circular-deque/>

  Implement a double-ended queue with controlled capacity.

### Hard

- **460. LFU Cache**  
  <https://leetcode.com/problems/lfu-cache/>

  Design a cache that evicts the least frequently used item.

- **432. All O'one Data Structure**  
  <https://leetcode.com/problems/all-oone-data-structure/>

  Maintain counts and retrieve minimum/maximum frequency keys efficiently.

- **895. Maximum Frequency Stack**  
  <https://leetcode.com/problems/maximum-frequency-stack/>

  Build a stack that prioritizes the most frequent elements.

- **981. Time Based Key-Value Store**  
  <https://leetcode.com/problems/time-based-key-value-store/>

  Design a historical key-value lookup system.

- **1206. Design Skiplist**  
  <https://leetcode.com/problems/design-skiplist/>

  Implement a probabilistic data structure for fast ordered operations.

---

## Pattern Recognition Checklist

Ask yourself:

- Does the problem ask me to implement a data structure?
- Are there strict time complexity requirements?
- Do multiple operations need to be efficient simultaneously?
- Can combining two simple structures solve the problem?
- Do I need to maintain extra state?

If yes, this is likely a Design Problem.

---

## Common Interview Keywords

Look for phrases like:

- "design a data structure";
- "implement";
- "support operations";
- "O(1)";
- "constant time";
- "cache";
- "frequency";
- "eviction";
- "recently used";
- "random access".

---

## Common Design Patterns

### Hash Map + Doubly Linked List

The classic LRU Cache design.

Goal:

```text
get(key): O(1)

put(key, value): O(1)
```

Solution:

Hash map:

```text
key -> node pointer
```

Doubly linked list:

```text
Most recent

    ...

Least recent
```

The hash map provides fast lookup.

The linked list provides fast removal and reordering.

Typical example:

- LRU Cache

---

### Hash Map + Array

Used when:

- lookup must be fast;
- elements can be stored compactly;
- deletion order does not matter.

Example:

```text
value -> index in array
```

Typical example:

- Insert Delete GetRandom O(1)

---

### Multiple Maps

Sometimes one mapping is not enough.

Example:

```text
frequency -> keys

key -> frequency
```

Used when operations depend on both:

- individual items;
- groups of items.

Typical examples:

- LFU Cache
- All O'one Data Structure

---

### Custom Data Structures

Some problems require implementing a structure from scratch.

Examples:

- Trie;
- Skiplist;
- Circular Queue;
- Circular Deque.

The goal is understanding the internal mechanics instead of relying on
library containers.

---

## Complexity Analysis

Design problems usually specify required complexity.

Examples:

### LRU Cache

Required:

```text
get(): O(1)

put(): O(1)
```

Typical implementation:

```text
unordered_map + doubly linked list
```

---

### LFU Cache

Required:

```text
get(): O(1)

put(): O(1)
```

Typical implementation:

```text
two hash maps + linked lists
```

---

### Randomized Data Structures

Required:

```text
insert(): O(1)

delete(): O(1)

random(): O(1)
```

Typical implementation:

```text
vector + unordered_map
```

---

## Common Pitfalls

### Choosing Only One Data Structure

Many design problems cannot be solved efficiently with one container.

Example:

```text
Hash map:

fast lookup

but

slow ordering
```

```text
Linked list:

fast ordering

but

slow lookup
```

The solution is combining them.

---

### Ignoring Edge Cases

Always consider:

- empty structure;
- duplicate values;
- capacity limits;
- deleting the only element;
- updating existing keys.

---

### Forgetting Invariants

A good design maintains clear rules.

Example:

LRU Cache:

```text
Every key in the map must exist in the linked list.
```

LFU Cache:

```text
Every key must belong to exactly one frequency group.
```

---

## Learning Goals

After completing this pattern, you should be able to:

- design custom data structures;
- translate requirements into operations;
- analyze complexity constraints;
- combine multiple containers effectively;
- implement production-style components.

---

## Progress

- [ ] 155. Min Stack
- [ ] 146. LRU Cache
- [ ] 208. Implement Trie (Prefix Tree)
- [ ] 380. Insert Delete GetRandom O(1)
- [ ] 641. Design Circular Deque
- [ ] 460. LFU Cache
- [ ] 432. All O'one Data Structure
- [ ] 895. Maximum Frequency Stack
- [ ] 981. Time Based Key-Value Store
- [ ] 1206. Design Skiplist
