# Problem 4 — Intermediate (Revised)

**Topic:** Bernoulli Variance and Variance of the Sum
**Source:** `42_covariance.pdf` (Section 4-2)
**Style:** \[Calculation + Proof\]

---

## Scenario

In a quality control line, each unit is independently inspected. Define:

$$B_i = \begin{cases} 1 & \text{if unit } i \text{ passes inspection} \\ 0 & \text{if unit } i \text{ fails} \end{cases}$$

with $P(B_i = 1) = \dfrac{3}{4}$ for each $i$. Let $S = B_1 + B_2 + B_3$ be the total number of passing units among 3 independent inspections.

---

## Questions

**(a)** Since $B_i \in \{0, 1\}$, note that $B_i^2 = B_i$.
Using the property $cov(X, X) = var(X)$ and the shortcut formula (slide 4):

$$var(B_i) = E[B_i^2] - (E[B_i])^2$$

compute $var(B_i)$.

$$var(B_i) = \underline{\hspace{70pt}}$$

---

**(b)** Applying the general rule $var(X + Y) = var(X) + var(Y) + 2\,cov(X, Y)$ (slide 13) twice to the three-term sum yields:

$$var(S) = \sum_{i=1}^{3} var(B_i) \;+\; \sum_{i \neq j} cov(B_i,\, B_j)$$

Using this formula and the independence of $B_1, B_2, B_3$, compute $var(S)$.

$$var(S) = \underline{\hspace{70pt}}$$

---

**(c)** **[Proof]** Using the covariance definition (slide 3) and the independence result (slide 6), prove that when $X$ and $Y$ are **independent**:

$$var(X + Y) = var(X) + var(Y)$$

*Hint: Start by expanding $var(X+Y) = E\bigl[(X + Y - E[X+Y])^2\bigr]$.*

---

## Answer

**(a)** $var(B_i) = \dfrac{3}{16}$

**(b)** $var(S) = \dfrac{9}{16}$

**(c)** See full proof in the Explanation section below.

---

## Explanation

**Step 1 — Compute $E[B_i]$.**

$$E[B_i] = 1 \cdot \frac{3}{4} + 0 \cdot \frac{1}{4} = \frac{3}{4}$$

**Step 2 — Exploit the Bernoulli identity $B_i^2 = B_i$.**

Because $B_i$ only takes values 0 and 1, $B_i^2 = B_i$, so:

$$E[B_i^2] = E[B_i] = \frac{3}{4}$$

**Step 3 — Part (a): Apply the variance shortcut (slide 4).**

$$var(B_i) = E[B_i^2] - \bigl(E[B_i]\bigr)^2 = \frac{3}{4} - \left(\frac{3}{4}\right)^{\!2} = \frac{3}{4} - \frac{9}{16} = \frac{12}{16} - \frac{9}{16} = \boxed{\frac{3}{16}}$$

> This is the general Bernoulli variance: for $B \sim \text{Bernoulli}(p)$, $var(B) = p(1-p)$.
> Here $p = 3/4$, so $var(B_i) = \tfrac{3}{4} \cdot \tfrac{1}{4} = \tfrac{3}{16}$. ✓

**Step 4 — Part (b): Apply the general variance-of-sum formula (slide 13).**

Applying $var(X+Y) = var(X) + var(Y) + 2\,cov(X,Y)$ twice:

$$var(S) = \sum_{i=1}^{3} var(B_i) + \sum_{i \neq j} cov(B_i, B_j)$$

Since $B_1, B_2, B_3$ are **independent**, by slide 6:

$$cov(B_i, B_j) = E[B_i B_j] - E[B_i]\,E[B_j] = E[B_i]\,E[B_j] - E[B_i]\,E[B_j] = 0 \quad (i \neq j)$$

Therefore all cross-covariance terms vanish:

$$var(S) = 3 \cdot \frac{3}{16} + 6 \cdot 0 = \boxed{\frac{9}{16}}$$

> There are $\binom{3}{2} = 3$ ordered pairs $(i,j)$ with $i < j$, giving $3 \times 2 = 6$ terms in $\sum_{i \neq j}$, all zero.

---

**Step 5 — Part (c): Proof that $var(X+Y) = var(X) + var(Y)$ when $X \perp Y$.**

**Step 5-1.** Start from the definition of variance and expand the square.

$$var(X + Y) = E\bigl[(X + Y - E[X + Y])^2\bigr]$$

Since $E[X+Y] = E[X] + E[Y]$, rewrite as:

$$= E\bigl[\,\bigl((X - E[X]) + (Y - E[Y])\bigr)^2\,\bigr]$$

Expanding the square:

$$= E\bigl[(X - E[X])^2\bigr] + 2\,E\bigl[(X - E[X])(Y - E[Y])\bigr] + E\bigl[(Y - E[Y])^2\bigr]$$

Recognizing each term by their definitions (slides 3–4):

$$= var(X) + 2\,cov(X, Y) + var(Y)$$

**Step 5-2.** Apply the independence result (slide 6).

When $X$ and $Y$ are independent, $E[XY] = E[X]\,E[Y]$. Therefore:

$$cov(X, Y) = E[XY] - E[X]\,E[Y] = E[X]\,E[Y] - E[X]\,E[Y] = 0$$

**Step 5-3.** Substitute back.

$$var(X + Y) = var(X) + 2 \cdot 0 + var(Y) = \boxed{var(X) + var(Y)} \qquad \blacksquare$$
