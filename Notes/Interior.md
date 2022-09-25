# Definition

Let $(X, \mathcal{T}_{X})$ be a [[Topological Space]].

The **interior** of a set $A$, $A^o$, is a subset of $X$ such that

1. $A^o \in \mathcal{T}_{X}$ and $A^o \subseteq A$
2. For any $U \in \mathcal{T}_{X}$ with $U \subseteq A$, then $U \subseteq A^o$.

i.e $A^o$ is the largest open set contained in $A$.

## Characterisation with Interior Points

Alternatively, the interior is also the set of all [[Interior Point]] of $A$.

**Proof** - 

Let $R$ be the set of interior points of $A$. We want to show that $A^o \subseteq R$ and $R \subseteq A^o$.

Let $x \in A^o$. To show that $x \in R$, we need to show that it is an interior point. By definition of $A^o$, $A^o$ is open. So $A^o \in \mathcal{N}(x)$ and $A^o \subseteq A$, so $x$ is an interior point.

Now let $x \in R$. Since $x$ is an interior point, then there exists $N \in \mathcal{N}(x)$. There exists $U \in \mathcal{T}_{X}$ with $x \in U$ and $U \subseteq N$. But if $U \subseteq N \subseteq A$ then $U \subseteq A^o$. Hence $x \in A^o$.