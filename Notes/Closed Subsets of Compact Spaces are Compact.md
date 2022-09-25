# Statement

Let $(X, \mathcal{T})$ be a [[Topological Space]], and suppose $X$ is [[Compact]]. Then any [[Closed]] subset $A$ of $X$ is also compact.

# Proof

Let $\left\{ U_{i} \right\}_{i \in I}$ be an open [[Cover]] for $A$. Then we have
$$
X = A \cup(X\backslash A) \subseteq \bigcup_{i \in I}  U_{i} \cup (X \backslash A)
$$
this is an open cover for $X$ as $A$ is closed so $X \backslash A$ is open. Hence there must exist a finite subcover $\left\{ X\backslash A, U_{n_{1}}, U_{n_{2}}, \dots , U_{n_{k}} \right\}$, and since $A \subseteq X$ we are done.


