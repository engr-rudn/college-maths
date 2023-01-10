---
layout: default
---

# 3-5 Derivatives of Trigonometric Functions

## Learning Targets

You will be able to
- [ ] Use rules for differentiating the six trig functions

### Concepts / Definitions

$$\frac{d}{dx}\sin(x) = \cos(x)$$
$$\frac{d}{dx}\cos(x) = -\sin(x)$$
$$\frac{d}{dx}\tan(x) = \sec^2(x)$$
$$\frac{d}{dx}\cot(x) = -\csc^2(x)$$
$$\frac{d}{dx}\sec(x) = \sec(x)\tan(x)$$
$$\frac{d}{dx}\csc(x) = -\csc(x)\cot(x)$$

### Proof of Derivative of Sine

$$f'(x) = \lim_{h\to 0} \frac{\sin(x+h) - \sin x}{h}$$
$$f'(x) = \lim_{h\to 0} \frac{\sin x \cos h + \cos x \sin h - \sin x}{h}$$
$$f'(x) = \lim_{h\to 0} \frac{\sin x (\cos h -1)}{h} + \lim_{h\to 0}\frac{\cos x \sin h}{h}$$
$$f'(x) = \cos x$$

[==>](3-5-5-squeeze-theorem-and-limit-of-composite-functions.md)
