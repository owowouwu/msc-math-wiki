# Definition

Let $(X, d_{x})$ be a [[Metric Space]]. Let $A \subseteq X$. The set $A$ is **complete**, or **Cauchy compact** if any Cauchy sequence in $A$ converges.

## Examples

- $\mathbb{R}_{>0}$ is not complete as $a_n = \frac{1}{n}$ does not converge in $\mathbb{R}_{>0}$ (0 does not exist)

Note that all convergent sequences in $\mathbb{R}$ are Cauchy - 

Let $a_n \in \mathbb{R}$ be a sequence such that $\lim_{n\rightarrow \infty} a_n = \ell < \infty$.

Let $\varepsilon > 0$ be arbitrary. As $a_n$ is convergent, for some $K \in \mathbb{N}$ we have $n>K \implies |a_n - \ell| < \frac{\varepsilon}{2}$.

Now let $n, m > K$,
$$ |a_n - a_m| = |a_n - \ell - (a_m -\ell)| \leq |a_n - \ell| + |a_m - \ell| < \varepsilon$$
Hence all convergent sequences are Cauchy. 

But the converse is not necessarily true e.g

