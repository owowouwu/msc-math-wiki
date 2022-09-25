# [[Kolmogorov's Extension Theorem#Proof |KET Proof]]

# Constructing IID RVs

We want to construct a sequence of [[Random Variable]] $\{X_{n}\}$ such that they are independent and follow a distribution $F$.

Let $\Omega = \mathbb{R}^\infty$, $\mathcal{F} = \mathcal{B}(\mathbb{R}^\infty)$.

Define a family of probability measures
$$
\nu^{(n)} = \nu_{1} \otimes \dots \otimes \nu_{n} : \mathcal{B(\mathbb{R}^n)} \to [0,1]
$$
Check this satisfies consistency -
$$
\nu^{(n+1)}(G_{n} \times \mathbb{R}) = \nu^{(n)}(G_{n})\nu(\mathbb{R}) = \nu^{(n)}(G_{n})
$$
By [[Kolmogorov's Extension Theorem]] there is a unique measure $\mu$ which extends this to $\mathbb{R}^\infty$.

Now define the sequence - 
$$
\begin{align}
X_{n} : & \mathbb{R}^\infty \to \mathbb{R} \\
& (x_{1}, x_{2}, \dots) \mapsto x_{n}
\end{align}
$$
Check independence - 
$$
\begin{align}
P(X_{1} \in A_{1}, \dots , X_{n} \in A_{n}) &= \mu(A_{1}\times \dots \times A_{n} \times \mathbb{R}^{>n}) \\
 &= \nu^{(n)} (A_{1} \times \dots \times A_{n}) \\
&= \nu_{1}(A_{1}) \dots \nu_{n}(A_{n}) \\
&= P(X_{1} \in A_{1}) \dots P(X_{n} \in A_{n})
\end{align}
$$



