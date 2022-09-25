## Real Numbers

How to deal with

$$
(\mathbb{R}, \mathcal{B}(\mathbb{R})) \otimes (\mathbb{R}, \mathcal{B}(\mathbb{R}))\dots
$$

The underlying sample space is $\mathbb{R}^\infty$ i.e the [[Sequence Spaces]].

### some set classes

$\mathcal{F}_{n} = \left\{ G_{n} \times \mathbb{R}^{>n} : G_{n} \in \mathcal{B}(\mathbb{R}^n)\right\}$ (cylinders)
$\mathcal{A} = \bigcup_{n} \mathcal{F}_{n}$ (algebra of cylindrical subsets)

**Lemma** $\mathcal{A}$ is an algebra

(1) $\mathbb{R}^\infty = \mathbb{R} \times \mathbb{R}^{>1} \in \mathcal{F_{1}} \subseteq \mathcal{A}$
(2) Let $B \in \mathcal{A}$, $B = G_{n} \times \mathbb{R}^{>n}$, and $B^c = G_{n}^c \times \mathbb{R}^{>n}$.
(3) Let $A, B \in \mathcal{A}$.

Without loss of generality have $m > n$

$$
\begin{align}
A \cap B &= (G_{n} \times \mathbb{R}^{>n}) \cap (G_{m} \times \mathbb{R}^{>m}) \\
&= (G_{m} \cap (G_{n} \times \mathbb{R}^{m-n})) \times \mathbb{R}^{>m}
\end{align}
$$
so $A \cap B \in \mathcal{A}$.


### Sigma Algebra

The [[Borel Sigma Algebra]] over $\mathcal{B}(\mathbb{R}^\infty) = \sigma(\mathcal{A})$