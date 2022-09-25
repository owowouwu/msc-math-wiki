# Statement

Let $(X, \mathcal{T})$ be a [[Topological Space]]. 

Recall that sets in $\mathcal{T}$ are called **open** sets. An alternative characterisation is that if $A \subseteq X$ contains all its [[Interior Point]], then it is **open**.

This is equivalent to saying that $A$ is open if and only if it **contains a [[Neighbourhood]] of all its points.

# Proof
$\implies$ Suppose $A$ is open. Trivially, $A$ is an open neighbourhood of all its points, so $A$ contains all its interior points.

$\impliedby$ Let $A \subseteq X$ and suppose $A$ contains all its interior points. We want to show that $A \in \mathcal{T}$.

Since $A$ contains all its interior points, for each $x \in A$ there exists a [[Neighbourhood]] $N_{x}$ such that $N_{x} \subseteq A$. Each neighbourhood contains an open neighbourhood $U_{x}$ of $x$. Then $\bigcup_{x \in A}U_{x} \in \mathcal{T}$ (arbitrary union)

We want to show that $\bigcup_{x \in A}U_{x} = A$. 

Clearly since $\left\{ x \right\} \subseteq U_{x}$, we have the following relation
$$
A \subseteq\bigcup_{x \in A} \left\{ x \right\} \subseteq \bigcup_{x \in A} U_{x} \subseteq \bigcup_{x \in A}N_{x} \subseteq A
$$
Hence $A = \bigcup_{x \in A}U_{x} \in \mathcal{T}$. So $A$ is open.

## Metric Spaces

### Real Numbers

On $\mathbb{R}$, using this definition we can define a set $A \subseteq \mathbb{R}$ to be **open** if for any $x \in A$, there exists a $\delta >0$ such that
$$
B_{\delta}(x) \subseteq A
$$
