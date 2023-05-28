---
title:  Exams

questions:
- ""
objectives:
- Old exams questions and answers
---

## Mid-Semester Exam Ac.Year 2022/23
> ### Show that if $$f$$ and $$g$$ are bounded functions, both integrable on the interval $$[a,b]$$, then so is $$f+g$$.
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
> >$$\int \frac{1}{x^2 - 1} \, dx = \frac{1}{2} \ln|x - 1| - \frac{1}{2} \ln|x + 1| + C$$ -->
>{: .solution}
{: .challenge}