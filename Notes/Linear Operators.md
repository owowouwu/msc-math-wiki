# Linear Transformations

Let $K$ be a field and $V$ and $W$ be $K$-vector spaces.

A **linear operator** from $V\rightarrow W$ is a function
$$T: V\rightarrow W$$
that preserves linearity -
- $v_1, v_2 \in V \implies T(v_1+v_2) = T(v_1) +t(v_2)$
- $c \in K$ and $v\in V \implies T(cv) = cT(v)$

## Space of Linear Operators

Denote the space of linear operators from $V$ to $W$ by
$$
\text{End}(V,W) = \{T:V\rightarrow W : T \text{ is a linear operator} \}
$$
Define addition and scalar multiplication by

- $(T_{1} + T_2)(v)=T_{1}(v)+T_{2}(v)$
- $(cT)(v) = cT(v)$

Then this is a vector space. If we endow this with the [[Operator Norm]] it becomes a [[Normed Vector Space]] (and hence also a [[Metric Space]]).