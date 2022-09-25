# Definition

Let $X$ be a set. For $E \subseteq X \times X$ let 
$$
\sigma(E) = \left\{ (y,x) : (x,y)  \in E \right\} 
$$
$$
E \bowtie E = \left\{ (x,y) : (x,z) \in E , (z,y) \in E \right\} 
$$
$$
\Delta(X) = \left\{ (x,x) \in X \times X: x =x \right\} 
$$

A **uniformity** is a collection $\mathcal{E}_{X}$ of subsets of $X \times X$ such that  

1. If $E \in \mathcal{E}_{X}$ then $\Delta(X) \subseteq E$. (every $E$ contains a diagonal)
2. If $E \in \mathcal{E}_{X}$ and $D \subseteq X \times X$ and $E \subseteq D$ then $D \in \mathcal{E}_{X}$. (similar to [[Neighbourhood Filter]])
3. $\mathcal{E}_{X}$ is closed under finite intersections.
4. If $E \in \mathcal{E}_{X}$ then $\sigma(E) \in \mathcal{E}_{X}$.
5. If $E \in \mathcal{E}_{X}$ then there exists $D \in \mathcal{E}_{X}$ such that $D \bowtie D \subseteq E$.

We call sets in $\mathcal{E}_{X}$ "fat diagonals" or "entourages"
