# Problem 3 (Hard)

A server processes queries with two different difficulty levels (Y). The difficulty level Y has the following PMF:
- pY(1) = 0.8
- pY(2) = 0.2

The processing time X (ms) depends on the difficulty level Y, given by the following conditional PMFs:
- If Y = 1: pX|Y(10|1) = 0.7 and pX|Y(20|1) = 0.3
- If Y = 2: pX|Y(20|2) = 0.5 and pX|Y(30|2) = 0.5

(a) Derive the marginal PMF pX(x) for all possible values of processing time x.

(b) Calculate the expected processing time E[X] for a single random query.

(c) Let Sn be the sample mean of n = 100 independent queries. Prove that E[Sn] = E[X] and calculate the exact value of var(Sn).