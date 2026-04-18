### The Scenario
A cloud computing cluster (like the ones you might use for your computer vision or machine learning projects) consists of $n = 5$ independent server nodes.
- Each node has a probability $p = 0.2$ of failing during a high-traffic event.
- The system is "Fault-Tolerant," meaning the cluster only crashes if more than 2 nodes fail simultaneously.

### The Problem - Intermediate
1. What is the probability that exactly 2 nodes fail? 
2. What is the probability that the entire cluster crashes?
3. If the administrator installs a "Backup Controller" that only activates if exactly 3 nodes have failed, what is the probability that this controller is triggered?