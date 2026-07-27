# Data Structures & Algorithms

## What is this repo all about?

This repository contains explanations of 20 basic and 10 advanced topics.
The topics are organized from easiest to hardest. One file covers one pattern.
Each file contains explanations, examples, links to LeetCode problems, and
time and space complexity analysis for each case — everything one might need
to train pattern recognition skill.
You can use this repository as both a roadmap and a quick reference.

---

## What are LeetCode patterns?

**LeetCode patterns are common problem-solving techniques that appear repeatedly across coding interview problems.**

When you solve many LeetCode problems, you start noticing that a large number of them are not completely new problems. Instead, they are variations of the same underlying ideas and algorithms.

For example:

- Find two numbers that add up to a target value.
- Determine whether an array contains duplicates.
- Count how many times elements appear.
- Find pairs or groups of elements with certain properties.

Although these problems may look different, they often share the same solution strategy:

> Use a hash table to store information while scanning the data.

This is a **pattern**:

> **Hash Table / Frequency Counting**

Instead of memorizing hundreds of individual solutions, effective interview preparation focuses on learning a smaller set of fundamental patterns and understanding when to apply each one.

---

## Why do interviewers care about patterns?

During a real software engineering interview, interviewers are not testing whether you memorized a specific LeetCode problem.

They are evaluating your ability to:

1. Understand an unfamiliar problem quickly.
2. Identify the underlying structure of the problem.
3. Choose an appropriate algorithm and data structure.
4. Implement the solution correctly.
5. Explain your reasoning clearly.

Strong candidates usually do not think:

> "I remember LeetCode problem #217. I will reproduce the solution."

Instead, they think:

> "This is a membership lookup problem. I need fast access to previously seen values, so a hash set gives me O(1) average lookup time."

That ability to recognize the right approach quickly is what makes someone effective during technical interviews.

---

## What is "pattern recognition skill"?

**Pattern recognition skill is the ability to look at a new problem and quickly identify the underlying algorithmic technique that can solve it.**

It is the process of connecting a new problem to a familiar concept based on its characteristics and constraints.

A beginner often sees a problem like:

> "Given an array of numbers, find something..."

and thinks:

> "I need to figure out this specific problem from scratch."

An experienced engineer looks for clues:

- "I need fast lookup" → **Hash Table**
- "I need to compare values from both ends" → **Two Pointers**
- "I need the longest or shortest valid range" → **Sliding Window**
- "The data is sorted and I need efficient searching" → **Binary Search**
- "I need to explore every node or connection" → **DFS/BFS**

The difference is not about memorizing more problems. It is about developing the ability to recognize the structure behind the problem.

Pattern recognition is built through deliberate practice:

- solving problems,
- analyzing why a solution works,
- grouping problems by technique,
- and repeatedly applying the same patterns in different contexts.

Over time, unfamiliar problems start becoming familiar because you begin seeing the algorithms hidden underneath the problem statement.

---

## How to master pattern recognition skill?

Solving LeetCode problems is not only about learning algorithms and data
structures. The most important skill developed through consistent practice
is the ability to recognize patterns and systematically approach unfamiliar
problems.

A strong software engineer does not immediately jump into coding. Instead, they
follow a structured problem-solving process:

1. **Understand the problem completely**
   - Read the problem statement carefully.
   - Identify what the problem is asking for.
   - Restate the problem in your own words.
   - Clarify any ambiguities before writing code.

2. **Collect requirements and constraints**
   - Analyze input size and possible values.
   - Pay attention to constraints because they often determine the correct
     algorithm.
   - Ask questions such as:
     - How large can the input be?
     - Is the data sorted?
     - Can there be duplicates?
     - Are negative values possible?
     - Are there memory limitations?
     - Do we need the fastest possible solution, or is a simpler approach enough?

3. **Think out loud**

   During technical interviews, explaining your thought process is extremely
   important. Interviewers are not only evaluating the final solution — they
   want to understand how you approach problems.

   Good candidates communicate their reasoning:

   > "A brute-force solution would compare every element with every other
   > element, which would be O(n²). Since we need faster lookups, I am thinking
   > about using a hash table to reduce the lookup time."

   Thinking out loud helps:
   - demonstrate your problem-solving approach,
   - receive hints from the interviewer when needed,
   - catch mistakes before they become implementation problems.

4. **Identify the underlying pattern**

   Instead of treating every problem as completely unique, look for similarities
   with problems you have already solved.

   Ask yourself:
   - Have I seen this type of problem before?
   - What data structure would make this operation efficient?
   - Is this a lookup problem?
   - Is this a searching problem?
   - Is this about maintaining a range or window?
   - Is this about exploring relationships between nodes?
   - Does this require remembering previous states?

   Examples:
   - Fast lookup → **Hash Table**
   - Comparing elements from both ends → **Two Pointers**
   - Finding a range satisfying conditions → **Sliding Window**
   - Searching sorted data → **Binary Search**
   - Exploring connected structures → **DFS/BFS**
   - Making decisions based on previous results → **Dynamic Programming**

5. **Choose an approach and validate it**

   Before writing code, pause and ask:
   - Does this algorithm solve the problem correctly?
   - Does it handle all constraints?
   - What is the time complexity?
   - What is the space complexity?
   - Is there a simpler or more optimal solution?

   A useful habit is to challenge your own idea:

   > "Am I solving the right problem?"

   > "Am I using the right data structure?"

   > "Could this fail on a corner case?"

6. **Consider edge cases and corner cases**

   Many incorrect solutions fail not because the main algorithm is wrong,
   but because they ignore unusual inputs.

   Always consider cases such as:
   - Empty input.
   - A single element.
   - Duplicate values.
   - Extremely large inputs.
   - Minimum and maximum values.
   - Already sorted data.
   - Reverse-sorted data.
   - Unexpected combinations of values.

7. **Implement carefully and test mentally**

   Before running the code, simulate it manually:
   - Walk through a small example.
   - Track variables step by step.
   - Check whether each operation does what you expect.
   - Verify that the algorithm reaches the correct result.

   This habit improves both coding accuracy and debugging skills.

8. **Review and extract the pattern**

   After solving a problem, do not stop at "accepted."

   Ask:
   - Why did this solution work?
   - What clues suggested this pattern?
   - What other problems could use the same approach?
   - What mistakes did I make?
   - How can I recognize this pattern faster next time?

The goal is not to memorize hundreds of LeetCode solutions.

The goal is to develop the ability to recognize the structure of a problem,
select the appropriate algorithm, and confidently explain your reasoning.
