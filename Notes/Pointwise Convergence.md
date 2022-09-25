# Definition

Let $f_{n} : E \to \mathbb{R}$ be a sequence of functions. We say that $f_{n}$ converges pointwise if for every $x \in E$ and every $\varepsilon >0$, there exists $N \in \mathbb{N}$ such that if $n \geq N$ we have
$$
|f_{n}(x) - f(x)| < \varepsilon
$$
One way to think about this is that for every fixed $x \in \mathbb{E}$, we have
$$
\begin{align}
g : &E \to \mathbb{R}^{\infty}&  \\
&x \mapsto g_{n} : \mathbb{N} \to \mathbb{R} \\
&  n \mapsto f_{n}(x)
\end{align}
$$
a sequence in $n$, and this sequence converges.

## Characterisation Using Sup Norm

Alternatively we can simply say that
$$
\lim_{n \to \infty} f_{n} = f
$$
where the "distance" we use is the [[Uniform Norm]]
