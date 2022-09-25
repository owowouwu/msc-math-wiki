# Definition

Let $X$ be a set.

A **topology** is a set family $\mathcal{T}$ of subsets of $X$ which satisfies

1. $\phi \in \mathcal{T}_{X}$ and $X \in \mathcal{T}_{X}$.
2. For any $S \subseteq \mathcal{T}_{X}$, $\bigcup_{U \in S} U \in \mathcal{T}_{X}$ i.e $\mathcal{T}_{X}$ is closed under **countable** unions.
3. For any $k \in \mathbb{N}$, and $U_{1}, U_{2}, \dots U_{k} \in \mathcal{T}_{X} \implies \bigcap_{n=1}^k U_{n} \in \mathcal{T}_{X}$ i.e $\mathcal{T}_{X}$ is closed under **finite** intersection. 

An element of $\mathcal{T}_{X}$ is called an **open** set. On the other hand, for $A \subseteq X$ if $A^c \in \mathcal{T}_{X}$ then $A$ is called a **closed** set.