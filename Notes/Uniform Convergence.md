# Definition

Let $f_{n}: E \to \mathbb{R}$ be a sequence of functions. We say that $f_{n}$ **uniformly converges** to some $f$ if for every $\varepsilon>0$ there exists an $N \in \mathbb{N}$ such that if $n\geq N$ we have for every $x \in E$ that
$$
|f_{n}(x) - f(x)| < \varepsilon
$$
## Comparison with [[Pointwise Convergence]]
Written purely with quantifiers, uniform convergence is
$$
\forall \varepsilon>0 \,\exists N \in \mathbb{N} \, \text{ such that } n \geq N \implies \forall x \in E, |f_{n}(x) - f(x)| < \varepsilon
$$
On the other hand, for pointwise convergence the $x$ is fixed from the start:
$$
\forall x \in E, f_{n}(x) \to f(x)
$$
where $f_{n}(x) \to f(x)$ means that
$$
\forall \varepsilon>0 \, \exists N \in \mathbb{N} \text{ such that } n\geq N \implies |f_{n}(x) - f(x)| < \varepsilon
$$
i.e it converges as a sequence.

## Intuition

It is similar to the notion of a function being [[Uniformly Continuous]], in that if we fix an $\varepsilon>0$ all functions $f_{n}$ fall between an interval $f(x) - \varepsilon$ and $f(x) + \varepsilon$ for every $x$, just like how with uniform continuity our function $f$ does not escape a "box" around $f$.

