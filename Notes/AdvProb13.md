# Proving Bernstein's Theorem

[[Bernstein's Theorem]]

# Large Deviation Principle

[[Cramer's Theorem]]

## How to work out $I_{F}$?

Guessing $I_{F}$ : Let $F = [x, \infty)$. where $x > \overline{x}$.

Let $\lambda \geq 0$. Then we have
$$
\begin{align}
P(\overline{S}_{n} \in F) &= P(\overline{S}_{n} \geq x) \\
&= P(S_{n} \geq nx) \\
&= P(\lambda S_{n} \geq \lambda nx) \\
&= P(e^{\lambda S_{n}} \geq e^{\lambda nx}) \\
&\leq e^{-\lambda nx} \mathbb{E}(e^\lambda S_{n}) \\
&= e^{-\lambda nx} M(\lambda)^n \\
&= \exp \left\{ -\lambda nx + n \Lambda(\lambda) \right\}  \\
&= \exp\{-n(\lambda x - \Lambda(\lambda))\}
\end{align}
$$
Where $M(\lambda)$ is the [[Moment Generating Function]] and $\Lambda(\lambda)$ is the [[Cumulant Generating Function]]

We get the most optimal bound by taking the $\sup$
$$
P(\overline{S}_{n} \in F) \leq \exp \left\{ -n \sup_{\lambda \geq 0} (\lambda x - \Lambda(\lambda)) \right\} 
$$
This is known as the [[Legendre Transform]]. By monotonicty we have
$$
\sup_{\lambda \geq 0}(\lambda x - \Lambda(\lambda)) = \inf_{y \geq \overline{x}}(\lambda y - \Lambda(\lambda))
$$