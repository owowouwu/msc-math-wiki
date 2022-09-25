# Question 1

## (a)

Let $\lambda \in \mathbb{C}$, and
$$
A = \left(\begin{matrix}
\cos(\theta) & \sin(\theta) \\
-\sin(\theta) & \cos(\theta)
\end{matrix}\right)
$$
then $|A - \lambda I| = (\cos(\theta)-\lambda)^2 + \sin^2(\theta)$.

Let $|A - \lambda I| = 0$
$$
\begin{align}
(\cos(\theta)-\lambda)^2 &= -\sin^2(\theta) \\
\lambda &= \cos(\theta) \pm \sin(\theta)i
\end{align}
$$
For $\lambda_{1} = \cos(\theta) - \sin(\theta)i$,
$$
A - \lambda_{1}I = \left( \begin{matrix}
i\sin \theta & \sin \theta \\
-\sin \theta &i \sin \theta
\end{matrix} \right) \sim \left( \begin{matrix}
i\sin \theta & \sin \theta \\
i\sin \theta & \sin \theta
\end{matrix} \right)  
$$
Giving the eigenvector $v_{1} = (i, 1)$.

For $\lambda_{2} = \cos(\theta) + \sin(\theta)i$ we have
$$
A - \lambda_{2}I = \left( \begin{matrix}
-i\sin \theta & \sin \theta  \\
-\sin \theta &- i\sin \theta
\end{matrix} \right) \sim \left( \begin{matrix}
-i\sin \theta & \sin \theta \\
-i\sin \theta & \sin \theta
\end{matrix} \right)  
$$
Giving the eigenvector $v_{2} = (i, -1)$.

## (b)

Let
$$
A = \frac{1}{\sqrt{ 2 }}\left( \begin{matrix}
1 & 1  \\
-1 & 1
\end{matrix} \right) 
$$
The characteristic polynomial is
$$
|A - \lambda I| = \frac{1}{2}(1-\lambda)^2 + \frac{1}{2}
$$
This only has solutions for $\lambda \in \mathbb{C}$, hence $A$ has no eigenvectors as a linear operator on $\mathbb{R}$.

## (c) 

Let $A \in M_{n}(\mathbb{C})$. By the fundamental theorem of algebra, the characteristic polynomial $|A - \lambda I|$ has exactly $n$ roots $\lambda_{1},\dots, \lambda_{n}\in \mathbb{C}$.

Let $\alpha$ be one such root. Now since $|A - \alpha I| = 0$, $A - \alpha I$ is singular and hence there exists some $v \in \mathbb{C}^n \backslash\{0\}$ such that $(A-\alpha I)v = 0$, giving $Av = \alpha v$. Hence for any $A in M_{n}(\mathbb{C})$, there exists at least one eigenvector in $\mathbb{C}^n$.


# Question 2

It suffices to prove that if $\sum_{n=1}^\infty |a_{n}z^n|$ converges in $\mathbb{R}_{\geq 0}$, then $\sum_{n=1}^\infty a_{n}z_{n}$ converges in $\mathbb{C}$.

Since $\sum_{n=1}^\infty a_{n} \epsilon_{n}$ converges, $\lim_{n \to \infty}a_{n}\epsilon^n = 0$. Let $\delta \in \mathbb{R}_{\geq_{0}}$. By the definition of limits, there exists some $K \in \mathbb{Z}_{\geq 0}$ such that $n > K \implies |a_{n} \varepsilon^n| < \delta$. 
$$
\begin{align}
\sum_{n=1}^\infty |a_{n}z^n| &= \sum_{n=1}^K |a_{n}z^n| + \sum_{n = K+1}^\infty |a_{n}z^n| \\
&< \sum_{n=1}^K |a_{n}z^n| + \sum_{n=K+1}^\infty \frac{\delta |z^n|}{|\varepsilon|^n} \\
&= \sum_{n=1}^K |a_{n}z^n| + \delta\sum_{n=K+1}^\infty \left( \frac{|z|}{\epsilon} \right)^n
\end{align}
$$
Notice that $\frac{|z|}{\epsilon}<1$, so the summand on the right converges as a geometric series. On the other hand the summand on the left is a finite sum, so altogether the sum is finite. Hence $\sum_{n=1}^\infty |a_{n}z^n| < \infty$, and it can be concluded that $\sum_{n=1}^\infty a_{n}z_{n}$ converges in $\mathbb{C}$.

# Question 3

In each question denote
$$
A = \left\{\frac{\|\phi(v)\|}{\|v\|_{\mathbb{R}^2}}: v\in \mathbb{R}^2 \right\} 
$$
with $\|v\|_{\mathbb{R}^2}$ being whatever norm is specified.

## (a)

Let $c = \max\{|a|, |b|\}$, and $v = (x_{1}, x_{2}) \in \mathbb{R}^2$
$$
\begin{align}
\frac{|ax_{1} + bx_{2}|}{|x_{1}| + |x_{2}|} &\leq \frac{|ax_{1}| + |bx_{2}|}{|x_{1}|+|x_{2}|} \\
&= \frac{|a| |x_{1}| + |b| |x_{2}|}{|x_{1}| + |x_{2}|} \\
&\leq \frac{c|x_{1}| + c|x_{2}|}{|x_{1}| + |x_{2}|} \\
&=c
\end{align}
$$
Hence $c$ is an upper bound for $A$. Now it suffices to show that $c \in A$. Let $1$ denote the indicator function, and let
$$u = (1,0)1(|a| > |b|) + (0,1)1(|b| \geq |a|)$$
Note that $\|u\|_{1} = 1$. 

then
$$
\frac{\|\phi(u)\|}{\|u\|_{V}} = \frac{|a|1(|a|>|b|) + |b|1(|b|\geq |a|)}{1} = \max(|a|,|b|)
$$
Since $c \in A$ and $c$ is an upper bound for $A$, we conclude that
$$
c = \max(|a|, |b|) = \sup A = \|\phi\|
$$
## (b)

Let $c = |a| + |b|$, and $v = (x_{1}, x_{2}) \in \mathbb{R}^2$. Note that $\|v\|_{\infty} = \sup\{|x_{1}|, |x_{2}|\} = \max(|x_{1}|, |x_{2}|)$.

$$
\begin{align}
\frac{|ax_{1}+bx_{1}|}{\max(|x_{1}|, |x_{2}|)} & \leq \frac{|a| |x_{1}| + |b| |x_{2}|}{\max(|x_{1}|, |x_{2}|)} \\
&\leq \frac{(|a|+|b|)\max(|x_{1}|, |x_{2}|)}{\max(|x_{1}|, |x_{2}|)} \\
&=|a| + |b|
\end{align}
$$
Hence $|a| + |b|$ is an upper bound for $A$. Now consider the following cases - 

Suppose both of $a,b$ are 0. It is clear then that $\frac{\|\phi(v)\|}{\|v\|_{\infty}} = 0$ for all $v \in \mathbb{R}^2$. In this case, we clearly have that $|a|+|b| = 0 \in A$.

Now suppose without loss of generality that $a = 0$. Then $|a| + |b| = |b|$ Letting $u = (1,1)$ we have
$$
\frac{\|\phi(v)\|}{\|v\|_{\infty}} = \frac{|b|}{\max(1,1)} = |b|
$$
So in this case $|a| + |b| \in A$.

Now suppose neither of $a$ or $b$ are $0$. Define
$$
u = \left( \frac{|a|}{a}, \frac{|b|}{b} \right) 
$$
We can see that
$$\|u\|_{\infty} = \max\left( \left| \frac{|a|}{a} \right|, \left| \frac{|b|}{b} \right| \right) = \max(1,1) = 1$$$$
\|\phi(u)\| = \left| a \frac{|a|}{a} + b \frac{|b|}{b} \right| = |a| + |b| 
$$
So $|a|+|b| \in A$ for any $a,b$. Since it is an upper bound, it is the supremum of $A$ and so we conclude that 
$$
\|\phi\| = |a| + |b|
$$

## (c)

By Holder's inequality,
$$
\begin{align}
\frac{\|\phi(v)\|}{\|v\|_{p}} &= \frac{|ax_{1} + bx_{2}|}{\|x\|_{p}} \\
&\leq\|(a,b)\|_{q} \frac{\|x\|_{p}}{\|x\|_{p}} \\
&=\|(a,b)\|_{q}
\end{align}
$$
So $\|(a,b)\|_{q}$ is an upper bound for $A$. Now consider the following cases - 

Suppose both of $a,b$ are 0. It is clear then that $\frac{\|\phi(v)\|}{\|v\|_{p}} = 0$ for all $v \in \mathbb{R}^2$. In this case, we clearly have that $\|(a,b)\|_{q} = 0 \in A$.

Now suppose without loss of generality that $a = 0$. Then $\|(a,b)\|_{q} = |b|$ Letting $u = (1,1)$ we have
$$
\frac{\|\phi(v)\|}{\|v\|_{p}} = \frac{|b|}{\|x\|_{p}} = \frac{|b|}{1} = |b|
$$
Now suppose neither of $a$ or $b$ are $0$. Define
$$
u = \left( \frac{|a|^q}{a}, \frac{|b|^q}{b} \right) 
$$
then

$$
\frac{\|\phi(v)\|}{\|v\|_{p}} = \frac{\left| |a|^q + |b|^q \right| }{\left( \frac{|a|^{qp}}{|a|^p} +  \frac{|b|^{qp}}{|b|^p} \right)^{1/p} }
$$
Since $\frac{1}{p} + \frac{1}{q} = 0$, $qp - p = q$, so
$$
\begin{align}
\frac{\left| |a|^q + |b|^q \right| }{\left( \frac{|a|^{qp}}{|a|^p} +  \frac{|b|^{qp}}{|b|^p} \right)^{1/p} } &= \frac{\left| |a|^q + |b|^q \right| }{(|a|^q + |b|^q)} \\
&=\left( |a|^q  + |b|^q\right)^{1/q} 

\end{align}
$$
Hence for any $a,b \in \mathbb{R}$ there exists $v \in \mathbb{R}^2$ such that $\|(a,b)\|_{q} \in A$.

Since it is an upper bound as well, we conclude that $\|(a,b)\|_{q} = \sup A = \|\phi\|$.
