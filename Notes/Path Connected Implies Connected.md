# Statement

Let $(X, \mathcal{T})$ be a [[Topological Space]]. If a subset $E$ of $X$ with the usual [[Subspace Topology]] is path connected, then it is connected.

# Proof

Suppose for contradiction that $S \subseteq X$ is path connected but not connected.

Then there exists non-empty $A, B \in \mathcal{T}_{S}$ such that $A \cup B = S$ and $A \cap B = \phi$. Let $p \in A$ and $q \in B$. Since $S$ is path connected, there exists a [[Continuous]] $f:[0,1] \to X$ such that $f(0) = p$ and $f(1) = q$. 

By the continuity of $f$, $f^{-1}(A) \in \mathcal{T}_{[0,1]}$ and $f^{-1}(B) \in \mathcal{T}_{[0,1]}$ where $\mathcal{T}_{[0,1]}$ is the usual topology on $[0,1]$. Since preimages preserve union and intersection, $$
\begin{align}
f^{-1}(A) \cup f^{-1}(B) &= f^{-1}(A \cup B) = f^{-1}(S) = [0,1] \\
f^{-1}(A)\cap f^{-1}(B)&= f^{-1}(A \cap B) = \phi
\end{align}
$$
Which implies that $[0,1]$ is not connected, which is a contradiction as we know that $[0,1]$ is an interval, which is connected.


