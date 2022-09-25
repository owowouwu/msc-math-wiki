# Statement

Let $X_{n}$ be a sequence of [[Independent Random Variables]]. If

1. $\sum_{n}\mathbb{E}X_{n} < \infty$
2. $\sum_{n} \text{Var}(X_{n}) < \infty$

then $\sum_{n}X_{n}$ converges almost surely.

# Proof

Without loss of generality we can assume $\mathbb{E}X_{n} = 0$ (by centralising).
$$
\begin{align}
P(\max_{{n \leq l \leq N}} | S_{l} - S_{n}| \geq \varepsilon) &\leq \frac{1}{\varepsilon^2} \sum_{k = n+1}^N \text{Var}(X_{k}) \\
&\leq \frac{1}{\varepsilon^2}\lim_{n \to \infty}\sum_{k=n+1}^\infty \text{Var}(X_{k})
\end{align}
$$
Since $\sum_{k}\text{Var}(X_{k})$ is convergent, we know that the tail sum should converge to 0. Hence $S_{k}$ is Cauchy, so it converges. 

## Example

Consider the alternating series
$$
\sum_{n} \frac{X_{n}}{n}
$$
where $X_{n} =1$ with $p$ and $X_{n}=-1$ with $1-p$.

Let $X_{n}$ be i.i.d with $P(X_{n} = 1) = \frac{1}{2} = P(X_{n} = -1)$. Let $Y = \frac{X_{n}}{n}$. Now clearly for any $n$, $\mathbb{E}Y_{n} = 0$ so $\sum_{n} \mathbb{E}Y_{n} = 0$. On the other hand, 
$$
\begin{align}
\text{Var}(Y_{n}) = \frac{1}{n^2} \text{Var}(X_{n}) \implies \sum_{n}\text{Var}(Y_{n}) < \infty
\end{align}
$$
So $\sum_{n} \frac{X_{n}}{n}$ converges.