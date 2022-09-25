# Statement

Let $X_{n}$ be a sequence of [[Random Variable]] with $X_{n} \xrightarrow{p} X$. Then for any $f: \mathbb{R} \to \mathbb{R}$ continuous, $f(X_{n}) \xrightarrow{p} f(X)$.

By extension we also have that
$$
f(X_{n}) \xrightarrow{d} f(X)
$$
# Proof

We want to show for any $\varepsilon>0$, $P(|f(X_{n}) - f(X)| > \varepsilon) \to 0$. Fix $M \in \mathbb{N}$ large.
$$
\begin{align}
P(|f(X_{n}) - f(X)| > \varepsilon) &= P(|f(X_{n}) - f(X)| > \varepsilon; |X_{n}| \leq M; |X| \leq M) + P(|f(X_{n}) - f(X)| ; |X_{n}| > M; |X| > M) \\
&\leq P(|f(X_{n}) - f(X)| > \varepsilon; |X_{n}| \leq M; |X| \leq M) +P(|X| > M) \\
\end{align}
$$
Since $f$ is continuous, it is [[Uniformly Continuous]] on $[-M, M]$. This implies that for any $\varepsilon>0$, there exists $\delta_{\varepsilon}$ such that for any $x,y \in [-M, M]$, $|x-y| < \delta_{\varepsilon} \implies |f(x)-f(y)| < \varepsilon$.

Hece $\left\{ |f(X_{n}) - f(X)| > \varepsilon\right\} \subseteq \left\{ |X_{n} - X| > \delta_{\varepsilon} \right\}$ for $|X_{n}| < M$ and $|X| < M$.
$$
P(|f(X_{n}) - f(X)|) \leq P(|X_{n} - X| > \delta_{\varepsilon}) + P(|X| > M)
$$
Since $X_{n} \xrightarrow{p} X$ the first term can be made arbitrarily small, and with large enough $M$ $P(|X| > M)$ can also be made arbitrarily small.

Hence $f(X_{n}) \xrightarrow{p} f(X)$.