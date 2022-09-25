# Number Systems

## Formal Power Series
$$
\mathbb{Q}[[t]] = \left\{ a_{0} + a_{1}t + a_{2}t^2 +\dots : a_{n} \in \mathbb{Q} \right\} 
$$
## Laurel Series
$$
\mathbb{Q}((t)) = \left\{ a_{-l}t^{-l} +a_{-l+1}t^{-l+1}+ \dots : l \in \mathbb{Z}, a_{n} \in \mathbb{Q} \right\} 
$$
## Polynomials
$$
\mathbb{Q}[t] = \left\{ \text{polynomials with rational coefficients} \right\} 
$$

# Defining [[Metric Space|Metrics]]?

For the Laurel Series, define $d: \mathbb{Q}((t)) \times \mathbb{Q}((t)) \to \mathbb{R}_{\geq 0}$ by
$$
d(x,y) = 10^{-\mathrm{val}_{t}(x,y)}
$$
where$$
\mathrm{val}_{t}(a_{l}t^l + \dots) = l \text{ if $l$ is minimal s.t $a_{l} \neq 0$}
$$ i.e we take the minimal powers and take the difference between that as a metric.

# [[p-adic Numbers]]

## Defining Reals Using p-adic Numbers
$$
\mathbb{R}_{\geq 0} = \left\{ a_{-l}\left( \frac{1}{10} \right)^{-l} + a_{-l+1} \left( \frac{1}{10} \right)^{-l+1} + \dots : l \in \mathbb{Z}, a_{l} \in \mathbb{Z} / 10\mathbb{Z} \right\} 
$$
this is just decimal expansions.
$$
\mathbb{Z}_{\geq 0} = \left\{ a_{-l} \left( \frac{1}{10} \right)^{-l} + \dots + 10a_{1} + a_{0}: l \in \mathbb{Z}_{>0}, a_{l} \in \mathbb{Z} / 10\mathbb{Z} \right\} 
$$
We can similarly define metrics using the $\mathrm{val}$ function.

We can define the [[m-adic Topology]] and [[m-adic Uniformity]].
