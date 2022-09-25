# Definition

## Univariate Case

Let $X$ be a [[Random Variable]] on $(\Omega, \mathcal{F}, P)$.

The law of a random variable is defined as the probability a random variable takes certain values on a state space
$$
\mu_{X}(B) = P(X \in B)
$$
where $B \in \mathcal{B}(\mathbb{R})$.

## Joint Laws

For any $n$, the joint law of $(X_{1}, \dots X_{n})$ is the probability measure on $(\mathbb{R}^n, \mathcal{B}(\mathbb{R}^n))$
$$
\mu_{X}^{(n)}(G_{n}) = P(X_{1}, \dots , X_{n} \in G_{n})
$$

### Consistency Property
$$
\mu_{X}^{(n+m)}(G_{n} \times \mathbb{R}^m) = \mu_{X}^{(n)}(G_{n})
$$
for any $m,n \geq 1$. This is easy to see as $(X_{n+1}, \dots , X_{m+n}) \in \mathbb{R}^m$ has probability 1.



## Infinite Dimensional Case

Let $X = \left\{ X_{n} : n \geq 1 \right\}$ be a sequence of [[Random Variable]] on $(\Omega, \mathcal{F}, P)$. 
$$
X : \Omega \to \mathbb{R}^\infty \quad X(\omega ) = (X_{1}(\omega), X_{2}(\omega), \dots)
$$
The probability measure on $(\mathbb{R}^\infty, \mathcal{B}(\mathbb{R}^\infty))$ is defined by
$$
\mu_{X}(B) = P(X \in B)
$$

