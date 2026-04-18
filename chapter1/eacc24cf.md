# Hard Problem (Bayes' Theorem)

A factory has three machines M1, M2, M3.

M1 produces 40% of items, defect rate = 1%
M2 produces 35% of items, defect rate = 3%
M3 produces 25% of items, defect rate = 6%

If a randomly selected item is defective, find the probability that it was produced by M3.

## Solution

Let D = defective

P(M1)=0.40, P(D|M1)=0.01
P(M2)=0.35, P(D|M2)=0.03
P(M3)=0.25, P(D|M3)=0.06

Total probability:
P(D) =
0.40×0.01 + 0.35×0.03 + 0.25×0.06
= 0.004 + 0.0105 + 0.015
= 0.0295

Bayes theorem:
P(M3|D) =
(0.25×0.06) / 0.0295
= 0.015 / 0.0295 ≈ 0.508
