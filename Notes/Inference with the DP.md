## Posterior Distribution

Let $G \sim DP(H, \alpha)$, and $X_1,\dots X_n | G \stackrel{i.i.d}{\sim} G$ .

We want to know the posterior distribution of $G$ given the observed values $X_1, \dots, X_n$.  Then the posterior distribution is also a DP, with 

- $\alpha' = \alpha + n$
- $H' \sim \frac{\alpha H + \sum_{i=1}^n \delta_{X_i}}{\alpha + n}$

Can be rewritten as follows

$$
G | X_1, \dots X_n \sim DP\left(\alpha + n, \frac{\alpha}{\alpha + n}H + \frac{n}{\alpha + n}\frac{\sum_{i=1}^n \delta_{X_i}}{n}\right)
$$

We can see the influence of $\alpha$ and $n$ here - the higher the concentration parameter relative to the number of observations, the more the posterior distribution is influenced by the base/prior distribution $H$. On the other hand, as $n \rightarrow \infty$, the distribution simply approaches an empirical distribution $\frac{\sum_{i=1}^n \delta_{X_i}}{n}$. Which in turn gives an approximation of the true underlying distribution.

This is part of how the modle grows with the number of observations.

## Predictive Distribution

$$
X_{n+1} | X_1,\dots, X_n \sim \frac{1}{\alpha + n}\left(\alpha H + \sum_{i=1}^n \delta_{X_i} \right)
$$

This is actually the *base distribution* of the posterior distribution.

The idea is that we draw the next value $X_{n+1}$ either from the base distribution $H$ w.p $\frac{\alpha}{\alpha +n}$ or the empirical distribution w.p $\frac{n}{\alpha + n}$.

### Clustering Property

To make the above idea more clear,

let $$X_1^*, X_2^*, \dots,X_m^* $$

be the unique values among all $n$ draws and $n_k$ be the number of observations of $X_k^*$. We can rewrite the predictive distribution as

$$
\frac{1}{\alpha + n}\left( 
\alpha H + \sum_{k=1}^m n_k \delta_{X_k^*}
\right)
$$

Note that $X_k^*$ will be repeated with probability proportional to the number of times, $n_k$, that it has already been observed.

This gives a clustering property similar to what is seen in the [[Chinese Restaurant Process | CRP]], i.e the more observations we draw, the less likely we will see "newer" observations i.e more unique observations, and instead we will likely see previous values drawn.

This is useful in applications where we wish to perform clustering but don't want to or cannot specify a number of clusters before hand - this model automatically performs a kind of model selection.

## Mixture Models

Suppose we have a mixture model with an infinite number of components. We have observations $X$ under some distribution $F$ parameterised by $\theta$.

$$
\begin{aligned}
	x_i | \theta_i &\sim F(\theta_i)\\
	\theta_i | G &\sim G \\
	G|\alpha, H &\sim DP(\alpha, H)
\end{aligned}
$$

The DP mixture model is an *infinite* mixture model in the sense that there are a countably infinite number of clusters but they decrease exponentially quickly due to the 'rich get richer' clustering property of the DP. In this way we automatically infer the number of clusters.

The [[Pitman Yor Process]] can be used in a similar way, but has *polynomial* tail behaviour that can be tuned with another parameter.


