# Defintion ([[Metric Space]])

Let $(X, d_{x})$ and $(Y, d_{y})$ be [[Metric Space]].

Let $f: X \to Y$ be a function. We say that $f$ is **uniformly** continuous if for any $\varepsilon>0$, there exists $\delta >0$ such that for all $x \in X$ and $y \in Y$, $d_{x}(x,y) < \delta \implies d_{y}(f(x), f(y)) < \varepsilon$.

This differs from [[Continuous#Definition Metric Space]] where the $x$ is at the beginning, which means that $\delta$ can depend on $x$ as well. Whereas here we only need to choose one $\delta$ given $\varepsilon$ for all $x \in X$. Obviously uniform continuity also implies continuity but not the other way around (e.g $\frac{1}{x}$, $x^2$, $e^x$).

The intuition is that $f$ cannot "increase too fast".

## Examples of Fuctions that are Continuous But not Uniformly Continuous

- $e^x$
- $\frac{1}{x}$
- $x^n$ for $n>1$

# Definition ([[Uniform Space]])

Let $(X, \mathcal{E}_{X}), (Y, \mathcal{E}_{Y})$ be [[Uniform Space]].

Just like how we have pre-images of open sets of [[Continuous]] functions being open sets, we have that $f$ is uniformly continuous if
$$
E \in \mathcal{E}_{Y} \implies (f \times f)^{-1}(E) \in \mathcal{E}_{X}
$$
where 
$$
(f \times f)^{-1}(E) = \left\{ (a,b) \in X \times X : (f(a), f(b)) \in E \right\} 
$$
## Alternative Characterisation

If $E \in \mathcal{E}_{Y}$ then there exists $D \in \mathcal{E}_{X}$ such that if $x \in X$ and $a \in X$ then $(a,x) \in D \implies (f(a), f(x)) \in E$.