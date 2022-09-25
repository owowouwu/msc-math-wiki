# Motivation

Let $\left\{ X_{n} \right\}$ be i.i.d with finite mean $\overline{x}$. Define
$$
\overline{S}_{n} = \frac{X_{1}+X_{2}+\dots+X_{n}}{n}
$$
Suppose $F \subseteq \mathbb{R}$ is a set with positive distance at least $\varepsilon$ to $x$.
$$
\left\{ \overline{S}_{n} \in F \right\} \subseteq \left\{| \overline{S}_{n} - \overline{x}| \geq \varepsilon \right\}  
$$
Since [[Strong Law of Large Numbers]] implies weak convergence,
$$
P(\overline{S}_{n} \in F) \leq P(|\overline{S}_{n} - \overline{x}| \geq \varepsilon) \xrightarrow{p} 0
$$
The **large deviation principle** tells us how fast this probability vanishes -
$$
P(\overline{S}_{n} \in F) =O(e^{-n})
$$
i.e this probability decays exponentially in $n$. More precisely, there exists a constant $I_{F}$ uch that
$$
P(\overline{S}_{n} \in F) \approx e^{-nI_{F}}
$$
![[Pasted image 20220905200936.png]]

the above gives a graphical intuition - the shape of the "density" around $\overline{x}$ becomes more concentrated while the tail grows smaller and smaller.


# Statement

Let $X_{n}$ be i.i.d with $\overline{S}_{n} = \frac{X_{1} + \dots +X_{n}}{n}$. Then

For any closed set $F \subseteq \mathbb{R}$,
$$
\limsup\frac{1}{n} \log(P(\overline{S}_{n} \in F))  \leq - \inf_{x \in F}\Lambda^*(x)
$$
and for any open set $G \subseteq \mathbb{R}$, 
$$
\liminf \frac{1}{n}\log P(\overline{S}_{n} \in G) \geq -\inf_{x \in G} \Lambda^*(x)
$$
where $\Lambda^*$ is the [[Legendre Transform]] of the [[Cumulant Generating Function]].

# Proof

### Upper Bound

**Lemma** - For $x < \overline{x}$, $\mathbb{P}(\overline{S}_{n} \leq x) \leq e^{-n \Lambda^*(x)}$.

Let $F$ be a closed subset of $\mathbb{R}$. Assume $\overline{x} \notin F$. (recall from [[Legendre Transform#Properties]] that $\Lambda^*(\overline{x}) = 0$). Let
$$
\begin{align}
x^- &:= \sup\left\{ r < \overline{x}: r \in F \right\} \\
x^+ &:= \inf\{r > \overline{x} : r \in F\} 
\end{align}
$$
due to the fact that $F$ is closed, it contains its supremum and infimum. Then since $F \subseteq (-\infty, x^-] \cup [x^+, \infty)$, we have
$$
\begin{align}
P(\overline{S}_{n} \in F) &\leq P(\overline{S}_{n} \leq x^-) + P(\overline{S}_{n} \geq x^+) \\
&\leq e^{-n \Lambda^*(x^-)} + e^{-n\Lambda^*(x^+)} \\
&\leq 2e^{-n I_{F}} \\
\log \mathbb{P}(\overline{S}_{n} \in F)&\leq \frac{1}{n}\log_{2} - I_{F}
\end{align}
$$
(Lines 2 to 3 follow because $x^-$ and $x^+$ are in $F$ which means they must be greater than $\inf_{x \in F} \Lambda^*(x) = I_{F}$).

So we have 
$$
\limsup \frac{1}{n}\log \mathbb{P}(\overline{S}_{n}\in F) \leq -I_{F}
$$
### Lower Bound

**Lemma** : suppose $\left\{ X_{n} \right\}$ are i.i.d. For any $\delta >0$, 
$$
\liminf \frac{1}{n}\log \mathbb{P} (\overline{S}_{n} \in (-\delta, \delta)) \geq \inf_{\lambda \in \mathbb{R}} \Lambda(\lambda)
$$
Assuming this is true, we let $X_{n}$ be i.i.d and define $Y_{n} = X_{n}- x$, then
$$
\mathbb{P}(\overline{S}_{n}^X \in (x - \delta, x+ \delta)) = \mathbb{P}(\overline{S}_{n}^Y \in (-\delta, \delta))
$$
implies
$$
\liminf \frac{1}{n}\log \mathbb{P}(S_{n}^X \in (x-\delta, x+\delta)) \geq - \Lambda^*_{Y}(0)
$$
Since
$$
\Lambda_{Y}^*(y) = \sup_{\lambda \in \mathbb{R}}(\lambda y - \Lambda_{Y}(y)) = \sup_{\lambda \in \mathbb{R}}(\lambda y + \lambda x - \Lambda_{x}(\lambda)) = \Lambda_{X}^*(x+y)
$$
So $\Lambda_{Y}^*(0) = \Lambda_{X}^*(x)$. Hence
$$
\liminf \frac{1}{n} \log \mathbb{P}(S_{n} \in (x- \delta, x+ \delta)) \geq - \Lambda_{X}^*(x)
$$
for any $x \in \mathbb{R}$ and $\delta > 0$.

Now let $G \subseteq \mathbb{R}$ be an open set. Since we know that [[A set is Open iff Contains All Its Interior Points]], and $\mathbb{R}$ has the [[Metric Space Topology is formed By Open Balls]]
$$
\mathbb{P}(\overline{S}_{n} \in G) \geq \mathbb{P}(\overline{S}_{n} \in (x- \delta, x + \delta)) \geq -\Lambda_{X}^*(x) \geq \inf_{x \in G} - \Lambda_{X}^*(x)
$$

