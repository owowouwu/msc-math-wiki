# Statement

Let $H$ be a Hilbert space. Let $T: H \to H$ be a bounded compact self adjoint operator. Let $b_{0} \in H$. Define sequences 
$$
(b_{1}, b_{2}, \dots) \quad (\mu_{1}, \mu_{2}, \dots)
$$
by $$b_{k+1} = \frac{Tb_{k}}{\|Tb_{k}\|}$$ and $$\mu_{k+1} = \frac{\langle Tb_{k}, b_{k} \rangle} {\langle b_{k}, b_{k} \rangle} = \frac{\langle b_{k+1}, b_{k} \rangle}{\|b_{k}\|^2}$$
Then 
$$
\|T\| = \lim_{k \to \infty} \mu_{k}
$$
and
$$
v = \lim_{k \to \infty} b_{k}
$$
is an eigenvector of $T$ with eigenvalue $\|T\|$.