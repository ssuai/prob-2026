[Hard - Level 3: Conditional Expectation & Bayes' Theorem]
Problem 3: Latency Analysis in Multi-Factor Authentication (MFA)
When a user attempts to log in, the system randomly selects one of two authentication paths:
Path 1 (Prob. 0.8): Standard password authentication. The authentication time T follows a Poisson distribution with a mean of 2 seconds.
Path 2 (Prob. 0.2): Standard password plus biometric authentication. The authentication time T follows a Poisson distribution with a mean of 5 seconds.
1.Find the overall expected authentication time E[T] for an arbitrary login attempt.
2.Suppose a specific login attempt took more than 5 seconds. Derive the formula for the posterior probability that this user went through Path 2. 
(You may leave the final answer in symbolic/formula form.)