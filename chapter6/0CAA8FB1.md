# Problem 3 (Hard Level): Call Center Operations and Erlang Waiting Times

Calls arriving at a centralized technical support hotline are modeled as a continuous-time Poisson process with an arrival rate of $\lambda = 4$ calls per minute.

1. An agent logs on and must process exactly 10 calls before taking a break. Let $Y_{10}$ be the total time (in minutes) until the 10th call arrives. State the exact probability density function (PDF) of $Y_{10}$, and calculate its expected value (mean) and variance.
2. When a shift supervisor logs on, there are exactly 64 callers waiting in the queue. Callers are processed one by one by an automated system, and this departure process follows a Poisson process with a rate of $\lambda = 2$ callers per minute. Using the Central Limit Theorem (CLT) approximation, calculate the approximate probability that the supervisor will have to wait **more than 35 minutes** for the queue to completely clear.
