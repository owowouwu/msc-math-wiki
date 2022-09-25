# Definitions

## Normal Definition

If $T$ is a linear transformation on a vector space $V$ over a field $F$, $T$ has an eigenvector $v \in V$ with eigenvalue $\lambda \in F$ if
$$
Tv = \lambda v
$$

## As an element of an eigenspace

An eigenvector of eigenvalue $\lambda$ is an element of the [[Eigenspace]] $H_{\lambda}$ such that $v \in H_{\lambda}$

# Computing Eigenvectors and Existence

## [[MetHIlbert10]] - Eigenvectors for [[Bounded Compact Operator]]

notions of injectiveness and bijectiveness and existence of eigenvectors

[[Fredholm's Theorem]]

## [[MetHilbert11]] - Eigenvectors for [[Self-Adjoint]] Operators

constructing eigenvectors by using sequences of unit vectors


# Examples for Abstract Vector Spaces

## Example 1

Let $H = \mathbb{C}[x]$ (polynomials) and $T = \frac{d}{dx}$. 

$H$ has basis $\left\{ 1, x,x^2, \dots \right\}$ and the matrix of $T$ on the basis $\left\{ 1, x, x^2, \dots \right\}$ is
$$
A = \left( \begin{matrix}
0 & 1 & \\
& 0 & 2  \\
& & 0 & 3 \\
& & & & \dots
\end{matrix} \right) 
$$
Let $\lambda \in \mathbb{C}$. Notice how eigenvectors only exist for $\lambda = 0$ as no polynomial has a derivative as a constant of itself.

## Example 2

Let $H = \left\{ f : \mathbb{C} \to \mathbb{C} : \text{f is differentiable} \right\}$.

Let $\lambda \in \mathbb{C}$. Then $v = e^{\lambda x}$ is an eigenvector of eigenvalue $\lambda$.

