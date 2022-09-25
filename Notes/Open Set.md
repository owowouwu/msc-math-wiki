# Definition

There are many equivalent characterisations of "openess" in math.

### As an element of the [[Topology]]

Given a [[Topological Space]] $(X, \mathcal{T})$, we can say that an open set (in $X$) is just any element of $\mathcal{T}$. This definition is the most general and abstract.

### As the set of [[Interior Point]]

We can equivalently characterise open sets as [[A set is Open iff Contains All Its Interior Points]], or in other words **contains** a [[Neighbourhood]] of all its points.

### With respect to limits

When talking about **limits**, we can say a set $A$ is open if there exists a sequence which does not converge in $A$. 

### [[Metric Space]] and [[Epsilon Ball]]

A set $A$ in a metric space $(X, d)$ is **open** under the usual [[Metric Space Topology]] if and only if for every $x \in A$, there exists $\varepsilon>0$ such that $B_{\varepsilon}(x) \subseteq A$. The sketch proof is that the [[Metric Space Topology is formed By Open Balls]], which are [[Neighbourhood]] of their points, and if $A$ contains a neighbourhood of all its points, then it is open (see above definition).

**Proof** $\implies$ suppose for every $x \in A$ there exists $\varepsilon>0$ such that $B_{\varepsilon}(x) \subseteq A$. Then since $B_{\varepsilon}(x) \in \mathcal{N}(x)$, we have that every point in $x$ is covered by a neighbourhood, and this neighbourhood is contained in $A$. So $A$ contains a neighbourhood of all its points, so it is open.

$\impliedby$ suppose $A$ is open. Let $x \in A$. By the [[Metric Space Topology]], $A$ is an arbitrary union of $\varepsilon$-balls. At least one of these balls must contain $x$, and each ball must be contained in $A$. Let $B_{\varepsilon}(y)$ be such a ball. If we choose $\delta = \varepsilon - d(x,y)$ we have that for any $x' \in B_{\delta}(x)$,
$$
d(x',y) \leq d(x', x) + d(x, y) < \varepsilon - d(x,y) + d(x,y) = \varepsilon
$$
Hence
$$
B_{\delta}(x) \subseteq B_{\varepsilon}(y) \subseteq A
$$
and we are done.

