Here's a group project where I participated during the Mathematical Modelling course.
###Problem 1
Desert animals have to cover long distances between water sources. How does the jump height of an animal depend on its size? (Hint: The critical load that a relatively short column can withstand is proportional to its cross-sectional area. Assume that the answer depends solely on bone strength, and that muscle strength is matched precisely to the strength of the bones.)
Solution:

| Symbol | Quantity | Dimension |
| :--- | :--- | :--- |
| $h$ | Jump height | $[L]$ |
| $m$ | Animal mass | $[M]$ |
| $F$ | Jump force | $[MLT^{-2}]$ |
| $V$ | Animal volume | $[L^3]$ |
| $g$ | Acceleration due to gravity | $[LT^{-2}]$ |

$$\Pi_i = F^\alpha h^\beta m^\gamma V^\delta g^\varepsilon$$

For dimensionless products:

$$\begin{cases} 
\alpha = -\gamma \\ 
\alpha = -\varepsilon \\ 
\beta = -3\delta 
\end{cases}$$

When: 
$$\begin{cases} 
\alpha = 1 \\ 
\beta = 1 
\end{cases} \Rightarrow \begin{cases} \gamma = \varepsilon = 1 \\ \delta = -\frac{1}{3} \end{cases} \Rightarrow \Pi_1 = \frac{mgh}{FV^{\frac{1}{3}}}$$

When: 
$$\begin{cases} \alpha = 1 \\ \beta = 0 \end{cases} \Rightarrow \begin{cases} \gamma = \varepsilon = -1 \\ \delta = 0 \end{cases} \Rightarrow \Pi_2 = \frac{F}{mg}$$

$$h = \frac{FV^{\frac{1}{3}}}{mg} f\left(\frac{F}{mg}\right)$$
