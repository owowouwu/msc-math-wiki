## Theorem 7.1

Let $(H, <\cdot>)$ be a $K$-vector space with a [[Positive Definite Hermitian Form]].

If $x,y \in H$ and $\langle x,y \rangle = 0$ then

(a)  $\|x\|^2 + \|y\|^2 = \|x+y\|^2$ (general form of Pythagoras' Theorem)
(b) $\|x+y\|^2 + \|x-y\|^2 = 2\|x\|^2 +2\|y\|^2$
(c) $|\langle x,y \rangle | \leq \|x\|\|y\|$ (Cauchy Schwarz)
(d) $\|x+y\| \leq \|x\| + \|y\|$ (Triangle Inequality)

## Theorem 7.2

Let $(H, \langle \cdot \rangle)$ be a [[Hilbert Space]]. Let $W$ be a subset of $H$.
$$
W^\perp = \{x \in H : w \in W \implies \langle x, w \rangle = 0\}
$$
(a) $W^\perp$ is a closed subspace of $H$.
(b) If $W$ is a closed subspace of $H$, then $H = W \oplus W^\perp$.
(c) If $W$ is a subspace of $H$ and $H = W \oplus W^\perp$, then $W$ is closed.

## Proposition 7.1
[[Riesz Representation Theorem]]

Let $(H, \langle \rangle)$ be a [[Hilbert Space]], then
$$
\Phi: H \rightarrow H^*
$$
where $\varphi_{x} : H \to \mathbb{K}$, is a [[Skewlinear]] bijective [[Isometry]] of normed vector spaces with $\|\phi\|=1$.

### Proof

#### Skewlinear

Let $h \in H$. 
$$
\begin{align}
\varphi_{a+b}(h) &= \langle h, a+b \rangle \\
&= \langle h,a \rangle + \langle h, b \rangle \\
&= \varphi_{a}(h) + \varphi_{b}(h)
\end{align}
$$
Now let $c \in \mathbb{K}$.
$$
\varphi_{ca}(h) = \langle h, ca \rangle = \overline{c}\langle h, a\rangle = \overline{c}\varphi_{a}(h)
$$
#### Isometry

To see that $\varphi_{a+b}$ is an isometry - let $x \in H$. We want to show that $\|x\| = \|\Phi(x)\| = \|\varphi_{x}\|$

If $h \in H$, then by Cauchy Schwarz,
$$
|\varphi_{x}(h)| = |\langle h, x \rangle | \leq \|h\| \| x\|
$$
So
$$
\frac{|\varphi_{x}(h)|}{\|h\|} \leq \| x\|
$$
Hence $\sup \left\{\frac{|\varphi_{x}(h)|}{\|h\|} : h \in H  \right\} \leq \| x\|$, so $\|\varphi_{x}\| \leq \| x\|$.

Now let $h = x$, then 
$$
|\varphi_{x}(h)| = |\varphi_{x}(x)| = \|x\|^2 = \|x\| \\| x\| = \|h\| \| x\|
$$
Hence for $h =x$,
$$
\frac{|\varphi_{x}(h)|}{\|h\|} = \|x\|
$$
Thus 
$$
\|\varphi_{x}\| = \sup \left\{\frac{|\varphi_{x}(h)|}{\|h\|} : h \in H  \right\} = \|x\|
$$

#### Bijection

To see that $\Phi$ is bijective -

Let $a,b \in H$ and $\Phi(a) = \Phi(b)$. Then,
$$
\|a - b\| = \|\varphi_{a-b}\|
$$
by isometry. It then follows from $\|\varphi_{a-b}\| = \| \Phi(a) - \Phi(b)\| = 0$ that $\|a-b\| = 0$. Hence $\Phi$ is injective.

Now for surjectiveness we want to show that for every $\varphi \in H^*$ there exists $a \in H$ such that $\Phi(a) = \varphi$.

Assume $\varphi \in H^*$. Now since $\varphi$ is bounded, $\varphi$ is a continuous map


