# Statement

Let $(X, \mathcal{T}_{X}), (Y, \mathcal{T}_{Y})$ be [[Topological Space|topological spaces]] and $f: X \to Y$ be a [[Continuous]] function with $f(X)= Y$ (i.e $f$ is surjective). Then if $X$ is [[Compact]], $Y$ is [[Compact]].

# Proof

Let $\left\{ U_{i} \right\}_{i \in I}$ be an open cover for $Y$. By continuity and surjectiveness we have $X = f^{-1}(Y) \subseteq f^{-1}(\bigcup_{i \in I} U_{i})$.

Hence $\left\{ f^{-1}(U_{i}) \right\}_{i \in I}$ is an open cover for $X$. Since $X$ is compact there exists a finite subcover $f^{-1}(U_{n_{1}}), f^{-1}(U_{n_{2}}), \dots, f^{-1}(U_{n_{k}})$. So we have 
$$
X \subseteq \bigcup_{i=1}^k f^{-1}(U_{n_{k}})
$$
and again using surjectiveness we have
$$
Y = f(X) \subseteq \bigcup_{i=1}^k U_{n_{k}}
$$
