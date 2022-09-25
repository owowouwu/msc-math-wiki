Alternative view of/way of constructing the [[Dirchlet Process]].

Let

$$
\beta_k \sim Beta(1,\alpha)
$$

$$
\X_k ^* ~ H
$$

$$
\pi_k = \beta_k \prod_{l=1}^{k-1}(1-\beta_l)
$$

$$
G = \sum_{k=1}^\infty \pi_k \delta_{\theta_k ^*}
$$

Then $G \sim DP(\alpha, H)$.  

![[Pasted image 20220107175837.png]]

This is called the stick breaking process as we are effectively 'breaking' a stick of length 1 at point $\beta_1$ and assigning lengths to it according to $\pi_1$. We iteratively repeat this process on the remaining length $1-\beta_1$. Breaking at the point $\beta_2$ scaled to the new stick's length $1-\beta_1$ giving the weight $\pi_2 = \beta_2 (1 - \beta_1)$ and so on.

These weights are then assigned to point masses which are drawn from the base distribution $H$.

## How does this give what we want?

- $G$ is a weighted sum of point masses which is what the DP is effectively is - a distribution over discrete probability measures.
- Maintains 'rich get richer' property as the stick gets shorter with each break (weights become smaller and smaller)
- This simple construction can be used to very simply draw samples from the DP.

