Let $(H, <>)$ be a [[Hilbert Space]]. Let $\overline{W}$ be a closed subspace.

A projection is a function
$$
\mathcal{P}: H \rightarrow H
$$
such that if $x \in H$, $P(x) \in \overline{W}$

and if $w \in \overline{W}$, $<x,w> = <P(x), w>$

## Properties

Let $P$ and $Q$ be projections on $\overline{W}$. Then 
1. $P = Q$.
2. $P$ is a linear transformation.
3. $P^2 = P$
4. $(I - P)^2 = I - P$
5. $I - P$ is a projection onto $\overline{W}^\perp$
6. $H = \overline{W} \oplus \overline{W}^\perp$

3, 4 are idempotency

Using the idempotency part we can have an equivalent definition of a projection

(a) $P: H \to H$ is a function
(b) $x \in H \implies P(x) \in \overline{W}$
(c) $x \in H \implies (id - P)(x) \in \overline{W}^\perp$


### Proofs

#### 1. Uniqueness

$<Q(x), w> = <x,w> = <P(x), w>$

Hence $\langle P(x) - Q(x), w \rangle = 0$, so $P(x) - Q(x) \in \overline{W}$.

Since $\overline{W}$ is a subspace, $P(x)- Q(x) \in \overline{W}$ and we have $P(x)- Q(x) \in \overline{W} \cap \overline{W}^\perp = 0$

#### 2. Linearity

Let $x_{1}, x_{2} \in H$, and $c \in \mathbb{K}$.

**Addition** - 

$\langle x_{1} , w\rangle + \langle x_{2}, w \rangle = \langle x_{1} + x_{2}, w \rangle$
and
$\langle x_{1}+ x_{2},w \rangle = \langle P(x_{1}+ x_{2}), w \rangle$

so $\langle P(x_{1}), w \rangle + \langle P(x_{2}), w \rangle = \langle  P(x_{1} + x_{2}), w \rangle$
...*same argument as above*

#### 3. Idempotency

#### 6.
Use the fact that $x = P(x) + (I -P)(x)$. 