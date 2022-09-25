# Constructing Independent Random Variables

Let $F,G$ be distribution functions. How to make $X \sim F$, $Y \sim G$ such that $X \perp Y$?

Recall from [[AdvProb5]] how we constructed [[Product Measurable Spaces]].

Consider $(\mathbb{R}, \mathcal{B}(\mathbb{R}), \mu_{F})$ and $(\mathbb{R}, \mathcal{B}(\mathbb{R}), \mu_{G})$ and let

- $\Omega = \mathbb{R}^2$,
- $\mathcal{F} = \mathcal{B}(\mathbb{R}^2)$.
- $P = \mu_{F} \otimes \mu_{G}$

Define 
$$
X: \Omega \to \mathbb{R} ,\, X(x,y) = x
$$
and
$$
Y : \Omega \to \mathbb{R} ,\, Y(x,y) =y
$$
## Proof 

The idea is that we know that $\mu_{F} \otimes \mu_{G}$ is the unique measure such that for any rectangle $A_{1} \times A_{2}$ in $\mathbb{R}^2$, $\mu(A_{1} \times A_{2}) = \mu_{F}(A_{1}) \mu_{G}(A_{2})$. So we need to construct something similar and make use of the property.

### $X \sim F$

$P(X \in A) = \mu(A \times \mathbb{R}) = \mu_{F}(A) \times \mu_{G}(\mathbb{R}) = \mu_{F}(A)$. 

Hence $X \sim F$. A similar argument holds for $Y \sim G$.

### Indepdence 

Since we have established that $P(X \in A) = \mu_{F}(A)$ for any $A \in \mathcal{B}(\mathbb{R})$ and similarly for $Y$ and $\mu_{G}$,
$$
\begin{align}
F(x,y) &= P(X \leq x, Y \leq y)  \\
&= \mu((-\infty, x] \times (-\infty, y]) \\
&= \mu_{F}((-\infty, x])\mu_{G}((-\infty, y]) \\
&= P(X\leq x)P(Y \leq y)
\end{align}
$$
so independence holds.

# Fubini's Theorem for General Measurable Functions

[[Fubini's Theorem#^8c32b8]]

For general $\mu$-measurable functions $f$ we again use the standard argument of approximating $f$ as a limit of simple functions (i.e linear combinations of indicators).

Similar to how we construct the [[Lesbesgue Integration|lebesgue integral]] we need to consider cases where $f \geq 0$ and cases where $f$ is general.

In the case where $f \geq 0$ we can use the [[Monotone Convergence Theorem]] and there are no restrictions on $f$ (we can allow the integral to be $\infty$).

However in the general case we use the argument $f = f^+ - f^-$, which requires that $f$ itself be integrable i.e $f \in L^1$, otherwise we might have $\infty - \infty$ which is not well defined.