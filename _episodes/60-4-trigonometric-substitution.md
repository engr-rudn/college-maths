---
title:  Trigonometric Substitution

questions:
- "How to evaluate integrals using trigonometric substitution?"
objectives:
- "Evaluate integrals using trigonometric substitution"
---

# Trigonometric Substitution

## Concepts / Definitions

How do we solve these algebraically?

$$\int \sqrt{4 - x^2} dx$$

let $x = 2\sin\theta$, $\frac{dx}{d\theta} = 2\cos\theta$, $dx = 2\cos\theta d\theta$

$$\int \sqrt{4-4\sin^2\theta} 2\cos\theta d\theta$$

$$2\int \sqrt{4(1-\sin^2\theta)} \cos\theta d\theta$$

$$4\int \sqrt{\cos^2\theta)} \cos\theta d\theta$$

$$4\int \cos^2\theta d\theta$$

### Seperate

$$2[\sin\theta\cos\theta + \theta] + C$$

$$2[\frac x2  + \arcsin \frac x2] + C$$
