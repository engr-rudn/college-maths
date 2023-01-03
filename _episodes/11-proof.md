---
title: Proof
questions:
- "What basic?"
- "How can ?"
- "How do ?"
- "Can I ?"
objectives:
- "???"
- "???"
---
# Proof
A proof is a method of validating the truthfulness of a given statement

- [Proof](#proof)
  - [Topic overview](#topic-overview)
  - [Methods of proof](#methods-of-proof)
    - [Proof by deduction](#proof-by-deduction)
      - [Example:](#example)
    - [Proof by exhaustion](#proof-by-exhaustion)
      - [Example:](#example-1)
    - [Disproof by counter example](#disproof-by-counter-example)
      - [Example:](#example-2)

## Topic overview
Understand and use the structure of mathematical proof, proceeding from given assumptions through a series of logical steps to a conclusion
## Methods of proof
### Proof by deduction
Proving a statement through simplification and the application of well known mathematical principles (e.g $$x^2$$ will always be positive)
#### Example:

**Using completion of the square, prove that $$n^2-6n+10$$ is positive for all values of $$n$$**
>$$
n^2-6n+10 > 0
$$
>$$
n^2-6n > -10
$$
>$$
n^2-6n+9 > -1
$$
>$$
(n-3)^2 > -1
$$
>Because n is always squared, now value of n will result in $$
(n-3)^2
$$ being $$
\leq -1
$$

### Proof by exhaustion 
Proving a statement by exhaustion involes trying every possibility to validate a proof. This is only possible on functions with a countable domain and can be very inefficient for functions with a large domain.
#### Example:
**Supppose $$x$$ and $$y$$ are odd integers less than 7, prove that their sum is divisible by 2**
>Possible unique pairs:

| x             | 1   | 3   | 5   | 1   | 1   | 3   | 5   | 3   | 5   |
| ------------- | --- | --- | --- | --- | --- | --- | --- | --- | --- |
| y             | 1   | 3   | 5   | 3   | 5   | 1   | 1   | 5   | 3   |
| Sum           | 2   | 6   | 10  | 4   | 6   | 4   | 6   | 8   | 8   |
| Divisible by 2? | Yes | Yes | Yes | Yes | Yes | Yes | Yes | Yes | Yes |



### Disproof by counter example
Proving a statement to be false by applying basic mathematical principles.
#### Example:
**Show that the statement "$$n^2-n+1$$ is a prime number for all values of $$n$$" is untrue.**
*Method 1:*

$$
n = 5
$$

$$
5^2-5+1 = 25-5+1 = 21
$$

$$21$$ is not prime because 
$$
3*7 = 21
$$

*Method 2:*

$$
n^2-n+1 = n(n - 1) + 1
$$