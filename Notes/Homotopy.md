# Definition

Let $(X, \mathcal{T}_{X})$ and $(Y, \mathcal{T}_{Y})$ be [[Topological Space]]

Let $f_{1}, f_{2} \in \text{Map}(X,Y)$. The maps $f_{1}, f_{2}$ are **homotopic** if there exists $F \in \mathrm{Map}(X \times \mathbb{R}_{[0,1]}, Y)$  such that $F(x, 0) = f_{1}(x)$, $F(x,1) = f_{2}(x)$.

Think about $F$ as a [[Path (Topology)]] from $f_{1}$ to $f_{2}$. <- some sort of parametric equation in time?

We write that $f_{1} \cong f_{2}$ if they are homotopic.

## Intuition
![[Pasted image 20220925140420.png]]
we say that two maps are homotopic if there exists a **continuous deformation** between the two maps.