# Problem 2 — Random-Bias Coin: Conditional Expectation Meets Covariance

**Difficulty:** Intermediate

---

## Problem Statement

A coin has a *random* bias $Y \sim \mathrm{Uniform}[0, 1]$. Once $Y$ is realized, the coin is flipped $n$ times independently, and $X$ denotes the number of heads. Thus

$$
X \mid (Y = y) \sim \mathrm{Binomial}(n, y).
$$

You may use $E[Y] = \tfrac{1}{2}$, $\mathrm{var}(Y) = \tfrac{1}{12}$, and $\mathrm{var}(X \mid Y) = nY(1-Y)$ without re-derivation.

### Sub-parts

**(a)** Compute $E[X]$ using the law of total expectation.

**(b)** Compute $\mathrm{var}(X)$ using the total-variance identity
$$
\mathrm{var}(X) = E[\mathrm{var}(X \mid Y)] + \mathrm{var}(E[X \mid Y]).
$$
Show each of the two terms separately.

**(c)** Compute $\mathrm{cov}(X, Y)$ and the correlation coefficient $\rho(X, Y)$.

**(d)** For $n = 10$, evaluate $E[X]$, $\mathrm{var}(X)$, $\mathrm{cov}(X, Y)$, and $\rho(X, Y)$ as numerical values.

