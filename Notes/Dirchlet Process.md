## Background

The Dirchlet process is an infinite dimensional generalisation of the [[Dirchlet Distribution]].

Similar to the Dirchlet distribution, each realisation of a Dirchlet process is itself a probability measure.

## Definition

Two parameters -

- *Base distribution* $H$ over some support $\Theta$, which is like the mean of the DP.
- *Concentration parameter* $\alpha$, which is like the inverse-variance of the DP i.e the larger $\alpha$ is, the more the DP will concentrate its mass around the mean.

$$G \sim DP(\alpha, H)$$

if for any finite partition $A_1, \dots, A_n$ of $\Theta$, 

$$\left(G(A_1), \dots, G(A_n) \right) \sim \text{Dirchlet}(\alpha H(A_1),\dots,\alpha H(A_n))$$

## Properties

For any measurable set $A \subseteq \Theta$, 

- $\mathbb{E}G(A) = H(A)$
- $\text{Var}(G(A)) = \frac{H(A)(1-H(A))}{\alpha+1}$

### Role of $\alpha$ and $H$

- $\alpha$ can be thought of as the strength of using $H$ as a nonparametric prior over distributions in a Bayesian nonparametric model

As $\alpha \rightarrow \infty$, $G(A) \rightarrow H(A)$, i.e pointwise convergence exists. But this doesn't necessarily mean $G\rightarrow H$.

## Alternative Views and Constructions

 - [[Stick-breaking Construction]]
 - [[Chinese Restaurant Process]]

## Applications

Used in *Bayesian nonparametric statistics*, which is a model that grows as more data is observed. 

In particular, is good in clustering problems as we don't have to specify a number of clusters before hand - as we add more data the model will add more clusters.

- [[Inference with the DP]]

