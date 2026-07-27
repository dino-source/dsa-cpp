# LeetCode Pattern: Advanced Math (Number Theory, Combinatorics, Probability)

## Overview

The Advanced Math pattern covers problems where the main challenge is not
a data structure or algorithmic technique, but mathematical reasoning.

These problems often require recognizing hidden structures, deriving
formulas, or applying mathematical properties to reduce complexity.

Common areas include:

- number theory;
- combinatorics;
- probability;
- modular arithmetic;
- mathematical proofs;
- counting techniques.

Unlike many LeetCode patterns, these problems often have a very short
implementation after the key observation is found.

The main skill is learning to ask:

```text
Can I derive a mathematical relationship instead of simulating the process?
```

In C++, these problems commonly use:

- `long long`;
- modular arithmetic;
- greatest common divisor (`std::gcd`);
- prime factorization;
- fast exponentiation;
- combinatorial formulas.

The key skill is recognizing when mathematics can replace brute force.

---

## Practice Problems

Solve these problems in order. The early problems introduce basic
mathematical techniques, while the later ones require deeper insights.

### Easy

- **204. Count Primes**  
  <https://leetcode.com/problems/count-primes/>

  Learn the Sieve of Eratosthenes for finding prime numbers efficiently.

- **231. Power of Two**  
  <https://leetcode.com/problems/power-of-two/>

  Use mathematical properties of binary representations.

- **326. Power of Three**  
  <https://leetcode.com/problems/power-of-three/>

  Recognize number properties without repeated multiplication.

- **202. Happy Number**  
  <https://leetcode.com/problems/happy-number/>

  Combine number manipulation with cycle detection.

### Medium

- **50. Pow(x, n)**  
  <https://leetcode.com/problems/powx-n/>

  Implement fast exponentiation using divide and conquer.

- **172. Factorial Trailing Zeroes**  
  <https://leetcode.com/problems/factorial-trailing-zeroes/>

  Use mathematical counting instead of calculating the factorial.

- **343. Integer Break**  
  <https://leetcode.com/problems/integer-break/>

  Apply mathematical optimization to maximize a product.

- **372. Super Pow**  
  <https://leetcode.com/problems/super-pow/>

  Combine modular arithmetic with exponentiation.

- **365. Water and Jug Problem**  
  <https://leetcode.com/problems/water-and-jug-problem/>

  Apply Bézout's identity and number theory.

### Hard

- **60. Permutation Sequence**  
  <https://leetcode.com/problems/permutation-sequence/>

  Use combinatorics to directly construct permutations.

- **149. Max Points on a Line**  
  <https://leetcode.com/problems/max-points-on-a-line/>

  Apply slope normalization and mathematical representation.

- **233. Number of Digit One**  
  <https://leetcode.com/problems/number-of-digit-one/>

  Count digit occurrences using positional mathematics.

- **780. Reaching Points**  
  <https://leetcode.com/problems/reaching-points/>

  Use reverse operations and mathematical reduction.

- **878. Nth Magical Number**  
  <https://leetcode.com/problems/nth-magical-number/>

  Combine binary search with least common multiple.

---

## Pattern Recognition Checklist

Ask yourself:

- Is brute force too slow, but the input has mathematical structure?
- Can I derive a formula?
- Does the problem involve counting possibilities?
- Are numbers, primes, divisibility, or factors involved?
- Can I solve the problem by reasoning backward?
- Is there a repeating mathematical pattern?

If yes, Advanced Math is likely a strong candidate.

---

## Common Interview Keywords

Look for phrases like:

- "count the number of ways";
- "maximum possible";
- "minimum operations";
- "prime";
- "factor";
- "divisible";
- "modulo";
- "permutation";
- "combination";
- "probability";
- "expected value".

---

## Common Number Theory Techniques

### Greatest Common Divisor (GCD)

The GCD finds the largest number that divides two integers.

Common uses:

- simplifying fractions;
- checking divisibility;
- solving mathematical constraints.

Example:

```cpp
std::gcd(a, b);
```

Typical examples:

- Water and Jug Problem
- Reaching Points

---

### Prime Numbers

Prime-related problems often require efficient preprocessing.

Common technique:

```text
Sieve of Eratosthenes
```

Instead of testing every number individually:

```text
O(n sqrt(n))
```

generate all primes up to `n`:

```text
O(n log log n)
```

Typical example:

- Count Primes

---

### Modular Arithmetic

Many problems involve very large numbers.

Instead of storing:

```text
100000000000000000000
```

we store:

```text
value % MOD
```

Common modulus:

```text
1,000,000,007
```

Important properties:

```text
(a + b) % MOD

(a * b) % MOD
```

Typical examples:

- Super Pow
- Nth Magical Number

---

### Fast Exponentiation

Instead of multiplying:

```text
x * x * x * x * x
```

use divide and conquer:

```text
x^n

=

(x^(n/2))^2
```

Complexity:

```text
O(log n)
```

Typical examples:

- Pow(x, n)
- Super Pow

---

## Common Combinatorics Techniques

### Counting Combinations

Many problems ask:

"How many ways can we choose elements?"

The key idea:

Order does not matter.

Example:

```text
Choose 3 elements from 10:

C(10, 3)
```

Used in:

- subset counting;
- probability;
- arrangements.

---

### Permutations

When order matters:

```text
ABC

and

BAC
```

are different.

Used in:

- sequence construction;
- ranking problems.

Typical example:

- Permutation Sequence

---

### Inclusion-Exclusion Principle

Used when counting overlapping groups.

The main idea:

```text
Count everything.

Subtract overlaps.

Add back double overlaps.
```

Typical examples:

- counting divisible numbers;
- probability problems.

---

## Common Probability Techniques

Probability problems usually require identifying:

- independent events;
- expected values;
- conditional probabilities;
- counting possible outcomes.

A common strategy:

1. Count all possible outcomes.
2. Count favorable outcomes.
3. Divide.

The hardest part is usually defining the correct sample space.

---

## Complexity

Advanced Math problems vary significantly.

Typical examples:

### Mathematical Formula Complexity

Time:

```text
O(1)
```

Example:

- Power of Two

---

### Fast Exponentiation Complexity

Time:

```text
O(log n)
```

Example:

- Pow(x, n)

---

### Prime Sieve Complexity

Time:

```text
O(n log log n)
```

Example:

- Count Primes

---

### Combinatorial Enumeration Complexity

Can be:

```text
O(n!)

or

O(2^n)
```

depending on the problem.

---

## Common Pitfalls

### Brute Force Counting

Many counting problems look simple but have enormous search spaces.

Instead of:

```text
Try every possibility
```

look for:

```text
Mathematical pattern
```

---

### Integer Overflow

Always consider:

```cpp
long long
```

especially with:

- multiplication;
- factorials;
- powers.

---

### Modulo Mistakes

Remember:

```text
(a + b) % MOD

≠

a + b % MOD
```

Apply modulo consistently.

---

### Floating Point Errors

Avoid `double` when exact integer arithmetic is possible.

Prefer:

- fractions;
- gcd reduction;
- integer calculations.

---

## Learning Goals

After completing this pattern, you should be able to:

- recognize mathematical shortcuts;
- apply number theory concepts;
- solve counting problems using combinatorics;
- use modular arithmetic correctly;
- derive solutions instead of simulating.

---

## Progress

- [ ] 204. Count Primes
- [ ] 231. Power of Two
- [ ] 326. Power of Three
- [ ] 202. Happy Number
- [ ] 50. Pow(x, n)
- [ ] 172. Factorial Trailing Zeroes
- [ ] 343. Integer Break
- [ ] 372. Super Pow
- [ ] 365. Water and Jug Problem
- [ ] 60. Permutation Sequence
- [ ] 233. Number of Digit One
- [ ] 780. Reaching Points
- [ ] 878. Nth Magical Number
