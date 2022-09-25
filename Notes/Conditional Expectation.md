# Definition

Let $X$ be an integrable [[Random Variable]] on $(\Omega, \mathcal{F}, \mathbb{P})$ and $\mathcal{G} \subseteq \mathcal{F}$.

The **conditional expectation** of $X$ given $\mathcal{G}$ is an integrable, $\mathcal{G}$-measurable random variable $Y$ such that
$$
\int_{A}Y d\mathbb{P} = \int_{A} X d\mathbb{P}
$$
for any $A \in \mathcal{G}$. We denote $Y$ as $\mathbb{E}[X | \mathcal{G}]$. 

The intuition is given by [[AdvProb17#Partitions]].

# Properties

## Existence and Uniqueness

**Uniqueness** if $Y_{1}, Y_{2}$ satisfy the same properties, then $Y_{1} \stackrel{a.s}{=} Y_{2}$. For any $A \in \mathcal{G}$,
$$
\int_{A}Y_{1}d\mathbb{P} = \int_{A} Y_{2} d\mathbb{P} \implies \int_{A}(Y_{1} - Y_{2}) d\mathbb{P} = 0
$$
then $Y_{1} = Y_{2}$ almost surely.

**Existence** we know that
$$
\mathbb{E}[Y 1_{A}] = \mathbb{E}[X 1_{A}] \implies \mathbb{E}[(X-Y)1_{A}] = 0
$$
By the [[Simple Function Approximation]] we can show that for any $\mathcal{G}$-measurable functions, 
$$
\mathbb{E}[(X-Y) Z]=0
$$
We can consider this as an inner product, so $X -Y \perp Z$ on the space of $L^1$ functions (this is a [[Hilbert Space]]) with the inner product given by the expectation. We can therefore consider $Y$ to be the orthogonal [[Projections|projection]] of $X$.
