# Problem 3 (Hard)

Customers arrive at a service desk according to a Poisson process with rate $\lambda=6$ per hour. Each arriving customer independently chooses the express line with probability $1/3$ and the regular line with probability $2/3$. Let $T_E$ be the time until the first express-line customer arrives, and let $T_R$ be the time until the first regular-line customer arrives.

Task: Find $P(T_E<T_R)$.

---

# Solution

By Poisson splitting, express customers form a Poisson process with rate

$$
6\cdot \frac13=2,
$$

and regular customers form an independent Poisson process with rate

$$
6\cdot \frac23=4.
$$

Thus,

$$
T_E\sim \operatorname{Exp}(2), \qquad T_R\sim \operatorname{Exp}(4),
$$

independently. For competing exponentials,

$$
P(T_E<T_R)=\frac{2}{2+4}.
$$

Therefore,

$$
P(T_E<T_R)=\frac13.
$$
