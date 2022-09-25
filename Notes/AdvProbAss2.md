# Problem 1

## (i)

Consider the moment generating function of $S_{n}$ - 
$$
\begin{aligned}
M_{S_{n}}(t) &= \mathbb{E}e^{S_{n}t} \\
&= \mathbb{E}e^{(X_{1} + X_{2} + \dots + X_{n})t} \\
&= \left(\mathbb{E}e^{X_{1}t}\right)^n & \text{$X_{n}$ are iid} \\
&= \left(\int_{0}^\infty e^{xt} \lambda e^{-\lambda x}  \,dx \right)^n \\
&= \left( \frac{\lambda}{t-\lambda}e^{(t-\lambda)x}|_{0}^\infty \right)^n \\
&=\frac{\lambda^n}{(\lambda -t)^n}, t<\lambda
\end{aligned}
$$
Now let $Y \sim \mathrm{\Gamma}(n, \lambda)$.
$$
\begin{align}
M_{Y}(t) &= \int_{0}^\infty e^{xt} \frac{\lambda^n x^{n-1}}{(n-1)!}e^{-\lambda x}  \,dx  \\ \\
&= \frac{1}{\Gamma(n)} \int_{0}^\infty e^{(t-\lambda)x} \lambda^n x^{n-1} \,dx \\ 
&= \frac{\lambda^n}{\Gamma(n)} \int_{0}^\infty e^{-u} \frac{u^{n-1}}{(\lambda - t)^{n}}  \, du \\
&= \frac{\lambda^n}{(\lambda-t)^n}
\end{align}
$$
Since $M_{Y}(t) = M_{S_{n}}(t)$, $Y\stackrel{d}{=}S_{n}$ by uniqueness.

## (ii)



