# Construction of Product Measures

Let
$$
(\Omega, \mathcal{F}) = (\Omega_{1}\times \Omega_{2}, \mathcal{F}_{1} \otimes \mathcal{F}_{2})
$$
be a [[Product Measurable Spaces]]

Using [[Fubini's Theorem]], let $f = 1_{F}(\omega_{1}, \omega_{2})$. Define $\mu(F) = \int _{\Omega_{1}} I_{1}^f(\omega_{1})\, d\mu_{1}$

Then $\mu$ is a finite measure on the product space, and it is the unique measure such that
$$
\mu(A_{1} \times A_{2}) = \mu(A_{1})\mu(A_{2})
$$
for all $A_{1} \in \mathcal{F}_{1}$ and $A_{2} \in \mathcal{F}_{2}$. (independence). This is called $\mu = \mu_{1} \otimes \mu_{2}$

## Proof that $\mu$ is a Finite Measure on the Product Space

### Lemma - Fixing One Dimension
Let $f \in b\mathcal{F}$
1. $\forall \omega_{1} \in \Omega_{1}$, $\omega_{2} \mapsto f(\omega_{1} ,\omega_{2}) \in b \mathcal{F}_{2}$
2. $\forall \omega_{2} \in \Omega_{2}$, $\omega_{1} \mapsto f(\omega_{1}, \omega_{2}) \in b \mathcal{F}_{2}$
**Proof** - 
We want to prove for simple functions (i.e linear combinations of indicators) that converge pointwise to some arbitrary functions $f_{n} \to f$. By linearity, it suffices to prove the lemma for indicator functions $f = 1_{A}$, where $A \in \mathcal{F}$.

Let
$$
\mathcal{H} = \left\{ A \in \mathcal{F} : 1_{A} \text{ 
 satisifes 1 and 2} \right\} 
$$
Now for any $A_{1} \in \mathcal{F}_{1}, A_{2} \in \mathcal{F}_{2}$, 
$$
1_{A_{1} \times A_{2}} = 1_{A_{1}} 1_{A_{2}}
$$
Here if we fix $\omega_{1}$ we have a function $c 1_{A_{2}}(\omega_{2})$ which is clearly $\mathcal{F}_{2}$-measurable, and vice versa if we fix $\omega_{2}$.

So $\mathcal{F}_{1} \times \mathcal{F}_{2} \subseteq \mathcal{H}$, 

Note that $\mathcal{F}_{1} \times \mathcal{F}_{2}$ is a [[pi-System]]. Now we need to check that $\mathcal{H}$ is a [[lambda-System]].

**(L1)** $\Omega \in \mathcal{H}$ is obvious, $1_{\Omega_{1} \times \Omega_{2}}(\omega_{1}, \omega_{2}) = 1$ for any $(\omega_{1}, \omega_{2}) \in \Omega_{1} \times \Omega_{2}$.

**(L2)** Let $A,B \in \mathcal{H}$ with $A \subseteq B$.
$$
1_{B \backslash A} = 1_{B} - 1_{A}
$$
Since this is a linear combination of measurable functions, $1_{B \backslash A}$ is measurable, so $B \backslash A \in \mathcal{H}$.

**(L3)** Let $A_{n} \in \mathcal{H}$ be a sequence of increasing sets such that $A_{n} \uparrow A$. Since pointwise convergence holds for indicator functions, i.e $1_{A_{n}} \to 1_{A}$, $A \in \mathcal{H}$. 

Hence $\mathcal{H}$ is a [[lambda-System]]. By [[Dynkin's pi-lambda Theorem]], we conclude that $\sigma(\mathcal{F_{1} \times F_{2}}) \subseteq \mathcal{H}$, so the lemma holds for the sigma algebra.

### Proof

**(P1)** $\mu(\Omega) = \int_{\Omega_{1}}\left( \int_{\Omega_{2}} 1_{\Omega} d\mu_{2} \right) d\mu_{1} = \int_{\Omega_{1}} 1 d\mu_{1} = 1$
**(P2)** Let $A \in \mathcal{F}$. $\mu(A) \geq 0$ is obvious as indicator functions are non-negative.
**(P3)** We want to prove countable additivity. Suppose $F_{n}$ is a disjoint sequence in $\mathcal{F}$, with $F = \sum_{n=1}^\infty F_{n}$. Now define $G_{n} = \sum_{k=1}^n F_{k}$.
$$
\mu(G_{n}) = \int _{\Omega_{1}} \left( \int _{\Omega_{2}} 1_{G_{n}} \, d\mu_{2}  \right) \, d\mu_{1} 
$$
By disjointedness,
$$
1_{G_{n}} = \sum_{k=1}^n 1_{F_{k}}
$$
$$
\mu(G_{n}) = \sum_{k=1}^n\int _{\Omega_{1}} \left( \int _{\Omega_{2}} 1_{F_{k}} \, d\mu_{2}  \right) \, d\mu_{1} = \sum_{k=1}^n \mu (F_{k})
$$
We know that $G_{n} \uparrow F$ , so $1_{(G_{n})} \uparrow 1_{F}$, so by [[Monotone Convergence Theorem]] 
$$
\mu(F) = \sum_{n=1}^\infty \mu(F_{n})
$$
### Uniqueness

Since $\mu(A_{1} \times A_{2}) = \mu(A_{1})\mu (A_{2})$ holds on $\mathcal{F}_{1} \times \mathcal{F}_{2}$, which is a $\pi$-system, it holds on the [[Sigma Algebra]] and is unqiue

