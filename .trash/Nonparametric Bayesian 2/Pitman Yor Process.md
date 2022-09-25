# Pitman Yor Process

## Definition / Motivation

Similar to the [[Dirchlet Process]], the Pitman-Yor process is a stochastic process whose sample path is itself a distribution. 

It is an extension of the DP with a *discount parameter* $d$ which controls the tail behaviour of the DP. 

### Parameterisation

**Pitman-Yor** - $\text{PY}(\alpha, d, G_0)$
**Dirchlet Process** $\text{DP}(\alpha, G_0)$

Here $\alpha$ and $d$ are strength parameters, i.e how strong the prior $G_0$ is. If $d = 0$, then $PY \equiv DP$

## Relationship to CRP

Can be associated with the [[Chinese Restaurant Process]] again -

$$
X_{j+1} | X_1, \cdots X_j \sim \frac{1}{\alpha + j} \sum_{k=1}^K (n_k - d)\delta_{y_k} + \frac{\alpha + Kd}{\alpha + j}H
$$

Where $K$ is the total number of clusters, $n_k$ and $y_k$ are the cluster size and the first observation of cluster $k$.

Intuitively - we either draw from the base distribution $H$ with probability $\frac{\alpha + Kd}{\alpha + j}$ or from an existing cluster with probability $\frac{n_k - d}{\alpha + j}$.

## Tail Behaviours

From this we see the following

- the more we draw new clusters i.e draw from the base distribution, the more we will get a new draw from the base
- the more draws are assigned to a cluster, the more likely it is subsequent draws belong to that cluster
- $d$ controls how the probability of adding a new cluster grows as the number of clusters grows.

### Asymptotics

We actually have that for $d>0$, the number of unique clusters scales as $O(\theta K^d)$, whereas for $d=0$ (Dirchlet Process) we have $O(\theta \log K )$

## Stick Breaking

Can also construct the PYP as a [[Stick-breaking Construction | stick breaking representation]] similar to the DP.

Take $\beta_j \sim Beta(1-d, \alpha + jd)$, and weights $\pi_j = \beta_j \prod_{i=1}^{j-1}(1-\beta_i)$ and $\theta_i \sim H$, then

$$ G = \sum_{j=1}^\infty \pi_j \delta_{\theta_j}$$

is PY distributed, with concentration $\alpha$, discount $d$ and base distribution $H$.