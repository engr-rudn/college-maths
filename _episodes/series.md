---
layout: default
---

# Series

## Learning Targets

You should be able to
- [ ] Find Sums
- [ ] Write a series in summation / sigma notation

## Concepts / Definitions

A **series** is the sum of the terms of a sequence. A series can also be represented by using **summation notation**, which uses the Greek letter $\Sigma$ (capital *Sigma*) to denote the sum of a sequence in a condensed form, defined by a rule as shown.
$$\sum_{k=1}^{n} a_k = a_1 + a_2 + a_3 + ... + a_n$$

![Sum Series Formula](../assets/precalculus/series_1.jpg)

$$\sum_{k=1}^{5} 2k = 2(1) + 2(2) + 2(3) + 2(4) + 2(5)$$
and the sum would equal 30.

The **sum of a finite arithmetic series**: (Gauss Rule)
$\:\;S_n = a_1 \quad\qquad + (a_1 + d) + (a_1 + 2d) + ... + a_n$<br>
$\:\;S_n = a_n \quad\qquad + (a_n - d) + (a_n - 2d) + ... + a_1$<br>
___
$2S_n = (a_1 + a_n) + (a_1 + a_n) + (a_1 + a_n) + ... + (a_1 + a_n) _{(added\ n\ times)}$<br>
$2S_n = n(a_1 + a_n)$<br>
$\:\;S_n = \frac{n(a_1 + a_n)}{2},\ or\ S_n = n(\frac{a_1 + a_n}{2})$

The **sum of a finite geometric series**:
$\quad\qquad S_n = a_1 + a_1 r + a_1 r^2 + ... + a_1 r^{n-1}$<br>
$\,\;\;\quad -r S_n =\ \ - a_1 r - a_1 r^2 - ... - a_1 r^{n-1} - a_1 r^n$<br>
$S_n - \!\; r S_n = a - a_1 r^n$<br>
$S_n (1-r) = a_1 (1-r^n)$<br>
$\quad\qquad S_n = a_1 (\frac{1-r^n}{1-r})$

The **sum of an infinite geometric series** $S$ with common ratio $r$ and $\lvert r\rvert < 1$ is
$$S_{\infty} = \lim_{n \to \infty} a_1 (\frac{1-r^n}{1-r}),\ \lvert r\rvert < 1$$
$$S_{\infty} = \frac{a_1}{1-r}$$

### Other summation rules

$$\sum_{i=1}^{n} c = cn$$
$$\sum_{i=1}^{n} i = \frac{n (n+1)}{2}$$
$$\sum_{i=1}^{n} i^2 = \frac{n (n+1) (2n+1)}{6}$$
$$\sum_{i=1}^{n} i^3 = \frac{n^2 (n+1)^2}{4}$$
