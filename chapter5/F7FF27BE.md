Problem 1 — Easy: A Chebyshev Bound for Sample Means
Topic: Chebyshev's inequality and the Weak Law of Large Numbers
Problem Statement:
Let X1,X2,…,XnX_1, X_2, \ldots, X_n
X1​,X2​,…,Xn​ be i.i.d. random variables with mean μ=5\mu = 5
μ=5 and variance σ2=9\sigma^2 = 9
σ2=9. Define the sample mean

Xˉn=1n∑i=1nXi.\bar{X}_n = \frac{1}{n}\sum_{i=1}^{n} X_i.Xˉn​=n1​i=1∑n​Xi​.
(a) Using Chebyshev's inequality, find the smallest integer nn
n that guarantees

P(∣Xˉn−5∣≥0.5)≤0.05.P\left(|\bar{X}_n - 5| \geq 0.5\right) \leq 0.05.P(∣Xˉn​−5∣≥0.5)≤0.05.
(b) Briefly explain how your result in (a) is consistent with the Weak Law of Large Numbers — specifically, what happens to the probability bound as n→∞n \to \infty
n→∞, and why?
Assumptions / Given Information:

The XiX_i
Xi​ are independent and identically distributed.
The mean and variance are finite and known.
No distributional form (normal, etc.) is assumed — the bound must rely on Chebyshev only.