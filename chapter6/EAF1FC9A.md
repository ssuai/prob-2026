# Problem 2 (Intermediate)

Emails arrive to an inbox according to a Poisson process with rate $\lambda=3$ emails per hour. The inbox has already had no emails for the first 20 minutes of the hour. Let $T$ be the additional waiting time, in hours, until the next email arrives.

Task: Find $P(T>1/2 \mid \text{no email arrived in the first 20 minutes})$.

---

# Solution

In a Poisson process, the waiting time until the next arrival is memoryless.

Thus the past 20 minutes do not change the distribution of the additional waiting time:

$$
T \sim \operatorname{Exp}(3).
$$

Therefore,

$$
P(T>1/2)=e^{-3(1/2)}.
$$

Hence,

$$
P(T>1/2 \mid \text{no email arrived in the first 20 minutes})=e^{-3/2}.
$$
