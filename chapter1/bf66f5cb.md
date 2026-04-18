
# Easy (Bayes' Theorem)

**Problem Title**
* Bayesian Inference in Machine Learning Spam Classification

**Problem Statement**
* An email service provider at Soongsil University utilizes a Naive Bayes classifier to filter unsolicited mail.
* Based on historical logs, 20% of all incoming emails are classified as spam ($S$).
* The filter identifies the presence of the specific keyword "REWARD" ($R$). 60% of spam emails contain the keyword "REWARD" ($P(R|S) = 0.6$).
* Only 10% of legitimate (ham) emails contain the keyword "REWARD" ($P(R|S^c) = 0.1$).
* If an incoming email contains the keyword "REWARD", what is the calculated probability that it is spam?

**Mandatory Solution Protocol**
* To receive full credit, **students must construct a Tree Diagram**.
* The root **is required to** branch into $S$ (0.2) and $S^c$ (0.8). Each of these branches then splits into $R$ and $R^c$ with the given conditional probabilities.
* The final calculation must clearly show the division of the "Spam and Reward" path by the sum of all "Reward" paths (Total Probability).

**Professor's Insight**
* This problem demonstrates the importance of "prior probability" in decision-making. Even though the keyword "REWARD" is six times more likely in spam than in ham, the overall probability of it being spam given the word is only 60% because legitimate emails are much more frequent.
* This highlights why high false-positive rates can occur in ML models if priors are not carefully considered.