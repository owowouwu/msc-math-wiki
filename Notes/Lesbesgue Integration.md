# Motivations

We want to define more general notions of integration 

In probability, expectations are sums and integrals and we can consider integrating over [[Probability Space]].

## Construction

Let $(\Omega, \mathcal{F}, \mu)$ be a [[Measurable Space]]

To begin with we consider integration of indicator functions. Given an indicator $1_{A}(\omega)$, the Lebesgue integral to be
$$
\mu(A) = \int_{\Omega} 1_{A}(w) d\mu
$$
Linearity allows us to define this for simple functions, i.e linear combinations of indicator functions,
$$
\int_{\Omega} \sum_{n=1}^N a_{n}1_{A_{n}} d\mu = \sum_{n=1}^N \int a_{n} 1_{A_{n}}(\omega)d\mu = \sum_{n=1}^N \mu(A_{n})
$$

### Positive Case

For positive $\mu$-measurable functions, we approximate any function $f$ as a sequence of simple functions $f_{n}$ such that $f_{n} \to f$. Given that we have $f$ is bounded, the [[Dominated Convergence Theorem]] applies.

### General Case

Given that we have a construction that works for functions $f \geq 0$ that are $\mu$-measurable by breaking the function up into positive and negative parts
$$
f = f^+ - f^-
$$
where $f^+(x) = \max \{0, f(x)\}$ and $f^-(x) = \max \{0, -f(x) \}$.
