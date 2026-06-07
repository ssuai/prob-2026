# Problem 3: CLT Approximation for Matrix Optimization Bottleneck

**Problem Statement:**
You are building a custom linear algebra module to optimize an AI model. A critical step in the pipeline involves performing a batch of $n = 6000$ independent and identically distributed (i.i.d.) QR decompositions. Let $X_i$ be the time (in milliseconds) it takes the CPU to process the $i$-th QR decomposition. 

The processing time $X_i$ is modeled by a continuous random variable with the following probability density function (PDF):
$$f_X(x) = \begin{cases} \frac{3}{8}x^2 & \text{for } 0 < x < 2 \\ 0 & \text{otherwise} \end{cases}$$
Let $S_{6000} = \sum_{i=1}^{6000} X_i$ be the total time required to process the entire batch of 6000 matrices.

**Your Task:**
Using the Central Limit Theorem (CLT), approximate the probability that the total processing time for the batch exceeds $9045$ milliseconds, i.e., $P(S_{6000} > 9045)$. (Assume $\Phi(1.5) \approx 0.9332$ from the Standard Normal CDF table).