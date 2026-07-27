# LeetCode Pattern: Bit Manipulation

## Overview

The Bit Manipulation pattern uses binary operations to solve problems
efficiently by working directly with the bits of an integer.

Instead of treating an integer as a decimal number, think of it as a
sequence of bits:

```text
13

Decimal:

13

Binary:

1101
```

Bit manipulation is especially useful for:

- checking whether a bit is set;
- setting or clearing bits;
- toggling bits;
- representing sets with bitmasks;
- optimizing space and performance.

The most common operators in C++ are:

- `&` (AND)
- `|` (OR)
- `^` (XOR)
- `~` (NOT)
- `<<` (left shift)
- `>>` (right shift)

The key skill is recognizing when binary representations simplify a
problem that would otherwise require additional memory or nested loops.

---

## Practice Problems

Solve these problems in order. The early problems introduce basic bit
operations, while the later ones combine multiple bitwise techniques.

### Easy

- **191. Number of 1 Bits**  
  <https://leetcode.com/problems/number-of-1-bits/>

  Count the number of set bits in an integer.

- **338. Counting Bits**  
  <https://leetcode.com/problems/counting-bits/>

  Compute the number of set bits for every integer in a range.

- **190. Reverse Bits**  
  <https://leetcode.com/problems/reverse-bits/>

  Reverse the bit order of a 32-bit integer.

- **136. Single Number**  
  <https://leetcode.com/problems/single-number/>

  Use XOR to find the element that appears exactly once.

### Medium

- **137. Single Number II**  
  <https://leetcode.com/problems/single-number-ii/>

  Track bit frequencies to identify the unique element.

- **201. Bitwise AND of Numbers Range**  
  <https://leetcode.com/problems/bitwise-and-of-numbers-range/>

  Find the common binary prefix shared by all numbers.

- **1318. Minimum Flips to Make a OR b Equal to c**  
  <https://leetcode.com/problems/minimum-flips-to-make-a-or-b-equal-to-c/>

  Analyze each bit independently to determine the minimum number of
  changes.

- **260. Single Number III**  
  <https://leetcode.com/problems/single-number-iii/>

  Use XOR and bit partitioning to find two unique numbers.

### Hard

- **982. Triples with Bitwise AND Equal To Zero**  
  <https://leetcode.com/problems/triples-with-bitwise-and-equal-to-zero/>

  Combine bitmask optimization with efficient counting techniques.

- **1178. Number of Valid Words for Each Puzzle**  
  <https://leetcode.com/problems/number-of-valid-words-for-each-puzzle/>

  Represent words as bitmasks to answer queries efficiently.

---

## Pattern Recognition Checklist

Ask yourself:

- Can each value be represented as a bitmask?
- Am I checking individual binary digits?
- Does XOR naturally eliminate duplicate values?
- Can a set be represented by the bits of an integer?
- Would bit operations simplify the solution?

If yes, Bit Manipulation is likely a strong candidate.

---

## Common Interview Keywords

Look for phrases like:

- "binary";
- "bit";
- "XOR";
- "AND";
- "OR";
- "mask";
- "toggle";
- "power of two";
- "unique number";
- "set bits".

---

## Common Bit Manipulation Variations

### XOR Trick

XOR has several useful properties:

```text
x ^ x = 0

x ^ 0 = x

XOR is commutative and associative.
```

These properties make XOR ideal for canceling duplicate values.

Typical examples:

- Single Number
- Single Number III

---

### Bitmask Representation

Represent a set using the bits of an integer.

Example:

```text
Bitmask:

101101

Meaning:

Items 0, 2, 3, and 5 are present.
```

Typical examples:

- Number of Valid Words for Each Puzzle
- Subset-related problems

---

### Bit Counting

Count or manipulate individual bits.

Example:

```text
while (n != 0) {
    n &= (n - 1);
}
```

Each iteration removes the lowest set bit.

Typical examples:

- Number of 1 Bits
- Counting Bits

---

## Complexity

Bit operations themselves execute in constant time.

Typical complexities:

- Single integer operations: `O(1)`
- Iterating over all bits: `O(number of bits)`

For 32-bit integers:

- Time complexity: `O(32)`, which is effectively `O(1)`

Space complexity is usually:

- `O(1)`

---

## Learning Goals

After completing this pattern, you should be able to:

- understand the behavior of all basic bitwise operators;
- recognize when XOR simplifies a problem;
- represent sets using bitmasks;
- manipulate individual bits efficiently;
- apply bit tricks to optimize algorithms.

---

## Progress

- [ ] 191. Number of 1 Bits
- [ ] 338. Counting Bits
- [ ] 190. Reverse Bits
- [ ] 136. Single Number
- [ ] 137. Single Number II
- [ ] 201. Bitwise AND of Numbers Range
- [ ] 1318. Minimum Flips to Make a OR b Equal to c
- [ ] 260. Single Number III
- [ ] 982. Triples with Bitwise AND Equal To Zero
- [ ] 1178. Number of Valid Words for Each Puzzle
