# Problem 3 (Hard)

An online store packs $100$ orders in one hour. Let $X_i$ be the packing time, in seconds, for the $i$th order. Assume $X_1,\dots,X_{100}$ are i.i.d. with

$$
E[X_i]=50,
\qquad
\operatorname{Var}(X_i)=144.
$$

Let

$$
S=X_1+\cdots+X_{100}.
$$

Task: Use the central limit theorem to approximate $P(4880\le S\le 5240)$.

---

# Solution

For the total packing time,

$$
E[S]=100\cdot 50=5000,
\qquad
\operatorname{Var}(S)=100\cdot 144=14400.
$$

Thus, $\sigma_S=120$. By the central limit theorem,

$$
\frac{S-5000}{120}\approx N(0,1).
$$

Therefore,

$$
P(4880\le S\le 5240)
=P\left(-1\le \frac{S-5000}{120}\le 2\right).
$$

Hence,

$$
P(4880\le S\le 5240)\approx \Phi(2)-\Phi(-1).
$$

Using standard normal values,

$$
\Phi(2)-\Phi(-1)\approx 0.9772-0.1587=0.8185.
$$
