
## Problem Statement

For example a hidden Markov model where ${X_n}_{n\geq 1}$ is a Markov process with observations $Y_i$ dependent on $X_i$ at each state $i$.

We wish to determine recursively the posteriors, 

$$
\{p(x_{1:n}|y_{1:n});n\geq 1\}
$$

as well as the marginal likelihoods $p(y_{1:n})$.

More precisely we do this iteratively, first determining $p(x_1|y_1)$, $p(y_1)$, then $p(x_{1:2} | y_{1:2})$ and $p(y_{1:2})$ and so on

## Sequential MC Methods

Sequential Monte Carlo methods (SMC), also known as particle filtering methods are used in problems in which we want to interatively compute the posterior distributions given above.

The general approach is that posterior distributions are then approximated by a set of weighted samples $X_{0:n}$ called particles, giving an empirical distribution

$$
P(dx_{1:n} | y_{1:n}) = \sum_{k = 1}^N W_n^k \delta_{X_{1:n}^k}(dx_{1:n})
$$

where $W_n^k$ is called an 'importance weight', with $\sum_k W_n^k = 1$ and $\delta_{X_{1:n}^k}(dx_{1:n})$ represents the Dirac delta mass at $x_{1:n}$.

The weights are generally associated with the probabilities of drawing $x$ from a density and this can be done differently depending on the method.

## Bootstrapping

It will often  be the case that certain particles are assigned lower weights than others, to deal with particles with low weights we resample the particles according to a multinomial distribution with the probabilities being the weights.

We then reconstruct the estimator for the posterior 

$$
\frac{1}{N}\sum_{k = 1}^N N_k \delta_{X_{1:n}^k}(dx_{1:n})
$$

where $N_k$ is the number of times particle $k$ was sampled in this step. This potentially eliminates particles with very low weights, and also ensures the asymptotic unbiasedness of the estimator.

