# Statement

Let $\left\{ a_{n} \right\} \in \mathbb{R}$ be a sequence with $a_{n} \to l$. Then
$$
s_{n} = \frac{a_{1} + \dots + a_{n}}{n} \to l
$$

# Proof

Let $\varepsilon > 0$. There exists $K \in \mathbb{N}$ such that if $n \geq K$, $|a_{n}| < \varepsilon$. Hence
$$
\begin{align}
|s_{n} - l| &= \frac{1}{n}|a_{1} + \dots  +a_{n} -l | \\
&\leq \frac{1}{n}|a_{1} + \dots + a_{n-1}| + \frac{1}{n} |a_{n}- l| \\
&< \frac{1}{n}|a_{1}+ \dots + a_{n-1}| +\frac{\varepsilon}{n} \\
&< \frac{1}{n}|a_{1}+ \dots + a_{n-1}| + \varepsilon \\
&\to \varepsilon
\end{align}
$$
