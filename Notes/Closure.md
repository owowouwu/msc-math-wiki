# Definition - Metric Spaces

Let $(X, d)$ be a [[Metric Space]]. Let $W$ be a subspace of $X$, the *closure* of $W$ is $W$ together with the set of its limit points, i.e
$$
\overline{W} = \left\{ \lim_{n \to \infty} w_{n} : w_{1}, w_{2}, \dots \text{ is a sequence in $W$ and $\lim_{n \to \infty} w_{n}$ exists in $V$}\right\} 
$$
Now if it happens that all its limit points exist in $W$, i.e $\overline{W} = W$, then we say that $W$ is a **closed** subspace of $V$.

# Definition - Topology

Let $(X, \mathcal{T})$ be a [[Topological Space]], and $A \subseteq X$. The **closure** of $A$ is the set $\overline{A} \subseteq X$ such that -

1. $A \subseteq \overline{A}$ and $\overline{A}$ is [[Closed (Topology)]].
2. If $C$ is [[Closed (Topology)]] and $A \subseteq C$ then $\overline{A} \subseteq C$.

In other words, $\overline{A}$ is the smallest set containing $A$.

## Characterisations

### Limit Points

$A$ is closed if it contains all its [[Limit Point]]. (see the above definition for metric spaces).

### [[Close Point]]

