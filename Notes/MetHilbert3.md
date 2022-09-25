# Linear Transformations

Let $K$ be a field and $V$ and $W$ be $K$-vector spaces.

A [[Linear Operators]] from $V\rightarrow W$ is a function
$$T: V\rightarrow W$$
that preserves linearity -
- $v_1, v_2 \in V \implies T(v_1+v_2) = T(v_1) +t(v_2)$
- $c \in K$ and $v\in V \implies T(cv) = cT(v)$

Let
$$ \text{End}(V,W) = \{T : V \rightarrow W | \text{T is a linear operator}\}$$
this is a vector space, define $+$ by $(T_1 + T_2)(v) + T_1(v) + T_2(v)$ and scalar multiplication similarly as $(cT)(v) = cT(v)$ 

**remark** - if $V = \mathbb{R}^m$, $W = \mathbb{R}^n$, we have the set of $m\times n$ matrices

**Theorem** - show that $\text{End}(v,w)$ is a $K$-vector space.


### can we make a norm?

Let $(V, ||\cdot||_V)$ and $(W, ||\cdot||_W)$ be [[Normed Vector Space]]. Let $T:  V\rightarrow$ be a [[Linear Operators]],
$$ ||T|| = \sup \{\frac{||T_v||_W}{||v||_V} : v \in V\}$$
i.e $||T||$ is the maximum scaling factor that $T$ achieves when applied over all vectors in $V$. The division by $||v||_V$ allows us to only consider vectors of unit length in $V$.

Then the space of [[Bounded Linear Operators]] is
$$B(V,W) = \{T:V\rightarrow W : ||T|| < \infty\}$$
**hw** - show that $B(V,W)$ is a vector space.
**hw** - show that $B(V,W)$ is a normed vector space
**hw** - if $W$ is complete, $B(V,W)$ is complete

[[Dual Spaces]]

**Proposition** - let $K$ be $\mathbb{R}$ or $\mathbb{C}$ and let $(V, ||\cdot||_V)$ and $(W, ||\cdot||_W)$ are normed $K$-vector spaces. Let $T: V\rightarrow W$ be a linear operator, then the following are equivalent -

- $T$ is bounded
- $T$ is continuous
- $T$ is uniformly continuous

