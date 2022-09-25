# Statement

Let $X_{n}$ be i.i.d and $S_{n}:= X_{1} + \dots + X_{n}$. 

1. Suppose $\mathbb{E}|X_{1}| < \infty$. Then $\frac{S_{n}}{n} \xrightarrow{a.s} \mathbb{E}X_{1}$.
2. Suppose $\mathbb{E}|X_{1}| = \infty$. Then $\limsup \frac{|S_{n}|}{n} = \infty$ almost surely.

# Proof

The main idea is as follows - 

Let $Y_{n}$ where $Y_{n}= X_{n}$ with high probabiltiy (?)
...

Let $Y_{n} = X_{n} 1_{{|X_{m}| \leq n}}$ (truncating $X_{n}$).

show $P(X_{n} \neq Y_{n} \text{i.o}) = 0$ so eventually $X_{n} = Y_{n}$.

so this implies
$$
\frac{1}{n}\sum_{j=1}^n (X_{j}- Y_{j}) \xrightarrow{a.s} 0
$$
as $X_{j} - Y_{j}$ is a sequence that is eventually finite [[Sequence Spaces]]

now check convergence of $\sum_{n=1}^\infty \frac{Y_{n} -\mathbb{E}Y_{n}}{n}$ 

define $Z_{n} = \frac{Y_{n} - \mathbb{E}Y_{n}}{n}$

check [[Kolmogorov Two Series Theorem]],

$\sum_{n=1}^\infty \mathbb{E}Z_{n} = 0$ is trivial

$\text{Var}(Z_{n}) = \frac{1}{n^2}(\text{Var}(Y_{n})) \leq \frac{1}{n^2}\mathbb{E}Y_{n}^2 = \frac{1}{n^2}\mathbb{E}[X_{n}^2 1_{{|X_{n}| \leq n}}]$

$$
\text{Var}Z_{n} = \frac{1}{n^2} \int_{|X| \leq n}X^2 d\mu
$$
now we want to check the sum over $\text{Var}(Z_{n})$ is finite. 
$$
\begin{align}
\sum_{n=1}^\infty \frac{1}{n^2} \sum_{j=1}^n \int_{j-1 < |X| \leq j} X^2 d\mu &= \sum_{j=1}^\infty \sum_{n=j}^\infty \frac{1}{n^2} \int_{j-1 < |X| \leq j}X^2 d\mu \\
&\leq \sum_{j=1}^\infty \frac{2}{j} \int_{j-1 < |X| \leq j}X^2 d\mu \\
&\leq \sum_{j=1}^\infty \frac{2}{j} \int_{j-1 < |X| \leq j}jXd\mu \\
&= 2\int_{\mathbb{R}}Xd\mu = 2 \mathbb{E}X_{1} < \infty 
\end{align}
$$
here we exchange the order of summation and use the [[Bound for Sum of Squares of Reciprocals]]

hence $\sum_{n} \text{Var}(X_{n})$ is convergent. hence $\sum_{n}Z_{n}$ converges almost surely.

from [[Kronecker's Lemma]], 
$$
\frac{1}{n}\sum_{j=1}^n (Y_{j} - \mathbb{E}Y_{j}) \xrightarrow{a.s} 0
$$
it remains to show that
$$
\frac{1}{n}\sum_{j=1}^n \mathbb{E}Y_{j} \xrightarrow{a.s} \mathbb{E}X_{1}
$$
since [[Convergence of Sequence Implies Convergence of Average]] it suffices to prove $\mathbb{E}Y_{j} \to \mathbb{E}X_{1}$.
$$
\mathbb{E}Y_{n} = \int_{|X| \leq n} Xd\mu
$$
we know $X 1_{|X| \leq n} \to X$.

so using [[Dominated Convergence Theorem]]
$$
\lim_{n \to \infty} \mathbb{E}Y_{n} = \int_{\mathbb{R}} Xd\mu = \mathbb{E}X_{1}
$$

combining the above results we have the strong law of large numbers


