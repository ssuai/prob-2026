# Problem 3 — Hard | Central Limit Theorem

## Problem

A factory produces bolts whose lengths (in mm) are i.i.d. random variables $X_i$
with mean $\mu = 50$ mm and standard deviation $\sigma = 4$ mm
(the exact distribution is unknown).

A quality inspector randomly selects $n = 64$ bolts and measures the **total length**
$S_n = X_1 + X_2 + \cdots + X_{64}$.

**Standard normal CDF values (for reference):**

| $z$ | $\Phi(z)$ |
|-----|-----------|
| 1.00 | 0.8413 |
| 1.50 | 0.9332 |
| 1.75 | 0.9599 |
| 2.00 | 0.9772 |

**(a)** State the distribution that $Z_n = \dfrac{S_n - n\mu}{\sigma\sqrt{n}}$ converges to
as $n \to \infty$, and identify the values of $n\mu$ and $\sigma\sqrt{n}$ for this problem.

**(b)** Use the **Central Limit Theorem** to approximate:

$$P(S_{64} > 3268)$$

**(c)** Use the CLT to find a value $t$ such that $P(S_{64} > t) \approx 0.0668$.

**(d)** The inspector's machine can only handle a total load of 3,232 mm.
What is the approximate probability that the total length of 64 bolts **exceeds** this limit?
Briefly comment on the practical implication.
