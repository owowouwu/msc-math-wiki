# Problem 1 (Proof of [[Monotone Class Theorem]])

## (i)

Let $\mathcal{F}$ be a $\lambda$-system. It is clear by the properties of a $\lambda$-system that for $A_{n} \in \mathcal{F}$ with $A_{n} \uparrow A$, $A \in \mathcal{F}$. So we need to show for decreasing sequences $A_{n}\in \mathcal{F}$, $A_{n} \downarrow A \in \mathcal{F}$.

Consider a such a sequence and consider the complement, $A_{n}^c \uparrow A^c$. Since $\mathcal{F}$ is a $\lambda$-system, $\Omega \in \mathcal{F}$ and it is closed under set removal, so $A_{n}^c \in \mathcal{F}$, and since this is an increasing sequence $A^c \in \mathcal{F}$. Again we take the complement and get that $(A^c)^c = A \in \mathcal{F}$. Hence if $A_{n} \in \mathcal{F}$
$$
A_{n} \uparrow A \, \text{or} \, A_n\downarrow A \implies A \in \mathcal{F}
$$
An example a monotone system which is not a $\lambda$-system - 

Consider $\Omega = \left\{ 1,2,3,4 \right\}$ and the set class $\mathcal{C} = \{\{1,2 \}, \{1,2,3\},\{1,2,3,4\} \}$. It is clear that $\mathcal{C}$ is a montone system, but it is not a $\lambda$-system as it is not closed under set removal - $\{1,2,34\} \backslash \{1,2,3\} = \{1 \} \notin \mathcal{C}$.

## (ii)

Let $\mathcal{F}$ be a set class which is an algebra and also a montone system.

From the definition of an algebra we have that $\Omega \in \mathcal{F}$, and that for any $A \in \mathcal{F}$, $A^c \in \mathcal{F}$. So it remains to show that $\mathcal{F}$ is closed under countable union.

Let $A_{n} \in \mathcal{F}$ be a sequence of sets and define $B_{n} = \bigcup_{k=1}^n A_{k}$. Clearly $B_{n} \in \mathcal{F}$ as this is a finite union. But it is also an increasing sequence of sets, hence its limit is in $\mathcal{F}$ since $\mathcal{F}$ is a montone system.

But
$$
\bigcup_{n=1}^\infty B_{n} = \bigcup_{n=1} ^\infty \bigcup_{k=1}^n A_{k} = \bigcup_{n=1}^\infty A_{n}
$$
Hence $\bigcup_{n=1}^\infty A_{n} \in \mathcal{F}$.

## (iii)

Let $A_{n} \in \sigma(\mathcal{A})$, such that $A_{n} \uparrow \mathcal{A}$. By the properties of a $\sigma$-algebra, $A = \bigcup_{n=1}^\infty A_{n} \in \sigma(\mathcal{A})$.
$$
\bigcup_{n=1}^\infty B_{n} = \bigcup_{n=1}^\infty A_{n}
$$
Similarly, if $A_{n} \downarrow A$, then $A_{n}^c  \in \sigma(\mathcal{A})$, and since $A_{n}^c \uparrow A^c$ we have $A^c \in \sigma(\mathcal{A})$ and hence $A \in \sigma(\mathcal{A})$.

Hence $\sigma(\mathcal{A})$ is a monotone system. By the definition of $m(\mathcal{A})$, $m(\mathcal{A}) \subseteq \sigma(\mathcal{A})$.

Now it remains to show that $\sigma(\mathcal{A}) \subseteq m(\mathcal{A})$. 

From the previous part it suffices to show that $m(\mathcal{A})$ is an algebra. In other words we want to show that for any $A,B \in m(\mathcal{A})$, $A \cap B \in m(\mathcal{A})$ and $A^c \in m(\mathcal{A})$.

Let $B \in m(\mathcal{A})$. 
$$
\mathcal{H}_{B} = \{A \in m(\mathcal{A}) : A \cap B \in m(\mathcal{A})\} \bigcap\left\{ A \in m(\mathcal{A}) : A^c \in m(\mathcal{A}) \right\} 
$$
Let $A_{n} \in \mathcal{H}_{B}$ be a sequence of increasing sets with limit $A_{n} \uparrow A$. By assumption each $A_{n} \cap B \in m(\mathcal{A})$. Hence $A \cup B = \bigcup_{n}(A_{n} \cap B) \in m(\mathcal{A})$ by the definition of a monotone system. Similarly, $A^c = \bigcap_{n}A_{n}^c \in m(\mathcal{A})$, as $A_{n}^c$ is a sequence of monotonically decreasing sets. 

Now similarly if $A_{n} \in \mathcal{H}_{B}$ is a sequence of decreasing sets with limit $A_{n} \downarrow A$ we have $A_{n} \cap B \in m(\mathcal{A}) \implies \bigcap_{n}(A_{n} \cap B) = A  \in m(\mathcal{A})$. On the other hand, $A^c = \bigcup_{n}A_{n}^c$ and since each $A_{n}^c$ is increasing and in $m(\mathcal{(A)})$ we have $A^c \in \mathcal{A}$.

Hence $\mathcal{H}_{B}$ is a monotone system. Let $A \in \mathcal{A}$ and $B \in \mathcal{A}$. We have by the definition of an algebra that $A \cap B \in \mathcal{A}$ and $A^c \in \mathcal{A}$, hence $A \in \mathcal{H}_{B}$ so $\mathcal{A} \subseteq \mathcal{H}_{B}$ for any fixed $B \in \mathcal{A}$. 

On the other hand, since $\mathcal{H}_{B}$ is a monotone system we have $m(\mathcal{A}) \subseteq \mathcal{H}_{B}$. But by the definition of $\mathcal{H}_{B}$ we have $\mathcal{H}_{B} \subseteq m(\mathcal{A})$ so $m(\mathcal{A}) = \mathcal{H}_{B}$. 

By symmetry we also have that if $A \in \mathcal{H}_{B}$ then $B \in \mathcal{H}_{A}$ since both $A$ and $B$ are in $m(\mathcal{A})$. But since $B \in \mathcal{A}$ we have $\mathcal{A} \subseteq \mathcal{H}_{A}$. We have $m(\mathcal{A}) = \mathcal{H}_{A}$ again. 

Since $A$ is an arbitrary element in $m(\mathcal{A})$ we conclude that $m(\mathcal{A})$ satisfies the properties of an algebra. Hence $m(\mathcal{A})$ is a $\sigma$-algebra, and we have $\sigma(\mathcal{A}) = m(\mathcal{A})$.

# Problem 2

## (i)

This is equivalent to showing that
$$
F(b)G(b) - F(a)G(a) = \int_{(a,b]}F(x) \, d\mu_{G} + \int_{(a,b]} G(x^-)d\mu_{F}
$$
Let $(\mathbb{R}^2, \mathcal{B}(\mathbb{R}^2), \mu)$ be the product space $(\mathbb{R}, \mathcal{B}(\mathbb{R}), \mu_{F}) \otimes (\mathbb{R}, \mathcal{B}(\mathbb{R}),\mu_{G})$.

We have that
$$
\begin{align}
F(b)G(b)  &= \left( \int 1(x \leq b)d\mu_{F} \right)\left( \int 1(y \leq b)d\mu_{G} \right)  \\
&= \int \int 1(x\leq b) 1 (y\leq b) d\mu
\end{align}
$$
by Fubini's theorem.

So
$$
\begin{align}
F(b)G(b) - F(a)G(a) &= \int \int 1((x,y)\in (-\infty ,b]^2) d\mu - \int \int 1((x,y) \in (-\infty, a]^2)d\mu \\
&= \int \int 1((x,y)\in (-\infty ,b]^2) - 1((x,y)\in (-\infty ,a]^2) d\mu \\
&= \int \int 1((x,y) \in (a,b]^2) d\mu
\end{align}
$$
Now consider the following sets
$$
\begin{align}
A &= \{(x,y) \in \mathbb{R}^2 : x \in (a,b], y < x\} \\
B &= \left\{ (x,y) \in \mathbb{R}^2 : x \leq y, y \in (a,b]\right\} 
\end{align}
$$
Clearly $(a,b]^2 = A + B$. Note that $\mu_{G}(A) = G(x^-)1(x \in (a,b])$ due to the strict inequality.
$$
\begin{align}
F(b)G(b) - F(a)G(a) &= \int \int 1_{A} d\mu + \int \int 1_{B}d\mu \\
&= \int \left( \int 1_{A} d\mu_{G} \right) d\mu_{F} + \int \left( \int {1}_{B} d\mu_{F} \right) d\mu_{G}  \\
&= \int G(x^-) 1(x \in (a,b])1\mu_{F}(dx) + \int F(x)1(x \in (a,b]) d\mu_{G}(dx) \\
&= \int_{(a,b]}G(x^-) d\mu_{F}(dx) + \int_{(a,b]} F(x) d\mu_{G}(dx)
\end{align}
$$
as required.

## (ii)

In a similar manner,
$$
\begin{align}
F(b^-)G(b^-) - F(a^-)G(a^-) &= \int \int 1((x,y)\in (-\infty ,b)^2) d\mu - \int \int 1((x,y) \in (-\infty, a)^2)d\mu \\
&= \int \int 1((x,y)\in (-\infty ,b)^2) - 1((x,y)\in (-\infty ,a)^2) d\mu \\
&= \int \int 1((x,y) \in [a,b)^2) d\mu
\end{align}
$$
Now take
$$
\begin{align}
A &= \{(x,y) \in \mathbb{R}^2 : x \in [a,b), y < x\} \\
B &= \left\{ (x,y) \in \mathbb{R}^2 : x \leq y, y \in [a,b)\right\} 
\end{align}
$$
$$
\begin{align}
F(b^-)G(b^-) - F(a^-)G(a^-) &= \int \int 1_{A} d\mu + \int \int 1_{B}d\mu \\
&= \int \left( \int 1_{A} d\mu_{G} \right) d\mu_{F} + \int \left( \int {1}_{B} d\mu_{F} \right) d\mu_{G}  \\
&= \int_{[a,b)}G(x^-) d\mu_{F}(dx) + \int_{[a,b)} F(x) d\mu_{G}(dx)
\end{align}
$$
Which gives

$$
\int_{[a,b)} F(x)d\mu_{G}(dx) = F(b^-)G(b^-) - F(a^-)G(a^-) - \int_{[a,b)} G(x^-) d\mu_{F}(dx)
$$

## (iii)

$$
\begin{align}
\int_{\mathbb{R}} F(x) d\mu_{F}(x) &= \int_{\mathbb{R}} \left(\int_{\mathbb{R}} 1(y \in (-\infty, x]) d\mu_{F}(y) \right) d\mu_{F}(x)\\ 
&= \int_{\mathbb{R}} \left( \int_{\mathbb{R}} 1(x \in [y, \infty)) d\mu_{F}(x) \right) d\mu_{F}(y) \\
&= \int_{\mathbb{R}}1-F(y) d\mu_{F}(y) \\
&= 1 - \int_{\mathbb{R}} F(y) d\mu_{F}(y) \\
&= 1- \int_{\mathbb{R}} F(x) d\mu_{F}(x) 
\end{align}
$$
Hence
$$
\int_{\mathbb{R}}F(x) d\mu_{F}(x) = \frac{1}{2}
$$
(continuity of $F$ used in line 2 to 3)

  
# Question 3

## (i)

We want to show (a) that $I^f$ is bounded and that (b) it is $\mathcal{F}_{1}$-measurable.

### (a) boundedness

Since $f$ is bounded, there exists $M >0$ s.t $|f| \leq M$. Boundedness is clear -
$$
\begin{align}
|I^f(\omega_{1})| &= \left| \int_{\Omega_{2}}f(\omega_{1}, \omega_{2}) 
 \,p(\omega_{1}, d\omega_{2})\right| \\
&\leq \int_{\Omega_{2}} |f(\omega_{1}, \omega_{2})| \, p(\omega_{1}, d\omega_{2}) \\
&\leq M \int_{\Omega_{2}} p (\omega_{1}, d\omega_{2}) \\
&= M
\end{align}
$$

### (b) measurability

Since any bounded measurable function can be approximated as a sequence of simple functions, first it will be shown that $I^f$ is $\mathcal{F}_{1}$ measurable for indicator functions.

Let $A \in \mathcal{F}_{1}$, $B \in \mathcal{F}_{2}$ and define $g : \Omega_{1} \times \Omega_{2} \to \mathbb{R} \, g(\omega_{1}, \omega_{2}) = 1_{A \times B} (\omega_{1}, \omega_{2})$. Clearly $g$ is bounded and $\mathcal{F}$-measurable as $A \times B \in \mathcal{F}_{1} \otimes \mathcal{F}_{2}$. Now we want to show that $1^g(\omega_{1})$ is measurable.
$$
\begin{align}
1^g(\omega_{1}) &= \int_{\Omega_{2}} 1_{A \times B}(\omega_{1}, \omega_{2})  \, p(\omega_{1}, d\omega_{2}) \\
&=1_{A}(\omega_{1}) \int_{\Omega_{2}} 1_{B}(\omega_{2}) p (\omega_{1}, d\omega_{2}) \\
&= 1_{A}(\omega_{1}) p(\omega_{1}; B)
\end{align}
$$
Notice that $1_{A}(\omega_{1})$ is obviously $\mathcal{F}_{1}$ measurable, and by property $(B)$ of $p$, $p(\omega_{1}; B)$ is also $\mathcal{F}_{1}$ measurable. Hence $1^g(\omega_{1})$ is the product of two $\mathcal{F}_{1}$ measurable functions, so it itself is measurable. Hence for the class of sets
$$
\mathcal{C} = \{A \times B \subseteq \Omega_{1} \times \Omega_{2} : A \in \mathcal{F}_{1}, B\in\mathcal{F_{2}}\}
$$
the indicator of a set is $\mathcal{F}_{1}$-measurable. We know that this is a $\pi$-system and that $\sigma(\mathcal{C}) = \mathcal{F}_{1} \otimes \mathcal{F}_{2}$.

Now define the following class set
$$
\mathcal{H} = \{A \in \mathcal{F} : I^{1_{A}}(\omega_{1}) \text{ is $\mathcal{F}_{1}$-measurable} \}
$$
It is easy to see that $\mathcal{C} \subseteq \mathcal{H}$. Now it will be shown that $\mathcal{H}$ is a $\lambda$-system.

**(L1)** $\Omega \in \mathcal{H}$ is obvious.
**(L2)** Let $A, B \in \mathcal{H}$ be such that $A \subseteq B$. 

$$
\begin{align}
1^{1_{B\backslash A}}(\omega_{1}) &= \int_{\Omega_{2}} 1_{B\backslash A}(\omega_{1}, \omega_{2})  \, p(\omega_{1}, d\omega_{2}) \\
&= \int_{\Omega_{2}} 1_{B}(\omega_{1},\omega_{2}) p(\omega_{1}, d\omega_{2}) - \int_{\Omega_{2}} 1_{A}(\omega_{1}, \omega_{2}) \, p(\omega_{1}, d\omega_{2}) \\
&= I^{1_{B}}(\omega_{1}) - I^{1_{A}}(\omega_{1})
\end{align}
$$
Since this is a linear combination of measurable functions, $I^{1_{B \backslash A}}$ is also $\mathcal{F}_{1}$ measurable, hence $B \backslash A \in \mathcal{H}$. 

**(L3)** Let $\{A_{n} \} \in \mathcal{H}$ be such that $A_{n} \uparrow A$. Since $1_{A_{n}} \to 1_{A}$,
$$
\begin{align}
I^{1_{A}}(\omega_{1}) &= \int_{\Omega_{2}} 1_{A}(\omega_{1}, \omega_{2}) \, p(\omega_{1}, d\omega_{2}) \\
&= \int_{\Omega_{2}} \lim_{n \to \infty} 1_{A_{n}}(\omega_{1}, \omega_{2}) \, p(\omega_{1}, d\omega_{2}) \\
\end{align}
$$
By the [[Monotone Convergence Theorem]], 
$$
\begin{align}
I^{1_{A}}(\omega_{1}) &= \lim_{n \to \infty}\int_{\Omega_{2}}  1_{A_{n}}(\omega_{1}, \omega_{2}) \, p(\omega_{1}, d\omega_{2}) \\
&= \lim_{n \to \infty} 1^{1_{A_{n}}}(\omega_{1})
\end{align}
$$
Since measurability is preserved under limit, $I^{1_{A}}(\omega_{1})$ is measurable, hence $A \in \mathcal{H}$.

Since $\mathcal{H}$ is a $\lambda$-system, by [[Dynkin's pi-lambda Theorem]], $\sigma(\mathcal{C}) = \mathcal{F}$ satisfies the property that for any $A \in \mathcal{F}$, $I^{1_{A}}(\omega_{1})$ is $\mathcal{F}_{1}$-measurable. 

Hence since we can approximate any $\mathcal{F}$-measurable function $f$ with a sequence of simple functions, each of which are $\mathcal{F}_{1}$ measurable, we conclude that $I^f(\omega_{1})$ is $\mathcal{F}_{1}$ measurable.

## (ii)

This is similar to construction of [[Product Measures]]

Let $A_{1} \in \mathcal{F}_{1}$ and $A_{2} \in \mathcal{F}_{2}$ and let $g := 1_{A_{1} \times A_{2}}$. Recall from the result in (i),
$$
\begin{align}
1^g(\omega_{1}) &= \int_{\Omega_{2}} 1_{A_{1} \times a_{2}}(\omega_{1}, \omega_{2})  \, p(\omega_{1}, d\omega_{2}) \\
&=1_{A_{1}}(\omega_{1}) \int_{\Omega_{2}} 1_{A_{2}}(\omega_{2}) p (\omega_{1}, d\omega_{2}) \\
&= 1_{A_{1}}(\omega_{1}) p(\omega_{1}; A_{2})
\end{align}
$$
Then
$$
\int_{\Omega_{1}} 1_{A}(\omega_{1}) p(\omega_{1}, A_{2}) \, d\mu_{1}(\omega_{1}) = \int_{A_{1}} p(\omega_{1}, A_{2}) \, d\mu_{1}(\omega_{1})
$$So naturally we define $\mu$ as follows :
$$
\mu : \mathcal{F} \to \mathbb{R}\quad \mu(A) = \int_{\Omega_{1}} I^{1_{A}}(\omega_{1}) \, d\mu_{1}(\omega_{1})
$$
Clearly the uniqueness is satisfied by the calculation above.

It remains to show that this is actually a probability measure.

**(P1)** 
$$
\begin{align}
\mu(\Omega) &= \int_{\Omega_{1}} I^{1_{\Omega}}(\omega_{1}) d\mu_{1}(\omega_{1}) \\
&= \int_{\Omega_{1}} I^{1_{\Omega_{1}\times \Omega_{2}}}(\omega_{1}) \, d\mu(\omega_{1}) \\
&= \int_{\Omega_{1}} 1_{\Omega_{1}} (\omega_{1}) p(\omega_{1}; \Omega_{2})  \, d\mu(\omega_{1}) \\
&= \int_{\Omega_{1}} d\mu(\omega_{1}) = 1
\end{align}
$$
**(P2)** Non-negativity is obvious.
**(P3)** Suppose $\left\{ A_{n} \right\} \in \mathcal{F}$ is a disjoint sequence of sets with $A = \bigcup_{n} A_{n}$. Let $G_{n} = \sum_{k=1}^n A_{k}$.

Then 

$$I^{1_{G_{n}}} = \int_{\Omega_{2}} 1_{G_{n}} \, p(\omega_{1}, d\omega_{2}) = \int_{\Omega_{2}} \sum_{k=1}^n 1_{A_{k}} 
 \, p(\omega_{1}, d\omega_{2})$$
So
$$
\begin{align}
\mu(G_{n}) &= \int_{\Omega_{1}} \int_{\Omega_{2}} \sum_{k=1}^n 1_{A_{k}} 
 \, p(\omega_{1}, d\omega_{2}) \, d\mu_{1}(\omega_{1}) \\
&= \sum_{k=1}^n \int_{\Omega_{1}} \int_{\Omega_{2}} 1_{A_{k}}  \, p(\omega_{1}, d\omega_{2}) \, d\mu(\omega_{1})
\end{align}
$$
But this is
$$
\mu(G_{n}) = \sum_{k=1}^n \mu(A_{k})
$$
Since $G_{n} \uparrow A$, the indicators also have $1_{G_{n}} \uparrow 1_{A}$, hence by the [[Monotone Convergence Theorem]]
$$
\sum_{k=1}^\infty \mu(A_{k}) = \lim_{n \to \infty} \mu (G_{n}) = \int_{\Omega_{1}} \int _{\Omega_{2}} 1_{A} \, p(\omega_{1}, d\omega_{2}) \, d\mu(\omega_{1}) = \mu(A)
$$
Hence $\mu$ is a probability measure.

## (iii) *incomplete*

Consider the algebra of subsets
$$
\mathcal{A} = \{G_{n} \times \prod_{k>n} \Omega_{k} : n \geq 1, G_{n} \in \mathcal{F}_{(n)}\}
$$
Let $\Gamma_{n} = G_{n} \times \prod_{k>n}\Omega_{k}$. 

Now define $\mu : \mathcal{A} \to [0,1]$ by 
$$
\mu\left( \Gamma_{n}\right) = \int_{\Omega_{1}} \dots \int_{\Omega_{n}} 1_{G_{n}}(\omega_{1}\dots \omega_{n}) p(\omega_{1}, \omega_{2}, \dots, d\omega_{n})p(\omega_{1}, \omega_{2}, \dots, d\omega_{n-1}) \dots d\mu(\omega_{1})
$$
It is clear that $\mu$ is finitely additive by linearity of the integral. 

It remains to show that it is also countably additive, or equivalently showing that for any $\Gamma_{n} \in \mathcal{A}, \Gamma_{n} \downarrow \phi \implies \lim_{n \to \infty} \mu(\Gamma_{n}) = 0$.

Suppose on the contrary that $\mu(\Gamma_{n}) \geq \varepsilon >0$ for any $n$. We want to show that there exists a point in $\omega' \in \bigcap_{n}\Gamma_{n}$. Consider for a fixed $\omega_{1}$ the function
$$
\phi_{1,n}(\omega_{1}) = \int_{\Omega_{2}} \dots \int_{\Omega_{n}} 1_{G_{n}}p(\omega_{1}, \omega_{2}, \dots, d\omega_{n})p(\omega_{1},\omega_{2}, \dots, d\omega_{n-1}) \dots p(\omega_{1}, d\omega_{2})
$$
Now as $p(\omega_{1}, \dots, d\omega_{k})$ is a probability measure on $\mathcal{F}_{(k-1)}$ for all $k$, the following
$$
\phi_{1, n +1}(\omega_{1}) = \int_{\Omega_{2}} \dots \int_{\Omega_{n}} \int_{\Omega_{n+1}} 1_{G_{n}}p(\omega_{1}, \omega_{2}, \dots, d\omega_{n+1})\dots
$$
must have the property that $\phi_{1,n+1}(\omega_{1}) \leq \phi_{1,n}(\omega_{1}) \leq 1$.



# Q4

## (i)

Let $X_{n}$ be a sequence of i.i.d standard normal random variables.
$$
\begin{align}
P(X_{1} > x) &= \int_{x}^\infty \frac{1}{\sqrt{ 2\pi }} e^{-\frac{t^2}{2}} dt \\
&= \int_{0}^ \infty  \frac{1}{\sqrt{ 2\pi }} e^{-\frac{(x+t)^2}{2}} dt \\
&\leq \int_{0}^ \infty  \frac{1}{\sqrt{ 2\pi }} e^{-\frac{x^2+t^2}{2}}dt \\
&= e^{-\frac{x^2}{2}} \int_{0}^\infty  \frac{1}{\sqrt{ 2\pi }} e^{-\frac{t^2}{2}}dt \\
&= \frac{1}{2}e^{-\frac{x^2}{2}} \leq e^{-\frac{x^2}{2}}
\end{align}
$$
as required.

## (ii)

Now notice that using the result from (i) we have that
$$
\begin{align}
P\left( \frac{X_{m}}{\sqrt{ 2\log m }} > 1 \right)  &= P(X_{m} > \sqrt{ 2\log m }) \\
&\leq e^{-\frac{2\log m}{2}} = e^{-\log m} = \frac{1}{m}
\end{align}
$$
Hence $P\left( \frac{X_{m}}{\sqrt{ 2\log m }} \leq 1 \right) \geq 1 - \frac{1}{m}$. So we have
$$
\sum_{m=0}^\infty P\left( \frac{X_{m}}{\sqrt{ 2\log m }} \leq 1 \right) = \sum_{m=0}^\infty 1 - \frac{1}{m} = \infty
$$
Since the $X_{m}$ are independent, by the second Borel-Cantelli Lemma, 
$$
P\left( \frac{X_{m}}{\sqrt{ 2\log m }} \leq 1 \text{   i.o} \right) =1
$$
Which in turn implies that $L = \overline{\lim_{n \to \infty}} \frac{X_{n}}{\sqrt{ 2\log n }} \leq 1$ almost surely

## (iii)

First note that over $t \in [x, \infty)$ we have that $\frac{t}{x} \geq 1$. Hence
$$
\begin{align}
\int_{x}^\infty e^{-t^2/2}dt & \geq \int_{x}^\infty \frac{t}{x} e^{-t^2/2}dt \\
&= \frac{1}{x} \int_{x}^\infty te^{-t^2/2}dt \\
&= \frac{1}{x} e^{-x^2/2} \\
&\geq \frac{1}{\frac{1}{x}+ x}e^{-x^2/2} \\
&= \frac{x}{1+x^2}e^{-x^2/2}
\end{align}
$$
as required.

Now we want to show that $L = \limsup_{n \to \infty} \frac{X_{n}}{\sqrt{ 2\log n }} \geq 1$ almost surely. Let $A_{n} = \left\{ \frac{X_{n}}{\sqrt{ 2\log n }} \right\}$We know that
$$
\limsup_{n \to \infty} \left\{ \frac{X_{n}}{\sqrt{ 2\log n }} \geq 1 \right\} \subseteq \left\{ \frac{X_{n}}{\sqrt{ 2\log n }} \geq 1 \right\}  
$$
Hence it suffices to show that $P(A_{n} \text{ i.o}) = 1$.

From the result above we have that
$$
\begin{align}
P (A_{n}) = P\left( \frac{X_{n}}{\sqrt{ 2\log n }} \geq 1 \right) &= P(X_{n} \geq \sqrt{ 2\log n }) \\
&\geq \frac{\sqrt{ 2\log n }}{1+2\log n} \frac{1}{n} \\
&\geq \frac{1}{3 n\log n}
\end{align}
$$
So
$$
\sum_{n} P(A_{n}) \geq \sum_{n} \frac{1}{3n \log n} = \infty
$$
Since each $X_{n}$ are independent, by the [[Borel-Cantelli Lemma#2nd Lemma|second Borel Cantelli Lemma]], $P(A_{n} \text{ i.o}) = 1$. Hence $L \geq 1$ almost surely. 

We conclude using the result from $(ii)$ that $L=1$ almost surely.

## (iv)

We want to show that 
$$
P(|S_{n}| \le 2\sqrt{ n\log n } \text{ eventually}) = 1
$$
Taking complement this is equivalent to showing that
$$
P(|S_{n}| > 2\sqrt{ n\log n } \text{ i.o}) = 0
$$
Let $A_{n} = \left\{ |S_{n}| > 2\sqrt{ n\log n } \right\} = \left\{ \frac{|S_{n}|}{\sqrt{2 \log n }} > \sqrt{ 2n} \right\}$.

By the Markov Inequaltiy,
$$
P(A_{n}) = P(|S_{n}| > 2\sqrt{ n\log n }) \leq \frac{E[S_{n}^4]}{16 n^2 \log^2 n}
$$
Now consider
$$
E[S_{n}^4] = E\left[ (X_{1}+X_{2}+ \dots + X_{n})^4 \right] 
$$
Since $X_{n}$ are independent, the mixed moments $E[X_{j}^k X_{i}^{4-k}] = 0$ for $j \neq i$. Hence
$$
E[S_{n}^4]  = E[X_{1}^4] + \dots + E[X_{n}^4] =n E[X_{1}^4] = O(n)
$$
Hence
$$
\sum_{n=0}^\infty P(A_{n}) \leq \sum_{n=0}^\infty \frac{E[S_{n}^4]}{16 n^2 \log^2 n} = K \sum_{n = 0}^\infty \frac{1}{n\log^2n}  <\infty
$$
Hence $P(A_{n} \text{ i.o}) = P(|S_{n}| > 2 \sqrt{ n\log n } \text{ i.o}) = 0$.

Since $P(|S_{n}| \le 2\sqrt{ n\log n } \text{ eventually}) = 1$ for large enough $n$ we have
$$
-\frac{2\sqrt{ n\log n }}{n} \leq \frac{S_{n}}{n} \leq \frac{2\sqrt{ n\log n }}{n} = 2\sqrt{ \frac{\log n}{n} }
$$
Taking $n \to \infty$ we have
$$
\frac{S_{n}}{n} \to 0 \text{ a.s}
$$

## (v)

Let $M_{n} = \max_{n} |X_{n}|$. By Jensen's inequality we have
$$
\begin{align}
\mathbb{E}M_{n} &= \log \exp \mathbb{E}M_{n} \\
&\leq \log  \mathbb{E} e^ {M_{n}} \\
&= \log \mathbb{E} e^{\max_{n} |X_{n}|} \\
& \leq \log \mathbb{E} \max_{n} e^{|X_{n}|} \\
&\leq \log \sum_{k=1}^n \mathbb{E}e^{|X_{k}|} \\
&= \log n \mathbb{E}e^{|X_{1}|} &\text{since $X_{i}$ are iid}\\
&= \log n + \log \mathbb{E}e^{|X_{1}|}\\
\frac{\mathbb{E}M_{n}}{\sqrt{ \log n }} &\leq \sqrt{ \log n } + \frac{1}{\sqrt{ \log n }} \log \mathbb{E}e^{|X_{1}|}
\end{align}
$$
Now note that for any $t>0$,
$$
\begin{align}
\mathbb{E}tM_{n} &= \mathbb{E}t \max_{k \leq n} |X_{k}| =\mathbb{E} \max_{k \leq n} |t X_{k}| 
\end{align}
$$
So
$$
\mathbb{E}M_{n} \leq \sqrt{ \log n } + \frac{1}{\sqrt{ \log n }} \log \mathbb{E}e^{|X_{1}|/\sqrt{ \log n }}
$$
Now as $n \to \infty$, $\frac{|X_{1}|}{\sqrt{ \log n }} \xrightarrow{a.s} 0$. Since $e^{|X_{1}|/\sqrt{ \log n }}$ is clearly bounded by $e^{|X_{1}|}$ which is integrable, by the dominated convergence theorem we have $\lim_{n \to \infty}\log \mathbb{E} e^{|X_{1}|/\sqrt{ \log n }} = \log \mathbb{E}e^0 = 0$. Hence we clearly have that
$$
\frac{\log \mathbb{E} e^{|X_{1}| / \sqrt{ \log n }}}{\sqrt{ \log n }} = O(1)
$$
 So
$$
\mathbb{E}M_{n} \leq \sqrt{ \log n } + O(1)
$$
Hence there exists $M >0$ such that
$$
\mathbb{E}M_{n} \leq M \sqrt{ \log n }
$$

$$
\begin{align}
\mathbb{E}e^{|X_{1}|\sqrt{ \log n }} &= \int_{-\infty}^\infty e^{|x|\sqrt{ \log n }} e^{-x^2/2} \,dx \\
&= \int_{-\infty}^0 e^{-x\sqrt{ \log n }} e^{-x^2/2} \, dx + \int_{0}^\infty e^{x\sqrt{ \log n }} e^{-x^2/2} \, dx \\
&= e^{\frac{1}{2}\log n}\int_{-\infty}^0 e^{-\frac{1}{2}(x+\sqrt{ \log n })^2} \, dx +e^{\frac{1}{2}\log n}\int_{0}^\infty e^{-\frac{1}{2}(x-\sqrt{ \log n })^2} \,dx \\
&\leq 2e^{\frac{1}{2}\log n}
\end{align}
$$
So
$$
\begin{align}
\mathbb{E}M_{n} &\leq \sqrt{ \log n } + \frac{1}{\sqrt{ \log n }} \log \left( 2e^{\frac{1}{2}\log n} \right)  \\
&= \sqrt{ \log n } + 1 + \frac{\log(2)}{\sqrt{ \log n }}  \\
&\leq 3\sqrt{ \log n }
\end{align}
$$

