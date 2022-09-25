# Statement

Let $X > 0$ be a [[Random Variable]]. Then
$$
\mathbb{E}X < \infty \iff \sum_{n=1}^\infty P(X>n) < \infty
$$

# Proof

$\implies$ 
$$
\begin{align}
\infty > \mathbb{E}X &= \int_{0}^\infty P(X>x)dx \\
&= \sum_{n=1}^\infty \int_{n-1}^n P(X > x)dx \\
&\geq \sum_{n=1}^\infty \int_{n-1}^n P(X > n)dx \\
&= \sum_{n=1}^\infty P(X > n) \int_{n-1}^n dx = \sum_{n=1}^\infty P(X>n)
\end{align}
$$
$\impliedby$ 
$$
\begin{align}
\infty > \sum_{n=1}^\infty P(X > n)  &= \sum_{n=1}^\infty \int_{n}^\infty \mu(dx) \\
&=\int_{0}^\infty 1(y \in \mathbb{N})\int_{y}^\infty \mu(dx) \, dy
 \\ 
&=\int_{0}^\infty \int_{y}^\infty 1(y \in \mathbb{N}) \mu(dx)dy \\
&=\int_{0}^\infty \int_{0}^x 1(y \in \mathbb{N}) dy \, \mu(dx) \\
&= \int_{0}^ \infty \left( 1 + \dots + \mathrm{floor}(x) \right) \mu(dx) \\
&=\int_{0}^\infty x\mu(dx) = \mathbb{E}X 
\end{align}
$$


