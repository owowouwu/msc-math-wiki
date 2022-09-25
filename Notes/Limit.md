# Definition (Topological Space)

Let $(X, \mathcal{T}_{X})$, $(Y, \mathcal{T}_{Y})$ be [[Topological Space]] and $f: X \to Y$ and $a \in X$ and $y \in Y$. then
$$
\lim_{ x \to a} f(x) = y
$$
if $f$ satisfies $P \in \mathcal{N}(y)$ then there exists $N \in \mathcal{N}(a)$ such that $f(N) \subseteq P$.

## For Sequences 

Specifically for a sequence $\left\{ a_{n} \right\} \in X$ we say the limit exists and is equal to $a \in X$ if for any $N \in \mathcal{N}(a)$ there exists a $k \in \mathbb{Z}_{>0}$ such that
$$
\left\{ a_{k}, a_{k+1}, \dots \right\} \subseteq N 
$$
i.e for every $n \geq k$, $a_{n} \in N$.

See [[Limit Point]]
