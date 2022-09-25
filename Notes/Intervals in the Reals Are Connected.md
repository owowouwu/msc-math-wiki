# Statement

Let $X = \mathbb{R}$ with the standard topology and let $E \subseteq X$. Then $E$ is connected if and only if $E$ is an interval.

# Proof

$\implies$ (contrapositive) Assume $E$ is not an interval. Then there exists $x,y \in E$ with $x<z<y$ but $z \notin E$. Let $A = (-\infty, z) \cap E$ and $B = E \cap (z, \infty)$. Since these intervals are open in $\mathbb{R}$ they are open in $E$ ( with the subspace topology). Then $A \cup B = E$ and $A \cap B \neq \phi$ so $E$ is disconnected.

$\impliedby$ (contrapositive) Suppose $E$ is not connected.

Then there exists $A,B \in \mathcal{T}_{E}$ such that $A \cup B = E$ but $A \cap B = \phi$. Since $A,B$ are open, then there exist arbitrary index sets $I_{A}$, $I_{B}$ be such that 
$$
\begin{align}
A &= \bigcup_{\alpha \in I_{A}} B_{\varepsilon_{\alpha}}(x_{\alpha}) \\
B&= \bigcup_{\beta \in I_{B}} B_{\varepsilon_{\beta}}(x_{\beta}) 
\end{align}
$$
Choose any $x = x_{\alpha}$, with $\delta = \varepsilon_{\alpha}$ and $y = x_{\beta}$ with $\varepsilon = \varepsilon_{\beta}$. Then by assumption we have that 
$$
B_{\delta}(x) \cap B_{\varepsilon}(y) = \phi
$$
