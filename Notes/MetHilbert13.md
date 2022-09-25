## Example for [[Spectral Theorem]]

Consider $H = \mathbb{C}^5$ with
$$
\langle x,y \rangle = x_{1}\overline{y}_{1}+ \dots + x_{5}\overline{y}_{5}
$$
with $T: H \to H$ the linear transformation in which the basis $e_{1}, e_{2}, \dots e_{5}$ is given the matrix
$$
A = 
$$

This is [[Self-Adjoint]] since $A = \overline{A}^T$. The spectral theorem says that there is an orthormal basis $\left\{ u_{1}, \dots u_{5} \right\}$ of $\mathbb{C}^5$ consisting of eigenvectors of $T$. Let
$$
U = \left( \begin{matrix}
u_{1} & u_{2} & \dots & u_{5}
\end{matrix} \right) 
$$
be the change of basis matrix from $e_{n}$ to $u_{n}$. Since $u_{1},u_{2}, \dots, u_{5}$ are orthonormal,
$$
U\overline{U}^T=I
$$
i.e $U$ is unitary (equivalently, $U$ is an [[Isometry]])

Let $D = U^{-1} A U = \text{diag}(\lambda_{n})$. Then 
$$
\frac{1}{\lambda_{1}}D = \left( \begin{matrix}
1 & \\
& \frac{\lambda_{2}}{\lambda_{1}} & \\
& &  \frac{\lambda_{3}}{\lambda_{2}} & \\
& & & \dots
\end{matrix} \right) 
$$
Since we assume $\lambda_{1} > \dots > \lambda_{5}$,
$$
\left( \frac{1}{\lambda_{1}}D \right)^{1000} = \left( \begin{matrix}
1 &  \\
& 0 & \\
&& 0 & \\
&&& 0 & \\
&&&& 0
\end{matrix} \right)  
$$
So
$$
\lim_{n \to \infty}\left( \frac{1}{\lambda_{1}}A \right)^n = \lim_{n \to \infty}\left( \frac{1}{\lambda_{1}} UDU^{-1}\right)^n =U \left( \lim_{n \to \infty} \left( \frac{1}{\lambda_{1}}D \right)^n \right)U^{-1}   
$$
This is a projection onto $H_{\lambda_{1}}$, i.e it 
$$
\lim_{n \to \infty}\left( \frac{1}{\lambda_{1}}A \right)^n x = ku_{1}
$$
where $k \in \mathbb{C}$. This is how [[Power Iteration]] works.

## How about matrices that are NOT self adjoint?

If $B$ is not self adjoint, we define
$$
A = B^*B
$$
where $B^* = \overline{B}^T$. Which gives
$$
\overline{A}^T = \overline{(B^*B)}^T = \overline{B}^T B = A
$$
We claim that
$$
\|B\| = \max\left\{ \sqrt{ |\lambda_{1}| }, \dots , \sqrt{ |\lambda_{5}| } \right\} 
$$
where $\lambda_{i}$ are the eigenvalues of $A$. Why is this true?

If $u_{j} \in H$ and $A_{u_{j}} = \lambda_{j}u_{j}$ then
$$
\|Bu_{j}\|^2 = \langle Bu_{j}, Bu_{j} \rangle = \langle u_{j}, B^*Bu_{j} \rangle = \langle u_{j}, Au_{j} \rangle= \overline{\lambda}_{j} \langle u_{j},u_{j}  \rangle=\overline{\lambda}_{j}    
$$
So 
$$
\frac{\|Bu_{j}\|}{\|u_{j}\|} = \sqrt{ |\lambda_{j}| } 
$$
Hence $\|B\| \geq \max\left\{ \sqrt{ |\lambda_{1}| }, \dots, \sqrt{ |\lambda_{5}| } \right\}$.

On the other hand, let $x \in H$ be arbitrary 
$$
\begin{align}
\|Bx\|^2 &= \langle Bx, Bx \rangle  \\
&= \langle x, Ax \rangle \\
&= \langle x_{1}u_{1} + \dots + x_{5}u_{5}, A(x_{1}u_{1} + \dots x_{5}u_{5}) \rangle   \\
&= x_{1}^2\lambda_{1} + \dots + x_{5}^2\lambda_{5} \\
&= \leq \max\left\{ \lambda_{1}, \dots,\lambda_{5} \right\}(x_{1}^2 + \dots + x_{5}^2) = \max\left\{ \lambda_{1}, \dots ,\lambda_{5} \right\}\|x\|^2 
\end{align}
$$
in lines 3 to 4 we use the fact that $u_{n}$ is an orthonormal basis for $H$.

This gives $\|B\| \leq \max\left\{ \sqrt{ |\lambda_{1}| }, \dots ,\sqrt{ |\lambda_{5}| } \right\}$
