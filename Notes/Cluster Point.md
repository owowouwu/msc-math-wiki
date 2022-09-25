# Definition

Let $(X,\mathcal{T}_{X})$ be a [[Topological Space]].

Let $x_{n}$ be a sequence in $X$.

A cluster point of $x_{n}$ is $z \in X$ such that there exists a subsequence $(x_{n_{1}}, x_{n_{2}}, \dots)$ with
$$
\lim_{k \to \infty}x_{n_{k}} = z
$$

## Example

Let $x = \mathbb{R}$ and the sequence given by
$$
x_{n} = (-1)^n\left( 1-\frac{1}{n} \right)
$$
$\lim_{n \to \infty} x_{n}$ does not exist in $\mathbb{R}$ but has two cluster points (-1 and 1)

# Not a Cluster Point

Let $A \subseteq X$.

$z$ is **not** a cluster point of $(a_{1}, a_{2}, \dots)$ if there exists an open set $U$ of $A$ such that
$$
U \cap (a_{1}, a_{2}, \dots) \text{ is finite}
$$

(open sets of $A$ defined using the [[Subspace Topology]]).

