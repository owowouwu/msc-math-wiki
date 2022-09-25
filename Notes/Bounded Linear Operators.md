A **bounded** linear operator is a [[Linear Operators|linear operator]] whose [[Operator Norm|norm]] exists in $\mathbb{R}_{\geq_{0}}$

Recall that the [[Operator Norm]] is defined to be
$$
\|\varphi\| = \sup\left\{\frac{\|\varphi(v)\|_{W}}{\|v\|_{V}}  : v \in V \right\} 
$$
i.e if $v$ is a unit vector, how much does $\varphi$ scale $v$ by?

## Space of Bounded Linear Operators

Recall that
$$
\text{End}(V,W) = \{T:V\rightarrow W : T \text{ is a linear operator} \}
$$
is a the space of all linear operators mapping $V$ to $W$. It is a vector space. If it happens that we have $\|T\|<\infty$ for each $T$ then it is a space of bounded linear operators. Denote
$$
B(V,W) = \{T : V\rightarrow W : \|T\|<\infty \}
$$
