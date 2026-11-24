Here's a group project where I participated during the Mathematical Modelling course.
# Problem 1
Desert animals have to cover long distances between water sources. How does the jump height of an animal depend on its size? (Hint: The critical load that a relatively short column can withstand is proportional to its cross-sectional area. Assume that the answer depends solely on bone strength, and that muscle strength is matched precisely to the strength of the bones.) 

## Solution: 

### Model 1:

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
\end{cases} 
\Rightarrow 
\begin{cases} 
\gamma = \varepsilon = 1 \\ 
\delta = -\frac{1}{3} \end{cases} 
\Rightarrow 
\Pi_1 = \frac{mgh}{FV^{\frac{1}{3}}}$$

When: 

$$\begin{cases} 
\alpha = 1 \\ 
\beta = 0 
\end{cases} 
\Rightarrow 
\begin{cases} 
\gamma = \varepsilon = -1 \\ 
\delta = 0 
\end{cases} 
\Rightarrow 
\Pi_2 = \frac{F}{mg}$$

$$h = \frac{FV^{\frac{1}{3}}}{mg} f\left(\frac{F}{mg}\right)$$

### Model 2:

| Symbol | Quantity | Dimension |
| :--- | :--- | :--- |
| $h$ | Jump height | $[L]$ |
| $m$ | Animal mass | $[M]$ |
| $F$ | Jump force | $[MLT^{-2}]$ |
| $V$ | Animal volume | $[L^3]$ |
| $g$ | Acceleration due to gravity | $[LT^{-2}]$ |
| $A$ | Cross-sectional area | $[L^2]$ |

$$\Pi_i = F^\alpha h^\beta m^\gamma V^\delta g^\varepsilon A^\zeta$$

For dimensionless products:

$$\begin{cases}
\alpha + \gamma = 0 \\
\alpha + \varepsilon + 3\delta + 2\zeta = -\beta \\
2\alpha = -2\varepsilon
\end{cases}$$

For $\zeta = 0$, we take $\Pi_1$ and $\Pi_2$ as from the 1st model.

For $\zeta = 1$, we have:

$$\begin{cases} 
\alpha = 0 \\ 
\beta = 0 
\end{cases} 
\Rightarrow 
\begin{cases} 
\gamma = 0 \\ 
\varepsilon = 0 \\ 
\delta = -\frac{2\zeta}{3} \end{cases} 
\Rightarrow 
\Pi_3 = \frac{A}{V^{\frac{2}{3}}}$$

$$h = \frac{FV^{\frac{1}{3}}}{mg} \tilde{f}\left(\frac{A}{V^{\frac{2}{3}}}, \frac{F}{mg}\right)$$

### Model 3

| Symbol | Quantity | Dimension |
| :--- | :--- | :--- |
| $h$ | Jump height | $[L]$ |
| $m$ | Animal mass | $[M]$ |
| $F$ | Jump force | $[MLT^{-2}]$ |
| $V$ | Animal volume | $[L^3]$ |
| $g$ | Acceleration due to gravity | $[LT^{-2}]$ |
| $A$ | Cross-sectional area | $[L^2]$ |
| $\theta$ | Jump angle | dimensionless |
| $\rho$ | Bone density | $[ML^{-3}]$ |
| $R_v$ | Ratio of bone volume to body volume | dimensionless |

$$\Pi_i = F^\alpha h^\beta m^\gamma V^\delta g^\varepsilon A^\zeta \rho^\eta \Theta R_v$$

where $\Theta$ — jump angle,  
$R_v$ — ratio of bone volume to body volume.  
Note that $\Theta$ and $R_v$ are dimensionless coefficients.

For dimensionless products:

$$\begin{cases}
\alpha + \gamma + \eta = 0 \\
\alpha + \beta + 3\delta + \varepsilon + 2\zeta - 3\eta = 0 \\
-2\alpha - 2\varepsilon = 0
\end{cases}$$

For $\eta = 0$ and without considering $\Theta$ and $R_v$, we take $\Pi_i$ for $i \in \{1, 2, 3\}$ from model 2.

For $\eta = 1$, we have:

$$\begin{cases} \alpha = 0 \\ \zeta = 0 \end{cases} \Rightarrow \begin{cases} \varepsilon = 0,\; \gamma = -\eta \\ \delta = \eta \end{cases} \Rightarrow \Pi_4 = \frac{m}{\rho V}$$

Let $\Pi_5 = R_v$, $\Pi_6 = \Theta$.

**Answer:**

$$h = \frac{FV^{\frac{1}{3}}}{mg} \hat{f}\left(\frac{A}{V^{\frac{2}{3}}}, \frac{F}{mg}, \frac{m}{\rho V}, R_v, \Theta\right)$$

# Problem 2

In the given dataset, $W$ denotes the weight of a fish (perch), and $g$ denotes its girth. Fit the model $W = cg^3$ to the available data using the least-squares criterion.

| Girth, (in.) | 9.75 | 8.375 | 11.0 | 9.75 | 8.5 | 12.5 | 9.0 | 8.5 |
| :--- | :---: | :---: | :---: | :---: | :---: | :---: | :---: | :---: |
| Weight, (oz) | 27 | 17 | 41 | 26 | 17 | 49 | 23 | 16 |

## Solution 

$$S = \sum_{i=1}^{n} (W_i - c g_i^3)^2$$ — Must be minimized.

$$\frac{dS}{dc} = -2 \sum_{i=1}^{n} (W_i - c g_i^3) g_i^3 = 0$$ — Set the derivative to zero to find the minimum, since the derivative represents a straight line.

$$c = \frac{\sum_{i=1}^{n} W_i g_i^3}{\sum_{i=1}^{n} (g_i^3)^2}$$ — Express our coefficient from the resulting equation.


# Problem 3 

The temperature distribution $u$ in a thin, infinite metal rod with a thermally insulated lateral surface is studied. The initial temperature distribution in the rod has the form $u = \dots$, where $H$ is the Heaviside step function. There is no heat source inside the rod. The thermal diffusivity coefficient of the rod is $k = \dots$Solve the problem using the Fourier transform and plot a 3D graph of the resulting solution.Create an animation of the spatiotemporal temperature distribution in the rod for $0 \dots 7$ (i.e., $t \in [0, 7]$).
