# 1st Lemma

Suppose that we have a sequence of events $A_{n}$, then

$$
\sum_{n=1}^\infty P(A_{n}) < \infty \implies P(A_{n} \text{ i.o}) = 0
$$

# 2nd Lemma

Suppose that $A_{n}$ are [[Independent Random Variables|independent]]. Then 
$$
\sum_{n=1}^\infty P(A_{n}) = \infty \implies P(A_{n} \text{ i.o})
$$

## Why is Independence Needed?

Let's assume $X \sim U[0,1]$. Define $A_{n} = \left\{ X \leq \frac{1}{n} \right\}$. Then $P(A_{n}) = \frac{1}{n} \implies \sum_{n} P(A_{n}) = \infty$.

But
$$
P(A_{n} \text{ i.o}) = P\left( \bigcap_{n>0}\bigcup_{m\geq n} \left\{ X_{m} \leq \frac{1}{m} \right\}  \right)  = P(X = 0) = 0
$$

## Proof of 2nd BCL

It suffices to show that the complement of $A_{n}$ occuring infinitely often is $0$.

Consider $P(\left\{ A_{n} \text{ i.o} \right\}^c) = P(\bigcup_{n>1}\bigcap_{m\geq n} A_{m}^c)$. We can see that $\bigcap_{m \geq n} A_{m}^c$ is an increasing sequence. Hence
$$
\begin{align}
P(\bigcup_{n>1} \bigcap_{m \geq n} A_{m}^c) &= \lim_{n \to \infty}P(\bigcap_{m=n}^\infty A_{m}^c) \\
&= \lim_{n \to \infty}\lim_{N \to \infty} P(\bigcap_{m=n}^N A_{m}^c) \\
&= \lim_{n \to \infty}\lim_{N \to \infty} (1 - P(A_{n})) \dots (1-P(A_{N})) \\
\exp\log \left( P\left( \bigcup_{n >1}\bigcap_{m \geq n}A_{m^c} \right)  \right) &= \exp  \lim_{n \to \infty} \lim_{N \to \infty} \sum_{m=n}^N \log(1 - P(A_{m})) \\
&\leq \exp  \lim_{n \to \infty}\lim_{N \to \infty} \sum_{m=n}^N -P(A_{m})  
\end{align}
$$
Since $\sum_{m}P(A_{m}) = \infty$, we have $\exp\left( -\sum_{m}P(A_{m}) \right) = 0$. Which completes the proof as we have
$$
P(\bigcup_{n>1} \bigcap_{m \geq n} A_{m}^c) = 0
$$


 
