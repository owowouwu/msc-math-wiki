# Definition

Let $X$ be a [[Random Variable]] and $\Lambda(\lambda)$ be its [[Cumulant Generating Function]], i.e
$$
\Lambda(\lambda) = \log \mathbb{E}[e^{\lambda X_{1}}]
$$
The **Legendre** transform of $\Lambda$ is defined to be
$$
\Lambda^*(x) = \sup_{\lambda \in \mathbb{R}}(\lambda x - \Lambda(\lambda))
$$
where $x \in \mathbb{R}$.

## Properties

Suppose $X \in L^1$ and $\mathbb{E}X < \infty$.

1. $\Lambda^*(\mathbb{E}X) = 0 = \inf_{x} \Lambda^*(x)$ (proof - use Jensen's to show a upper bound)
2. If $x > \overline{x}$ then $\Lambda^*(x) = \sup_{\lambda \geq 0}(\lambda x - \Lambda(\lambda))$, and in this case $\Lambda^*$ is increasing. Similarly we have a case for $x< \overline{x}$. (proof - show that for $\lambda <0$, $\lambda \overline{x} - \Lambda(\lambda)=0$).

### Can be Unbounded

Consider $X_{1}=1$ with 0.5 and $X_{1} = -1$ with 0.5

For $x>1$, $\Lambda^*(x) = \infty$.

 