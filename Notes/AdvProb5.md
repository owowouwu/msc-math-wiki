# Constructing Independent Random Variables

Given a [[Distribution Function]] $F$, we can construct a probabiltiy space given by
$$
(\mathbb{R}, \mathcal{B}\left( \mathbb{R} \right), \mu_{F} )
$$
And construct a [[Random Variable]] to simply be the identity -
$$
X(\omega ) = \omega 
$$
(since we are mapping ($\mathbb{R}, \mathcal{B}(\mathbb{R}))$ to the same space) ,

Given $F,G$ that are distribution functions, how do we construct $X \sim F$, $Y\sim G$ such that $X \perp Y$? How do we produce a product of the above space?

## Constructing the Product Space

Given two [[Measurable Space]] $(\Omega_{1}, \mathcal{F}_{1})$ and $(\Omega_{2}, \mathcal{F}_{2})$ it may be natural to take the Cartesian products $\Omega_{1} \times \Omega_{2}$ and $\mathcal{F}_{1} \times \mathcal{F}_{2}$ but the issue is that the latter is NOT a [[Sigma Algebra]] but it is an [[Algebra of Sets]]. 

Instead the natural and canonical thing to do is to take the $\sigma$-algebra *generated* by $\mathcal{F}_{1} \times \mathcal{F}_{2}$. This is the [[Product Sigma Algebra]].

i.e $\mathcal{F} = \sigma(\mathcal{F}_{1} \times \mathcal{F}_{2})$

then
$$
(\Omega, \mathcal{F}) = (\Omega_{1}\times \Omega_{2}, \mathcal{F}_{1} \otimes \mathcal{F}_{2})
$$
is a [[Product Measurable Spaces]]

## Constructing the Product Measure

Using [[Fubini's Theorem]], we construct [[Product Measures]] by defining the [[Measure]] on a set $F$ to be the partial integral of the indicator function of $F$. This will give a measure $\mu$ with the **unique** property that
$$
\mu(A_{1} \times A_{2}) = \mu(A_{1}) \mu (A_{2})
$$
which is denoted as $\mu = \mu_{1} \otimes \mu_{2}$.

