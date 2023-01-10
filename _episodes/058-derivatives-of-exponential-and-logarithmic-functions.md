---
layout: default
---

# 3-9 Derivatives of Exponential and Logarithmic Functions

## Learning Targets

You will be able to
- [ ] Derive rules for derivatives of exponential and logs
- [ ] Compute derivatives of problems that contain exponentials and logs

## Concepts / Definitions

### Figuring out the derivative of $y = a^x$

$$\frac{d}{dx}y = \lim_{h\to 0}\frac{a^{x+h}-a^x}{h}$$

$$\frac{dy}{dx} = \lim_{h\to 0}\frac{a^xa^h-a^x}{h}$$

$$\frac{dy}{dx} = \lim_{h\to 0}a^x\frac{a^h-1}{h}$$

Notice that the limit does not depend on $a^x$.

What does $\lim_{h\to 0}\frac{a^h-1}{h}$ equal?

$\lim_{h\to 0}\frac{a^h-1}{h} = ?$

If $a=e$, then...

#### Definitions with the number $e$
  1. $e = \lim_{n\to \infty}(1+\frac{1}{n})^n$
  2. $e$ is the unique positive number for which $\lim_{h\to 0}\frac{e^h -1}{h} = 1$
  3. $e = \sum_{n=0}^{\infty}\frac{1}{n!}$

$\frac{dy}{dx} = a^x \lim_{h\to 0}\frac{a^h-1}{h}$

The first part, $a^x$ does not depend on $h$, and we have some number, a derivative times $a^x$. The derivative of rate of change of $a^x$ is proportional to the function itself, $ka^x$. What is that number?

If $a$ is a number other than $e$, let $f(a) = \frac{a^{0.001}-1}{0.001}$

$X$ | $Y_1$
---|---
0 | -1000
1 | 0
2 | .69339
3 | 1.0992
4 | 1.3873
5 | 1.6107
6 | 1.7934

### Derivative of a exponential function

$$\frac{d}{dx}a^x = a^x\ln a$$

$$\frac{d}{dx}e^x = e^x\ln e = e^x$$

### Finding the derivative of a logarithmic function

$$\frac{d}{dx}f(x) = \frac{d}{dx}\ln x$$

$$\frac{df}{dx} = \lim_{h\to 0}\frac{\ln(x+h) - \ln x}{h}$$

$$\frac{df}{dx} = \lim_{h\to 0}\frac{\ln(\frac{x+h}{x})}{h}$$

$$\frac{df}{dx} = \lim_{h\to 0}\frac{1}{h}\ln(1+\frac{h}{x})$$

$$\frac{df}{dx} = \lim_{h\to 0}\frac{1}{kx}\ln(1+k),\ for\ k = \frac{h}{x}$$

$$\frac{df}{dx} = \lim_{h\to 0}\frac{1}{x}\ln(1+k)^{1/k},\ for\ k = \frac{h}{x}$$

$$\frac{df}{dx} = \lim_{h\to 0}\frac{1}{x}\ln(\lim_{k\to\infty}(1+\frac{1}{k})^k),\ for\ k = \frac{h}{x}$$

$$\frac{df}{dx} = \lim_{h\to 0}\frac{1}{x}\ln e = \frac{1}{x}$$

---

$$y = \log_ax,\ for\ y = f(x)$$

$$a^y = x$$

$$\frac{d}{dx}a^y = \frac{d}{dx}x$$

$$a^y \ln a \frac{dy}{dx} = 1$$

$$\frac{dy}{dx} = \frac{1}{a^y \ln a}$$

$$\frac{dy}{dx} = \frac{1}{a^{\log_ax}\ln a}$$

$$\frac{df}{dx} = {1}{x\ln a}$$

### Derivative of a logarithmic function

$\frac{d}{dx}\log_a\lvert x \rvert = \frac{1}{x\ln a}$ $\qquad$ $\frac{d}{dx}\log_ax = \frac{1}{x\ln a},\ for\ x > 0$

$\frac{d}{dx}\ln\lvert x \rvert = \frac{1}{x\ln e} = \frac{1}{x}$ $\qquad$ $\frac{d}{dx}\ln x = \frac{1}{x\ln e} = \frac{1}{x},\ for\ x > 0$

### Differentiate $x^{\sin x}

Let $y = x^{\sin x}$

$$\ln y = ln x^{\sin x}$$

$$\ln y = \sin x \ln x$$

$$\frac{d}{dx}\ln y = \frac{d}{dx}(\sin x \ln x)$$

$$\frac{1}{y}\frac{d}{dx}y = \frac{d}{dx}\sin x \ln x + \sin x \frac{d}{dx} \ln x$$

$$\frac{1}{y}\frac{d}{dx}y = \cos x \ln x + \sin x \frac{1}{x}$$

$$\frac{dy}{dx} = y(\cos x \ln x + \sin x \frac{1}{x})$$

$$\frac{dy}{dx} = x^{\sin x}(\cos x \ln x + \sin x \frac{1}{x})$$

[==>](4-1-extreme-values-of-functions.md)
