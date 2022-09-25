# Statement

For any $j \in \mathbb{N}$,
$$
\sum_{n=j}^\infty \frac{1}{n^2} \leq \frac{2}{j}
$$
# Proof

For $j=1$ we have
$$
\sum_{n=1}^\infty \frac{1}{n^2} = \frac{\pi^2}{6} < 2
$$
For $j > 1$ we have
$$
\begin{align}
\sum_{n=j}^\infty \frac{1}{n^2} &\leq \sum_{n=j}^\infty \frac{1}{n^2 -n} \\
&= \sum_{n=j}^\infty \frac{1}{n-1} - \frac{1}{n} \\
&= \frac{1}{j-1}  \\
&\leq \frac{2}{j}
\end{align}
$$
