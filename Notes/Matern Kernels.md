## Definition

$$
C_\nu (d) = \sigma^2 \frac{2^{1-\nu}}{\Gamma(\nu)}\left(\sqrt{2\nu}\frac{d}{\rho}\right)^\nu K_\nu\left(\sqrt{2\nu}\frac{d}{\rho} \right)
$$

where $K_\nu$ is the modified Bessel function of the second kind, and $\rho$ and $\nu$ are positive parameters that control the covariance.

## Use in GPR

The squared exponential function is used when we want to model smooth (i.e infinitely differentiable functions). 

If we don't have such well behaved functions, we can use the Matern kernel instead, which is $\lceil \nu \rceil - 1$ times differentiable.