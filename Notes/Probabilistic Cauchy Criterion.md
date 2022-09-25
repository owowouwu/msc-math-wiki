# Motivation

Recall that since $\mathbb{R}$ is a [[Complete]] [[Metric Space]], we know that if a sequence in $\mathbb{R}$ is Cauchy then it converges. We can use this to create a definition for convergence of random variables.

# Statement

Recall that we say that a sequence of real numbers $X_{1}, X_{2}, \dots$ converges almost surely if for any $\varepsilon>0$, there exists $k \in \mathbb{Z}_{\geq 0}$ such that if $r,s \geq k$, then $|X_{r} - X_{s}| < \varepsilon$. 

Probabilistically, "for all/any" turns into $\bigcap$ while "exists" turns into $\bigcup$. We can hence rewrite the above as the event
$$
 \bigcap_{\varepsilon \in \mathbb{Q}} \bigcup_{k >0} \bigcap_{r,s \geq k}  \left\{ |X_{r} - X_{s}| < \varepsilon \right\}
$$
Note that we need to make sure $\varepsilon$ is in a countable set here. Equivalently we may have something like
$$
\bigcap_{d \in \mathbb{Z}}\bigcup_{k >0}\bigcap_{r,s \geq k}\left\{ |X_{r} - X_{s}| < 10^{-d} \right\} 
$$
So the **probabilistic Cauchy criterion** is as follows - 
$$
X_{n} \text{ converges almost surely} \iff \mathbb{P}\left(  \bigcap_{\varepsilon \in \mathbb{Q}} \bigcup_{k >0} \bigcap_{r,s \geq k}  \left\{ |X_{r} - X_{s}| < \varepsilon \right\} \right) =1
$$
