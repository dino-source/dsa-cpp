# LeetCode Pattern: Rolling Hash

## Overview

The Rolling Hash pattern is used to efficiently compare substrings and
search for patterns inside strings.

The main idea is to convert a string into a numeric hash value so that
substrings can be compared quickly.

Instead of comparing every character:

```text
Compare substring A:

O(n)

Compare substring B:

O(n)
```

Rolling Hash allows substring comparison in approximately:

```text
O(1)
```

after preprocessing.

This pattern is commonly based on the Rabin-Karp algorithm.

Rolling Hash is especially useful for:

- substring search;
- duplicate substring detection;
- string matching;
- palindrome checking;
- comparing many substrings.

The key idea is that when the window moves by one character, the hash can
be updated instead of recalculated from scratch.

In C++, this pattern commonly uses:

- `long long`;
- modular arithmetic;
- prefix hashes;
- powers of a base number;
- `std::unordered_set`.

The key skill is recognizing when many substring comparisons make direct
character-by-character comparison too slow.

---

## Practice Problems

Solve these problems in order. The early problems introduce basic string
hashing, while the later ones require combining hashing with binary search
or advanced techniques.

### Medium

- **28. Find the Index of the First Occurrence in a String**  
  <https://leetcode.com/problems/find-the-index-of-the-first-occurrence-in-a-string/>

  Implement substring search using hashing techniques.

- **187. Repeated DNA Sequences**  
  <https://leetcode.com/problems/repeated-dna-sequences/>

  Detect repeated fixed-length substrings efficiently.

- **1044. Longest Duplicate Substring**  
  <https://leetcode.com/problems/longest-duplicate-substring/>

  Combine rolling hash with binary search to find the longest duplicate
  substring.

- **1392. Longest Happy Prefix**  
  <https://leetcode.com/problems/longest-happy-prefix/>

  Use prefix hashing to compare prefixes and suffixes.

### Hard

- **214. Shortest Palindrome**  
  <https://leetcode.com/problems/shortest-palindrome/>

  Find the longest palindromic prefix using string hashing.

- **718. Maximum Length of Repeated Subarray**  
  <https://leetcode.com/problems/maximum-length-of-repeated-subarray/>

  Use hashing to compare subarrays efficiently.

- **1923. Longest Common Subpath**  
  <https://leetcode.com/problems/longest-common-subpath/>

  Apply rolling hash with binary search across multiple paths.

---

## Pattern Recognition Checklist

Ask yourself:

- Do I need to compare many substrings?
- Is direct string comparison too slow?
- Am I searching for repeated substrings?
- Do I need to check whether two substrings are equal quickly?
- Can I transform strings into comparable hash values?

If yes, Rolling Hash is likely a strong candidate.

---

## Common Interview Keywords

Look for phrases like:

- "substring";
- "duplicate substring";
- "pattern matching";
- "find occurrence";
- "longest repeated";
- "common substring";
- "prefix";
- "suffix".

---

## Common Rolling Hash Variations

### Rabin-Karp Algorithm

Use a rolling hash to search for a pattern inside a larger string.

Example:

```text
Text:

abcdefghi

Pattern:

def
```

Instead of comparing every window:

```text
abc
bcd
cde
def
...
```

compute hashes and compare:

```text
hash(window) == hash(pattern)
```

Typical examples:

- Find the Index of the First Occurrence in a String
- Repeated DNA Sequences

---

### Prefix Hash

Precompute hashes for all prefixes.

Example:

```text
String:

abcdef

Prefix hashes:

a
ab
abc
abcd
abcde
abcdef
```

Then any substring hash can be calculated quickly.

Typical examples:

- Longest Happy Prefix
- Longest Duplicate Substring

---

### Rolling Window Hash

When moving a fixed-size window:

```text
Current:

abcd

Move:

bcde
```

Remove the contribution of the outgoing character and add the incoming
character.

Typical examples:

- Repeated DNA Sequences
- Rabin-Karp

---

### Hash + Binary Search

Some problems ask for the longest or shortest substring satisfying a
condition.

A common strategy:

```text
1. Guess the length.
2. Check if a duplicate/common substring exists.
3. Binary search the answer.
```

Typical examples:

- Longest Duplicate Substring
- Longest Common Subpath

---

## Hash Function Basics

A common polynomial rolling hash:

```text
hash = (s[0] * base^(n-1)
      + s[1] * base^(n-2)
      + ...
      + s[n-1]) % mod
```

When choosing parameters:

- `base` is usually a small prime number;
- `mod` is usually a large prime number.

Example:

```text
base = 31

mod = 1,000,000,007
```

Multiple hash functions can be used to reduce collisions.

---

## Complexity

Typical complexities:

### Substring Hash Query Complexity

After preprocessing:

- Time complexity: `O(1)`

### Building Prefix Hashes Complexity

- Time complexity: `O(n)`
- Space complexity: `O(n)`

### Rabin-Karp Search Complexity

Average:

- Time complexity: `O(n + m)`

Worst case:

- `O(n × m)`

because of possible hash collisions.

### Hash + Binary Search Complexity

Typical:

- Time complexity: `O(n log n)`
- Space complexity: `O(n)`

---

## Common Pitfalls

### Hash Collisions

Different strings can produce the same hash.

Solutions:

- use a large modulus;
- use two independent hashes;
- verify matches character-by-character when needed.

---

### Integer Overflow

Hash multiplication can overflow.

Use:

```cpp
long long
```

and apply modulo operations carefully.

---

### Negative Values

When subtracting the outgoing character:

```text
hash = hash - removed_value
```

the result may become negative.

Normalize:

```text
(hash + mod) % mod
```

---

## Learning Goals

After completing this pattern, you should be able to:

- implement a rolling hash;
- understand polynomial hashing;
- compare substrings efficiently;
- use hashing with binary search;
- recognize when string hashing is preferable to direct comparison.

---

## Progress

- [ ] 28. Find the Index of the First Occurrence in a String
- [ ] 187. Repeated DNA Sequences
- [ ] 1044. Longest Duplicate Substring
- [ ] 1392. Longest Happy Prefix
- [ ] 214. Shortest Palindrome
- [ ] 718. Maximum Length of Repeated Subarray
- [ ] 1923. Longest Common Subpath
