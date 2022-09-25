# Statement

[link](http://math.soimeme.org/~arunram/Teaching/2022MetricHilbert/LimitsandTopologies220714.pdf)

Let $(X, \mathcal{T}_{X})$ and $(Y, \mathcal{T}_{Y})$ be [[Topological Space|topological spaces]]. Suppose $f: X \to Y$ is a function. We say that $f$ is [[Continuous]] if and only if it is [[Continuous at a Point|continuous for every point]] $a \in X$.

## Proof

$\implies$ Suppose $f$ is continuous.

Let $a \in X$. Let $V \in \mathcal{N}(f(a))$. We want to show that $f^{-1}(V) \in \mathcal{N}(a)$. In other words, we want to show that $\mathcal{N}(a)$ contains an [[Open Neighbourhood]] of $a$. 

Since $V$ is a neighbourhood of $f(a)$ there contains an open neighbourhood of $f(a)$. Let $U$ be such an open set. Then since $f$ is continuous, the preimage of $U$ is an open set, and clearly $a \in f^{-1}(U)$ since $U$ contains $f(a)$. Hence $f^{-1}(U)$ is an open neighbourhood of $a$.

Since $U \subseteq V$, since preimages preserve subset relations we have $f^{-1}(U) \subseteq f^{-1}(V)$. Hence $f^{-1}(V)$ contains an open set whch contains $a$, so it is a neighbourhood of $a$.

$\impliedby$ Suppose $f$ is continuous at every point $a \in X$. We want to show that the preimage of every open set in $Y$ is an open set in $X$.




