# LeetCode Pattern: Tree DFS

## Overview

The Tree DFS pattern is used to explore binary trees by recursively
visiting nodes and processing their children.

The main idea is to go as deep as possible along one branch before
returning and exploring other branches.

Tree DFS is commonly used for:

- calculating tree properties;
- searching paths;
- validating tree structure;
- comparing trees;
- processing nodes recursively.

There are three common DFS traversal orders:

- preorder: node → left → right;
- inorder: left → node → right;
- postorder: left → right → node.

In C++, this pattern commonly uses:

- recursion;
- `std::stack`;
- binary tree node pointers.

The key skill is recognizing when a tree problem can be solved by defining
the answer for one node and combining results from its children.

---

## Practice Problems

Solve these problems in order. The early problems introduce basic tree
traversal, while the later ones require more complex recursive reasoning.

### Easy

- **104. Maximum Depth of Binary Tree**  
  <https://leetcode.com/problems/maximum-depth-of-binary-tree/>

  Recursively calculate the longest path from the root to a leaf.

- **100. Same Tree**  
  <https://leetcode.com/problems/same-tree/>

  Compare two trees by recursively checking corresponding nodes.

- **226. Invert Binary Tree**  
  <https://leetcode.com/problems/invert-binary-tree/>

  Swap left and right children recursively.

- **101. Symmetric Tree**  
  <https://leetcode.com/problems/symmetric-tree/>

  Check whether the left and right subtrees mirror each other.

### Medium

- **98. Validate Binary Search Tree**  
  <https://leetcode.com/problems/validate-binary-search-tree/>

  Verify that every node satisfies BST ordering rules.

- **102. Binary Tree Level Order Traversal**  
  <https://leetcode.com/problems/binary-tree-level-order-traversal/>

  Traverse the tree level by level using BFS concepts.

- **105. Construct Binary Tree from Preorder and Inorder Traversal**  
  <https://leetcode.com/problems/construct-binary-tree-from-preorder-and-inorder-traversal/>

  Rebuild a tree using traversal information.

- **236. Lowest Common Ancestor of a Binary Tree**  
  <https://leetcode.com/problems/lowest-common-ancestor-of-a-binary-tree/>

  Use recursion to find the shared ancestor of two nodes.

### Hard

- **124. Binary Tree Maximum Path Sum**  
  <https://leetcode.com/problems/binary-tree-maximum-path-sum/>

  Combine subtree results to calculate the best path through a tree.

- **297. Serialize and Deserialize Binary Tree**  
  <https://leetcode.com/problems/serialize-and-deserialize-binary-tree/>

  Convert a tree into a format that can be stored and reconstructed.

---

## Pattern Recognition Checklist

Ask yourself:

- Is the input a binary tree?
- Can the problem be solved by looking at each node once?
- Can the answer for a node be built from answers of its children?
- Do I need information from subtrees?
- Does recursion naturally describe the solution?

If yes, Tree DFS is likely a strong candidate.

---

## Common Interview Keywords

Look for phrases like:

- "binary tree";
- "subtree";
- "depth";
- "height";
- "path";
- "ancestor";
- "leaf";
- "validate";
- "traverse".

---

## Common Tree DFS Variations

### Preorder DFS

Visit the node before visiting children.

Order:

```text
Node
Left subtree
Right subtree
```

Typical examples:

- Serialize and Deserialize Binary Tree
- Construct Binary Tree

---

### Inorder DFS

Visit the left subtree, then the node, then the right subtree.

Order:

```text
Left subtree
Node
Right subtree
```

For a Binary Search Tree, inorder traversal produces sorted values.

Typical examples:

- Validate Binary Search Tree

---

### Postorder DFS

Visit children before processing the current node.

Order:

```text
Left subtree
Right subtree
Node
```

This is useful when the parent depends on information from children.

Typical examples:

- Maximum Depth of Binary Tree
- Binary Tree Maximum Path Sum
- Lowest Common Ancestor

---

## Complexity

Most Tree DFS solutions have:

- Time complexity: `O(n)`

because every node is visited once.

Space complexity depends on the tree height:

- Balanced tree: `O(log n)`
- Worst case tree: `O(n)`

The space is used by the recursion stack.

---

## Learning Goals

After completing this pattern, you should be able to:

- recognize recursive tree problems;
- choose the correct DFS traversal order;
- define recursive states for tree nodes;
- solve subtree-based problems;
- analyze recursion depth and complexity.

---

## Progress

- [ ] 104. Maximum Depth of Binary Tree
- [ ] 100. Same Tree
- [ ] 226. Invert Binary Tree
- [ ] 101. Symmetric Tree
- [ ] 98. Validate Binary Search Tree
- [ ] 102. Binary Tree Level Order Traversal
- [ ] 105. Construct Binary Tree from Preorder and Inorder Traversal
- [ ] 236. Lowest Common Ancestor of a Binary Tree
- [ ] 124. Binary Tree Maximum Path Sum
- [ ] 297. Serialize and Deserialize Binary Tree
