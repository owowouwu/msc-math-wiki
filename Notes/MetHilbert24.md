# [[Connected Set]]

## [[Interval]]

Let $(S, \leq)$ be a partially ordered set. Let $E \subseteq S$. Then $E$ is an **interval** if $E$ satisfies - if $x,y \in E$ and $z \in S$ and $x<z<y$ then $z \in E$. (anything between two elements in $E$) is also in $E$.

[[Intervals in the Reals Are Connected]]

**Theorem** 

Let $X = \mathbb{R}$ with the standard topology and let $E \subseteq X$. Then $E$ is connected if and only if $E$ is an interval.

**Proof**

$\implies$ (contrapositive) Assume $E$ is not an interval. Then there exists $x,y \in E$ with $x<z<y$ but $z \notin E$. Let $A = (-\infty, z) \cap E$ and $B = E \cap (z, \infty)$. Since these intervals are open in $\mathbb{R}$ they are open in $E$ ( with the subspace topology). Then $A \cup B = E$ and $A \cap B \neq \phi$ so $E$ is disconnected.

$\implies$ Assume $E$ is an interval. Let $A \subseteq E$ and $B \subseteq E$ be non-empty open sets in $E$ with $A \cup B = E$. 

Let $x_{1} \in A$ and $y_{1} \in B$ and without loss of generality $x_{1} < y_{1}$. Construct sequences $x_{1},x_{2},\dots$ and $y_{1},y_{2},\dots$ by
$$
x_{i+1} = x_{1} \text{ and } y_{i+1} = \frac{1}{2}(x_{i}+y_{i}) \text{ if } \frac{1}{2}(x_{i}+y_{i}) \in B
$$
and
$$
x_{i+1} = \frac{1}{2}(x_{i}+ y_{i}) \text{ and } y_{i+1}= y_{i} \text{ if } \frac{1}{2}(x_{i}+y_{i}) \in A
$$
Then $x_{1},x_{2},\dots$ is an increasing sequence in $A$ and $y_{1}, y_{2},\dots$ is a decreasing sequence in $B$ with
$$
x_{i} \leq x_{i+1} < y_{i+1} \leq y_{i}
$$
So
$$
\left| x_{i+1}-y_{i+1} \right| \leq \frac{1}{2}|x_{i}- y_{i}| 
$$
so
$$
\left| x_{i+1} -y_{i+1} \right| \leq \frac{1}{2^i}|x_{1} - y_{1}| 
$$
Since increasing/decreasing bounded sequences converge in $\mathbb{R}$, $\lim x_{n}$ exists and $\lim y_{n}$ exists. By the above we have
$$
\lim_{n \to \infty}|x_{n} - y_{n}| = \lim_{n \to \infty} \frac{1}{2^n}|x_{1} -y_{1}| = 0
$$
so
$$
z = \lim_{n \to \infty}x_{n} = \lim_{n \to \infty} y_{n}
$$
So $z \in \overline{A} \cap \overline{B}$. Since $x_{1} \leq z \leq y$, $z \in E = A \cup B$

By cases

**Case 1** $z \in A$, then there exists $\varepsilon \in \mathbb{R}_{>0}$ with $B_{\varepsilon}(z) \subseteq A$. But since $z$ is a [[Close Point]] to $B$, 
$$
B_{\varepsilon}(z) \cap B \neq \phi
$$
Since $B_{\varepsilon}(z) \cap B \subseteq A \cap B$, $A \cap B$ is non-empty.

**Case 2** is the same
