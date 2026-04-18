---
title: "Discrete Random Variables: Conditioning and Independence - Easy"
subject: "Probability & Statistics"
textbook: "Bertsekas & Tsitsiklis, Introduction to Probability, 2nd Ed."
chapter: "Ch.2 — Discrete Random Variables, §2.6–2.7"
difficulty: "Easy"
language: "Korean + English"
---

━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━
[Difficulty: Easy]  |  [Topic: Conditioning and Independence of Discrete RVs]  |  [Textbook Ref: Bertsekas Ch.2, Section 2.6–2.7]
━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━

## Problem

🇰🇷 **Korean**

공정한 동전을 두 번 던지는 실험을 생각하자.
확률변수 $X$를 첫 번째 던지기에서 앞면(H)이 나오면 $X = 1$, 뒷면(T)이 나오면 $X = 0$으로 정의한다.
확률변수 $Y$를 두 번째 던지기에서 앞면(H)이 나오면 $Y = 1$, 뒷면(T)이 나오면 $Y = 0$으로 정의한다.

두 던지기는 서로 독립이며, 각 결과의 확률은 $\frac{1}{2}$이다.

다음을 구하라.

1. $X$와 $Y$ 각각의 확률질량함수(PMF) $p_X(x)$와 $p_Y(y)$를 명시하라.
2. $X = 1$이라는 조건 하에서 $Y$의 조건부 PMF $p_{Y \mid X}(y \mid 1)$를 구하고, 이 결과가 $X$와 $Y$의 독립성과 어떻게 일치하는지 설명하라.
3. 사건 $A = \{X = 1\}$과 사건 $B = \{Y = 1\}$이 독립임을 $P(A \cap B) = P(A)\cdot P(B)$ 조건을 직접 확인하여 증명하라.

---

🇺🇸 **English**

Consider the experiment of flipping a fair coin twice.
Define the random variable $X$ to be $1$ if the first flip results in heads (H) and $0$ if it results in tails (T).
Define the random variable $Y$ to be $1$ if the second flip results in heads (H) and $0$ if it results in tails (T).

The two flips are independent, and each outcome has probability $\frac{1}{2}$.

Answer the following:

1. State the probability mass functions (PMFs) $p_X(x)$ and $p_Y(y)$ explicitly.
2. Find the conditional PMF $p_{Y \mid X}(y \mid 1)$, and explain how this result is consistent with the independence of $X$ and $Y$.
3. Prove that the events $A = \{X = 1\}$ and $B = \{Y = 1\}$ are independent by directly verifying $P(A \cap B) = P(A)\cdot P(B)$.

---

## Solution

> **[Step 1] Model Setup**
>
> The sample space is:
> $$\Omega = \{HH,\ HT,\ TH,\ TT\}$$
> with each outcome equally likely, so $P(\omega) = \frac{1}{4}$ for each $\omega \in \Omega$.
>
> The random variables are defined as:
> $$X(\omega) = \begin{cases} 1 & \text{if the first flip is H} \\ 0 & \text{if the first flip is T} \end{cases}, \qquad Y(\omega) = \begin{cases} 1 & \text{if the second flip is H} \\ 0 & \text{if the second flip is T} \end{cases}$$

---

> **[Step 2] Key Observation / Diagram**
>
> Visualizing the joint sample space with a probability tree:
>
> ```
>               [Start]
>              /        \
>       P(H)=1/2     P(T)=1/2
>       X=1              X=0
>       /    \           /    \
>    Y=1    Y=0       Y=1    Y=0
>   P=1/4  P=1/4    P=1/4  P=1/4
>   (HH)   (HT)    (TH)   (TT)
> ```
>
> Since each branch is independent, the joint probability factorizes across every combination.
> The key insight from §2.7: **two discrete RVs $X$ and $Y$ are independent if and only if**
> $$p_{X,Y}(x,y) = p_X(x)\cdot p_Y(y) \quad \text{for all } x, y$$

---

> **[Step 3] Derivation**
>
> ### Part (1) — PMFs of $X$ and $Y$
>
> Collecting outcomes from the tree:
> $$p_X(x) = \begin{cases} \frac{1}{2} & x = 0 \\ \frac{1}{2} & x = 1 \\ 0 & \text{otherwise} \end{cases} \qquad p_Y(y) = \begin{cases} \frac{1}{2} & y = 0 \\ \frac{1}{2} & y = 1 \\ 0 & \text{otherwise} \end{cases}$$
>
> Verification: $\sum_x p_X(x) = \frac{1}{2} + \frac{1}{2} = 1$ ✓, $\sum_y p_Y(y) = 1$ ✓
>
> ---
>
> ### Part (2) — Conditional PMF $p_{Y \mid X}(y \mid 1)$
>
> By the definition of the conditional PMF (Bertsekas §2.6):
> $$p_{Y \mid X}(y \mid 1) = \frac{p_{X,Y}(1, y)}{p_X(1)}$$
>
> The joint PMF values involving $X = 1$ (from the tree, outcomes $HH$ and $HT$):
> $$p_{X,Y}(1, 1) = P(HH) = \frac{1}{4}, \qquad p_{X,Y}(1, 0) = P(HT) = \frac{1}{4}$$
>
> Since $p_X(1) = \frac{1}{2}$:
> $$p_{Y \mid X}(1 \mid 1) = \frac{1/4}{1/2} = \frac{1}{2}, \qquad p_{Y \mid X}(0 \mid 1) = \frac{1/4}{1/2} = \frac{1}{2}$$
>
> Therefore:
> $$p_{Y \mid X}(y \mid 1) = p_Y(y) \quad \text{for all } y$$
>
> This confirms that conditioning on $X = 1$ does **not** change the distribution of $Y$ — the defining property of independence (§2.7).
>
> ---
>
> ### Part (3) — Direct Verification of Independence
>
> Let $A = \{X = 1\}$ and $B = \{Y = 1\}$. Then:
> $$P(A) = p_X(1) = \frac{1}{2}, \qquad P(B) = p_Y(1) = \frac{1}{2}$$
>
> The intersection $A \cap B = \{X = 1\} \cap \{Y = 1\} = \{HH\}$, so:
> $$P(A \cap B) = P(HH) = \frac{1}{4}$$
>
> Check independence condition:
> $$P(A)\cdot P(B) = \frac{1}{2} \cdot \frac{1}{2} = \frac{1}{4} = P(A \cap B) \quad \checkmark$$
>
> Therefore $A$ and $B$ are independent. $\blacksquare$

---

> **[Step 4] Computation**
>
> | Quantity | Value |
> |---|---|
> | $p_X(1) = p_X(0)$ | $\dfrac{1}{2}$ |
> | $p_{Y \mid X}(1 \mid 1)$ | $\dfrac{1}{2} = p_Y(1)$ |
> | $P(A \cap B)$ | $\dfrac{1}{4}$ |
> | $P(A)\cdot P(B)$ | $\dfrac{1}{4}$ |

---

> **[Step 5] Verification**
>
> - All PMF values lie in $[0, 1]$ and sum to 1 ✓
> - $p_{Y \mid X}(y \mid 1)$ sums to $\frac{1}{2} + \frac{1}{2} = 1$ ✓
> - $P(A \cap B) = P(A)\cdot P(B)$ confirmed ✓
> - Four joint probabilities $\frac{1}{4}\times 4 = 1$ ✓

**Answer:**
$$p_{Y \mid X}(y \mid 1) = p_Y(y) = \frac{1}{2} \text{ for } y \in \{0,1\}, \qquad P(A \cap B) = \frac{1}{4} = P(A)\cdot P(B)$$

$X$ and $Y$ are **independent** discrete random variables.
