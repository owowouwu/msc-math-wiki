# Statement

Let $H$ be a [[Hilbert Space]] and let $T: H \to H$ be a [[Self-Adjoint]], [[Cover Compact]], [[Bounded Linear Operators]]. Then
$$
H = \overline{\oplus_{\lambda \in \sigma_{p}(T)}H_{\lambda}}
$$
If $H$ is separable, then $H$ has a countable orthonormal basis consisting of eigenvectors $T$ (using Gram-Schmidt).

From [[MetHilbert11#Theorem 11 4 Spectral Theorem]] the following are equivalent

1. If $H_{\lambda} \neq 0 \implies \lambda \in \mathbb{R}$.
2. If $\lambda, \gamma \in \mathbb{C}$ with $\lambda \neq \gamma$ then $H_{\lambda} \perp H_{\gamma}$ i.e if $x \in H_{\lambda}, y \in H_{\gamma}$, then $<x,y> = 0$.
3. If $T$ is compact then $H_{\lambda}$ is finite dimensional. (this is why $I$ is not compact - the space of eigenvectors ie everything which can be infinite dimensional)\
4. If $(\lambda_{1}, \lambda_{2}, \dots)$ is a sequence of distinct eigenvalues then the limit is 0. 
5. If $T$ is compact then $H$ is the closure of $\oplus_{\lambda} H_{\lambda}$ over all eigenvalues (H is made of a basis of eigenvectors.)
