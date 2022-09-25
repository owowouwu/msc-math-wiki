# Proof

Suppose we have a continuous function $f$ on $[0,1]$. We want to approximate this with a sequence of polynomials.

Fix $x \in [0,1]$. Let $X_{n} \sim B(x)$.

We know $S_{n} := X_{1} + \dots + X_{n} \sim B(n,x)$.

$$
\begin{align}
p_{n}(x) :=\mathbb{E}\left[ f\left( \frac{S_{n}}{n} \right) \right] &= \sum_{k=0}^n \binom{n}{k}f\left( \frac{k}{n} \right) x^k(1-x)^{n-k}
\end{align}
$$
this is a polynomial of degree $n$.

By the [[Strong Law of Large Numbers]], $\frac{S_{n}}{n} \xrightarrow{a.s} \mathbb{E}X_{1} = x$. By the continuity of $f$, $f\left( \frac{S_{n}}{n} \right) \xrightarrow{a.s} f(x)$. By the [[Dominated Convergence Theorem]],
$$\mathbb{E}\left[ f\left( \frac{S_{n}}{n} \right) \right] \xrightarrow{a.s} \mathbb{E}[f(x)] = f(x)$$
