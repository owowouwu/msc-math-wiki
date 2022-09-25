## Function Spaces

Consider $\mathbb{R}^2$. We can consider the space of functions 

$$
W = \{f:\{1,2\} \rightarrow \mathbb{R}\}
$$
i.e 

Then 
$$
\mathbb{R}^2 \rightarrow W
$$
$(x_1, x_2) \mapsto \phi({1,2}) \rightarrow \mathbb{R}$

is a bijection, we can identify $W$ with $\mathbb{R}^2$

## What is a Sequence?

[[Sequences]]

Let $V$ be a set. A sequence in $V$ is a function

$\phi : \mathbb{N}\rightarrow V$ 


## How do we deal with Infinite Dimensional Spaces?

[[Sequence Spaces]]
$$\mathbb{R}^\infty = \{f : \mathbb{N} \rightarrow \mathbb{R}\}$$
i.e set of all sequences 

We define addition by 
$$(f+g)(\cdot) = f(\cdot)  + g(\cdot)$$
and scalar multiplication by
$$
(cf)(\cdot) = c f(\cdot)
$$
How do we define norms?

## $\ell ^p$ Norms

[[l-p Norms]]

The $\ell^p$ norm is
$$
||x||_p = \left(\sum_i |x_i|^p\right)^{\frac{1}{p}} 
$$
with

$$
||x||_\infty = \sup\{|x_i| \}
$$
However, $\mathbb{R}^\infty$ is not a normed vector space with any of these norms(many of the sums fail to converge)

## $\ell^p$ Spaces

[[l-p Spaces]]

Define
$$
\ell^p = \{x\in \mathbb{R}^\infty :||x||_p <\infty \}
$$
where $||x||_p$ is the [[l-p Norms |l-p norm]].

**Properties**

- $\ell^p$ with the $\ell_p$ norm is a [[Banach Space]] for $p>1$
- $\ell^1$ with the $\ell_1$ norm is a normed vector space.

If $p<q$, then $\ell^p \subseteq \ell^q$

**Theorem**

$\ell^p$ with $||\cdot ||_p$ is a [[Normed Vector Space]].

Check - 

- Triangle inequality ->hard
- Length scaling -> easy 
- If $x\in \mathbb{R}^\infty$ and $||x||_p =0$, then $x = 0$. -> easy

How to prove triangle inequality property?

[[Minkowski Inequality]]