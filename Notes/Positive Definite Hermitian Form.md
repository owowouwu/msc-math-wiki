A positive definite Hermitian form on $V$ (inner product) is a function $<> : V \times V \rightarrow \mathbb{K}$ such that if 

1.  Addition - $x_{1}, x_{2}\in V$ and $y_{1}, y_{2}\in V$ then
$$
<x_{1}+x_{2},y> = <x_{1},y > + <x_{2},y>
$$
$$
<x, y_{1}+y_{2}> = <x,y_{1}> + <x, y_{2}>
$$
2. Scalar multiplication, if $c \in \mathbb{K}$
$$
<cx,y> =c<x,y>
$$
and
$$
<x,cy> =\overline{c}<x,y>
$$
Linear on the left, sesquilinear

3. Hermitian part - 
$$
<y,x> = \overline{<x,y>}
$$
4. If $x \in V$,  $<x,x> \in \mathbb{R}_{\geq_{0}}$ (positive semidefiniteness)
5. If $x \in V$, $<x,x> =0 \implies x = 0$

Define $\|\cdot\|$ as $\|x\| = \sqrt{ <x,x> }$. This makes $V$ a [[Normed Vector Space]].