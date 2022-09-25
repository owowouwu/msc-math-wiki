# Statement

Let $(\Omega, \mathcal{F}, P)$ be a [[Probability Space]]

Let $\mathcal{G}_{n}$ be a [[Independence of Sigma Algebras|independent sequence of sub sigma algebras]] of $\mathcal{F}$.

Then for any $A$ in $\mathcal{F}$, $P(A) = 0$ or 1.

An equivalent formulation for random variables $X_{n}$ and [[Tail Events]] can obtained by taking $\mathcal{G}_{n}$ to be $\sigma(X_{n})$. 

# Proof

Let $\mathcal{F}_{n} = \sigma(\mathcal{G}_{1}, \dots, \mathcal{G}_{n})$ and $\mathcal{F}_{\infty} = \sigma(\bigcup_{n}\mathcal{F_{n}})$.

By independence, $\mathcal{F}_{n} \perp T_{n}$ where $T_{n}=\sigma(\mathcal{F_{n+1}}, \mathcal{F_{n+2}}, \dots)$. Hence $\mathcal{F}_{n} \perp T$, the tail $\sigma$-algebra of $\mathcal{F}_{n}$. By extension $F_{\infty} \perp T$.

Suppose $A \in T$ and consider
$$P(A) = P(A \cap A)$$
Take the first $A$ as a member of $\mathcal{F}_{\infty}$ and the second $A$ as a member of $T$. By independence,
$$
P(A) = P(A)^2 
$$
Which implies $P(A)= 0$ or $P(A) = 1$.