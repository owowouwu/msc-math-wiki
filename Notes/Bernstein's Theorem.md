# Statement

Recall from the [[Stone Weierstrass Using SLLN]] proof that we can approximate any continuous function $f :[0,1] \to \mathbb{R}$ by a sequence of polynomials 
$$
p_{n}(x) = \sum_{k=0}^n \binom{n}{k} f\left( \frac{k}{n}\right) x^k (1-x)^{n-k}
$$
and $p_{n}$ converges **pointwise** for each $x$.

**Bernstein's** theorem states that $p_{n}$ converges to $f$ **uniformly** on $[0,1]$.

We call these polynomials **Bernstein polynomials**.

# Proof
We want to show [[Uniformly Continuous|uniform continuity]]

Given a fixed $x \in [0,1]$, $p_{n}(x) = \mathbb{E}\left[ f\left( \frac{S_{n}}{n} \right) \right]$.

Since $f$ is continuous on a bounded interval, it is [[Uniformly Continuous]]. Hence if $\left| \frac{S_{n}}{n} - x \right| < \delta$ then we have $\left| f\left( \frac{S_{n}}{n} \right) - f(x) \right| < \varepsilon$.

So
$$
\begin{align}
|p_{n}(x) - f(x)| &= |\mathbb{E}\left[ f\left( \frac{S_{n}}{n} \right) \right] - f(x)|  \\
& \leq \mathbb{E}\left[ |f\left( \frac{S_{n}}{n} \right) - f(x) \right] \\
&= \mathbb{E}\left[ |f\left( \frac{S_{n}}{n} \right) - f(x)| ; |\frac{S_{n}}{n}-x| < \delta \right]  + \mathbb{E}\left[ \left| f\left( \frac{S_{n}}{n} \right) - f(x) \right| ; | \frac{S_{n}}{n} -x | \geq \delta\right]  \\
&\leq \varepsilon + 2M P\left( \left| \frac{S_{n}}{n} - x \right| \geq \delta  \right) \\
&\leq \varepsilon +2M \frac{1}{\delta^2} \mathrm{Var}\left( \frac{S_{n}}{n} \right) \\
&= \varepsilon + 2M \frac{x(1-x)}{n\delta^2} \\
&\leq \varepsilon + 2M \frac{1}{n\delta^2}
\end{align}
$$
Choose $N$ s.t $n>N$, $\frac{1}{n\delta^2} < \varepsilon$.

