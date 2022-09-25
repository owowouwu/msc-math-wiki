# Statement

Let $(\Omega, \mathcal{F}, \mu)$ be a measurable space, and 
 
Let $f_{n}\geq 0$ be a sequence of $\mu$-measurable functions. Then,

$$
\int _{\Omega}\lim_{}\inf f_{n} \, d\mu \leq \lim\inf \int _{\Omega}f_{n} \, d\mu  
$$

## Intuition - 

- LHS is integrating the $\lim\inf$ which 'loses' some part of the sequence $f_{n}$
- RHS is taking the smallest integral of all sequences $f_{n}$, and each integral should always be larger than the integral of $\lim\inf f_{n}$ due to the above reason
- [ ] similar to [[Jensen's Inequality]] kind of?

