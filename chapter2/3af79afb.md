## Problem
A cloud computing system processes user tasks. The system load varies, and the number of active nodes processing tasks is a random variable $Y$. Based on historical data, $Y$ takes the value of either $10$ nodes (Low load) or $50$ nodes (High load), with the marginal PMF:
$p_Y(10) = 0.6$, $p_Y(50) = 0.4$.

The processing time of a single task, $X$ (in milliseconds), depends heavily on the system load $Y$. The conditional PMF of $X$ given $Y$, $p_{X|Y}(x|y)$, is given as follows:
- If $Y = 10$, $X$ is extremely fast: $p_{X|Y}(1 \mid 10) = 0.8$, and $p_{X|Y}(5 \mid 10) = 0.2$.
- If $Y = 50$, $X$ becomes slower due to congestion: $p_{X|Y}(1 \mid 50) = 0.3$, and $p_{X|Y}(5 \mid 50) = 0.7$.

To account for network routing overhead, the total time experienced by the end-user is modeled as a new random variable $Z = 2X + 3$ (in ms).
1) Using the multiplication rule and marginalization, find the unconditional (marginal) PMF of the processing time $X$, $p_X(x)$.
2) Calculate the expected value $E[Z]$ and the variance $Var[Z]$ of the total user experienced time.