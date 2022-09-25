
## Formal Mathematical Definition

A kernel is a generalisation of a positive definite matrix (i.e one where $y^T X y >0$ for all $y$).

Let $\mathcal{X}$ be a nonempty set. A symmetric function $K: \mathcal{X} \times \mathcal{X} \rightarrow \mathbb{R}$ is a kernel on $\mathcal{X}$ if

$$
\sum_{i=1}^n \sum_{j=1}^n c_i c_j K(x_i, x_j) \geq 0
$$

for arbitrary $c_n \in \mathbb{R}$

notice how if we have a matrix $M$ and let $K(x_i,x_j) = M_{ij}$, we have the definition of a PSD matrix. It is effectively a generalised dot product.

## Motivation

Many simple ML algorithms such as linear regression and [[PCA]] imply linearity in the data. However if the assumption is not met, the algorithms can perform poorly. 

One way to fix this in the case of linear regression is to use a different [[Basis]] for our model, for example for data that is quadratic we would use the basis $<1, x, x^2>$ and have the model

$$ y = \beta_0 + \beta_1 x + \beta_2 x^2$$

However with a higher dimensional basis we end up in a situation where the feature space grows larger and thus computations become expensive.

Let $\varphi : \mathbb{R}^d \rightarrow \mathbb{R}^k$ be such a feature expansion, $k>d$. 

Using the [[Dual Form]] of linear regression, the problem now becomes to calculate dot products $<\varphi(x_i), \varphi(x_j)>$. 

*However if we can find a function $k$ such that*

$$
k(x,x') = $<\varphi(x), \varphi(x')>$
$$

then we effectively do not ever need to do the basis function expansion and visit a higher dimensional space; we can do our computations on a lower dimensional space but still get the same result.




