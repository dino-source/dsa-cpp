# LeetCode Pattern: Sliding Window

## Overview

The Sliding Window pattern is used to efficiently process contiguous
parts of arrays or strings.

The main idea is to maintain a window of elements and move it through the
data structure instead of recalculating every possible range.

This pattern is especially useful for:

- finding the longest or shortest substring;
- processing contiguous subarrays;
- tracking frequency inside a range;
- optimizing repeated calculations.

There are two main variations:

- fixed-size sliding window;
- variable-size sliding window.

In C++, this pattern commonly uses:

- `std::vector`
- `std::string`
- `std::unordered_map`
- `std::unordered_set`

The key skill is recognizing when a problem involves a contiguous range
and the answer can be maintained while the window moves.

---

## Practice Problems

Solve these problems in order. The early problems introduce fixed-size
windows, while the later ones require dynamic window adjustments.

### Easy

- **643. Maximum Average Subarray I**  
  <https://leetcode.com/problems/maximum-average-subarray-i/>

  Maintain a fixed-size window and update the running sum.

### Medium

- **1456. Maximum Number of Vowels in a Substring of Given Length**  
  <https://leetcode.com/problems/maximum-number-of-vowels-in-a-substring-of-given-length/>

  Track the number of vowels inside a fixed-size window.

- **3. Longest Substring Without Repeating Characters**  
  <https://leetcode.com/problems/longest-substring-without-repeating-characters/>

  Expand and shrink the window while maintaining unique characters.

- **209. Minimum Size Subarray Sum**  
  <https://leetcode.com/problems/minimum-size-subarray-sum/>

  Use a variable-size window to find the shortest valid subarray.

- **424. Longest Repeating Character Replacement**  
  <https://leetcode.com/problems/longest-repeating-character-replacement/>

  Track character frequencies while expanding the window.

- **567. Permutation in String**  
  <https://leetcode.com/problems/permutation-in-string/>

  Compare character frequencies between a pattern and a sliding window.

### Hard

- **76. Minimum Window Substring**  
  <https://leetcode.com/problems/minimum-window-substring/>

  Maintain the smallest window containing all required characters.

---

## Pattern Recognition Checklist

Ask yourself:

- Is the problem about a contiguous subarray or substring?
- Do I need the longest or shortest valid range?
- Can I update the answer when moving one element at a time?
- Can I avoid recalculating information for every window?
- Do I need to track frequency or counts inside a range?

If yes, Sliding Window is likely a strong candidate.

---

## Common Interview Keywords

Look for phrases like:

- "longest substring";
- "shortest substring";
- "maximum length";
- "minimum length";
- "contiguous";
- "subarray";
- "window";
- "at most";
- "no more than";
- "contains all characters".

---

## Common Sliding Window Variations

### Fixed-Size Window

The window size stays constant while moving through the input.

Example:

```text
Array:
[2, 4, 6, 8, 10]

Window size: 3

[2, 4, 6]
   [4, 6, 8]
      [6, 8, 10]
```

Typical examples:

- Maximum Average Subarray I
- Maximum Number of Vowels in a Substring

---

### Variable-Size Window

The window grows and shrinks depending on whether the current range
satisfies the required condition.

Example:

```text
Expand:

[left ........ right]

Shrink:

   [left ... right]
```

Typical examples:

- Longest Substring Without Repeating Characters
- Minimum Size Subarray Sum
- Minimum Window Substring

---

### Sliding Window + Hash Map

Combine a sliding window with a hash map when you need to track
frequencies or occurrences.

Typical examples:

- Longest Repeating Character Replacement
- Permutation in String
- Minimum Window Substring

The hash map stores information about the current window.

---

## Complexity

Most Sliding Window solutions have:

- Time complexity: `O(n)`
- Space complexity: `O(k)`

where `k` is the amount of data stored inside the window.

For problems involving character frequencies, `k` is often a constant
such as the alphabet size.

---

## Learning Goals

After completing this pattern, you should be able to:

- recognize substring and subarray problems quickly;
- choose between fixed and variable-size windows;
- maintain window state efficiently;
- use hash maps with sliding windows;
- explain why the solution runs in linear time.

---

## Progress

- [ ] 643. Maximum Average Subarray I
- [ ] 1456. Maximum Number of Vowels in a Substring of Given Length
- [ ] 3. Longest Substring Without Repeating Characters
- [ ] 209. Minimum Size Subarray Sum
- [ ] 424. Longest Repeating Character Replacement
- [ ] 567. Permutation in String
- [ ] 76. Minimum Window Substring
