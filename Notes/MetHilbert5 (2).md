## Hilbert Spaces

Let $V$ be a $\mathbb{K}$-vector space.

A positive definite Hermitian form on $V$ (inner product) is a function $<> : V \times V \rightarrow \mathbb{K}$ such that if 

1.  Addition - $x_{1}, x_{2}\in V$ and $y_{1}, y_{2}\in V$ then
$$
<x_{1}+x_{2},y> = <x_{1},y > + <x_{2},y>
$$
$$
<x, y_{1}+y_{2}> = <x,y_{1}> + <x, y_{2}>
$$
2. Scalar multiplication, if $c \in \mathbb{K}$
$$
<cx,y> =c<x,y>
$$
and
$$
<x,cy> =\overline{c}<x,y>
$$
Linear on the left, sesquilinear

3. Hermitian part - 
$$
<y,x> = \overline{<x,y>}
$$
4. If $x \in V$,  $<x,x> \in \mathbb{R}_{\geq_{0}}$ (positive semidefiniteness)
5. If $x \in V$, $<x,x> =0 \implies x = 0$

Define $\|\cdot\|$ as $\|x\| = \sqrt{ <x,x> }$. This makes $V$ a [[Normed Vector Space]]. If it complete, it is also a [[Hilbert Space]]

## Theorem

Let $(H, <\cdot>)$ by a separable Hilbert space, then 
$$
H=H^*
$$
### Isometries

### Metric Spaces

Let $(X, d_{x})$ and $(Y, d_{y})$ be metric spaces. An isometry from $X$ to $Y$ is a function 
$$
\varphi : X\rightarrow Y
$$
such that if $x_{1},x_{2} \in X$ $d_{X}(x_{1}, x_{2}) = d_{Y}(\varphi(x_{1}), \varphi(x_{2}))$ i.e preserves distance (isometric).

### Normed Vector Spaces

Let $(V, \|\|_{V})$ and $(W, \|\|_{W})$ by normed vector spaces. An isometry from $V\rightarrow W$ is a function
$$
\varphi: V\rightarrow W
$$
such that if $x\in V$ then $\|x\|_{V} = \|\varphi(x)\|_{W}$

### Hilbert Spaces

same thing, but with inner product, also called **unitary operators**

**hw** if $\varphi$ is an isometry then it is injective
