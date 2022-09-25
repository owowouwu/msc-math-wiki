# Definition

Let $(X, d_{x})$ be a [[Metric Space]]. 

Then the **metric space topology** on $(X, d_{x})$ is
$$
\mathcal{T}_{X} = \left\{ U \subseteq X : \text{if } x \in U \text{ there exists } \varepsilon >0 \text{ such that } B_{\varepsilon}(x) \subseteq U \right\} 
$$
In other words, $\mathcal{T}_{X}$ is the topology formed by the [[Epsilon Ball|open balls]] of $x$.

## Properties

### Uniqueness of Limits ([[Hausdorff Space|Hausdorff]])

**Proof** Let $a_{1}, a_{2}, \dots$ be a sequence in $X$. Suppose there exists $z_{1}, z_{2} \in X$ with $\lim_{n \to \infty}a_{n} = z_{1}$ and $\lim_{n \to \infty} a_{n} = z_{2}$.

Let $\varepsilon = d_{x}(z_{2}, z_{1})$. We need to show that $z_{1}=z_{2}$, i.e $d(z_{1}, z_{2}) = 0$. Let $N_{1} = B_{\leq \frac{\varepsilon}{3}}(z_{1}) = \left\{ x \in X : d(x, z_{1}) \leq \frac{\varepsilon}{3} \right\}$ and similarly for $N_{2}$.

Since $\lim_{n \to \infty} a_{n} = z_{1}$ there exists $l_{1} \in \mathbb{Z}_{> 0}$ such that $N_{1 } \subseteq \left\{ a_{l_{1}}, a_{l_{1}+1},\dots \right\}$ and similarly for $N_{2}$. Let $l = \max(l_{1}, l_{2})$. Then $N_{1} \cap N_{2} \subseteq \left\{ a_{l}, a_{l+1}, \dots \right\}$.

So
$$
\varepsilon = d_{x}(z_{1}, z_{2}) \leq d_{x}(z_{1}, a_{l}) + d_{x}(a_{l}, z_{2}) \leq \frac{\varepsilon}{3} + \frac{\varepsilon}{3}
$$

### Closure and Limit Points

Let $$R = \left\{ z \in X : \text{there exists a sequence in $A$ that converges to $z$}\right\}$$ and $\overline{A}$ be the closure of $A$.

Let $z \in \overline{A}$. To show $z \in R$ we want to show there exists a sequence in $A$ that converges to that closed point in $A$. Using that $z$ is a closed point to $A$, let $a_{1} \in B_{0.1}(\varepsilon) \cap A$, $a_{2} \in B_{0.01}(\varepsilon)\cap A$ and so on. 

Assume $N \in \mathcal{N}(z)$. We want to show that there exists $l \in \mathbb{Z}_{>0}$ such that $N \subseteq \left\{ a_{l}, a_{l+1}, \dots \right\}$. Let $l = \text{ceil}\left( \frac{1}{\varepsilon} \right)$. Then
$$
\left\{ a_{l}, a_{l+1}, \dots \right\} \subseteq B_{10^{-l}}(z) = B_{\varepsilon} \subseteq N 
$$

Now let $z \in R$. We want to show that for any $N \in \mathcal{N}(z)$, $N \cap A \neq \phi$.

Assume $N \in \mathcal{N}(z)$. Since $z \in \mathbb{R}$, then there exists a sequence $(a_{1}, a_{2}, \dots)$ in $A$ with $\lim_{n \to \infty}a_{n} = z$. So there exists $l \in \mathbb{Z}_{>0}$ with $\left\{ a_{l}, a_{l+1}, \dots \right\} \subseteq N$.

So $\left\{ a_{l}, a_{l+1}, \dots \right\} \subseteq N \cap A$.