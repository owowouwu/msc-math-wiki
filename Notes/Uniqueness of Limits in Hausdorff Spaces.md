# Statement

Let $(X, \mathcal{T}_{X})$ be a [[Hausdorff Space]]. Let $a_{n}$ be a sequence in $X$ and $z_{1}, z_{2} \in X$ be such that $\lim_{n \to \infty}a_{n}=z_{1}$ and $\lim_{n \to \infty}a_{n} = z_{2}$.

Then $z_{1} = z_{2}$.

In other words, limits are **unique** in Hausdorff spaces.

# Proof

Let $N_{1} \in \mathcal{N}(z_{1})$ and $N_{2} \in \mathcal{N}(z_{2})$. 

There exists $l_{1} \in \mathbb{Z}_{\geq 0}$ with
$$
a_{l_{1}:} \subseteq N_{1}
$$
and similarly there exists $l_{2} \in \mathbb{Z}_{> 0}$ with
$$
a_{l_{2}:} \subseteq N_{2}
$$
Then if we let $l = \max\{l_{1}, l_{2}\}$ we have
$$
a_{l:} \subseteq N_{1}\cap N_{2}
$$
Since $(X, \mathcal{T}_{X})$ is Hausdorff, $z_{1}=z_{2}$.