### Problem 02 — Difficulty: Intermediate
**Topic**: Poisson Merging, Splitting, Erlang, Independence

A hospital emergency department receives patients from two independent sources. Walk-in patients arrive according to a Poisson process at rate $\lambda_1 = 3$ patients/hr, and ambulance patients arrive according to a Poisson process at rate $\lambda_2 = 1$ patient/hr. Every patient arriving at the emergency department, regardless of their source, is independently classified as a critical patient requiring immediate surgery with probability $p = 0.2$, or a non-critical patient requiring only standard care with probability $0.8$.

**(a)** It is currently 9:00 AM. Find the probability that no patients at all (walk-in or ambulance) arrive between 9:00 AM and 9:30 AM.

**(b)** Find the probability that exactly 2 critical patients arrive between 9:00 AM and 10:00 AM.

**(c)** The surgical team begins standby at 9:00 AM. Let $Y_5$ denote the waiting time until the 5th critical patient arrives.

1. Identify the distribution of $Y_5$ and write its PDF.
2. Compute $E[Y_5]$ and $\text{Var}(Y_5)$.
3. Find $P(Y_5 > 8)$.

**(d)** The head surgeon has declared: "We will activate the full surgical team only if at least 3 critical patients arrive within the next 2 hours." Starting from 9:00 AM, find the probability that the full surgical team is activated. Express your answer as an exact formula and compute the numerical value.