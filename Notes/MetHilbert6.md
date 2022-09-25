# Completions
Recall from [[MetHilbert4]] that $\mathbb{Q}_{\geq_{0}}$ has [[Completion]] $\mathbb{R}_{\geq_{0}}$.

How can we make a metric space complete i.e that Cauchy sequences converge in that space?

### Theorem 6.1

**Theorem 6.1** Let $(X,d)$ be a [[Metric Space]]. 

Let $\hat{X}$ be the set of Cauchy sequences in $X$ with a metric
$$
\hat{d}(\hat{x}, \hat{y}) = \lim_{n \to \infty} d(x_{n}, y_{n})
$$
and a map $\iota:X\rightarrow \hat{X}$ given by $\iota(x) = (x,x,x,x,\dots)$ for $x \in X$ 

such that $\hat{x}= \hat{y}$ if $d(\hat{x}, \hat{y}) = 0$.

Then $(\hat{X}, \hat{d})$ is a complete metric space, and $\hat{X}$ is the [[Closure]] of $X$ under $\iota$.

**Proof** - 

#### is a metric space

Check axioms.


#### is complete

#### $\iota$ is an isometry (preserves distance)

This is clear from the definition
$$
\hat{d}(\iota(x), \iota(y)) = \lim_{n \to \infty}d(\iota(x)_{n}, \iota(y)_{n}) = d(x,y)
$$
since we define $\iota(x) = (x,x,x,x, \dots)$

#### closure of X under $\iota$ is $\hat{X}$

$\overline{\iota(X)} \subseteq \hat{X}$ is by definition of closure.

Now let $x \in \hat{X}$. Let $z_{n} \in X$ be such that $z_{n} = \hat{x}_{n}$

we want to show
$$
\lim_{n \to \infty}\iota(z_{n}) = x
$$
this is equivalent to showing that
$$
\lim_{n \to \infty}\hat{d}(\iota(z_{n}), x) = 0
$$
(follows from definition of limit of sequences)

Since $\hat{x} \in \hat{X}$ is Cauchy, there exists $M \in \mathbb{N}$ such that if $r,s \in \mathbb{Z}_{\geq M}$, $d(x_{r}, x_{s}) < \frac{\epsilon}{100}$. 

Now let $n \in \mathbb{Z}_{\geq M}$.
$$
\hat{d}(\iota(z_{n}), x) = \lim_{k \to \infty} d(\iota(z_{n})(k), x(k)) = \lim_{k \to \infty}d(x_{n}, x_{k}) \leq \frac{\epsilon}{100} < \epsilon 
$$



