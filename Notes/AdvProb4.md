# Distribution Functions and Laws

## Distribution Function
$$
F_{x} : \mathbb{R} \rightarrow \mathbb{R} \, F_{X}(x) = P(X\leq x)
$$

Properties

- Monotonicity $F(x) \leq F(y)$ for all x,y
- Right continuity 
- $F(-\infty) = 0$, $F(\infty) = 0$

**Proof** of 2

Let $h_{n} = \frac{1}{n}$. The sequence of events $\{X \leq x + \frac{1}{n} \}$ is a decreasing sequence of events,
$$
\{X \leq x + \frac{1}{n} \} \downarrow \{X\leq x\}
$$
So by the continuity of probability measures,
$$
\lim_{n\rightarrow \infty} F\left( x + \frac{1}{n} \right) = \lim_{n\rightarrow \infty}P\left( X\leq x + \frac{1}{n} \right) = P(X\leq x)= F(x)
$$

Any function $f: \mathbb{R}\rightarrow \mathbb{R}$ satisfying 1-3 is a DF.

## Law

The law is a probability measure on $\mathbb{R}$. 
$$
\mu_{X}(B) = P(X \in B)
$$
for any $B\in \mathcal{B}(\mathbb{R})$.


**Theorem** - there is a 1-1 correspondence between DFs and probability measures on $\mathbb{R}$.

### Constructing Probability Measures from DFs

Recall from [[AdvProb3]]. Define

- $\mu_{F}((-\infty, b]) = F_{X}(b)$
- $\mu_{F}((a,b]) = F_{X}(b) - F_{X}(a)$
- $\mu_{F}((a, \infty)) = 1-F_{X}(a)$

Extend $\mu_{F}$ to $\mathcal{A}$ by finite additivity. Now need to check countable additivity and use [[Caratheodory Extension Theorem]].

Natural extensions exist for $\mathbb{R}^n$.

## Constructing RVs from F

How do we construct a RV $X$ such that $X\sim F$?

We want 

- A probability space for $X$
- $X$ itself.

Just take $(\mathbb{R}, \mathcal{B}(\mathbb{R}), \mu_{F})$, and let $X(\omega) = \omega$.

## Limit Theorems

When can we change limits with integrals

**def**  - almost everywhere

Let $(\Omega, \mathcal{F}, \mu)$ be a measure space.

A $\mu$-null set is a measurable set $N\in \mathcal{F}$ such that $\mu(N) = 0$. We say that a property holds "$\mu$ almost everywhere" if it holds for all $\omega$ outside some $\mu$-null set. In a probability context, we say it holds "almost surely".

[[Monotone Convergence Theorem]]
[[Fatou's Lemma]]
[[Dominated Convergence Theorem]]
