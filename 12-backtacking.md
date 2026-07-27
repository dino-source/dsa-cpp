# LeetCode Pattern: Backtracking

## Overview

The Backtracking pattern is used to explore all possible solutions by
making choices, exploring the result, and undoing those choices.

The main idea is:

1. Make a choice.
2. Explore the next step recursively.
3. Undo the choice.
4. Try another possibility.

Backtracking is commonly used for:

- generating all combinations;
- generating all permutations;
- solving constraint problems;
- exploring decision trees;
- finding valid configurations.

In C++, this pattern commonly uses:

- recursion;
- `std::vector`;
- `std::string`;
- `std::unordered_set`.

The key skill is recognizing when a problem asks for all possible answers
or requires trying different choices until a valid solution is found.

---

## Practice Problems

Solve these problems in order. The early problems introduce basic
recursive exploration, while the later ones require pruning and stronger
constraint handling.

### Easy

- **78. Subsets**  
  <https://leetcode.com/problems/subsets/>

  Generate all possible subsets using recursive choices.

- **1863. Sum of All Subset XOR Totals**  
  <https://leetcode.com/problems/sum-of-all-subset-xor-totals/>

  Explore all subsets and calculate their XOR values.

### Medium

- **46. Permutations**  
  <https://leetcode.com/problems/permutations/>

  Generate all possible orderings of elements.

- **39. Combination Sum**  
  <https://leetcode.com/problems/combination-sum/>

  Explore combinations while allowing repeated choices.

- **17. Letter Combinations of a Phone Number**  
  <https://leetcode.com/problems/letter-combinations-of-a-phone-number/>

  Build all possible strings from digit mappings.

- **22. Generate Parentheses**  
  <https://leetcode.com/problems/generate-parentheses/>

  Construct valid combinations while maintaining constraints.

- **79. Word Search**  
  <https://leetcode.com/problems/word-search/>

  Use DFS and backtracking to search through a grid.

### Hard

- **51. N-Queens**  
  <https://leetcode.com/problems/n-queens/>

  Place queens while maintaining row and diagonal constraints.

- **37. Sudoku Solver**  
  <https://leetcode.com/problems/sudoku-solver/>

  Use backtracking with constraint checking to solve a puzzle.

---

## Pattern Recognition Checklist

Ask yourself:

- Do I need to generate all possible solutions?
- Am I choosing elements step by step?
- Can I undo a previous decision and try another option?
- Does the problem have constraints that can prune invalid paths?
- Does the solution naturally form a decision tree?

If yes, Backtracking is likely a strong candidate.

---

## Common Interview Keywords

Look for phrases like:

- "all combinations";
- "all permutations";
- "generate";
- "find all";
- "possible arrangements";
- "choose";
- "place";
- "partition";
- "constraint".

---

## Common Backtracking Variations

### Subsets

Choose whether to include each element.

Example:

```text
Input:

[1, 2, 3]

Choices:

Take 1
Skip 1
Take 2
Skip 2
Take 3
Skip 3
```

Typical examples:

- Subsets
- Combination Sum

---

### Permutations

Choose an unused element at every step.

Example:

```text
[1, 2, 3]

Results:

[1,2,3]
[1,3,2]
[2,1,3]
...
```

Typical examples:

- Permutations
- Letter Combinations of a Phone Number

---

### Constraint Backtracking

Build a solution while checking whether the current state is valid.

Example:

```text
Place a value.

Check constraints.

If invalid:
    undo.

Otherwise:
    continue.
```

Typical examples:

- N-Queens
- Sudoku Solver
- Word Search

---

## Complexity

Backtracking solutions usually have exponential complexity because they
explore many possible states.

Common complexities:

- Subsets: `O(2^n)`
- Permutations: `O(n!)`
- Combination problems: depends on constraints

Space complexity:

- `O(n)`

for the recursion stack and current path.

Pruning invalid branches is the main technique used to improve performance.

---

## Learning Goals

After completing this pattern, you should be able to:

- recognize decision tree problems;
- implement recursive exploration;
- correctly add and remove choices;
- use pruning to reduce search space;
- solve combinations, permutations, and constraint problems.

---

## Progress

- [ ] 78. Subsets
- [ ] 1863. Sum of All Subset XOR Totals
- [ ] 46. Permutations
- [ ] 39. Combination Sum
- [ ] 17. Letter Combinations of a Phone Number
- [ ] 22. Generate Parentheses
- [ ] 79. Word Search
- [ ] 51. N-Queens
- [ ] 37. Sudoku Solver
