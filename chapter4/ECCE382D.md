# **Problem 2(Intermediate):**  **Decoding Signals via Unbiased Estimators**

##### \[Condition]

##### An IoT acoustic sensor array is deployed to monitor machinery health. The true acoustic intensity is modeled as a continuous random variable $X$, and the distorted sensor recording is modeled as $Y$. 

##### The joint probability density function linking the true machinery signal $X$ and the distorted sensor recording $Y$ is defined by the planar algebraic surface:$f\_{X,Y}(x,y) = x + y$, for the region $0 \\le x \\le 1$ and $0 \\le y \\le 1$ (and 0 everywhere else).

##### The system's embedded Digital Signal Processor (DSP) requires a hardcoded estimator function $\\hat{X}(y)$ that intakes the raw sensor reading $Y=y$ and outputs an optimized prediction of the true acoustic intensity.

##### \[Problem]

##### Derive the mathematical formula for the estimator $\\hat{X}(y) = E\[X|Y=y]$.

##### Prove rigorously that the designed function acts as an unbiased estimator by mathematically demonstrating that $E\[\\hat{X}] = E\[X]$.

