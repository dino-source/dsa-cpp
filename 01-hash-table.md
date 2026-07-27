# LeetCode Pattern: Hash Table / Frequency Counting

## Overview

Hash Table is one of the most common patterns in coding interviews.

Use a hash table when you need fast lookups, frequency counting, or a way
to remember information while iterating through data.

In C++, this pattern usually uses:

- `std::unordered_map`
- `std::unordered_set`

The main idea is to replace repeated searching with constant-time average
lookups.

A common transformation:

```text
Brute force:
For each element, search the rest of the array.
Time complexity: O(n²)

Hash table approach:
Store information while iterating once.
Time complexity: O(n)
```

---

## Practice Problems

Solve these problems in order. The early problems introduce the basic
concepts, while the later ones combine multiple ideas.

### Easy

- **1. Two Sum**  
  <https://leetcode.com/problems/two-sum/>

  Use a hash map to store previously seen numbers and their indices.

- **217. Contains Duplicate**  
  <https://leetcode.com/problems/contains-duplicate/>

  Use a hash set to detect whether a value appears more than once.

- **219. Contains Duplicate II**  
  <https://leetcode.com/problems/contains-duplicate-ii/>

  Track both values and their positions.

- **242. Valid Anagram**  
  <https://leetcode.com/problems/valid-anagram/>

  Count character frequencies and compare the results.

- **383. Ransom Note**  
  <https://leetcode.com/problems/ransom-note/>

  Track available character counts and consume them.

- **205. Isomorphic Strings**  
  <https://leetcode.com/problems/isomorphic-strings/>

  Build a one-to-one mapping between characters.

- **290. Word Pattern**  
  <https://leetcode.com/problems/word-pattern/>

  Maintain a bijection between pattern characters and words.

### Medium

- **49. Group Anagrams**  
  <https://leetcode.com/problems/group-anagrams/>

  Use a canonical representation to group equivalent strings.

- **347. Top K Frequent Elements**  
  <https://leetcode.com/problems/top-k-frequent-elements/>

  Count frequencies and find the most common elements.

---

## Pattern Recognition Checklist

Ask yourself:

- Do I need to know whether I have seen this value before?
- Do I need to count how many times something appears?
- Am I looking for duplicates?
- Can I replace a nested loop with a lookup?
- Do I need to map one value to another?

If the answer is yes, a hash table is likely a good candidate.

---

## Common Interview Keywords

Look for phrases like:

- "frequency";
- "count";
- "duplicate";
- "unique";
- "group";
- "anagram";
- "previously seen";
- "lookup";
- "mapping".

---

## Complexity

Typical hash table operations:

- Lookup: `O(1)` average
- Insert: `O(1)` average
- Delete: `O(1)` average

Most interview solutions using this pattern have:

- Time complexity: `O(n)`
- Space complexity: `O(n)`

---

## Learning Goals

After completing this pattern, you should be able to:

- recognize hash table problems quickly;
- choose between `unordered_map` and `unordered_set`;
- reduce brute-force solutions using hashing;
- explain time and space complexity clearly.

---

## Progress

- [ ] 1. Two Sum
- [ ] 217. Contains Duplicate
- [ ] 219. Contains Duplicate II
- [ ] 242. Valid Anagram
- [ ] 383. Ransom Note
- [ ] 205. Isomorphic Strings
- [ ] 290. Word Pattern
- [ ] 49. Group Anagrams
- [ ] 347. Top K Frequent Elements
