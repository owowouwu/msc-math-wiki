# Cramer's Theorem

[[Cramer's Theorem#Proof]]

## Some Observations

Consider $B \in \mathcal{B}(\mathbb{R})$. We know that
$$
B^o \subseteq B \subseteq \overline{B}
$$
where $B^o$ is the [[Interior]] of $B$ and $\overline{B}$ is the [[Closure]] of $B$. We can say that
$$
\limsup \frac{1}{n} \log(\overline{S}_{n} \in B) \leq \liminf \frac{1}{n} \log(\overline{S}_{n} \in \overline{B}) \leq -\inf_{x \in B} \Lambda^*(x) = -I_{\overline{B}}
$$
and similarly for an upper bound. We can then conclude that all [[Cluster Point]] of $\left\{ \frac{1}{n}\log \mathbb{P}(\overline{S}_{n} \in B) \right\}$ must be in $[-I_{B^o}, -I_{\overline{B}}]$.

If $I_{B^o} = I_{\overline{B}}$ then $\frac{1}{n}\log \mathbb{P}(\overline{S}_{n} \in B) \xrightarrow{a.s} -I_{B}$. 

For $B = [y, \infty)$ this occurs.

