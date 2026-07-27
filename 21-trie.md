# LeetCode Pattern: Trie (Prefix Tree)

## Overview

The Trie, also known as a Prefix Tree, is a specialized tree data
structure for storing and searching strings efficiently.

Unlike a hash table, which stores complete keys, a Trie stores one
character per node. This allows common prefixes to be shared among
multiple words.

A Trie is especially useful for:

- prefix searches;
- autocomplete systems;
- spell checking;
- dictionary lookups;
- word search problems.

The most common operations are:

- **Insert** a word;
- **Search** for a complete word;
- **StartsWith** a prefix.

In C++, a Trie is commonly implemented using:

- `struct` or `class` for trie nodes;
- `std::array<TrieNode*, 26>` for lowercase English letters;
- `std::unordered_map<char, TrieNode*>` for arbitrary character sets;
- recursion or iteration.

The key skill is recognizing when repeated prefix lookups are more
important than fast whole-word lookups.

---

## Practice Problems

Solve these problems in order. The early problems introduce the core Trie
operations, while the later ones combine Tries with DFS and other
algorithms.

### Medium

- **208. Implement Trie (Prefix Tree)**  
  <https://leetcode.com/problems/implement-trie-prefix-tree/>

  Implement the basic Trie operations.

- **211. Design Add and Search Words Data Structure**  
  <https://leetcode.com/problems/design-add-and-search-words-data-structure/>

  Extend a Trie to support wildcard searches.

- **648. Replace Words**  
  <https://leetcode.com/problems/replace-words/>

  Replace words using the shortest matching dictionary prefix.

- **677. Map Sum Pairs**  
  <https://leetcode.com/problems/map-sum-pairs/>

  Store key-value pairs and compute prefix sums.

### Hard

- **212. Word Search II**  
  <https://leetcode.com/problems/word-search-ii/>

  Combine a Trie with DFS to efficiently search for multiple words in a
  grid.

- **336. Palindrome Pairs**  
  <https://leetcode.com/problems/palindrome-pairs/>

  Use a Trie to efficiently find matching word pairs.

- **745. Prefix and Suffix Search**  
  <https://leetcode.com/problems/prefix-and-suffix-search/>

  Design a data structure supporting both prefix and suffix queries.

---

## Pattern Recognition Checklist

Ask yourself:

- Am I searching many words with common prefixes?
- Do I need fast prefix lookups?
- Does the problem involve a dictionary of words?
- Am I repeatedly searching for strings?
- Would comparing entire strings be inefficient?

If yes, a Trie is likely a strong candidate.

---

## Common Interview Keywords

Look for phrases like:

- "dictionary";
- "prefix";
- "starts with";
- "autocomplete";
- "word search";
- "lexicon";
- "spell checker";
- "insert word";
- "search word".

---

## Common Trie Variations

### Standard Trie

Each node represents one character.

Example:

```text
Insert:

cat
car
can

Trie:

(root)
  |
  c
  |
  a
 /|\
t r n
```

Typical examples:

- Implement Trie
- Replace Words

---

### Trie with Wildcards

Support wildcard characters such as `.`.

Example:

```text
Search:

c.t

Matches:

cat
cot
cut
```

DFS is typically used whenever a wildcard is encountered.

Typical examples:

- Design Add and Search Words Data Structure

---

### Trie + DFS

Use a Trie to prune impossible searches while exploring a board.

Example:

```text
Board

o a a n
e t a e
i h k r
i f l v

Dictionary

oath
pea
eat
rain
```

Instead of searching for every word independently, DFS follows only
prefixes that exist in the Trie.

Typical examples:

- Word Search II

---

## Complexity

Let:

- `L` be the length of a word.

Typical operations:

- Insert: `O(L)`
- Search: `O(L)`
- Prefix search: `O(L)`

Space complexity:

- `O(total characters)`

because each Trie node stores one character and links to its children.

---

## Learning Goals

After completing this pattern, you should be able to:

- implement a Trie from scratch;
- understand how prefixes are shared;
- perform efficient prefix searches;
- combine Tries with DFS;
- choose between a Trie and a hash table.

---

## Progress

- [ ] 208. Implement Trie (Prefix Tree)
- [ ] 211. Design Add and Search Words Data Structure
- [ ] 648. Replace Words
- [ ] 677. Map Sum Pairs
- [ ] 212. Word Search II
- [ ] 336. Palindrome Pairs
- [ ] 745. Prefix and Suffix Search
