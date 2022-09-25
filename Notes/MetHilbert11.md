# Constructing eigenvalues and eigenvectors

Let $H$ be a [[Hilbert Space]] and $T: H \to H$ be a [[Bounded Linear Operators]].

The operator $T$ is self-adjoint if $T$ satisfies that if $x,y \in H$, then $\langle Tx, y \rangle = \langle x, Ty \rangle$.

## Theorem 11.1

Let $(H, \langle  \rangle)$ be a [[Hilbert Space]] and let $T: H \to H$ be a bounded [[Self-Adjoint]] operator.

Let $\lambda = \sup \left\{  |\langle  Tu, u \rangle | : u \in H, \|u\| =  1\right\}$

Then $\lambda = \|T\|$ and $\lambda - T$ is not a bijection.

### Remark

By Cauchy-Schwarz, $|\langle  Tu, u \rangle| \leq \| Tu\| \| u\|$. Let $\theta = \arccos \left( \langle Tu, u \rangle /\|Tu\| \| u\| \right)$ . Then $u$ is an eigenavlue for $T$ when $\theta = 0$ or $\pi$.

## Theorem 11.2

Let $(H, \langle  \rangle)$ be a [[Hilbert Space]] and $T: H \to H$ be a bounded, self adjoint and compact linear operator. Let $u_{n}$ be a sequence of unit vectors in $H$ such that $\lim_{n \to \infty} |\langle Tu_{n}, u_{n} \rangle| = \|T\|$. 

Let $y$ be a [[Cluster Point]] of $(Tu_{n})$, then $\|y\| = \|T\|$, $Ty = \|T\|y$ <- eigenvector


## Theorem 11.3 - Power Iteration/ Rayleigh Quotient Iteration

Let $H$ be a Hilbert space. Let $T: H \to H$ be a bounded compact self adjoint operator. Let $b_{0} \in H$. Define sequences 
$$
(b_{1}, b_{2}, \dots) \quad (\mu_{1}, \mu_{2}, \dots)
$$
by $b_{k+1} = \frac{Tb_{k}}{\|Tb_{k}\|}$ and $\mu_{k+1} = \langle Tb_{k}, b_{k} \rangle / \langle b_{k}, b_{k} \rangle = \frac{\langle b_{k+1}, b_{k} \rangle}{\|b_{k}\|^2}$.

Then 
$$
\|T\| = \lim_{k \to \infty} \mu_{k}
$$
and
$$
v = \lim_{k \to \infty} b_{k}
$$
is an eigenvector of $T$ with eigenvalue $\|T\|$.

## Theorem 11.4 (Spectral Theorem)

Let $H$ be a [[Hilbert Space]] and $T: H \to H$ be a [[Cover Compact]], [[Self-Adjoint]], [[Bounded Linear Operators]]. Then 

1. If $H_{\lambda} \neq 0 \implies \lambda \in \mathbb{R}$.
2. If $\lambda, \gamma \in \mathbb{C}$ with $\lambda \neq \gamma$ then $H_{\lambda} \perp H_{\gamma}$ i.e if $x \in H_{\lambda}, y \in H_{\gamma}$, then $<x,y> = 0$.
3. If $T$ is compact then $H_{\lambda}$ is finite dimensional. (this is why $I$ is not compact - the space of eigenvectors ie everything which can be infinite dimensional)\
4. If $(\lambda_{1}, \lambda_{2}, \dots)$ is a sequence of distinct eigenvalues then the limit is 0. 
5. If $T$ is compact then $H$ is the closure of $\oplus_{\lambda} H_{\lambda}$ over all eigenvalues (H is made of a basis of eigenvectors.)

### Remark

If $H$ is separable (i.e has a countable basis) then $\sigma_{p}(T)$ is also countable then $\|T\|$ is the largest (absolute value) eigenvalue. To use this with theorem 11.3 we find $\lambda_{1}$ then consider $T: H_{\lambda_{1}}^\perp \to H_{\lambda_{1}}^\perp$ and find its eigenvalue which should be $\lambda_{2}$.

$T$ is compact if and only if $\lim_{k \to \infty} \lambda_{k} = 0$.

