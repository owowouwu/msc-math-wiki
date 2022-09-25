# Statement

Let $(X, d_{x})$ be a [[Metric Space]] with the usual [[Metric Space Topology]] $\mathcal{T}$. Let $\mathcal{B}$ be the set of all [[Epsilon Ball|open balls]] in $X$.

Then a subset $U \subseteq X$ is open (i.e $U \in \mathcal{T}$) if and only if there exists $\mathcal{S} \subseteq \mathcal{B}$ such that
$$
U = \bigcup_{B \in \mathcal{S}} B
$$
i.e there exists a collection of open balls such that make up $U$.

## Proof

$\implies$ (this is easy since this is the definition of the metric space topology) Assume $U$ is open. By the definition of the metric space topology for each $x \in U$ there exists an $\varepsilon >0$ such that $B_{\varepsilon_{x}}(x) \subseteq U$. 

Let $\mathcal{S} = \left\{ B_{\varepsilon_{x}}(x) : x \in U \right\}$. Since each $B \in \mathcal{S}$ is a subset of $U$, then the union over all $B \in \mathcal{S}$ needs to also be a subset of $U$. On the other hand, for any $x \in U$ we have that there exists an $\varepsilon$-ball $B_{\varepsilon}(x)$ containing $x$. But $B_{\varepsilon}(x)\subseteq \bigcup_{B \in \mathcal{S}}B$ so we have $x \in \bigcup_{B \in \mathcal{S}}B$. Hence $U = \bigcup_{B \in \mathcal{S}}B$

$\impliedby$ Assume there exists a collection $\mathcal{S}$ of open balls such that $U = \bigcup_{B \in \mathcal{S}}B$. We want to show that $U \in \mathcal{T}$.  By the definition of $\mathcal{T}$, this is equivalent to showing that for any $x \in U$ there exists a $B_{\varepsilon}(x) \in \mathcal{B}$ such that $B_{\varepsilon}(x) \subseteq U$.

But this is clear to see. Since $U = \bigcup_{B \in \mathcal{S}} B$ then if $x \in U$ there must exist at least one $B \in \mathcal{S}$ such that $x \in B$. From the definition of $U$ as well it is obvious that $B \subseteq U = \bigcup_{B \in \mathcal{S}} B$.

This completes the proof.