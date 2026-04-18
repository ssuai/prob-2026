# 3.md

### [Hard Level] Question 3: Data Pipeline Processing Times (25 Points)

A machine learning data pipeline consists of two sequential phases: Data Preprocessing and Model Training. 
Let the discrete random variable $X$ represent the Data Preprocessing Time (in seconds).
Let the discrete random variable $Y$ represent the Model Training Time (in seconds).

The Joint Probability Mass Function (Joint PMF), $p_{X,Y}(x,y)$, of the two processing times is given by the following table:

| $X \backslash Y$ | $Y = 2$ | $Y = 4$ | $Y = 6$ |
| :--- | :---: | :---: | :---: |
| **$X = 1$** | $\frac{2}{20}$ | $\frac{3}{20}$ | $\frac{1}{20}$ |
| **$X = 2$** | $\frac{4}{20}$ | $\frac{4}{20}$ | $\frac{2}{20}$ |
| **$X = 3$** | $\frac{1}{20}$ | $\frac{1}{20}$ | $\frac{2}{20}$ |

**(3-a)** [Marginal PMF] Calculate the Marginal PMF for the preprocessing time, $p_X(x)$, for all possible values of $X$. Then, calculate the Marginal PMF for the training time, $p_Y(y)$, for all possible values of $Y$.

**(3-b)** [Independence] Are the random variables $X$ and $Y$ strictly independent? Mathematically prove your answer by checking the condition for independence using the joint and marginal PMFs. 

**(3-c)** [Conditional Expectation] Suppose the system monitoring tool records that the preprocessing phase took exactly $2$ seconds (i.e., $X = 2$). First, find the Conditional PMF of the training time, $p_{Y|X}(y|2)$. Then, use it to calculate the Conditional Expectation of the training time, $E[Y|X=2]$.

**(3-d)** [Sum of RVs] Let the random variable $Z$ represent the total pipeline processing time, such that $Z = X + Y$. Calculate the expected total processing time, $E[Z]$.