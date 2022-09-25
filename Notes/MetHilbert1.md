## Lecture 1

### Banach Space

A Banach space is a normed vector space which is [[Complete |complete]].

A normed vector space is a vector space with a function $||\quad || : V \rightarrow \mathbb{R}_{\geq 0}$ such that

Let $\mathbb{K}$ be $\mathbb{R}$ or $\mathbb{C}$ which has an absolute value function.

- If $x,y \in V$ then $||x+y|| \leq ||x|| + ||y||$ (triangle inequality)
- If $x\in V$ and $c \in \mathbb{K}$ then $||cx|| = |c| ||x||$  
- If $v \in V$ and $||v|| =0$ then $v = 0$

e.g  $\mathbb{R}^2$ with Euclidean norm

## Accuracy

Let the *tolerance* set be 
$$
\mathbb{E} = \{10^{-1}, 10^{-2}, \dots \}
$$
Define $d : V \times V \rightarrow \mathbb{R}_{\geq 0}$ by $d(x,y) = || y - x ||$ (distance metric).

For $\varepsilon \in \mathbb{E}$, define the $\epsilon$-ball as 

$$
B_\epsilon (x) = \{ y \in V | d(y,x) < \epsilon \}
$$
and the $\epsilon$-diagonal as

$$
B_\epsilon = \{(x,y) \in V\times V | d(y,x) < \epsilon \}
$$
## Cauchy Sequence

A Cauchy sequence in $V$ is a sequece in $V$ such that if $\epsilon \in \mathbb{E}$ then there exists a $N \in \mathbb{N}$ such that if $m, n \in \mathbb{N}$ then $(x_m, x_n) \in B_\epsilon$, i.e $d(x_m, x_n) = ||x_m - x_n|| < \epsilon$.

## Convergence

A sequence converges in $V$ if there exists a vector $v \in V$ such that if $\epsilon \in \mathbb{E}$ there exists $N \in \mathbb{N}$ such that if $n > N$, $x_n \in B_\epsilon (v)$.

[[Complete]]

