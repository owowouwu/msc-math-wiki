If $(X, d_{x})$ is  a [[Metric Space]] we can easily make it into a [[Uniform Space]] by considering the diagonals (the [[Metric Space Uniformity]]), so every metric space IS a uniform space.

Recall that every [[Metric Space]] is [[Hausdorff Space|hausdorff]]. But there exist uniform spaces which are not.

Let $(X, \mathcal{E}_{X})$ be a uniform space. Let $E \in \mathcal{E}_{X}$.

Consider these three constructions -

### 1.
Let $D_{0}=E$, and let $E_{1} = D_{0} \cap \sigma(D_{0})$ (force symmetry).
Let $D_{1} \in \mathcal{E}_{X}$ such that $D_{1} \bowtie D_{1} \subseteq E_{1}$.
Let $E_{2} = D_{1} \cap \sigma(D_{1})$.
Let $D_{2} \in \mathcal{E}_{X}$ such that $D_{2} \bowtie D_{2} \subseteq E_{2}$. and so on...

We have a sequence $E_{1}, E_{2}, E_{3}, \dots$

Define
$$
\chi_{E} = \left\{ D \subseteq X \times X : \text{ exists $k \in \mathbb{Z}_{>0}$ with } E_{k} \subseteq D \right\} 
$$
**Claim** - $\chi_{E}$ is a [[Uniformity]] on $X$.

### 2.
Let $F_{0} = E$ and let $U_{1} = F_{0} \cap \sigma(F_{0})$.
Let $F_{1} \in \mathcal{E}_X$ such that $F_{1} \bowtie F_{1} \bowtie F_{1} \subseteq U_{1} \cap F_{0}$.
Let $U_{2} = F_{1} \cap \sigma(F_{1})$.
Let $F_{2} \in \mathcal{E}_{X}$ be such that $F_{2} \bowtie F_{2} \bowtie F_{2}\subseteq U_{2} \cap F_{1}$.

We have a sequence $U_{1}, U_{2},\dots$

and define $\chi_{U}$ in a similar way as above.

### 3.
Define $g: X \times X \to \mathbb{R}_{\geq 0}$ by the following -
$$
g(x,y) = \begin{cases}
1 & (x,y) \notin U_{1} \\
2^{-k} &(x,y) \in \bigcap_{n=1}^k U_{k} \cap U_{k+1}^c\\
0 & (x,y) \in \bigcap_{n=1}^\infty U_{n}
\end{cases}
$$
Define $d: X \times X \to \mathbb{R}_{\geq 0}$ by
$$
d(x,y) = \inf\left\{ g(x, z_{1}) + g(z_{2},z_{1}) + \dots + g(z_{p-1}, y) : p \in \mathbb{Z}_{>0}, z_{1},z_{2},\dots,z_{p-1},y \in X  \right\} 
$$
Intuitively we take all possible paths between $x$ and $y$ with respect to the $g$ distance and then take the shortest path.

Define 
$$
\chi_{d}^E = \left\{ D \subseteq X \times X : \text{there exists $\varepsilon \in \mathbb{E}$ with $B_{\varepsilon} \subseteq D$} \right\} 
$$
Notice that this looks similar to the [[Metric Space Uniformity]]

Then $d: X \times X \to \mathbb{R}_{\geq 0}$ satisfies

1. If $x \in X$, $d(x,x) = 0$.
2. If $x,y \in X$ then $d(x,y) = d(y,x)$
3. If $x,y,z \in X$ then $d(x,y) \leq d(x,z) + d(z,y)$.

But we don't have uniqueness, i.e if $x,y \in X$ and $d(x,y) = 0$ then $x=y$. This property is not satisfied so $d$ is not really a metric.

# Theorem
$$\chi_{E} = \chi_{U} = \chi_{d}^E$$


$(X ,\mathcal{E}_{X})$ is a limit of almost metric space uniformities.