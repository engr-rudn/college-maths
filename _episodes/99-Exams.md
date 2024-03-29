---
title:  Exams

questions:
- ""
objectives:
- Old exams questions and answers
---

## Mid-Semester Exam Ac.Year 2022/23
> #### Solve the following integrals. Show your detailed answers by writing the step-by-step analysis:
> #### a)  $$\int (x^2 \sin x)dx$$
> >
> > ## Solution
> > 
> >To solve the integral $$\left(\int (x^2 \sin x) \, dx\right)$$, we can use integration by parts. Let's apply the formula $$\left(\int u \, dv = uv - \int v \, du\right)$$ with $$\left(u = x^2\right)$$ and $$\left(dv = \sin x \, dx\right)$$.\
> >We have:\
> >$$du = 2x \, dx$$\
> >$$v = -\cos x$$\
> >Applying the integration by parts formula, we get:\
> >$$\int (x^2 \sin x) \, dx = -x^2 \cos x - \int (-\cos x) \cdot (2x \, dx)$$\
> >Simplifying the integral on the right-hand side, we have:\
> >$$\int (x^2 \sin x) \, dx = -x^2 \cos x + 2 \int (x \cos x) \, dx$$\
> >Now, let's apply integration by parts again, this time with $$\left(u = x\right)$$ and $$\left(dv = \cos x \, dx\right)$$.\
> >We have:\
> >$$du = dx$$\
> >$$v = \sin x$$\
> >Applying the integration by parts formula, we get:\
> >$$\int (x^2 \sin x) \, dx = -x^2 \cos x + 2 \left(x \sin x - \int \sin x \, dx\right)$$\
> >Simplifying the integral on the right-hand side, we have:\
> >$$\int (x^2 \sin x) \, dx = -x^2 \cos x + 2 \left(x \sin x + \cos x\right) + C$$\
> >Therefore, the solution to the integral $$\left(\int (x^2 \sin x) \, dx\right) is:$$\
> >$$\int (x^2 \sin x) \, dx = -x^2 \cos x + 2 \left(x \sin x + \cos x\right) + C$$
>{: .solution}
{: .challenge}
> #### b) $$\int(xe^{2x})dx$$
> >
> > ## Solution
> > 
> >To solve the integral $$\left(\int (xe^{2x}) \, dx\right)$$, we can use integration by parts. Let's apply the formula $$\left(\int u \, dv = uv - \int v \, du\right)$$ with $$\left(u = x\right)$$ and $$\left(dv = e^{2x} \, dx\right)$$.\
> >We have:\
> >$$du = dx$$\
> >$$v = \frac{1}{2}e^{2x}$$\
> >Applying the integration by parts formula, we get:\
> >$$\int (xe^{2x}) \, dx = \frac{1}{2}xe^{2x} - \int \frac{1}{2}e^{2x} \, dx$$\
> >Simplifying the integral on the right-hand side, we have:\
> >$$\int (xe^{2x}) \, dx = \frac{1}{2}xe^{2x} - \frac{1}{4}e^{2x} + C$$\
> >Therefore, the solution to the integral $$\left(\int (xe^{2x}) \, dx\right)$$ is:\
> >$$\int (xe^{2x}) \, dx = \frac{1}{2}xe^{2x} - \frac{1}{4}e^{2x} + C$$
>{: .solution}
{: .challenge}
> #### c) $$\int (x^2/(1-x^2)dx$$
> >
> > ## Solution
> > 
> >To solve the integral $$\int \frac{x^2}{1-x^2} \, dx$$, we can use partial fraction decomposition. First, we factor the denominator $$1-x^2\) as \left((1-x)(1+x)$$.\
> >We can write $$\frac{x^2}{1-x^2}$$ as $$\frac{A}{1-x} + \frac{B}{1+x}$$, where $$A$$ and $$B$$ are constants.\
> >To find $$A$$ and $$B$$, we can equate the numerators:\
> >$$x^2 = A(1+x) + B(1-x)$$\
> >Expanding and simplifying the right-hand side:\
> >$$x^2 = (A + B) + (A - B)x$$\
> >Equating the coefficients of the terms on both sides, we have the following system of equations:\
> >$$A + B = 0 \quad \text{(coefficient of the constant term)}$$\
> >$$A - B = 1 \quad \text{(coefficient of the term with x)}$$\
> >Solving this system of equations, we find $$\left(A = \frac{1}{2}\right)$$ and $$\left(B = -\frac{1}{2}\right)$$.\
> >Now, we can rewrite the integral as:\
> >$$\int \frac{x^2}{1-x^2} \, dx = $$
> >$$\int \frac{\frac{1}{2}}{1-x} - \frac{\frac{1}{2}}{1+x} \, dx$$\
> >Simplifying the integrals on the right-hand side, we have:\
$$\int \frac{x^2}{1-x^2} \, dx = \frac{1}{2}\int \frac{1}{1-x} \, dx - \frac{1}{2}\int \frac{1}{1+x} \, dx$$\
> >Applying the integral formulas, we get:\
$$\int \frac{x^2}{1-x^2} \, dx = \frac{1}{2}(-\ln|1-x|) - \frac{1}{2}(\ln|1+x|) + C$$\
> >Therefore, we have:\
> >$$\int \frac{x^2}{1-x^2} \, dx = \frac{1}{2}(-\ln|1-x|) - \frac{1}{2}(\ln|1+x|) + C$$
>{: .solution}
{: .challenge}
> #### d) $$\int \frac{1}{x^2-1} dx$$
> >
> > ## Solution
> > 
> >To solve the integral $$\int \frac{1}{x^2-1} \, dx$$, we can use partial fraction decomposition. First, we factor the denominator $$x^2-1\) as \((x-1)(x+1)$$.\
> >We can write $$\frac{1}{x^2-1}$$ as $$\frac{A}{x-1} + \frac{B}{x+1}$$, where $$A$$ and $$B$$ are constants.\
> >To find $$A$$ and $$B$$, we can equate the numerators:\
$$1 = A(x+1) + B(x-1)$$\
> >Expanding and simplifying the right-hand side:\
$$1 = (A + B)x + (A - B)$$\
> >Equating the coefficients of the terms on both sides, we have the following system of equations:\
$$A + B = 0 \quad \text{(coefficient of the term with \(x\))}$$\
$$A - B = 1 \quad \text{(coefficient of the constant term)}$$\
> >Solving this system of equations, we find $$A = \frac{1}{2}\) and \(B = -\frac{1}{2}$$.\
> >Now, we can rewrite the integral as:\
> >$$\int \frac{1}{x^2-1} \, dx = \int \left(\frac{\frac{1}{2}}{x-1} - \frac{\frac{1}{2}}{x+1}\right) \, dx$$\
> >Simplifying the integrals on the right-hand side, we have:\
$$\int \frac{1}{x^2-1} \, dx = \frac{1}{2}\int \frac{1}{x-1} \, dx - \frac{1}{2}\int \frac{1}{x+1} \, dx$$\
> >Applying the integral formulas, we get:\
$$\int \frac{1}{x^2-1} \, dx = \frac{1}{2}\ln|x-1| - \frac{1}{2}\ln|x+1| + C$$\
> >Therefore, the solution to the integral $$\int \frac{1}{x^2-1} \, dx$$ is:\
$$\int \frac{1}{x^2-1} \, dx = \frac{1}{2}\ln|x-1| - \frac{1}{2}\ln|x+1| + C$$
>{: .solution}
{: .challenge}
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
> ### $$\frac{d \cot x}{dx}=−\csc ^2 x$$
> >
> > ## Solution
> >
> >To prove the formula $$\frac{d}{dx}(\cot x) = -\csc^2 x$$, we'll differentiate the left-hand side of the equation and simplify it to match the right-hand side.\
> >Starting with the left-hand side, we have:\
> >$$\frac{d}{dx}(\cot x)$$\
> >Using the quotient rule for differentiation, we can write this as:\
> >$$\frac{d}{dx}\left(\frac{\cos x}{\sin x}\right)$$\
> >Now, applying the quotient rule, we get:\
> >$$\frac{(-\sin x)(\sin x) - (\cos x)(\cos x)}{(\sin x)^2}$$\
> >Simplifying further, we have:\
> >$$\frac{-\sin^2 x - \cos^2 x}{(\sin x)^2}$$\
> >Recall the Pythagorean identity $$\sin^2 x + \cos^2 x = 1$$. Substituting this into the equation, we get:\
> >$$\frac{-1}{(\sin x)^2}$$\
> >Which is equalt to $$-\csc^2 x$$.\
> >Therefore, we have shown that:\
> >$$\frac{d}{dx}(\cot x) = -\csc^2 x$$
>{: .solution}
{: .challenge}
> ### Prove the following formulas.
> #### a) $$1 + \tan^2 x = \sec^2 x$$
> >
> > ## Solution
> >
> >We start with the definition of the tangent function:\
> >$$\tan x = \frac{\sin x}{\cos x}$$\
> >Squaring both sides of this equation yields:\
> >$$\tan^2 x = \left(\frac{\sin x}{\cos x}\right)^2$$\
> >Using the property that the square of a fraction is equal to the square of the numerator divided by the square of the denominator, we can rewrite this as:\
> >$$\tan^2 x = \frac{\sin^2 x}{\cos^2 x}$$\
> >Next, we recall the Pythagorean identity for trigonometric functions:\
> >$$\sin^2 x + \cos^2 x = 1$$\
> >Rearranging this equation gives:\
> >$$\sin^2 x = 1 - \cos^2 x$$
> >Substituting this into our previous expression for $$\left(\tan^2 x\right)$$, we have:\
> >$$\tan^2 x = \frac{1 - \cos^2 x}{\cos^2 x}$$\
> >Now, we can simplify the expression on the right-hand side by combining the terms:\
> >$$\tan^2 x = \frac{1}{\cos^2 x} - \frac{\cos^2 x}{\cos^2 x}$$\
> >Simplifying further:\
> >$$\tan^2 x = \sec^2 x - 1$$\
> >Finally, adding 1 to both sides of the equation, we obtain:\
> >$$1 + \tan^2 x = \sec^2 x$$\
> >Thus, we have proven the equation\
 $$\left(1 + \tan^2 x = \sec^2 x\right)$$\
> > using the definitions and properties of trigonometric functions.
>{: .solution}
{: .challenge}
> #### b) $$\cos 2x = 2\cos^2 x - 1$$
> >
> > ## Solution
> >
> >To prove the equation $$\cos 2x = 2\cos^2 x - 1$$, we can use the double-angle formula for cosine and the Pythagorean identity for trigonometric functions.\
> >Starting with the double-angle formula for cosine:\
> >$$\cos 2x = \cos^2 x - \sin^2 x$$\
> >We can rewrite the left-hand side using the cosine double-angle identity:\
> >$$\cos 2x = \cos^2 x - (1 - \cos^2 x)$$\
> >Simplifying the expression on the right-hand side:\
> >$$\cos 2x = \cos^2 x - 1 + \cos^2 x$$\
> >Combining like terms:\
> >$$\cos 2x = 2\cos^2 x - 1$$
>{: .solution}
{: .challenge}
> ### Compute the following limits by interpreting them as Riemann sums:
> #### a)  $$lim_{n->\infty} \sum_{k=1}^n \frac{(n+2)}{(n^2*(n+1))}*k$$ 
> >
> > ## Solution
> >
> >a) To compute the given limit by interpreting it as a Riemann sum, we can start by rewriting the summation using the limit definition of a Riemann sum. The Riemann sum is an approximation of the definite integral of a function over a given interval.\
Let's break down the given expression step by step:\
$$\lim_{n\to\infty} \sum_{k=1}^n \frac{n+2}{n^2(n+1)} \cdot k$$\
Notice that the term inside the summation, $$\left(\frac{n+2}{n^2(n+1)}\right)$$, does not depend on the index variable $$\left(k\right)$$. Therefore, we can factor it out of the summation:\
$$\lim_{n\to\infty} \frac{n+2}{n^2(n+1)} \cdot \sum_{k=1}^n k$$\
Now, let's focus on the remaining summation term, $$\left(\sum_{k=1}^n k\right)$$. This is a sum of consecutive positive integers, which can be expressed as the closed-form formula:\
$$\sum_{k=1}^n k = \frac{n(n+1)}{2}$$\
Substituting this back into our expression, we get:\
$$\lim_{n\to\infty} \frac{n+2}{n^2(n+1)} \cdot \frac{n(n+1)}{2}$$\
Simplifying further:\
$$\lim_{n\to\infty} \frac{n+2}{2n}$$\
Now, we can compute the limit directly by dividing the leading terms of the numerator and denominator:\
$$\lim_{n\to\infty} \frac{1 + \frac{2}{n}}{2} = \frac{1}{2}$$\
Therefore, the limit of the given expression, interpreted as a Riemann sum, is equal to $$\left( \frac{1}{2} \right)$$.
>{: .solution}
{: .challenge}
> ### b) $$lim_{n->\infty} \sum_{k=1}^n \frac{2}{(n+1)^2)}*k$$ 
> >
> > ## Solution
> >
> > $$\lim_{n\to\infty} \sum_{k=1}^n \frac{2}{(n+1)^2} \cdot k$$
Notice that the term inside the summation, $$\frac{2}{(n+1)^2}$$, does not depend on the index variable $$k$$. Therefore, we can factor it out of the summation:\
$$\lim_{n\to\infty} \frac{2}{(n+1)^2} \cdot \sum_{k=1}^n k$$\
The summation term $$\sum_{k=1}^n k$$ can be expressed as the closed-form formula:\
$$\sum_{k=1}^n k = \frac{n(n+1)}{2}$$\
Substituting this back into our expression:\
$$\lim_{n\to\infty} \frac{2}{(n+1)^2} \cdot \frac{n(n+1)}{2}$$\
Simplifying further:\
$$\lim_{n\to\infty} \frac{n}{n+1}$$\
Now, we can compute the limit directly by dividing the leading terms of the numerator and denominator:\
$$\lim_{n\to\infty} \frac{1}{1+\frac{1}{n}}$$\
As $$n$$ approaches infinity, $$\frac{1}{n}$$ approaches zero. Therefore:\
$$\lim_{n\to\infty} \frac{1}{1+\frac{1}{n}} = \frac{1}{1+0} = 1$$\
Therefore, the limit of the given expression, interpreted as a Riemann sum, is equal to 1.
>{: .solution}
{: .challenge}
## Final Semester Exam
> a) Let $$f$$ be defined on all of $$R$$. For each real number $$c$$, we define the translated function $$f_c$$ by: $$f_c(x) = f (x − c)$$. Suppose that $$f$$ is integrable on all bounded intervals. Show that: $$\int_{a}^{b} f = \int_{a+c}^{b+c} f_c$$ for all $$a$$ and $$b$$.
> >
> >## Solution
> >
> >To show that $$\int_a^b f = \int_{a+c}^{b+c} f_c$$ for all $$a$$ and $$b$$, we need to demonstrate that the integrals of the two functions are equal.\
> >First, let's consider the integral of $$f$$ over the interval $$[a, b]$$.\
We can define a new variable $$u$$ such that $$u = x - c$$.\
Rearranging the equation, we have $$x = u + c$$.\
> >When $$x = a$$, $$u + c = a$$, and when $$x = b$$, $$u + c = b$$.\
 This means that the new interval of integration for the function $$f_c$$ will be $$[u + c]_a^b$$.\
> >Now, let's substitute $$u + c$$ for $$x$$ in the expression for $$f_c$$.\
We get $$f_c(u + c) = f(u)$$.\
The integrand for $$f_c$$ is essentially the same as $$f$$, but the variable has been changed to $$u$$.\
> >Therefore, we can rewrite the integral of $$f_c$$ over the interval $$[a + c, b + c]$$ as\
$$\int_{a + c}^{b + c} f_c = \int_a^b f(u) du$$.\
> >Now, we have shown that the integral of $$f_c$$ over the interval $$[a + c, b + c]$$ is equivalent to the integral of $$f$$ over the interval $$[a, b]$$, but with a change of variable from $$x$$ to $$u$$.\
> >Since the choice of variable does not affect the value of the integral, we can conclude that\
$$\int_a^b f = \int_{a+c}^{b+c} f_c$$ for all $$a$$ and $$b$$.\
> >Thus, we have established the desired result.
>{: .solution}
{: .challenge}
> ### b) Suppose that  f  is bounded on $$[a,b]$$  and for each $$ε > 0$$, it is integrable on $$[a + ε,b]$$. Show that  $$f$$  is integrable on $$[a,b]$$ and $$\lim_{ε→0+}\int_{a+ε}^{b} f =   \int_{a}^{b} f$$. 
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
> >Since $$\lim_{\varepsilon \to 0^+} M \cdot \varepsilon = 0$$ (as $$\varepsilon$$ approaches 0), we have:\
> >$$\int_a^b f \leq \lim_{\varepsilon \to 0^+} \int_{a + \varepsilon}^b f \leq \int_a^b f$$\
> >Hence, $$\lim_{\varepsilon \to 0^+} \int_{a + \varepsilon}^b f = \int_a^b f$$, which shows that $$f$$ is integrable on $$[a, b]$$ and satisfies the desired limit property.
>{: .solution}
{: .challenge}
<!-- > ### b) Suppose that $$f$$  is bounded on $$[a,b]$$ and for each $$ε > 0$$, it is integrable on $$[a + ε,b]$$. Show that $$f$$ is integrable on $$[a,b]$$ and $$\lim_{ε→0+} \int_{a+ε}^{b} f = \int_{a}^{b} f$$.
> >
> >## Solution
> >
> >To show that $$f$$ is integrable on $$[a, b]$$ and $$\lim_{\varepsilon \to 0^+} \int_{a + \varepsilon}^{b} f = \int_{a}^{b} f$$, we need to demonstrate that $$f$$ satisfies the conditions of Riemann integrability and that the limit of the integral as $$\varepsilon$$ approaches zero is equal to the integral over the entire interval.\
> >Since $$f$$ is bounded on $$[a, b]$$, we can assume that there exists a constant $$M > 0$$ such that $$|f(x)| \leq M$$ for all $$x \in [a, b]$$. Additionally, for each $$\varepsilon > 0$$, we are given that $$f$$ is integrable on $$[a + \varepsilon, b]$$. This means that there exists a partition $$P_\varepsilon$$ of $$[a + \varepsilon, b]$$ such that the upper sum and lower sum of $$f$$ with respect to $$P_\varepsilon$$ satisfy the condition $$U(f, P_\varepsilon) - L(f, P_\varepsilon) < \varepsilon$$.\
> >Now, consider the interval $$[a, b]$$. For each $$\varepsilon > 0$$, we can choose a partition $$P_\varepsilon$$ of $$[a + \varepsilon, b]$$. Let $$P = \{a = x_0 < x_1 < \ldots < x_n = b\}$$ be a common refinement of $$P_\varepsilon$$ and $$[a, b]$$. Since $$P$$ is a refinement of both partitions, it follows that $$P$$ is a partition of $$[a, b]$$.\
> >Let $$U(f, P)$$ and $$L(f, P)$$ denote the upper sum and lower sum of $$f$$ with respect to the partition $$P$$, respectively. Since $$P$$ is a refinement of $$P_\varepsilon$$, we have $$U(f, P) \leq U(f, P_\varepsilon)$$ and $$L(f, P) \geq L(f, P_\varepsilon)$$. Thus, we have:\
> >$$U(f, P) - L(f, P) \leq U(f, P_\varepsilon) - L(f, P_\varepsilon) < \varepsilon$$\
> >Since this holds for any $$\varepsilon > 0$$, it follows that $$f$$ is integrable on $$[a, b]$$.\
> >Now, let's consider the limit as $$\varepsilon$$ approaches zero of the integral $$\int_{a + \varepsilon}^{b} f$$. Using the limit definition of the integral, we have:\
> >$$\lim_{\varepsilon \to 0^+} \int_{a + \varepsilon}^{b} f = \lim_{\varepsilon \to 0^+} \left( \int_{a}^{b} f - \int_{a}^{a + \varepsilon} f \right)$$\
> >Since $$f$$ is integrable on $$[a, b]$$, we have:\
> >$$\lim_{\varepsilon \to 0^+} \int_{a + \varepsilon}^{b} f = \int_{a}^{b} f - \lim_{\varepsilon \to 0^+} \int_{a}^{a + \varepsilon} f$$\
> >Now, let's focus on the second term in the expression. Since $$f$$ is integrable on $$[a + \varepsilon, b]$$ for each $$\varepsilon > 0$$, we can apply the result of the previous analysis:\
> >$$\lim_{\varepsilon \to 0^+} \int_{a}^{a + \varepsilon} f = \int_{a}^{a} f = 0$$\
> >Substituting this result back into the expression, we get:\
> >$$\lim_{\varepsilon \to 0^+} \int_{a + \varepsilon}^{b} f = \int_{a}^{b} f - 0 = \int_{a}^{b} f$$\
> >Thus, we have shown that $$f$$ is integrable on $$[a, b]$$ and $$\lim_{\varepsilon \to 0^+} \int_{a + \varepsilon}^{b} f = \int_{a}^{b} f$$.
>{: .solution}
{: .challenge} -->
>### Solve the following integrals. Show your detailed answers by writing the step-by-step analysis:
> #### a)  $$\int (x^2 \tan x)dx$$
> >
> > ## Solution
> >
> >a) To solve the integral $$\int (x^2 \tan x)dx$$:\
> >We can use integration by parts, which states:\
$$\int u dv = uv - \int v du$$\
> >Let's choose $$u = x^2$$ and $$dv = \tan x dx$$. Taking the derivatives and antiderivatives, we have $$du = 2x dx$$ and $$v = \int \tan x dx = -\ln|\cos x|$$.\
> >Now, applying the integration by parts formula, we get:
$$\int (x^2 \tan x)dx = -x^2 \ln|\cos x| - \int (-\ln|\cos x| \cdot 2x)dx$$\
> >Simplifying, we have:\
> >$$\int (x^2 \tan x)dx = -x^2 \ln|\cos x| + 2\int x \ln|\cos x| dx$$\
> >Now, we need to solve the remaining integral, $$\int x \ln|\cos x| dx$$. We can use integration by parts again.\
> >Let's choose $$u = \ln|\cos x|$$ and $$dv = x dx$$. Taking the derivatives and antiderivatives, we have $$du = -\frac{\sin x}{\cos x} dx$$ and $$v = \frac{x^2}{2}$$.\
> >Applying the integration by parts formula, we get:\
> >$$\int x \ln|\cos x| dx = \frac{x^2}{2} \ln|\cos x| - \int \frac{x^2}{2} \cdot \frac{\sin x}{\cos x} dx$$\
> >Simplifying, we have:\
$$\int x \ln|\cos x| dx = \frac{x^2}{2} \ln|\cos x| - \frac{1}{2} \int x^2 \tan x dx$$\
> >Now, let's substitute this result back into the equation for the original integral:\
> >$$\int (x^2 \tan x)dx = -x^2 \ln|\cos x| + 2\left(\frac{x^2}{2} \ln|\cos x| - \frac{1}{2} \int x^2 \tan x dx\right)$$\
> >Simplifying further, we have:\
> >$$\int (x^2 \tan x)dx = -x^2 \ln|\cos x| + x^2 \ln|\cos x| - \int x^2 \tan x dx$$\
> >Combining like terms, we obtain:\
> >$$2\int (x^2 \tan x)dx = -x^2 \ln|\cos x|$$\
> >Dividing both sides by 2, we get the final result:\
$$\int (x^2 \tan x)dx = -\frac{1}{2}x^2 \ln|\cos x| + C$$\
> >Therefore, $$\int (x^2 \tan x)dx = -\frac{1}{2}x^2 \ln|\cos x| + C$$, where $$C$$ is the constant of integration.
>{: .solution}
{: .challenge}
> #### b) $$\int(x^2e^{2x})dx$$
> >
> > ## Solution
> >
> >To solve the integral $$\int(x^2e^{2x})dx$$:\
> >We can use integration by parts, similar to the previous problem.\
> >Let's choose $$u = x^2$$ and $$dv = e^{2x} dx$$. Taking the derivatives and antiderivatives, we have $$du = 2x dx$$ and $$v = \frac{1}{2} e^{2x}$$.\
> >Applying the integration by parts formula, we get:\
> >$$\int(x^2e^{2x})dx = \frac{1}{2}x^2e^{2x} - \int 2x \cdot \frac{1}{2} e^{2x} dx$$\
> >Simplifying, we have:\
> >$$\int(x^2e^{2x})dx = \frac{1}{2}x^2e^{2x} - \int x e^{2x} dx$$\
> >Now, we need to solve the remaining integral, $$\int x e^{2x} dx$$. We can use integration by parts again.\
> >Let's choose $$u = x$$ and $$dv = e^{2x} dx$$. Taking the derivatives and antiderivatives, we have $$du = dx$$ and $$v = \frac{1}{2} e^{2x}$$.\
> >Applying the integration by parts formula, we get:\
> >$$\int x e^{2x} dx = \frac{1}{2}x e^{2x} - \int \frac{1}{2} e^{2x} dx$$\
> >Simplifying, we have:\
> >$$\int x e^{2x} dx = \frac{1}{2}x e^{2x} - \frac{1}{4} e^{2x}$$\
> >Now, substituting this result back into the equation for the original integral, we have:\
> >$$\int(x^2e^{2x})dx = \frac{1}{2}x^2e^{2x} - \left(\frac{1}{2}x e^{2x} - \frac{1}{4} e^{2x}\right)$$\
> >Combining like terms, we obtain:\
> >$$\int(x^2e^{2x})dx = \frac{1}{2}x^2e^{2x} - \frac{1}{2}x e^{2x} + \frac{1}{4} e^{2x} + C$$\
> >Therefore, $$\int(x^2e^{2x})dx = \frac{1}{2}x^2e^{2x} - \frac{1}{2}x e^{2x} + \frac{1}{4} e^{2x} + C$$, where $$C$$ is the constant of integration.
>{: .solution}
{: .challenge}
>#### c) $$\int (x^2/(x-x^2)dx$$
> >
> > ## Solution
> >
> >First, we will simplify it to $$\int \frac{x}{x-1} \, dx$$ just by canceling $$x$$ from the denominator and numerator.\
> >To solve the simplified integral $$\int \frac{x}{x-1} \, dx$$,\
we can use a simple substitution.\
> >Let's substitute $$u = x - 1$$, which implies $$x = u + 1$$ and $$dx = du$$.\
> >Substituting these values, the integral becomes:\
> >$$\int \frac{u + 1}{u} \, du$$\
> >We can expand the integrand:\
> >$$\int \left(1 + \frac{1}{u}\right) \, du$$\
> >Now, we can integrate each term separately:\
> >$$\int 1 \, du + \int \frac{1}{u} \, du$$\
> >The integral of the constant term $$1$$ with respect to $$u$$ is simply $$u$$:\
> >$$u + \ln|u| + C$$\
> >Since we initially substituted $$u = x - 1$$, we can substitute back to obtain the final result:\
> >$$x - 1 + \ln|x - 1| + C$$\
> >Therefore, the solution to the integral is:\
> >$$\int \frac{x}{x-1} \, dx = x - 1 + \ln|x - 1| + C$$\
> >where $$C$$ is the constant of integration.
>{: .solution}
{: .challenge}
> #### d) $$\int \frac{x}{x^3-1} dx$$
> >
> > ## Solution
> >
> > $$\int \frac{x}{x^3-1} dx = \int \frac{x}{(x-1)(x^2+x+1)} dx$$\
$$= \frac{1}{3}\ln|x-1| - \frac{1}{3}\int \frac{x-1}{x^2+x+1} dx$$.\
> >To evaluate the second term, we complete the square in the denominator:\
> >$$x^2 + x + 1 = \left(x+\frac{1}{2}\right)^2 + \frac{3}{4}$$.\
> >Making the substitution $$\left(u = x+\frac{1}{2}\right)$$, we have $$\left(du = dx\right)$$ and the integral becomes:\
> >$$-\frac{1}{3}\int \frac{u-\frac{3}{2}}{u^2+\frac{3}{4}} du$$.\
> > Expanding the numerator, we get:\
> >$$-\frac{1}{3}\int \frac{u-\frac{3}{2}}{u^2+\frac{3}{4}} du = -\frac{1}{3}\int \frac{u}{u^2+\frac{3}{4}} du + \frac{1}{2}\int \frac{1}{u^2+\frac{3}{4}} du$$.\
> >The first integral can be evaluated using a substitution $$\left(v = u^2 + \frac{3}{4}\right)$$, resulting in $$\left(-\frac{1}{6}\ln|v| + E_1\right)$$, where $$\left(E_1\right)$$ is the constant of integration.\
> >The second integral is the integral of the standard form $$\left(\frac{1}{u^2+a^2}\right)$$, which has the antiderivative $$\left(\frac{1}{a}\arctan\left(\frac{u}{a}\right)\right)$$. In this case, we have $$\left(a = \frac{\sqrt{3}}{2}\right)$$. Therefore, the second integral evaluates to $$\left(\frac{2}{\sqrt{3}}\arctan\left(\frac{2u}{\sqrt{3}}\right) + E_2\right)$$, where $$\left(E_2\right)$$ is the constant of integration.\
> >Substituting back $$\left(u = x+\frac{1}{2}\right)$$, we obtain:\
> >$$-\frac{1}{3}\int \frac{x-1}{x^2+x+1} dx = -\frac{1}{6}\ln\left|u^2+\frac{3}{4}\right| + \frac{2}{\sqrt{3}}\arctan\left(\frac{2u}{\sqrt{3}}\right) + E_3$$,\
> > where $$\left(E_3 = E_1 + E_2\right)$$ is the combined constant of integration.\
> >Putting it all together, the integral of $$\left(\frac{x}{x^3-1}\right)$$ is:\
> >$$\int \frac{x}{x^3-1} dx = \frac{1}{3}\ln|x-1| - \frac{1}{6}\ln\left|x^2+x+1\right| + \frac{2}{\sqrt{3}}\arctan\left(\frac{2(x+\frac{1}{2})}{\sqrt{3}}\right) + D$$,\
> >where $$\left(D = E + E_3\right)$$ is the combined constant of integration.
>{: .solution}
{: .challenge}
> #### Prove the following formulas.
>#### a) $$\cos 3x = 4\cos^3x - 3\cos x$$
> >
> > ## Solution
> >
> >To prove the formula $$\cos 3x = 4\cos^3 x - 3\cos x$$, we can use the trigonometric identities and properties. Let's start with the left-hand side of the equation $$\cos 3x$$\:\
> >Using the triple angle formula for cosine, we have:\
> >$$\cos 3x = 4\cos^3 x - 3\cos x$$\
> >This formula expresses $$\cos 3x$$ in terms of $$\cos x$$ and $$\cos^3 x$$.\
Now, let's simplify the right-hand side of the equation $$4\cos^3 x - 3\cos x$$:\
> >Factoring out $$\cos x$$ from both terms, we get:\
> >$$\cos x(4\cos^2 x - 3)$$\
> >Now, we can use the Pythagorean identity $$\sin^2 x + \cos^2 x = 1$$ to rewrite $$\cos^2 x$$ as $$1 - \sin^2 x$$:\
> >$$\cos x(4(1 - \sin^2 x) - 3)$$\
> >Simplifying further, we have:\
> >$$\cos x(4 - 4\sin^2 x - 3)$$ = $$\cos x(1 - 4\sin^2 x)$$\
> >Since $$\sin^2 x = 1 - \cos^2 x$$, we can substitute this into the equation:\
> >$$\cos x(1 - 4(1 - \cos^2 x))$$ = $$\cos x(1 - 4 + 4\cos^2 x)$$\
> >= $$\cos x(-3 + 4\cos^2 x)$$\
> >Notice that this expression is equal to the right-hand side of the original equation. Therefore, we have shown that:\
> >$$\cos 3x = 4\cos^3 x - 3\cos x$$\
> >This completes the proof.
>{: .solution}
{: .challenge}
> #### b) $$\sin 3x =3\sin x − 4\sin^3 x$$
> >
> >## Solution
> >
> >To prove the formula $$\sin 3x = 3\sin x - 4\sin^3 x$$, we can use the trigonometric identities and properties. Let's start with the left-hand side of the equation $$\sin 3x$$:\
> >Using the triple angle formula for sine, we have:\
> >$$\sin 3x = 3\sin x - 4\sin^3 x$$\
> >This formula expresses $$\sin 3x$$ in terms of $$\sin x$$ and $$\sin^3 x$$. Now, let's simplify the right-hand side of the equation:\
> >$$3\sin x - 4\sin^3 x$$\
> >Factoring out $$\sin x$$ from both terms, we get:\
> >$$\sin x(3 - 4\sin^2 x)$$\
> >Now, we can use the Pythagorean identity $$\sin^2 x + \cos^2 x = 1$$ to rewrite $$\sin^2 x$$ as $$1 - \cos^2 x$$:\
> >$$\sin x(3 - 4(1 - \cos^2 x))$$\
> >Simplifying further, we have:\
> >$$\sin x(3 - 4 + 4\cos^2 x)$$ = $$\sin x(-1 + 4\cos^2 x)$$\
> >Since $$\cos^2 x = 1 - \sin^2 x$$, we can substitute this into the equation:\
> >$$\sin x(-1 + 4(1 - \sin^2 x))$$ = $$\sin x(-1 + 4 - 4\sin^2 x)$$\
> >=$$\sin x(3 - 4\sin^2 x)$$\
> >Notice that this expression is equal to the right-hand side of the original equation. Therefore, we have shown that:\
> >$$\sin 3x = 3\sin x - 4\sin^3 x$$\
> >This completes the proof.
>{: .solution}
{: .challenge}
> ### Compute the following limits by interpreting them as Riemann sums:
> #### a)  $$lim_{n->\infty} \frac{n}{n^{p+1}}\sum_{k=1}^n k^p$$ 
> >
> > ## Solution
> >
> >$$\lim_{n\to\infty} \frac{n}{n^{p+1}}\sum_{k=1}^n k^p$$
To compute this limit as a Riemann sum, we interpret it as the limit of a Riemann sum for the function $$\left(f(x) = x^p\right)$$ on the interval $$\left([1, n]\right)$$.\
> >The Riemann sum for $$\left(f(x)\right)$$ on $$\left([1, n]\right)$$ with $$\left(n\right)$$ subintervals can be written as:\
> >$$\frac{n}{n^{p+1}} \sum_{k=1}^n k^p =  \sum_{k=1}^n \left(\frac{k}{n}\right)^p$$\
> ><!-- Notice that the term $$\left(\frac{1}{n^p}\right)$$ can be factored out from the sum. Now we have:\
> >$$\frac{1}{n^p} \sum_{k=1}^n \left(\frac{k}{n}\right)^p$$\ -->
> >As $$\left(n\right)$$ approaches infinity, the sum $$\left(\sum_{k=1}^n \left(\frac{k}{n}\right)^p\right)$$ can be approximated by the integral of the function $$\left(f(x) = x^p\right)$$ over the interval $$\left([0, 1]\right)$$.\
> >Therefore, the limit can be computed as:\
> >$$\lim_{n\to\infty} \frac{n}{n^{p+1}} \sum_{k=1}^n k^p = \lim_{n\to\infty} \sum_{k=1}^n \left(\frac{k}{n}\right)^p = \int_{0}^{1} x^p dx$$\
> >To evaluate the integral $$\left(\int_{0}^{1} x^p dx\right)$$, we can use the power rule for integration:\
> >$$\int_{0}^{1} x^p dx = \left[\frac{x^{p+1}}{p+1}\right]_{0}^{1} = \frac{1^{p+1}}{p+1} - \frac{0^{p+1}}{p+1} = \frac{1}{p+1}$$\
> >Therefore, the limit is:\
> >$$\lim_{n\to\infty} \frac{n}{n^{p+1}} \sum_{k=1}^n k^p = \int_{0}^{1} x^p dx = \frac{1}{p+1}$$\
Hence, the limit is $$\left(\frac{1}{p+1}\right)$$.
>{: .solution}
{: .challenge}
> #### b) $$lim_{n->\infty} \sum_{k=1}^n \frac{2*(n+2)}{n*(n+1)^2}*k$$
> >
> > ## Solution
> >
> >To compute the limit\
> >$$\lim_{n\to\infty} \sum_{k=1}^n \frac{2(n+2)}{n(n+1)^2} \cdot k$$,\
> > we observe that the sum can be rewritten as\
> >$$\sum_{k=1}^n \frac{2}{n(n+1)^2} \cdot (n+2) \cdot k = \frac{2}{n(n+1)^2} \sum_{k=1}^n (n+2) \cdot k$$.\
> >The term $$\left(\frac{2}{n(n+1)^2}\right)$$ can be taken out of the sum, resulting in\
> >$$\frac{2}{n(n+1)^2} \cdot (n+2) \cdot \sum_{k=1}^n k = \frac{2(n+2)}{n(n+1)^2} \cdot \frac{n(n+1)}{2}$$.\
> >Simplifying further, we obtain\
> >$$\frac{2(n+2)}{n(n+1)^2} \cdot \frac{n(n+1)}{2} = \frac{n+2}{n+1}$$.\
> >Taking the limit as \(n\) approaches infinity, we find\
> >$$\lim_{n\to\infty} \sum_{k=1}^n \frac{2(n+2)}{n(n+1)^2} \cdot k = \lim_{n\to\infty} \frac{n+2}{n+1} = 1$$.\
> >Therefore, the limit $$lim_{n->\infty} \sum_{k=1}^n \frac{2*(n+2)}{n*(n+1)^2}*k$$ is 1.
>{: .solution}
{: .challenge}
> #### c) $$lim_{n->\infty} \sum_{k=1}^n k/\sqrt(n^2 + k^2)$$
> >
> > ## Solution
> >
> >To compute the limit\
$$\lim_{n\to\infty} \sum_{k=1}^n \frac{k}{\sqrt{n^2 + k^2}}$$,\
we observe that the sum can be interpreted as a Riemann sum for the function $$\left(f(x) = \frac{x}{\sqrt{n^2 + x^2}}\right)$$ over the interval $$\left([1, n]\right)$$.\
Using the properties of Riemann sums, we have\
$$\lim_{n\to\infty} \sum_{k=1}^n \frac{k}{\sqrt{n^2 + k^2}} = \int_{1}^{n} \frac{x}{\sqrt{n^2 + x^2}} \, dx$$.\
evaluate this integral, we can make the substitution $$\left(u = \frac{x}{n}\right)$$, which leads to $$\left(dx = n \, du\right)$$.\
The integral becomes\
$$\int_{1}^{n} \frac{x}{\sqrt{n^2 + x^2}} \, dx = \int_{\frac{1}{n}}^{1} \frac{n u}{\sqrt{n^2 + (nu)^2}} \, n \, du = \int_{\frac{1}{n}}^{1} \frac{nu}{\sqrt{1 + u^2}} \, du$$.\
As $$\left(n\right)$$ approaches infinity, the limits of integration become $$\left(\frac{1}{\infty} = 0\right)$$ and $$\left(1\right)$$.\
Therefore, we have\
$$\lim_{n\to\infty} \sum_{k=1}^n \frac{k}{\sqrt{n^2 + k^2}} = \lim_{n\to\infty} \int_{\frac{1}{n}}^{1} \frac{nu}{\sqrt{1 + u^2}} \, du$$.\
Now we can evaluate the integral using standard techniques.\
$$\int_{\frac{1}{n}}^{1} \frac{nu}{\sqrt{1 + u^2}} \, du = \left[-\sqrt{1 + u^2}\right]_{\frac{1}{n}}^{1} = -\sqrt{2} + \sqrt{1 + \frac{1}{n^2}}$$.\
Taking the limit as $$\left(n\right)$$ approaches infinity, we find\
$$\lim_{n\to\infty} \sum_{k=1}^n \frac{k}{\sqrt{n^2 + k^2}} = \lim_{n\to\infty} \left(-\sqrt{2} + \sqrt{1 + \frac{1}{n^2}}\right) = -\sqrt{2} + 1$$.\
Therefore, the limit $$\lim_{n\to\infty} \sum_{k=1}^n \frac{k}{\sqrt{n^2 + k^2}}$$ is $$\left(-\sqrt{2} + 1\right)$$.
>{: .solution}
{: .challenge}
> ### The real factorisation of $$x^4 + 4$$ into irreducible quadratic factors is needed to calculate the integral $$1/(x^4 + 4) dx$$. Obtain the factorisation using complex numbers by noting that the roots of  $$w_1 = e^{i\pi/4}$$, $$w_2 = e^{3i\pi/4}$$, $$w_3 = e^{5i\pi/4}$$, and $$w_4 = e^{7i\pi/4}$$.
> #### Find the integral $$\int \frac{1}{x^4 + 4} \, dx$$
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



