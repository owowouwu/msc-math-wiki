# Statement

Let $(X, d_{x})$ be a [[Metric Space]] with the usual [[Metric Space Topology]].

The following are equvalent -

1. $A$ is [[Cover Compact]]
2. $A$ is [[Sequentially Compact]]
3. $A$ is [[Ball Compact]] AND [[Cauchy Compact]]

This is essentially a stronger version of [[Heine-Borel]].

# Proof

Now every finite set is compact so we only need to show results for infinite sets.

### Cover Compact  $\implies$ Sequentially Compact.

Here we show the contrapositive. Assume $A \subseteq X$ is not sequentially compact. We want to show that if $A$ has a cover then there does not exist a finite subcover of $A$.

Since $A$ is not sequentially compact any sequence in $A$ does not have a cluster point, in other words, if $a_{1}, a_{2}, \dots \in A$ then there exists an open set $U$ of $A$ such that
$$
U \cap (a_{1}, a_{2}, \dots) \text{ is finite}
$$
For $a \in A$ let $V_{a}$ be an open neighbourhood of $a$. Then $V_{a} \cap (a_{1}, a_{2}, \dots )$ is finite. Then let
$$
\mathcal{S} = \left\{ V_{a}:a \in A \right\} 
$$
then $\mathcal{S}$ is an open cover of $A$, as $\{a\} \subseteq V_{a}$ implies $A = \bigcup_{a \in A} \left\{ a \right\} \subseteq \bigcup_{U \in \mathcal{S}} U$. Now we need to show that $\mathcal{S}$ has no finite subcover. 

Let $V_{x_{1}}, V_{x_{2}}, \dots, V_{x_{n}}$ be such a finite collection of sets in $\mathcal{S}$. Since for any $x_{k}$, $V_{x_{k}} \cap (a_{1}, a_{2}, \dots )$ is finite, there exists a $N_{k}$ such that if $n> N_{k}$ then $a_{n}, a_{n+1}, \dots \notin V_{x_{k}}$. Take $N = \max_{k} N_{k}$ then we have for $n>N$
$$
a_{n}, a_{n+1}, \dots \notin \bigcup_{n=1}^k V_{x_{n}}
$$
So $\mathcal{S}$ has no finite subcover.

### Sequentially Compact $\implies$ Ball Compact

We will again show the contrapositive; if $A$ is not ball compact then $A$ is not sequentially compact. 

If $A$ is not ball compact there exists an $\varepsilon > 0$ such that $S_{\varepsilon} = \left\{ B_{\varepsilon}(a) : a \in A \right\}$ has no finite subcover. We want to show this implies that there exists $(a_{1}, a_{2},\dots)$ in $A$  with cluster points.

Let $a_{1} \in A$, $a_{2} \in A \backslash B_{\varepsilon}(a_{1})$, $a_{3} \in A \backslash (B_{\varepsilon}(a_{2}) \cup B_{\varepsilon}(a_{1}))$ and so on. We can guarantee the existence of $a_{2}, a_{3},\dots$ otherwise the finite unions would cover $A$. 

Then for any $a \in A$, $B_{\frac{\varepsilon}{10}}(a)$ contains at most one point of $a_{1}, a_{2}, \dots$. So $a_{1},a_{2},a_{3}\dots$ has no cluster point in $A$. So $A$ is not sequentially compact.

### Ball Compact + Cauchy Compact $\implies$ Cover Compact

Assume $A$ is ball compact. We will show that if $A$ is not cover compact then it is not Cauchy compact.

So there exists an open cover $\mathcal{S}$ with no finite subcover of $A$. So the union of every finite subset of $\mathcal{S}$ does not contain $A$.

Since $A$ is ball compact, for each $d \in \mathbb{Z}_{\geq 0}$, there exists $n_{d} \in \mathbb{Z}_{\geq 0}$ such that $a_{1}^{(d)}, a_{2}^{(d)},\dots a_{n_{d}}^{(d)}$ has
$$
A\subseteq B_{10^{-d}}(a_{1}^{(d)}) \cup \dots \cup B_{10^{-d}}(a_{n_{d}}^{(d)}) 
$$
and for each $d$ we can let $j_{d} \in \left\{ 1, 2, \dots, n_{d} \right\}$ be such that 
$$
A_{d} := A \cap B_{10^{-d}}(a_{j_{d}}^{(d)}) \cap B_{10^{-(d-1)}} (a_{j_{d-1}}^{(d-1)}) \cap \dots
$$
is not finitely covered by $\mathcal{S}$.

**Claim** - $(a_{j_{1}}, a_{j_{2}}, \dots)$ is a Cauchy sequence in $A$ with no cluster point.

**Cauchy** -

Let $r,s \in \mathbb{N}$ be large. 

Since $a_{j_{r}} \in B_{10^{-r}}(a_{j_{r}}^{(r)}) \cap B_{10^{-s}}(a_{j_{s}}^{(s)})$ and $a_{j_{s}} \in B_{10^{-r}}(a_{j_{r}}^{(r)}) \cap B_{10^{-s}}(a_{j_{s}}^{(s)})$ then we have 
$$
|a_{j_{r}} - a_{j_{s}}| < \min\left\{ 10^{-r},10^{-s} \right\} 
$$
Hence $a_{j_{n}}$ is Cauchy, since we can make $r,s$ are arbitrarily large.