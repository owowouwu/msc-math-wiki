# Limits

## Application of [[Borel-Cantelli Lemma#2nd Lemma]]

An application to random walks. Let $P(X_{n} = 1) = p$, and $P(X_{n} = -1) = 1-p = q$ and $S_{n} = X_{1} + \dots + X_{n}$ with $S_{0} = 0$.

Then the event that $S_{n} = 0$ infinitely often is $S_{2n} = 0$ infinitely often.
$$
\begin{align}
P(S_{2n} = 0) &= \binom{2n}{n} p^n q^n \\
&= \frac{(2n)!}{(n!)^2} (pq)^n \\
&\sim \frac{1}{\sqrt{ \pi n }} (4pq)^n \\
&= \frac{1}{\sqrt{ 2\pi }} \left( 1 - (1-2p)^2 \right) ^n
\end{align}
$$
Lines 2 to 3 use Stirling's Formula.

If $p \neq \frac{1}{2}$ the quadratic term is less than $1$ so by the 1st BC $P(S_{2n} = 0 \text{ i.o}) = 0$.

For $p = \frac{1}{2}$ consider the event
$$
\left\{ \limsup_{n \to \infty} \frac{S_{n}}{\sqrt{ n }} = \infty, \liminf \frac{S_{n}}{\sqrt{ n }} = -\infty \right\} \subseteq \left\{ S_{n} \text{ i.o} \right\}  
$$
 The first event implies that there are two subsequences of time such that the sequence drifts to $\infty$ and $-\infty$ respectively. But to do so it must cross the origin $0$. It suffices to show that 
 $$
P\left( \limsup_{n \to \infty} \frac{S_{n}}{\sqrt{ n }} = \infty \right) = 1
$$
We introduce $A_{M} = \left\{ \limsup_{n \to \infty} \frac{S_{n}}{\sqrt{ n }} \geq M \right\}$. Clearly $A_{M} \uparrow A$. So it suffices to show that $P(A_{M}) = 1$ for all $M$.

We claim that $A_{M}$ is a tail event of $X_{n}$.
$$
\frac{S_{n}}{\sqrt{ n }} = \frac{X_{1} + \dots + X_{M} + X_{{M+1}} + \dots + X_{n}}{\sqrt{ n }}
$$
Notice that as $n \to \infty$, the first $M$ terms go to $0$. So $M$ only depends on $X_{M+1}, \dots$. By [[Kolmogorov's Zero One Laws]], $P(A_{m}) = 0$ or $P(A_{m}) = 1$. We now need to show that $A_{M}$ is positive.

First observe that
$$
\limsup_{n \to \infty} \left\{ \frac{S_{n}}{\sqrt{ n }} \geq M \right\} \subseteq A_{M} 
$$
$$
\begin{align}
P\left( \bigcap_{n >0} \bigcup_{m \geq n} \left\{ \frac{S_{m}}{\sqrt{ m }} \geq M\right\}   \right) &= \lim_{n \to \infty} P \left( \bigcap_{m = n} \left\{ \frac{S_{m}}{\sqrt{ m }} \geq M \right\}  \right)  \\
& \geq \lim_{n \to \infty} P\left( \frac{S_{n}}{\sqrt{ n }}  \geq M\right)  \\
&= P(Z \geq M) >0
\end{align}
$$
Using the Central Limit Theorem.
