# Statement

Let 
$$
\left\{ \nu^{(n)} : n\geq 1 \right\} 
$$
be a family of probability [[Measure]] satisfying the consistency relation ([[Probability Law]]). Then there exists a unique probability measure $\mu$ on $(\mathbb{R}^\infty, \mathcal{B}(\mathbb{R}^\infty))$ such that 
$$
\mu(G_{n} \times \mathbb{R}^{>n}) = \nu^{(n)}(G_{n})
$$
for all $n \geq 1$, with $G_{n} \in \mathcal{B}(\mathbb{R}^n)$. Where $\mu$ is a measure on $(\mathbb{R}^\infty, \mathcal{B}(\mathbb{R}^\infty))$.

# Proof

The main idea is to use [[Caratheodory Extension Theorem]]. We first define that algebra
$$
\mathcal{A} = \left\{ G_{n} \times \mathbb{R}^{>n} : n\geq 0 \right\} 
$$
and the set function $\hat{\mu} : \mathcal{A} \to [0,1]$ such that
$$
\hat{\mu}(G_{n} \times \mathbb{R}^{>n}) = \nu^{(n)} (G_{n})
$$
We now need to check that it is well deifned. Let $m \in \mathbb{N}$.
$$
\hat{\mu}(G_{n} \times \mathbb{R}^m \times \mathbb{R}^{>m}) = \nu^{(m+n)} (G_{n} \times \mathbb{R}^m) = \nu^{(n)}(G_{n}) = \hat{\mu }(G_{n} \times \mathbb{R}^{>n})
$$
here we use [[Consistency of Probability Laws]]

Next we check that **it is finitely additive**. Let $\Gamma_{1} ,\dots ,\Gamma_{k}$ be disjoint $\in \mathcal{A}$. Recall that $\mathcal{A} = \bigcup_{n}\mathcal{F}_{n}$ where $\mathcal{F}_{n}$ are cylinders with bases on $\mathbb{R}^{>n}$. So we can write $\Gamma_{i} = G_{i} \times \mathbb{R}^{>n}$. So we have $\hat{\mu}(\Gamma_{i}) = \nu^{(n)}(G_{i})$. Since $\nu$ is finitely additive, then $\hat{\mu}$ is finitely additive.

**The main difficulty is trying to prove countable additivity**.

Recall from [[AdvProb2]] that $\Gamma_{n} \downarrow \phi \implies \lim_{n \to \infty}\hat{\mu}(\Gamma_{n})  =0$.

Suppose otherwise, i.e that $\hat{\mu}(\Gamma_{n}) \geq \varepsilon$ for all $n$. Then if we can show that $\bigcap_{n}\Gamma_{n} \neq \phi$ then we have a contradiction.

**Fact** Let $\nu$ be a probability measure on $(\mathbb{R}^n, \mathcal{B}(\mathbb{R}^n))$. For any $G \in \mathcal{B}(\mathbb{R}^n)$ and $\delta >0$ there exists a compact subset $K \subseteq G$ s.t $\nu(G \backslash K) < \delta$.

Recall : $\Gamma_{n} = G_{n} \times \mathbb{R}^{>n}$, $\hat{\mu}(\Gamma_{n}) = \nu^{(n)}(G_{n}) \geq \varepsilon$.

There exists compact $K_{n} \subseteq G_{n}$  s.t
$$
\nu^{(n)} (G_{n} \backslash K_{n}) < \frac{\varepsilon}{2^{n+1}}
$$
Let $\Lambda_{n} := K_{n} \times \mathbb{R}^{>n}$ by finite additivity,
$$
\nu^{(n)}(\Gamma_{n} \backslash \Lambda_{n}) = \nu^{(n)} (G_{n} \backslash K_{n}) < \frac{\varepsilon}{2^{n+1}}
$$
Let 
$$
\tilde{K}_{n} = \bigcap_{k=1}^n K_{k}\mathbb{R}^{n - k}
$$
correspondingly we define $\tilde{\Lambda}_{n} = \tilde{K}_{n} \times \mathbb{R}^{>n}$. Next we want to show that $\tilde{K}_{n} \neq \phi$.

We have 
$$
\begin{align}
\nu^{(n)}(\tilde{K}_{n}) &= \hat{\mu}(\tilde{\Lambda}_{n}) \\
&=\hat{\mu}(\Gamma_{n}) - \hat{\mu}(\Gamma_{n} \backslash \tilde{\Lambda}_{n}) \\
&= \hat{\mu}(\Gamma_{n}) - \hat{\mu}\left(\bigcup_{k=1}^n \Gamma_{n} \backslash \Lambda_{k}\right) \\
& \geq \hat{\mu}(\Gamma_{n}) - \sum_{k=1}^n \hat{\mu}(\Gamma_{n} \backslash \Lambda_{k}) \\
&= \hat{\mu}(\Lambda_{n}) - \sum_{k=1}^n \hat{\mu}(\Gamma_{k} \backslash \Lambda_{k}) \\
& \geq \varepsilon - \sum_{k=1}^n \frac{\varepsilon}{2^k+1} \\
& \geq \frac{\varepsilon}{2}
\end{align}
$$
Since the measure of $\tilde{K}_{n}$ is non-zero, $\tilde{K}_{n}$ is non-empty.

Hence there exists a point $(X_{1}^{(n)}, \dots , X_{n} ^{(n)}) \in \tilde{K}_{n}$.

Look at this triangle -
$$
\begin{align}
X_{1}^{(1)}  \\
X_{1}^{(2)} & X_{2}^{(2)} \\
X_{1}^{(3)} & X_{2}^{(3)}  X_{3}^{(3)}
\end{align}
$$
and so on. For each $n$ we have a vector of points in $\tilde{K}_{n}$. 

But note that for $l \leq n$, $X_{1:l}^{(n)} \in K_{l}$. We know also that $X_{1}^{(n)} \in K_{1}$ for all $n$.

By compactness, there exists a subsequence $m(n)$ such that $X_{1}^{m_{1}(n)} \to X_{1} \in K_{1}$.

Again we then have $(X_{1}^{m_{1}(n)}, X_{2}^{m_{1}(n)}) \in K_{2}$. But then there's a subsequence of $m_{1}(n)$ we denote as $m_{2}(n)$ such that we have convergence to $(X_{1}^`, X_{2}) \in K_{2}$. But since $m_{2}$ is a subsequence of $m_{1}$, we must have that $X_{1}^` = X_{1}$.

Inductively, $X_{1:n} \in K_{n}$.

This will give a point $x^* = (x_{1}, x_{2}, \dots, x_{n}, \dots)$

Now since $\Lambda_{n}$ is a cylinder on $K_{n}$, $x^* \in K_{n} \implies x^* \in \Lambda_{n}$. Since this is true for all $n$, $x^* \in \bigcap_{n} \Lambda_{n} \subseteq \bigcap_{n} \Gamma_{n}$.

Hence 
$$
\bigcap_{n}\Gamma_{n} \neq \phi
$$
which is a contradiction.

