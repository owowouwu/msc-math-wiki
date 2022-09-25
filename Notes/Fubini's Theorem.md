## Fubini's Theorem for Bounded Measurable Functions

Let
$$
(\Omega, \mathcal{F}) = (\Omega_{1}\times \Omega_{2}, \mathcal{F}_{1} \otimes \mathcal{F}_{2})
$$
be a [[Product Measurable Spaces]]

and $f \in b\mathcal{F}$

Define
$$
I_{1}^f : \Omega_{1} \to \mathbb{R}, \, \int _{\Omega_{2}} f(\omega_{1}, \omega_{2}) \, d\mu(\omega_{2}) 
$$
$$
I_{2}^f : \Omega_{2} \to \mathbb{R}, \, \int _{\Omega_{1}} f(\omega_{1}, \omega_{2}) \, d\mu(\omega_{1}) 
$$
then

$I_{1}^f \in b\mathcal{F}_{1}$, $I_{2}^f \in b\mathcal{F}_{2}$
$$
\int _{\Omega_{1}} I_{1}^f(\omega _{1})\, \mu_{1}(d\omega_{1}) = \int _{\Omega_{2}} I_{2}^f (\omega_{2})\, d\mu(\omega_{2})  
$$

### Proof

Prove for simple functions and use [[Dynkin's pi-lambda Theorem]].

## General Fubinis Theorem

^8c32b8

Let $f \geq 0$ and $\mathcal{F}_{1} \otimes \mathcal{F}_{2}$-measurable, then the order of integration doesn't matter -
$$
\int _{\Omega_{1}} \int _{\Omega_{2}}f \, d\mu_{2}  \, d\mu_{1} = \int _{\Omega_{2}} \int _{\Omega_{1}}f \, d\mu_{1}  \, d\mu_{2} = \int _{\Omega}f \, d\mu    
$$
Now let $f$ be a general measurable function s.t $f \in L^1(\mu)$. Then the above holds.

### Proof

Take $f_{n} \geq 0$ simple on the product space such that $f_{n} \to f$ Since $f_{n}$ is simple, it is bounded so Fubini's theorem holds for $f_{n}$.

By [[Monotone Convergence Theorem]], Fubini's holds for $f$.

For the general case, take $f = f^+ - f^-$. By linearity this is also true ($f \in L^1(\mu)$ means the two terms are bounded).

## Applications

Recall that if $X \geq 0$, $E(X) = \int _{0}^\infty P(X \geq x) \, dx$

### Proof Using Fubini's Theorem

Naturally we can consider the following spaces $(\Omega, \mathcal{F}, P)$ and $(\mathbb{R}_{\geq 0}), \mathcal{B}(\mathbb{R}_{\geq 0}, dx)$ where $dx$ is the Lebesgue measure.

Take the [[Product Measurable Spaces]] of these two. Let
$$
F = \{(\omega, x) : 0 \leq x \leq X(\omega)\}
$$
we know that the Lebesgue measure of $F$ would just be $X(\omega)$ while the probability of $F$ is $P(X \geq x)$.

So
$$
\begin{align}
\int_{\Omega} 1_{F} d\mu &= \int_{\Omega} \int_{\mathbb{R}} 1_{F}\,dx\, dP \\ \\
&= \int_{\Omega} \int_{\mathbb{R}} 1_{x \in [0, X(\omega)]}(x, \omega) \, dx \, dP\\
&= \int_{\Omega} X(\omega) dP = E[X]
\end{align}
$$
but taking the other direction
$$
\begin{align}
\int_{\Omega} 1_{F} d\mu &= \int_{\mathbb{R}} \int_{\Omega} 1_{F} \, dP \,dx \\
&= \int_{\mathbb{R}} P(X \geq x) 1(x \geq 0 ) dx \\
&= \int_{0}^\infty P(X \geq x) \, dx
\end{align}
$$

hence $E[X] = \int_{0}^\infty P(X \geq x) dx$