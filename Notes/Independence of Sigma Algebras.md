# Definition

Let $(\Omega, \mathcal{F}, P)$ be a [[Probability Space]], and let $\varphi_n$ be a sequence of sub-[[Sigma Algebra]] of $\mathcal{F}$.

We say that $\{\varphi_{n}\}$ are **independent** if whenever $G_{i} \in \varphi_{i}$ with $i_{1},\dots i_{n}$ distinct, we have that
$$
P(G_{i_{1}} \cap \dots \cap G_{i_{n}}) = P(G_{i_{1}}) \dots\cap\dots P(G_{n_{i}})
$$
## Example - Two $\sigma$-algebras

Let $\varphi_{1}$ and $\varphi_{2}$ be two [[Sigma Algebra]], then they are independent if for any $A \in \varphi_{1}$, $B \in \varphi_{2}$,
$$
P(A \cap B) = P(A) P(B)
$$

# [[Independence of Events]]

We can use this to say that a sequence of events $A_{1}, A_{2}, \dots, A_{n}$ are independent if and only if $\sigma(A_{1}), \dots, \sigma(A_{n})$ are independent.
