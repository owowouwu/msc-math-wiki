# Statement

If $T$ is a [[Bounded Compact Operator]] then the following are equivalent

(i) $T - \lambda$ is injective
(ii) $T-\lambda$ is bijective

# Proof
One direction is trivial. The main thing is to show that injectiveness implies bijectiveness. Which is to show that $\lambda -T$ is surjective.

We will show that if $\lambda - T$ is not surjective, then $T$ is not compact.

So $(\lambda - T)(H)$ is contained but not equal to $H$. We want to show that there exists a sequence of unit vectors $e_{1}, e_{2}, \dots$ in $H$ such that $Te_{1}, Te_{2}, \dots$ has no cluster point.

Construct
$$
(\lambda - T)^{n}(H) \subsetneq (\lambda-T)^{n-1}(H) \cdots
$$
The above sequence of inclusions follows from the fact that $\lambda -T$ is assumed to not be surjective.

Now let
$$
e_{n} \in (\lambda-T)^n (H) \cap (\lambda-T)^{n+1}(H)^\perp
$$
The idea is that for any $n$, $(\lambda-T)^n(H) = (\lambda-T)^{n+1}(H) + (\lambda-T)^{n+1}(H)^\perp$.

Then for any $m,n \in \mathbb{Z}_{\geq 0}$ with $m < n$,
$$
\begin{align}
\|Te_{m} - Te_{n}\| &= \langle Te_{m} - Te_{n}, Te_{m} - Te_{n} \rangle  \\
&= \langle Te_{m}, Te_{m} \rangle - \langle Te_{m}, Te_{n} \rangle - \langle Te_{n}, Te_{m} \rangle + \langle Te_{n}, Te_{n} \rangle \\
    
\end{align}
$$
