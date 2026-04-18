# Medium Problem — Total Probability with Conditional PDF

## Problem

The metro train arrives at the station every quarter hour starting at 6:00 AM. You walk into the station every morning between 7:10 and 7:30 AM, with the time in this interval being a uniform random variable. What is the PDF of the time you have to wait for the first train to arrive?

Let $X$ be your arrival time, and $Y$ be the waiting time. Define:

$$A = \{7:10 \leq X \leq 7:15\} = \{\text{you board the 7:15 train}\}$$
$$B = \{7:15 < X \leq 7:30\} = \{\text{you board the 7:30 train}\}$$

Find $f_Y(y)$ using the total probability theorem:

$$f_Y(y) = P(A)f_{Y|A}(y) + P(B)f_{Y|B}(y)$$

