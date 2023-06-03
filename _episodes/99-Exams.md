---
title:  Exams

questions:
- ""
objectives:
- Old exams questions and answers
---

## Mid-Semester Exam Ac.Year 2022/23
> ### 1. Show that if $$f$$ and $$g$$ are bounded functions, both integrable on the interval $$[a,b]$$, then so is $$f+g$$.
> >
> > ## Solution
> >
> >$$\textbf{Proof:}$$
> >1. Boundedness of $$f$$ and $$g$$:\
> >Since $$f$$ and $$g$$ are bounded functions on $$[a, b]$$, there exist constants $$M_1$$ and $$M_2$$ such that $$|f(x)| \leq M_1$$ and $$|g(x)| \leq M_2$$ for all $$x$$ in $$[a, b]$$. Let $$M = \max(M_1, M_2)$$. Then, we have $$|f(x) + g(x)| \leq |f(x)| + |g(x)| \leq M_1 + M_2 = M$$ for all $$x$$ in $$[a, b]$$. Therefore, $$f + g$$ is also bounded on $$[a, b]$$.\
> >2. Integrability of $$f$$ and $$g$$:\
> >Since $$f$$ and $$g$$ are integrable on $$[a, b]$$, they are both Riemann integrable. By definition, this means that for any given $$\epsilon > 0$$, there exist partitions $$P_1$$ and $$P_2$$ of $$[a, b]$$ such that the upper and lower Riemann sums of $$f$$ and $$g$$ satisfy:\
> >$$U(f, P_1) - L(f, P_1) < \frac{\epsilon}{2}$$
$$U(g, P_2) - L(g, P_2) < \frac{\epsilon}{2}$$\
> >Now, let $$P = P_1 \cup P_2$$ be a common refinement of $$P_1$$ and $$P_2$$. By the properties of Riemann sums, we have:\
> >$$U(f + g, P) - L(f + g, P) = U(f, P) + U(g, P) - L(f, P) - L(g, P)$$\
> >Since $$P$$ is a common refinement of $$P_1$$ and $$P_2$$, we can conclude that:\
> >$$U(f, P) - L(f, P) \leq U(f, P_1) - L(f, P_1) < \frac{\epsilon}{2}$$\
> >$$U(g, P) - L(g, P) \leq U(g, P_2) - L(g, P_2) < \frac{\epsilon}{2}$$\
> >Therefore, combining the above inequalities, we get:\
> >$$U(f + g, P) - L(f + g, P) < \frac{\epsilon}{2} + \frac{\epsilon}{2} = \epsilon$$\
> >This shows that $$f + g$$ is Riemann integrable on $$[a, b]$$, i.e., $$f + g$$ is integrable.\
> >Hence, we have demonstrated that if $$f$$ and $$g$$ are bounded functions, both integrable on the interval $$[a, b]$$, then their sum $$f + g$$ is also bounded and integrable on the same interval.
>{: .solution}
{: .challenge}
> ### 8.2.7 $$\int \frac{1}{x^2-1} dx$$
> >
> > ## Solution
> > 
 > >To solve the integral $$\int \frac{1}{x^2 - 1} \, dx$$, we can decompose the denominator $$x^2 - 1$$ into its factors using partial fraction decomposition. Let's start by factoring the denominator:\
> >$$x^2 - 1 = (x - 1)(x + 1)$$\
> >The factors $$(x - 1)$$ and $$(x + 1)$$ are linear factors, so we can write the given fraction as:\
> >$$\frac{1}{x^2 - 1} = \frac{A}{x - 1} + \frac{B}{x + 1}$$\
> >To determine the values of $$A$$ and $$B$$, we can use algebraic manipulation or the method of coefficients. I will use the method of coefficients here.\
> >Multiplying both sides of the equation by $$x^2 - 1$$, we have:\
> >$$1 = A(x + 1) + B(x - 1)$$\
> >Expanding and collecting like terms, we get:\
> >$$1 = (A + B)x + (A - B)$$\
> >Equating the coefficients of like powers of $$x$$, we have the following system of equations:\
> >$$A + B = 0$$    (1)\
> >$$A - B = 1$$    (2)\
> >Solving the system of equations, we find $$A = \frac{1}{2}$$ and $$B = -\frac{1}{2}$$.\
> >Now, we can rewrite the integral using the partial fraction decomposition:\
> >$$\int \frac{1}{x^2 - 1} \, dx = \int \left(\frac{\frac{1}{2}}{x - 1} - \frac{\frac{1}{2}}{x + 1}\right) \, dx$$\
> >Integrating each term separately, we have:\
> >$$\frac{1}{2} \int \frac{1}{x - 1} \, dx - \frac{1}{2} \int \frac{1}{x + 1} \, dx$$\
> >Using the natural logarithm function, we can write:\
> >$$\frac{1}{2} \ln|x - 1| - \frac{1}{2} \ln|x + 1| + C$$\
> >Therefore, the final result of the integral is:\
> >$$\int \frac{1}{x^2 - 1} \, dx = \frac{1}{2} \ln|x - 1| - \frac{1}{2} \ln|x + 1| + C$$
>{: .solution}
{: .challenge}
## Final Semester Exam
> Let $$f$$ be defined on all of $$R$$. For each real number $$c$$, we define the translated function $$f_c$$ by: $$f_c(x) = f (x − c)$$. Suppose that $$f$$ is integrable on all bounded intervals. Show that: $$\int_{a}^{b} f = \int_{a+c}^{b+c} f_c$$ for all $$a$$ and $$b$$.\
> >
> >## Solution
> >
> >To show that $$\int_a^b f = \int_{a+c}^{b+c} f_c$$ for all $$a$$ and $$b$$, we need to demonstrate that the integrals of the two functions are equal.\
> >First, let's consider the integral of $$f$$ over the interval $$[a, b]$$. We can define a new variable $$u$$ such that $$u = x - c$$. Rearranging the equation, we have $$x = u + c$$.\
> >When $$x = a$$, $$u + c = a$$, and when $$x = b$$, $$u + c = b$$. This means that the new interval of integration for the function $$f_c$$ will be $$[u + c]_a^b$$.\
> >Now, let's substitute $$u + c$$ for $$x$$ in the expression for $$f_c$$. We get $$f_c(u + c) = f(u)$$. The integrand for $$f_c$$ is essentially the same as $$f$$, but the variable has been changed to $$u$$.\
> >Therefore, we can rewrite the integral of $$f_c$$ over the interval $$[a + c, b + c]$$ as $$\int_{a + c}^{b + c} f_c = \int_a^b f(u) du$$.\
> >Now, we have shown that the integral of $$f_c$$ over the interval $$[a + c, b + c]$$ is equivalent to the integral of $$f$$ over the interval $$[a, b]$$, but with a change of variable from $$x$$ to $$u$$.\
> >Since the choice of variable does not affect the value of the integral, we can conclude that $$\int_a^b f = \int_{a+c}^{b+c} f_c$$ for all $$a$$ and $$b$$.\
> >Thus, we have established the desired result.
>{: .solution}
{: .challenge}
> ### $$x^4 + 4$$
> >
> > ## Solution
> >
> >The real factorization of $$x^4 + 4$$ into irreducible quadratic factors is needed to calculate the integral $$\int \frac{1}{x^4 + 4} \, dx$$. We can obtain the factorization using complex numbers by noting that the roots of $$x^4 + 4 = 0$$ are the four complex numbers $$w_1 = e^{i\pi/4}$$, $$w_2 = e^{3i\pi/4}$$, $$w_3 = e^{5i\pi/4}$$, and $$w_4 = e^{7i\pi/4}$$.\
> >To compute the integral, we use partial fraction decomposition. The integrand can be expressed as:\
> >$$\frac{1}{x^4 + 4} = \frac{\frac{1}{4}}{x^2 + 2x\sqrt{2} + 2} - \frac{\frac{1}{4}}{x^2 - 2x\sqrt{2} + 2}$$\
> >Next, we complete the square in the denominators:\
> >$$x^2 + 2x\sqrt{2} + 2 = (x + \sqrt{2})^2 + 2$$\
> >$$x^2 - 2x\sqrt{2} + 2 = (x - \sqrt{2})^2 + 2$$\
> >Using the substitutions $$u = x + \sqrt{2}$$ and $$v = x - \sqrt{2}$$, the integral becomes:\
> >$$\int \frac{1}{x^4 + 4} \, dx = \frac{1}{4} \int \frac{1}{(x + \sqrt{2})^2 + 2} \, dx - \frac{1}{4} \int \frac{1}{(x - \sqrt{2})^2 + 2} \, dx$$\
> >Applying the integral formulas for $$\frac{1}{u^2 + a^2}$$, the integrals can be evaluated as:\
> >$$\frac{1}{4\sqrt{2}} \left(\frac{1}{\sqrt{2}}\arctan\left(\frac{x + \sqrt{2}}{\sqrt{2}}\right)\right) - \frac{1}{4\sqrt{2}} \left(\frac{1}{\sqrt{2}}\arctan\left(\frac{x - \sqrt{2}}{\sqrt{2}}\right)\right) + C$$\
> >Simplifying further, we have:\
> >$$\frac{1}{8} \left(\arctan\left(\frac{x + \sqrt{2}}{\sqrt{2}}\right) - \arctan\left(\frac{x - \sqrt{2}}{\sqrt{2}}\right)\right) + C$$\
> >Therefore, the integral $$\int \frac{1}{x^4 + 4} \, dx$$ can be expressed as $$\frac{1}{8} \left(\arctan\left(\frac{x + \sqrt{2}}{\sqrt{2}}\right) - \arctan\left(\frac{x - \sqrt{2}}{\sqrt{2}}\right)\right) + C$$, where $$C$$ is the constant of integration.
>{: .solution}
{: .challenge}
> ### Suppose that  f  is bounded on $$[a,b]$$  and for each $$ε > 0$$, it is integrable on $$[a + ε,b]$$. Show that  $$f$$  is integrable on $$[a,b]$$ and $$\lim_{ε→0+}\int_{a+ε}^{b} f =   \int_{a}^{b} f$$. 
> >
> > ## Solution
> >
> > Suppose that $$f$$ is bounded on $$[a, b]$$ and for each $$\varepsilon > 0$$, it is integrable on $$[a + \varepsilon, b]$$. Show that $$f$$ is integrable on $$[a, b]$$ and
$$\lim_{\varepsilon \to 0^+} \int_{a+\varepsilon}^b f = \int_a^b f.
$$\
Since $$f$$ is bounded on $$[a, b]$$, there exists a constant $$M$$ such that $$|f(x)| \leq M$$ for all $$x \in [a, b]$$. This implies that $$|f(x)|$$ is bounded on $$[a, b]$$.\
> >Now, for any given $$\varepsilon > 0$$, we are given that $$f$$ is integrable on $$[a + \varepsilon, b]$$. This means that there exists a partition $$\mathcal{P}$$ of $$[a + \varepsilon, b]$$ such that the upper and lower Riemann sums of $$f$$ on $$\mathcal{P}$$ differ by at most $$\varepsilon$$.\
> >Let $$\mathcal{P}'$$ be a refinement of $$\mathcal{P}$$ obtained by adding the point $$a$$ to the partition. Note that $$\mathcal{P}'$$ is a partition of $$[a, b]$$.\
> >Using the properties of integrability, we have:\
> >$$
L(f, \mathcal{P}') \leq L(f, \mathcal{P}) \leq U(f, \mathcal{P}) \leq U(f, \mathcal{P}')
$$\
> >where $$L(f, \mathcal{P}')$$ and $$U(f, \mathcal{P}')$$ denote the lower and upper Riemann sums of $$f$$ on $$\mathcal{P}'$$, respectively.\
> >Since $$\mathcal{P}$$ and $$\mathcal{P}'$$ differ by only one point, the difference between the upper and lower Riemann sums of $$f$$ on $$\mathcal{P}'$$ and $$\mathcal{P}$$ is at most $$M \cdot \varepsilon$$ (as $$|f(x)| \leq M$$ for all $$x \in [a, b]$$).\
> >Therefore, we have:\
> >$$L(f, \mathcal{P}') \leq L(f, \mathcal{P}) \leq U(f, \mathcal{P}) \leq U(f, \mathcal{P}') \leq L(f, \mathcal{P}') + M \cdot \varepsilon
$$\
> >Taking the limit as $$\varepsilon$$ approaches 0, we have:\
> >$$
\lim_{\varepsilon \to 0^+} L(f, \mathcal{P}') \leq \lim_{\varepsilon \to 0^+} L(f, \mathcal{P}) \leq \lim_{\varepsilon \to 0^+} U(f, \mathcal{P}) \leq \lim_{\varepsilon \to 0^+} U(f, \mathcal{P}') \leq \lim_{\varepsilon \to 0^+} L(f, \mathcal{P}') + \lim_{\varepsilon \to 0^+} M \cdot \varepsilon$$\
> >Since $$f$$ is integrable on $$[a + \varepsilon, b]$$ for every $$\varepsilon > 0$$, the limit of the lower and upper Riemann sums as $$\varepsilon$$ approaches 0 is equal to the integral of $$f$$ over $$[a, b]$$. Therefore:\
> >$$\int_a^b f \leq \lim_{\varepsilon \to 0^+} \int_{a + \varepsilon}^b f \leq \int_a^b f \leq \lim_{\varepsilon \to 0^+} \int_{a + \varepsilon}^b f + \lim_{\varepsilon \to 0^+} M \cdot \varepsilon$$\
> >Since $$\lim_{{\varepsilon \to 0^+}} M \cdot \varepsilon = 0$$ (as $$\varepsilon$$ approaches 0), we have:\
> >$$\int_a^b f \leq \lim_{\varepsilon \to 0^+} \int_{a + \varepsilon}^b f \leq \int_a^b f$$\
> >Hence, $$\lim_{\varepsilon \to 0^+} \int_{a + \varepsilon}^b f = \int_a^b f$$, which shows that $$f$$ is integrable on $$[a, b]$$ and satisfies the desired limit property.
>{: .solution}
{: .challenge}