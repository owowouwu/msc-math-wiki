# Statement

Let $(X, \mathcal{T}_{X})$ be a toplogical space. Let
$$
\Delta : X \to X \times X, x \mapsto (x,x)
$$
then $(X, \mathcal{T}_{X})$ is a [[Hausdorff Space]] if and only if $\Delta(X)$ is [[Closed (Topology)]] in $X \times X$ equipped with the [[Product Topology]].

# Proof

$\implies$ Assume $(X ,\mathcal{T}_{X})$ is Hausdorff. We want to show $\Delta(X)$ is closed in $X \times X$.

To show : If $(z_{1}, z_{2}) \in X \times X$ is a [[Close Point]] to $\Delta(X)$ then $(z_{1}, z_{2}) \in \Delta(X)$.

Assume $(z_{1}, z_{2})$ is a close point to $\Delta(X)$. We want to show $z_{1}=z_{2}$ so that $(z_{1}, z_{2}) \in \Delta(X)$.

Let $U \in \mathcal{T}_{X}$ and $V \in \mathcal{T}_{X}$. Then $U \times V \in \mathcal{N}(z_{1}, z_{2})$. Since $(z_{1}, z_{2})$ is a close point to $\Delta(X)$ then $(U \times V) \cap \Delta(X) \neq \phi$.

So there exists $z \in X$ with $(z,z) \in U \times V$. So $U \cap V \neq \phi$. Since $(X, \mathcal{T}_{X})$ is Hausdorff, $z_{1}=z_{2}$. Hence $(z_{1},z_{2}) = (z_{1},z_{1}) \in \Delta(X)$. So $\Delta(X)$ is closed.

$\impliedby$ Assume $\Delta(X)$ is closed in $X \times X$. Now we want to show that $(X, \mathcal{T}_{X})$ is Hausdorff. 

Let $(z_{1}, z_{2}) \in X \times X$ with $z_{1}\neq z_{2}$. Since $z_{1} \neq z_{2}$ we have that $(z_{1}, z_{2}) \notin \Delta(X)$. Hence there exists a neighbourhood $N$ of $(z_{1}, z_{2})$ such that $N \cap \Delta(X) = \phi$. In other words for any $U, V \in \mathcal{T}_{X}$, $U \times V \subseteq N$ means that $(U \times V) \cap \Delta(X) = \phi$.

Fix $N_{1} \in \mathcal{N}(z_{1})$. We show that there exists $N_{2} \in \mathcal{N}(z_{2})$ such that $N_{1} \cap N_{2} = \phi$. Suppose this is not the case, i.e that $N_{1} \cap N_{2} \neq \phi$ for any $N_{2} \in \mathcal{N}(z_{2})$. 

Let $$