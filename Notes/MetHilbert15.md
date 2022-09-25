# Topologies

## From Metric Spaces

Let $(X, d_{x})$ be a [[Metric Space]]. Then the metric space toplogy is
$$
\mathcal{T}_{x} = \left\{ U \subseteq X : a \in U \implies U \in \mathcal{N}(a) \right\} 
$$
An element of $\mathcal{T}_{x}$ is called an **open set**, i.e it is a neighbourhood of each of its points.

### Using Closed Sets

Recall that closed sets are those whose complement is open i.e
$$
\mathcal{C}_{x} = \left\{ C \subseteq X : C^c \in \mathcal{T}_{x}\right\} 
$$

## General Topological Spaces

Now we throw away $d_{x}$.

**proposition** let $(X, \mathcal{T}_{X})$ be a [[Topological Space]]. Let $A \subseteq X$. Then

## limits and continuity

Let $(X, \mathcal{T}_{X})$, $(Y, \mathcal{T}_{Y})$ be [[Topological Space]] and $f: X \to Y$ and $a \in X$ and $y \in Y$. then
$$
\lim_{ x \to a} f(x) = y
$$
if $f$ satisfies $P \in \mathcal{N}(y)$ then there exists $N \in \mathcal{N}(a)$ such that $f(N) \subseteq P$.
a

