# Definition

Let $X_{n}$ be a sequence of random variables. We say that $X_{n}$ converges **weakly**, or in **distribution** if 
$$
f_{X_{n}}(x) \to f_{X}(x)
$$
for every continuity point of $f_{X}$.

## Laws

While it is clear that this means that
$$
\mu_{X_{n}}((-\infty,t]) \to \mu_{X}((\infty, t])
$$
for any $t \in \mathbb{R}$, it is not necessarily true that the [[Probability Law]] converges for any Borel set.

### Proof/Counterexample

Take $X_{n} \stackrel{a.s}{=} \frac{1}{n}$. Then $X_{n} \xrightarrow{a.s} 0$. Let $B = \{0\}$. Then for any $n$, $\mu_{X_{n}}(B) = 0$ but $\mu_{X}(B) = 1$.
