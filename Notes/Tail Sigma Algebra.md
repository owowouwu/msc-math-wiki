# Definition

Let $\varphi_{n}$ be a sequence of sub-[[Sigma Algebra]] of $\mathcal{F}$ and let 
$$
\tau_{n} = \sigma(\varphi_{n+1}, \varphi_{n+2}, \dots)
$$
Notice that $\tau_{n}$ becomes smaller and smaller as $n$ increases - we are taking less and less sets. We define the tail $\sigma$-algebra to be
$$
\tau = \bigcap_{n} \tau_{n}
$$
## Examples

### Convergence of Sums of RVs

Usually we like to take take $\mathcal{G}_n = \sigma(X_{n})$ where $X_{n}$ is a sequence of [[Random Variable]]. Consider the set $F = \left\{ \sum_{n=1}^\infty X_{n} \text{ converges} \right\}$. To see that this is in the tail sigma algebra $T$,

We want to show that for every fixed $n$, $F \in T_{n}$. But note that
$$
F = \left\{ \sum_{k=n+1}^\infty X_{k} \text { converges} \right\} 
$$
Since if the sum converges, any tail sum converges.

So clearly
$$
F \in T_{n} = \sigma(X_{n+1}, X_{n+2}, \dots)
$$

### Convergence of Sups

Now consider the event 
$$
G = \left\{ \sup_{n \geq 1}X_{n} \leq 0 \right\} 
$$
Clearly this is not a tail event as the $\sup$ of a sequence of real numbers becomes smaller as less terms are included in the sequence. More rigorously -
$$
G = \bigcap_{n=1}^\infty \left\{ X_{n} \leq 0 \right\} 
$$
So we need EVERY $X_{n}$ to be included