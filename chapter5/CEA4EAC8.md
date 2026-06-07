# **Problem3 (Hard): Asymptotic Sensor Stabilization (Law of Large Numbers)** 

#### 

#### **\[Condition]**

#### A 5G URLLC Industrial IoT network monitors the kinematic alignment of a high-speed factory robotic arm using an infinite stream of continuous sensor telemetry data. To maintain absolute operational safety and prevent mechanical destruction, the sequence of sensor error readings $\\{X\_1, X\_2, \\dots, X\_n\\}$ must mathematically stabilize to a mean of $0$ over time.Consider a theoretical, independent sensor error sequence where the physical probability of a transient calibration fault scales dynamically with the sample size as time approaches infinity. Specifically, for the $n$-th reading in the stream:



##### $P(X\_n = n) = \\frac{1}{2n^2}$

##### $P(X\_n = -n) = \\frac{1}{2n^2}$

##### $P(X\_n = 0) = 1 - \\frac{1}{n^2}$



#### **\[Problem]** 

#### Prove mathematically that the sequence satisfies the specific convergence condition for the WLLN as $n \\rightarrow \\infity$.

