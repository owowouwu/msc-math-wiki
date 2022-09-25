Recall [[MetHilbert11#Theorem 11 4]].

## Proof of (a)

Let $\lambda \in \mathbb{C}$ and $H_{\lambda}\neq 0$. Let $H_{\lambda}$ with $v \neq 0$. We want to show $\lambda \in \mathbb{R}$.

Using that $T$ is self adjoint,
$$
\begin{align}
\langle Tv, v \rangle &= \langle v, Tv \rangle \\
&= \overline{\langle Tv,v \rangle}  
\end{align}
$$
Hence $\langle Tv, v \rangle \in R$. But $v$ is an eigenvector, so $\langle Tv,v \rangle = \langle \lambda v, v \rangle = \lambda \langle v,v \rangle \in \mathbb{R}$. Since $\langle v,v \rangle \geq 0$ by psotiive definiteness, $\lambda \in \mathbb{R}$.

## Proof of (b)

Assume $\lambda, \gamma \in R$. We want to show that $H_{\lambda} \perp H_{\gamma}$. In other words, we want to show that for $x \in H_{\lambda}$, $y \in H_{\gamma}$, $\langle x,y \rangle = 0$.
$$
\begin{align}
\lambda \langle x,y \rangle &= \langle \lambda x, y \rangle \\
 &= \langle Tx,y \rangle  \\
&= \langle x, Ty \rangle \\
&= \langle x, \gamma y \rangle  \\
&= \overline{\gamma} \langle x,y \rangle = \gamma \langle x,y \rangle     
\end{align}
$$
So $(\lambda - \gamma)\langle x,y \rangle = 0$. Since $\gamma \neq \lambda$, $\langle x,y \rangle = 0$.

## Proof of (c)

We can equivalently show that if $\lambda \neq 0$ and $H_{\lambda}$ is **not** finite dimensional, then $T$ is not [[Cover Compact]].

In other words there exists some sequence $\left\{ e_{m} \right\}$ of unit vectors in $H$ such that there exist no cluster points for $\left\{ Te_{m} \right\}$. 

Since $H_{\lambda}$ is infinite dimensional we can form a basis using Gran Schmidt that is an orthonormal sequence of vectors.

Let $(e_{1}, e_{2}, \dots)$ be such a sequence. Now if $m\neq n$ then
$$
\begin{align}
\|Te_{m} - Te_{n}\| &= \| \lambda e_{m} - \lambda e_{n}\| \\
&= |\lambda| \| e_{m}  - e_{n}\| = |\lambda|\sqrt{ 2 }
\end{align}
$$
This implies that $(Te_{1}, Te_{2}, \dots)$ has no convergent subsequence, so it has no cluster point. Hence $T$ is not compact.

## Proof of (d)

We will show that if the limit is not 0, then $T$ is not compact.

Let $(\lambda_{1}, \lambda_{2}, \dots)$ be a sequence of distinct eigenvectors with $\lim_{k \to \infty}\lambda_{k} \neq 0$.

For each $n$, let $u_{n} \in H_{\lambda_{n}}$ with $\|u_{n}\| = 1$ and $W_{n} = \text{span}\left\{ u_{1:n} \right\}$. Recall that $(b)$ states the the eigenvectors are orthogonal, so this is an orthonormal basis. We have the following relationship
$$
0 \subsetneq W_{1} \subsetneq W_{2} \subsetneq \dots
$$
