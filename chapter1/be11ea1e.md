---
title: "Bayes' Rule - Intermediate"
subject: "Probability & Statistics"
textbook: "Bertsekas & Tsitsiklis, Introduction to Probability, 2nd Ed."
chapter: "Ch.1 — Sample Space and Probability (Section 1.4)"
difficulty: "Intermediate"
language: "Korean + English"
---

━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━
[Difficulty: Intermediate]  |  [Topic: Bayes' Rule]  |  [Textbook Ref: Bertsekas Ch.1, Section 1.4]
━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━

## Problem

🇰🇷 **Korean**

한 공장에서 세 대의 기계 $M_1$, $M_2$, $M_3$이 제품을 생산한다. 전체 생산량에서 각 기계가 차지하는 비율과, 각 기계가 생산하는 불량품의 비율은 다음과 같다.

| 기계 | 생산 비율 | 불량률 |
|------|-----------|--------|
| $M_1$ | $50\%$ | $2\%$ |
| $M_2$ | $30\%$ | $5\%$ |
| $M_3$ | $20\%$ | $3\%$ |

생산된 제품 중 한 개를 무작위로 선택하였더니 **불량품**이었다.

**(1)** 사건 $D$ = {선택된 제품이 불량품}, $A_i$ = {선택된 제품이 기계 $M_i$에서 생산됨} ($i = 1, 2, 3$)으로 정의하고, 주어진 확률들을 모두 명시하여라.

**(2)** 전확률 공식(Total Probability Theorem)을 이용하여 $P(D)$를 구하여라.

**(3)** 베이즈 공식을 적용하여, 불량품이 기계 $M_2$에서 생산되었을 확률 $P(A_2 \mid D)$를 구하여라.

**(4)** $P(A_1 \mid D)$, $P(A_2 \mid D)$, $P(A_3 \mid D)$의 합이 1임을 확인하고, 이로부터 어떤 기계가 불량품의 가장 유력한 원인인지 판단하여라.

---

🇺🇸 **English**

A factory produces items using three machines $M_1$, $M_2$, and $M_3$. The fraction of total output produced by each machine and the defect rate of each machine are given in the table below.

| Machine | Share of output | Defect rate |
|---------|----------------|-------------|
| $M_1$   | $50\%$         | $2\%$       |
| $M_2$   | $30\%$         | $5\%$       |
| $M_3$   | $20\%$         | $3\%$       |

One item is selected at random from the total output and is found to be **defective**.

**(1)** Define the event $D$ = {the selected item is defective} and the events $A_i$ = {the selected item was produced by machine $M_i$} for $i = 1, 2, 3$. List all given probabilities explicitly.

**(2)** Using the Total Probability Theorem, compute $P(D)$.

**(3)** Apply Bayes' Rule to find $P(A_2 \mid D)$, the probability that the defective item was produced by machine $M_2$.

**(4)** Verify that $P(A_1 \mid D) + P(A_2 \mid D) + P(A_3 \mid D) = 1$, and identify which machine is the most likely source of the defective item.

---

## Solution

> **[Step 1] Model Setup**
>
> The experiment is: select one item at random from the entire factory output.
>
> The events $A_1, A_2, A_3$ form a **partition** of the sample space $\Omega$, since every item is produced by exactly one machine and
>
> $$A_1 \cup A_2 \cup A_3 = \Omega, \qquad A_i \cap A_j = \emptyset \text{ for } i \neq j.$$
>
> The given probabilities are:
>
> $$P(A_1) = 0.50, \quad P(A_2) = 0.30, \quad P(A_3) = 0.20.$$
>
> $$P(D \mid A_1) = 0.02, \quad P(D \mid A_2) = 0.05, \quad P(D \mid A_3) = 0.03.$$
>
> We note that $P(A_1) + P(A_2) + P(A_3) = 0.50 + 0.30 + 0.20 = 1.00$, confirming that $\{A_1, A_2, A_3\}$ is a valid partition.

---

> **[Step 2] Key Observation / Diagram**
>
> The problem has a natural sequential (two-stage) structure: first a machine is "selected" (with probabilities $P(A_i)$), then the machine produces a defective or non-defective item. A probability tree makes this explicit.
>
> ```
>                      Start
>              ________|________
>             /         |       \
>        M₁ (0.50)  M₂ (0.30)  M₃ (0.20)
>          /   \       /   \      /   \
>        D    Dᶜ    D    Dᶜ   D    Dᶜ
>      0.02  0.98  0.05  0.95  0.03  0.97
>
>  Leaf prob:
>   M₁∩D: 0.50×0.02 = 0.0100
>   M₂∩D: 0.30×0.05 = 0.0150
>   M₃∩D: 0.20×0.03 = 0.0060
> ```
>
> The event $D$ consists of the three highlighted leaves. The Total Probability Theorem sums their probabilities, and Bayes' Rule identifies the fraction attributable to each machine.

---

> **[Step 3] Derivation — Part (2): Total Probability Theorem**
>
> Because $\{A_1, A_2, A_3\}$ is a partition of $\Omega$ and $P(A_i) > 0$ for all $i$, the **Total Probability Theorem** gives:
>
> $$P(D) = \sum_{i=1}^{3} P(A_i)\,P(D \mid A_i).$$
>
> Substituting the given values:
>
> $$P(D) = P(A_1)\,P(D \mid A_1) + P(A_2)\,P(D \mid A_2) + P(A_3)\,P(D \mid A_3)$$
>
> $$= (0.50)(0.02) + (0.30)(0.05) + (0.20)(0.03)$$
>
> $$= 0.0100 + 0.0150 + 0.0060$$
>
> $$= 0.0310.$$

---

> **[Step 4] Derivation — Part (3): Bayes' Rule**
>
> **Bayes' Rule** states that for any $i \in \{1,2,3\}$,
>
> $$P(A_i \mid D) = \frac{P(A_i)\,P(D \mid A_i)}{P(D)}.$$
>
> For $i = 2$:
>
> $$P(A_2 \mid D) = \frac{P(A_2)\,P(D \mid A_2)}{P(D)} = \frac{(0.30)(0.05)}{0.0310} = \frac{0.0150}{0.0310}.$$
>
> Computing the fraction:
>
> $$P(A_2 \mid D) = \frac{15}{31} \approx 0.4839.$$

---

> **[Step 5] Computation — Part (4): All posterior probabilities**
>
> Applying Bayes' Rule to all three machines:
>
> $$P(A_1 \mid D) = \frac{(0.50)(0.02)}{0.0310} = \frac{0.0100}{0.0310} = \frac{10}{31} \approx 0.3226,$$
>
> $$P(A_2 \mid D) = \frac{(0.30)(0.05)}{0.0310} = \frac{0.0150}{0.0310} = \frac{15}{31} \approx 0.4839,$$
>
> $$P(A_3 \mid D) = \frac{(0.20)(0.03)}{0.0310} = \frac{0.0060}{0.0310} = \frac{6}{31} \approx 0.1935.$$
>
> **Verification of the partition property:**
>
> $$P(A_1 \mid D) + P(A_2 \mid D) + P(A_3 \mid D) = \frac{10}{31} + \frac{15}{31} + \frac{6}{31} = \frac{31}{31} = 1. \checkmark$$
>
> This confirms that the posterior probabilities, conditioned on $D$, form a valid probability distribution over the partition $\{A_1, A_2, A_3\}$.

---

> **[Step 6] Verification and Conclusion**
>
> All posterior probabilities lie in $[0, 1]$ and sum to 1, satisfying the axioms. $\checkmark$
>
> Comparing the three posterior probabilities:
>
> $$P(A_2 \mid D) = \frac{15}{31} \approx 0.484 \;>\; P(A_1 \mid D) \approx 0.323 \;>\; P(A_3 \mid D) \approx 0.194.$$
>
> Although machine $M_2$ accounts for only 30% of production, its higher defect rate (5%) causes it to be the **most likely source** of a randomly drawn defective item.
>
> *Intuition:* Bayes' Rule "updates" our prior belief ($P(A_i)$ = machine share) with the likelihood of producing a defect ($P(D \mid A_i)$ = defect rate). Machine $M_2$ gains the most probability mass after the update because its defect rate is disproportionately high relative to its output share.

---

**Answers:**

$$P(D) = 0.0310 = \frac{31}{1000}.$$

$$P(A_2 \mid D) = \frac{15}{31} \approx 0.48.$$

$$P(A_1 \mid D) = \frac{10}{31} \approx 0.32, \quad P(A_2 \mid D) = \frac{15}{31} \approx 0.48, \quad P(A_3 \mid D) = \frac{6}{31} \approx 0.19.$$

**Machine $M_2$ is the most likely source of the defective item.**
