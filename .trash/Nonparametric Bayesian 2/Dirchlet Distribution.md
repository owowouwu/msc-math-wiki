## Background

Can be thought of as a distribution on the support of all $K$-dimensional categorical distributions - 

$$\Delta_K = \{(\pi_1, \dots, \pi_k)\}$$

where $\pi_k \geq 0$ and $\sum_k \pi_k = 1$. i.e distribution over the $K$-dimensional simplex.

## Definition

The Dirchlet distribution is parameterised by $K$ parameters $alpha$ - 

$$(\pi_1, \cdots, \pi_k) \sim \text{Dirchlet}(\alpha_1,\dots, \alpha_k)$$

with density

$$p(\pi_1,\dots,\pi_k) = \frac{\Gamma(\sum_k\alpha_k)}{\prod_k \Gamma(\alpha_k)}\prod_{k=1}^K \pi_k ^{\alpha_k - 1}$$


### Intuition behind $\alpha$ ?

For the special case where $\alpha_1 = \alpha_2 = \cdots = \alpha_K$ we have a *symmetric* distribution, and here $\alpha$ can be thought of as the parameter that controls how dispersed our distribution is - the *concentration* parameter. For higher $\alpha$, the distribution is more concentrated on a smaller subset of the support.

![[Pasted image 20211203120223.png]]

## Properties and Remarks

Has the property of being a conjugate prior for categorical variables and multinomial variables. MV generalisation of the beta distribution, which itself is the conjugate prior for the binomial distribution. 
-> the normalising constant is the *multivariate beta function.*

### Conjugate Prior

Suppose we have $\mathbf{x} \sim \text{Categorical}(\mathbf{p})$, where $\mathbf{p} \in [0,1]^K$. Then taking a Dirchlet prior on $\mathbf{p}$, we have

$$\mathbf{p} | {\mathbf{x}} \sim \text{Dir}(\boldsymbol{\alpha} + (c_1, \dots, c_k))$$

where $c_i$ is the number of observations in category $i$. For the multinomial case, we sum  over draws $\mathbf{x}_i$ from the multinomial.