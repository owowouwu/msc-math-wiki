A way of constructing the real numbers $\mathbb{R}$ from the rationals $\mathbb{Q}$

Denote $\hat{\mathbb{Q}}_{\geq_{0}}$ as the set of all Cauchy sequences in the positive rationals $\mathbb{Q}_{\geq_{0}}$ **with**
$$
(a_{1},a_{2},a_{3},\dots) = (b_{1},b_{2},b_{3},\dots)
$$
if $\lim_{n\rightarrow \infty} d(a_{n},b_{n})=0$. 

Define addition by the addition of sequences
$$
(a_{1},a_{2},\dots) + (b_{1},b_{2},\dots) = (a_{1}+b_{1},a_{2}+b_{2},\dots)
$$
and multiplication by
$$
(a_{1},a_{2},\dots)\times(b_{1},b_{2},\dots) = (a_{1}b_{1}, a_{2}b_{2},\dots)
$$

Define 
$$
\tau: \mathbb{Q}_{\geq_{0}}\rightarrow \hat{\mathbb{Q}}_{\geq_{0}}
$$
by 
$$
\tau(a) = (a,a,a,\dots)
$$
Define an order on $\hat{\mathbb{Q}}_{\geq_{0}}$ by $x\leq y$ if there exists $z\in \mathbb{Q}_{\geq 0}$ by

Define a distance $\hat{d}:\hat{\mathbb{Q}}_{\geq_{0}} \times \hat{\mathbb{Q}}_{\geq_{0}}$ by
$$
\hat{d}((a_{1},a_{2},\dots), (b_{1},b_{2},\dots)) = (d(a_{1},b_{1}), d(a_{2},b_{2}),\dots)
$$
## How is this Equivalent to $\mathbb{R}$?

Once we have a bijection, we can use the above operations to define addition and multiplication on the real numbers.

Recall that the decimal expansions of the real numbers can be written as
$$
z + \sum_{k=1}^\infty d_{k}10^{-k}
$$
where $z\in \mathbb{Z}$ and $d_{k} \in \{0,1,2,\dots\}$. This is a Cauchy sequence in $\mathbb{Q}_{\geq_{0}}$

So why is this a bijection? i.e how can we start with a Cauchy sequence in $\mathbb{Q}_{\geq_{0}}$ and end with a decimal expansion?

**Idea** - recall that for any Cauchy sequence, we can traverse the sequence until eventually the distances between terms $a_m$ and $a_n$ become less than some arbitrary value.

So we can go down the sequence to get a rational number up to some $10^{-k}$ precision i.e first $k$ decimal places.