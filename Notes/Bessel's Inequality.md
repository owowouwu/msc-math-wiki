Let $H$ be a [[Hilbert Space]]. 

If $x \in H$, then

$$
\sum_{n=1}^\infty |\langle x, e_{n} \rangle|^2 \leq \|x\|^2 
$$

## Proof

Since the sequence of partial sums is increasing, it suffices to show that the partial sums are bounded by $\|x\|^2$.

Let $x_{k} = \sum_{n=1}^k |\langle x, e_{n} \rangle|^2$.


sketch - show that $\|x_{k}\|^2 = <x_{k}, x_{k}> = x_{k}$

then use triangle inequality with $\|x\| = \|x_{k} + (x-x_{k})\|$

