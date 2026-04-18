# **Problem 2(Intermediate): Exponential Distributions in Hardware Reliability**

###### **Topic Category: Continuous Random Variables \& PDFs/CDFsDifficulty**

###### **Level: Intermediate**

###### **Domain Context: Distributed Storage / Server Component Lifespan**



##### **Problem Context and Statement**

* In a massive-scale distributed cloud storage facility, hardware telemetry indicates that mechanical and solid-state drives fail continuously over time. Network monitoring systems determine that a specific batch of legacy enterprise hard disk drives exhibits a failure profile that strictly follows an Exponential distribution.
* To simplify the mathematical scale for the predictive telemetry dashboard, the continuous time-to-failure $T$ is measured in "Hardware Epochs." The rate of failure for this specific batch is determined to be exactly $\\lambda = 1$ failure per epoch.
* The probability density function (PDF) representing the time to failure $T$ is given by:
* $$f\_T(t) = \\begin{cases} e^{-t}, \& \\text{if } t \\ge 0 \\\\ 0, \& \\text{otherwise} \\end{cases}$$



##### **Questions for the Student:**

**Part A (Testing Normalization and CDF Accumulation)**

* systems engineer requires a script that triggers a critical alert if a drive fails precisely between Epoch 1 and Epoch 2. Calculate the exact mathematical probability that a randomly selected drive fails within this specific continuous time window, $P(1 \\le T \\le 2)$. You must demonstrate the definite integral calculation to receive full credit.

**Part B (Testing the Memoryless Property)**

* A particular hard drive has successfully operated without any faults for exactly 1 Epoch (meaning it is known definitively that $T > 1$). Calculate the conditional probability that this specific drive will fail before reaching Epoch 2. Compare this mathematical result to the answer derived in Part A, and articulate the engineering implications of this property for scheduling preventative hardware replacements in the data center.

