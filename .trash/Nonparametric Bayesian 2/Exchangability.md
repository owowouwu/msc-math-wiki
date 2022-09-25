## Definition

A sequence of random variables $\{X_n\}$ is exchangeable if for any finite permutation of the indices $\sigma$, 

$$
X_1, X_2, X_3, \cdots, X_n \stackrel{d}{=} X_{\sigma(1)}, X_{\sigma(2)}, X_{\sigma(3)}, \cdots, X_{\sigma (n)}
$$

i.e the order of realisations of the RVs does not matter - the joint distribution is still the same.

## Relation to i.i.d RV

It is easy to see that if a sequence of RVs is i.i.d, then they must necessarily be exchangeable -

$$
	f_{X_1, X_2, \cdots X_n}(x_1, x_2, \cdots, x_n) =
	\prod_{i=1}^n f_{X_i}(x_i)
$$

the product is the same under any permutation of the indices.

But the converse is not true.
### Example

 e.g suppose we have a jar with 6 red balls and 4 green balls, and $(X_1, X_2)$ be a realisation of two draws from this jar. Clearly $X_1$ and $X_2$ are not independent, but

$P(X_1=G, X_2=R) = \frac{4}{10}\cdot \frac{6}{9} = \frac{6}{10}\cdot\frac{4}{9} = P(X_1=R, X_2=G)$

so the joint distributions are the same even with reordering, which means $X_1$ and $X_2$ are *exchangeable but not independent*.

### De Finetti's Theorem

In a sense, the converse can be made true - 


