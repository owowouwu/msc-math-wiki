# Construction

Let $X$ be a [[Random Variable]] on $(\Omega, \mathcal{F}, P)$. The **expectation** of a [[Random Variable]] is simply the [[Lesbesgue Integration|lesbesgue integral]] of $X$ over the measure $P$.

1. $X$ is simple i.e a linear combination of indicators
$$
X = \sum_{k=1}^n c_{k}1_{A_{k}}
$$
then
$$
\int X \, dP = \sum_{k=1}^n c_{k}P(A_{k})
$$
2. $X\geq 0$. $\exists X_{n}$ simple such that $0\leq X_{n} \uparrow X$
We take the limit
$$
\int X \, dP = \lim_{n\rightarrow \infty} \int X_{n} \, dP   
$$
3. If $X$ is general we define $X = X^+ X^-$, and use the positive case above
$$
\int X \, dP = \int X^+ \, dP + \int X^- \, dP  
$$
