# Hard Problem: Random Variable Nested Transformation

### Situation
The Probability Mass Function (PMF) of a discrete random variable $X$ is given below:

**PMF Conditions for $X$:**
* **Sample Space**: $x \in \{-2, -1, 0, 1, 2, 3\}$
* **Probability Law**: $p_X(x) = \frac{1}{6}$ for all $x$ (Discrete Uniform Distribution)

Define a new random variable $W$ by performing the following two-step nested transformation, $Z = h(g(X))$
1. **Intermediate Transformation ($Y$):** $Y = g(X) = X^2 - X$
2. **Final Transformation ($Z$):** $Z = h(Y) = \min(Y, 2)$
3. **Linear Transformation ($W$):** $W = 3Z + 1$ 

---

### Question
Find the **variance of $W$**, denoted as **$var(W)$**.
