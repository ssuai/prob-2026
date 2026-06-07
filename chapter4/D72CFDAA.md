# **Problem3 (Hard): Profiling Delay Distributions via MGF Inversion**

#### 

#### **\[Condition]**

#### A profiling tool is analyzing the end-to-end packet routing latency across a software-defined network (SDN). The total latency is a hybrid variable consisting of a deterministic physical propagation delay and a randomized queueing delay. The tool reports that the Moment Generating Function (MGF) of the total routing delay $Z$ (measured in milliseconds) is precisely defined as:

#### $M\_Z(s) = \\frac{2}{2-s} e^{5s}$, for the region $s < 2$.

#### **\[Problem]**

#### Using the property of MGF differentiation, calculate the expected value of the total routing delay, $E\[Z]$.

#### Using derived distribution properties and MGF pattern recognition, invert the transform to identify and mathematically write the exact piecewise probability density function $f\_Z(z)$ of the system's end-to-end delay.

