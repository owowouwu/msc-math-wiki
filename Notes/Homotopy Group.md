# Definition

Let $(X, x_{0})$ be a [[Based Space]]. The **nth homotopy [[Group]] of $X$** is
$$
\pi_{n}(X, x_{0}) = [(S^n, p), (X, x_{0})] = \frac{\mathrm{Map}((S^n, p), (X, x_{0}))}{\cong}
$$
with product
$$
(f_{1} \cdot f_{2})(s_{1}, s_{2}, \dots, s_{n}) = \begin{cases}
f_{1}(2s_{1}, s_{2}, \dots, s_{n}) & 0 \leq s_{1} \leq \frac{1}{2} \\
f_{2}(2s_{1}-1, s_{2}, \dots, s_{n}) & \frac{1}{2} < s_{1} \leq 1
\end{cases}
$$
and the identity being the constant map
$$
0 : (S^n, p) \to (X, x_{0}), (s_{1}, s_{2}, \dots, s_{n}) \mapsto x_{0}
$$
(i.e shrinks everything in the sphere to the base point)

https://en.wikipedia.org/wiki/Homotopy_group

## Fundamental Group

The **fundamental group** of $X$ is $\pi_{1}(X, x_{0})$.

https://en.wikipedia.org/wiki/Fundamental_group 