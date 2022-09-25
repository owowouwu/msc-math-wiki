## Existence

## Construction

### 1.

Let $d(x, \overline{W}) = \inf \left\{ d(x,w) : w \in \overline{W} \right\}$.

Define $P : H \to H$ by
$$
P(x) = y
$$
where $y \in \overline{W}$ such that $d(x,y) = d(x,W)$.
(i.e the projection minimises the distance between the two points)

### 2.

Let $(e_{1}, e_{2}, \dots)$ be an orthonormal sequence in $H$, (i.e $\langle e_{i}, e_{j} \rangle = \delta_{ij}$ )

Let $\overline{W} = \overline{\text{span}\left\{ e_{1}, e_{2}, \dots \right\}}$

Define
$$
P : H \to H \, P(x) = \sum_{n=1}^\infty \langle x, e_{n} \rangle e_{n}
$$
(orthonormal basis expansion)

### Why are these valid constructions?

#### 1. Why does $y$ exist?

Let $x \in H$. Since $d(x,W) = \inf \left\{ d(x,w) : w \in \overline{W} \right\}$, then there is a sequence $w_{1}, w_{2}, \dots \in \overline{W}$ such that $\lim_{n \to \infty} d(x, w_{n}) = d(x,W)$.

Let $y = \lim_{n \to \infty} w_{n}$. Since $\overline{W}$ is closed, $y \in \overline{W}$.
