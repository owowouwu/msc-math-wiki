# Orthogonality and Projections cont.

Let $(V, \langle  \rangle)$ be a $K$-vector space with a [[Positive Definite Hermitian Form]].

If $S$ is a subset of $V$,

1. $S^\perp$ is a subspace of $V$
2. $S^\perp$ is a closed subspace of $V$
3. $S \subseteq (S^\perp)^\perp$
4. In general $S \neq (S^\perp)^\perp$.

How do we decompose $V = W \oplus W^\perp$?

## Theorem 2 - Orthonormal Basis

Let $(H, \langle \cdot \rangle)$ be a [[Hilbert Space]] and $(e_{1}, e_{2}, \dots)$ be an orthonormal sequence in $H$. Then
$$
\overline{W} = \overline{\text{span}(e_{1}, e_{2}, \dots)}
$$
and $H = \overline{W} \oplus \overline{W}^\perp$. This means that the basis formed by $e_{n}$ is not a basis for $H$ but for its closure.

How to get this? Let $P: H \to H$ by the basis expansion $P(x) = \sum_{n=1}^\infty \langle x, e_{n} \rangle e_{n}$.

Then $P$ is a projection on $\overline{W}$ in $H$.

### proof

We want to show the properties for a [[Projections]] hold.

First we want to show $P(x) \in H$ for any $x \in H$. It suffices to show that the partial sum converges
$$
S_{k} = \sum_{n=1}^k \langle x, e_{n} \rangle e_{n}
$$
Since [[Hilbert Space]] is complete, Cauchy sequences converge. It suffices to show that $S_{k}$ is Cauchy.

By [[Bessel's Inequality]], $(\|x_{1}\|^2, \|x_{2}\|^2, \dots)$ is an increasing bounded sequence in $\mathbb{R}_{\geq 0}$. So there is an $N \in \mathbb{N}$ such that if $k \geq N$, then
