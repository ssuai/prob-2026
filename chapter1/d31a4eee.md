## Problem 3 (Hard)

A company screens job applicants using two stages.

First, each applicant belongs to exactly one of three background groups:

- $G_1$: applicants with no prior internship experience, 40% of all applicants
- $G_2$: applicants with one internship, 35% of all applicants
- $G_3$: applicants with two or more internships, 25% of all applicants

Within each group, the proportion of applicants who are actually well-qualified for the job is:

- $P(Q \mid G_1)=0.10$
- $P(Q \mid G_2)=0.35$
- $P(Q \mid G_3)=0.60$

Each applicant first takes Screening Test A. The probability of passing Test A is:

- $P(A \mid Q,G_1)=0.80$, $P(A \mid Q^c,G_1)=0.30$
- $P(A \mid Q,G_2)=0.85$, $P(A \mid Q^c,G_2)=0.25$
- $P(A \mid Q,G_3)=0.90$, $P(A \mid Q^c,G_3)=0.20$

Only applicants who pass Test A are interviewed. Among applicants who reach the interview stage, the probability of passing the interview is:

- $P(B \mid Q)=0.90$
- $P(B \mid Q^c)=0.20$

Assume that, conditional on whether the applicant is actually well-qualified, the interview result is independent of both the background group and the Test A result.

Let $Q$ be the event that a randomly selected applicant is actually well-qualified, and let $A$ and $B$ be the events that the applicant passes Test A and the interview, respectively.

**Task:** A randomly selected applicant passed both Test A and the interview. Determine the probability that this applicant is actually well-qualified.
