# Definition

Let $X_{n}$ be a sequence of [[Random Variable]]. We say that $X_{n}$ converges almost surely to $X$ if 

For any $\varepsilon >0$,
$$
\mathbb{P}\left(|X_{k}- X| > \varepsilon \text{ i.o}  \right) = 0
$$
It is similar to [[Pointwise Convergence]], except we say "almost surely" as we do not require pointwise convergence on sets of [[Measure]] 0 (in measure theory, "almost everywhere")
$$
\mathbb{P}(\omega \in \Omega : \lim_{n \to \infty}X_{n}(\omega) = X(\omega)) =1
$$

## Typical Ways of Proving Almost Sure Converge

Use [[Borel-Cantelli Lemma]],

or for random series use [[Kolmogorov Two Series Theorem]]