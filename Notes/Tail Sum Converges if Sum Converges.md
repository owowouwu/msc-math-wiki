# Statement

Let $\left\{ a_{n} \right\}_{n=1}^\infty \in \mathbb{R}$. Then
$$
\sum_{n}a_{n} < \infty \implies \lim_{m \to \infty} \sum_{n=m+1}^\infty a_{n} = 0
$$

# Proof

Let $\left\{ a_{n} \right\}$ be a sequence in $\mathbb{R}$. Suppose $\sum_{n}a_{n}$ converges. Let $T_{m} = \sum_{n=m+1}^\infty a_{n}$. We want to show that $\lim_{m \to \infty}T_{m} = 0$.

Let $\varepsilon >0$. We want to show there exists a $K \in \mathbb{N}$ such that if $n > K$, $|T_{n}| < \varepsilon$.

Since $\sum_{n}a_{n}$ converges, the sequence of partial sums $S_{n} = \sum_{k=1}^n a_{k}$ is [[Cauchy]]. So there exists $N \in \mathbb{N}$ such that for any $r,k > N$, 
$$
|S_{k} - S_{r}| = |\sum_{n=r+1}^k a_{n}| <\varepsilon 
$$Now notice that
$$
|T_{n}| = |\sum_{k=1}^\infty a_{n} - \sum_{k=1}^n a_{k}| = |\sum_{k=1}^\infty a_{n} - S_{n}| 
$$
Let $K = N$, and suppose $n, m >K$. Then we have
$$
|T_{n}| = \lim_{m \to \infty}|S_{m} - S_{n} | < \varepsilon
$$
