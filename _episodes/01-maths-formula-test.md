---
title: Python Fundamentals
teaching: 20
exercises: 10
questions:
- "What basic data types can I work with in Python?"
- "How can I create a new variable in Python?"
- "How do I use a function?"
- "Can I change the value associated with a variable after I create it?"
- 
objectives:
- "Assign values to variables."
keypoints:
- "Basic data types in Python include integers, strings, and floating-point numbers."
- "Use `variable = value` to assign a value to a variable in order to record it in memory."
- "Variables are created on demand whenever a value is assigned to them."
- "Use `print(something)` to display the value of `something`."
- "Built-in functions are always available to use."
usemathjax: true
use_math: true
{% include mathjax.html %}
{% if page.usemathjax %}
<script type="text/javascript" async
 src="https://cdn.mathjax.org/mathjax/latest/MathJax.js?config=TeX-MML-AM_CHTML">
  </script>
{% end if %}
---

$$
K(a,b) = \int \mathcal{D}x(t) \exp(2\pi i S[x]/\hbar)
$$

$$E=mc^2$$

Let's test some inline math \$$x, y, x_1, y_1$$.

Now a inline math with special character: $$|\psi\rangle$$, $$x'$$, $$x^\*$$.

Test a display math:
$$
   |\psi_1\rangle = a|0\rangle + b|1\rangle
$$
Is it O.K.?

Test a display math with equation number:
\begin{equation}
   |\psi_1\rangle = a|0\rangle + b|1\rangle
\end{equation}
Is it O.K.?

Test a display math with equation number:

$$
  \begin{align}
    |\psi_1\rangle &= a|0\rangle + b|1\rangle \\\\
    |\psi_2\rangle &= c|0\rangle + d|1\rangle
  \end{align}
$$

Is it O.K.?

And test a display math without equaltion number:

$$
  \begin{align\*}
    |\psi_1\rangle &= a|0\rangle + b|1\rangle \\\\
    |\psi_2\rangle &= c|0\rangle + d|1\rangle
  \end{align\*}
$$

Is it O.K.?

Test a display math with equation number:
\begin{align}
    |\psi_1\rangle &= a|0\rangle + b|1\rangle \\\\
    |\psi_2\rangle &= c|0\rangle + d|1\rangle
\end{align}
Is it O.K.?

And test a display math without equaltion number:
\begin{align\*}
    |\psi_1\rangle &= a|0\rangle + b|1\rangle \\\\
    |\psi_2\rangle &= c|0\rangle + d|1\rangle
\end{align\*}
Is it O.K.?

$$a^2 + b^2 = c^2$$

$$ x = {-b \pm \sqrt{b^2-4ac} \over 2a} $$



$$\begin{eqnarray}
x' &=& &x \sin\phi &+& z \cos\phi \\
z' &=& - &x \cos\phi &+& z \sin\phi \\
\end{eqnarray}$$.