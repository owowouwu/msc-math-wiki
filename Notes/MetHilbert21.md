# Uniform Continuity

functions [[Uniformly Continuous]]

sequence of functions [[Uniform Convergence]] vs [[Pointwise Convergence]]


## Examples

LEt $X = \mathbb{R}_{[0,1]}$ and $d_{x}(x,y) = |y-x|$ and $C = \mathbb{R}_{[0,1]}$ with $d_{c}(x,y) = |y-x|$.

Let $f_{n} : \mathbb{R}_{[0,1]} \to \mathbb{R}_{[0,1]}$ given by $f_{n}(x) = x^n$ for $n \in \mathbb{Z}_{>0}$.

![[Pasted image 20220912204714.png]]

Let $f: \mathbb{R}_{[0,1]} \to \mathbb{R}_{[0,1]} = 1(x = 1)$. Then pointwise we have
$$
\lim_{n \to \infty}f_n(x) = f(x)
$$
As for $0<x < 1$ we have $f_{n}(x) = x^n \to 0$ but for $x=1$ we have $f_{n}(x) = 1$ for all $n$. 

but $\lim_{n \to \infty}f_{n} \neq f$ using the [[Uniform Norm]].
