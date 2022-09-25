# Definition

Let $(X, \mathcal{T}_{X})$ be a [[Topological Space]]. The **neighbourhood filter** of $x$ is the collection of all [[Neighbourhood|neighbourhoods]] of $x$.
$$
\mathcal{N}(x) = \left\{ N \subseteq X : \text{there exists } U \in \mathcal{T}_{X} \text{ with } x \in U \text{ and } U \subseteq N   \right\} 
$$
In other words, $\mathcal{N}(x)$ is the set of all subsets containing an [[Open Neighbourhood]] of $x$.

# Properties

1. If $N \in \mathcal{N}(x)$, then for any set $A \subseteq X$ with $N \subseteq A$, $A \in \mathcal{N}(x)$

The intuition here is that a "larger" set is also a neighbourhood.

2. The intersection of any finite collection of neighbourhoods is a neighbourhood.

This follows from taking the intersection of the open neighbourhoods.

