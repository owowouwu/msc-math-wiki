# Definition (Real Numbers)

A subset $A \subseteq \mathbb{R}$ is **compact** if it can be approximated by a sequence of subsets of $\mathbb{R}$ (has a cover).

# Notions of Compact

In compact spaces, limits **exist**.

If $(X, d_{x})$ is a metric space then

![[Pasted image 20220905205638.png]]

usually when we say "compact" we mean "cover compact".

See [[Compactness Equivalencies]]


## Defintions

[[Cover Compact]] (cover compact)
[[Sequentially Compact]]
[[Complete]] (Cauchy compact)
[[Ball Compact]]
[[Bounded (Topology)]]
[[Closed]]

## Implications

### Sequentially Compact $\implies$ Cauchy Compact

Provided we are in a [[Metric Space]], sequential compactness implies Cauchy compact since a sequence having a [[Cluster Point]] implies a Cauchy sequence is convergent.

### Cover Compact $\implies$ Ball Compact

Look at the set $\mathcal{S} = \left\{ B_{\varepsilon}(x) : x \in X \right\}$ this is a cover of $A$ (it literally contains all the points $x \in X$). Since $A$ is cover compact, it has a finite subcover from the cover which consists of these $\varepsilon$-balls. Hence it is ball compact. 

### Ball Compact $\implies$ Bounded

Let $(X, d)$ be a metric space and $A \subseteq X$ be ball compact.

Since $A$ is ball compact we can have $\delta >0$ and let $x_{1}, \dots, x_{n} \in A$ be such that $A \subseteq \bigcup_{k=1}^n B_{\delta}(x_{k})$.

Now let $a \in A$ be arbitrary, and define
$$
\varepsilon = 2\delta + \max\left\{ d(a,x_{1}), d(a, x_{2}),\dots d(a, x_{n}) \right\} 
$$
Then for any $k \in 1\dots n$ we have $B_{\delta}(x_{k}) \subseteq B_{\varepsilon}(a)$. So
$$
A \subseteq \bigcup_{k=1}^n B_{\delta}(x_{k}) \subseteq B_{\varepsilon}(a)
$$
Hence $A$ is bounded.

### Cauchy Compact $\implies$ Closed

See the definition of [[Complete]].