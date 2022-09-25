# [[Cramer's Theorem#Proof]]

## Proving the Lemma

How to prove $$
\liminf \frac{1}{n}\log \mathbb{P} (\overline{S}_{n} \in (-\delta, \delta)) \geq \inf_{\lambda \in \mathbb{R}} \Lambda(\lambda)
$$
Assume $\mathbb{P}(X_{1} >0) >0$ and $\mathbb{P}(X_{1} < 0) >0$ and $\Lambda(\lambda)$ is finite for all $\lambda$.

The first assumption implies that
$$
\lim_{\lambda \to \pm \infty} \Lambda(\lambda) = \lim_{\lambda \to \pm \infty}\log \mathbb{E}[e^{\lambda X_{1}}]  =\infty
$$
Given this there exists an $\eta \in \mathbb{R}$ such that $\Lambda'(\eta) =0$. (there is a global maximum, think about $x^2$)

$$
0=\Lambda'(\eta) = \frac{M'(\eta)}{M(\eta)} = \int_{\mathbb{R}} xe^{\eta x - \Lambda(\eta)} \mu(dx) 
$$
Let $\mu$ be the [[Probability Law]] of $X_{1}$. The idea is to apply a change of measure to $\nu$ s.t $\int_{\mathbb{R}} X d\nu=0$.

Define the [[Density]]
$$
\nu(dx) = e^{\eta x - \Lambda(\eta)} \mu(dx)
$$
This means that given any $A \in \mathcal{B}(\mathbb{R})$,
$$
\nu(A) = \int_{A} e^{\eta x - \Lambda \eta} \mu(dx)
$$
How does this help? We define a new sequence $Y_{n}$ i.i.d such that $X_{1} \sim \nu$. Fix $\delta >0$. For $\varepsilon < \delta$, using the [[Product Measures]]
$$
\begin{align}
\mathbb{P}(\overline{S}^X_{n} \in (-\delta , \delta)) &\geq \mathbb{P}(\overline{S}^X_{n} \in (-\varepsilon, \varepsilon)) \\
&=\int_{A(n, \varepsilon)} \mu(dx_{1})\dots \mu(dx_{n}) \\
&=\int_{A(n, \varepsilon)} e^{-n(\eta\overline{x} + \Lambda(\eta))}\nu(dx_{1})\dots \nu(dx_{n})
\end{align}
$$
Where $A(n, \varepsilon) = \left\{ S_{n}^X \in (-\varepsilon, \varepsilon) \right\}$. Now
$$
\left| \frac{x_{1} + \dots + x_{n}}{n} \right| < \varepsilon \implies \left| \eta(x_{1}+\dots+x_{n}) \right| < |\eta| n\varepsilon
$$
So $e^{-\eta(n\overline{x})} \geq e^{-n |\eta| \varepsilon}$. So
$$
\begin{align}
\mathbb{P}(\overline{S}_{n}^X \in (-\delta, \delta)) &\geq \int_{A(n, \varepsilon)} e^{-n|\eta| \varepsilon + n \Lambda(\eta)} \nu(dx_{1}) \dots \mu(dx_{n}) \\
&= e^{-n\varepsilon|\eta| + n\Lambda(\eta)} \mathbb{P}(\overline{S}_{n}^Y \in (-\varepsilon, \varepsilon))
\end{align}
$$
So 
$$
\frac{1}{n} \log \mathbb{P}(\overline{S}^X_{n} \in (-\delta, \delta)) \geq -\varepsilon|\eta| + \Lambda(\eta) + \frac{1}{n}\log \mathbb{P}(\overline{S}_{n}^Y \in (-\varepsilon, \varepsilon))
$$
From the [[Strong Law of Large Numbers]], 
$$
\mathbb{P}(\overline{S}_{n}^Y \in (-\varepsilon, \varepsilon)) \xrightarrow{p} 1
$$
Since $\mathbb{E}Y_{1} = 0$ (this is why we perform the change of measure)

So we have
$$
\liminf \frac{1}{n} \log \mathbb{P}(\overline{S}_{n}^X \in (-\delta, \delta)) \geq - \varepsilon |\eta| + \Lambda(\eta) \geq -\varepsilon |\eta| + \inf_{\lambda \in \mathbb{R}} \Lambda(\lambda)
$$

## Example Usage of Large Deviation Principle

Suppose $X_{n} \sim N(0,1)$. We have $\overline{S}_{n} \sim N\left( 0, \frac{1}{n} \right)$. Recall that $\Lambda^*(x) = \frac{x^2}{2}$. Let $I = [a,b]$, where $a >0$. We want to estimate $\mathbb{P}(\overline{S}_{n} \in I) = \int_{a}^b \frac{\sqrt{ n }}{\sqrt{ 2\pi }}e^{-nx^2/2} \,dx$. We can get a bound by
$$
\frac{1}{n} \mathbb{P}(\overline{S}_{n} \in I) \leq \frac{1}{n} \log\left( \frac{\sqrt{ n }(b-a)}{\sqrt{ 2\pi }} \right) - \frac{a^2}{2} 
$$
So 
$$
\limsup \frac{1}{n} \log \mathbb{P}(\overline{S}_{n} \in I) \leq -\frac{a^2}{2} = - \Lambda^*(a) = -\inf_{x \in I} \Lambda^*(a)
$$

# Introduction to Martingales

Assume $X_{n}$ is independent with $\mathbb{E}X_{n} = 0$. Let $S_{n}= X_{1} + \dots + X_{n}$. Let 
$$
\mathcal{F}_{n} = \sigma(X_{1}, \dots, X_{n})
$$
Given this, 
$$
\mathbb{E}[S_{n+1} |\mathcal{F}_{n}] = S_{n} + \mathbb{E}X_{n+1} = S_{n}
$$
So we have the property that
$$
\mathbb{E}[S_{n+1}| \mathcal{F_{n}}] = S_{n}
$$
which is the Martingale property.
