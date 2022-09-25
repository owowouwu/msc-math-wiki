# Statement

Let $(X, \mathcal{T})$ be a [[Topological Space]] and let $A \subseteq X$ with the usual induced [[Subspace Topology]] $\mathcal{T}_{A}$. Then $A$ is [[Compact]] if and only if $(A, \mathcal{T}_{A})$ is a compact space.

# Proof

$\implies$ Suppose $A$ is compact in $X$. Let $\left\{ O_{i} \right\}_{i \in I} \in \mathcal{T}_{A}$ be an open cover for $A$. For each $O_{i}$ we let $V_{i} \in \mathcal{T}$ be such that $O_{i} = V_{i} \cap A$. Then we have that
$$
A \subseteq \bigcup_{i \in I}O_{i} \subseteq \bigcup_{i \in I} V_{i}
$$
so $\left\{ V_{i} \right\}_{i \in I}$ is an open cover for $A$ in $(X, \mathcal{T})$. Hence there exists a finite subcover $V_{n_{1}}, V_{n_{2}}, \dots, V_{n_{l}}$ where $l \in \mathbb{Z}_{> 0}$. Hence $\left\{ O_{n_{k}} \right\}_{k=1}^l$ is a finite subcover for $A$ in $(A, \mathcal{T}_{A})$. So $(A, \mathcal{T}_{A})$ is a compact space.

$\impliedby$ Suppose $(A, \mathcal{T}_{A})$ is a compact space. Let $\left\{ U_{i}  \right\}_{i \in I} \in \mathcal{T}$ be an open cover for $A$. Then $W = \left\{ A \cap U_{i} : i \in I\right\} \subseteq \mathcal{T}_{A}$ is also an open cover for $A$, and since $(A, \mathcal{T}_{A})$ is a compact space, there exists a finite subcollection $A \cap U_{n_{1}}, A \cap U_{n_{2}}, \dots, A \cap U_{n_{l}}$ which covers $A$. Observe then that we have
$$
A \subseteq \bigcup_{k=1}^l (A \cap U_{n_{k}}) \subseteq \bigcup_{k=1}^l U_{n_{k}}
$$
which implies there exists a finite subcover for $A$. Hence $A$ is compact in $(X, \mathcal{T})$.