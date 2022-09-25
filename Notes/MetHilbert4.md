**Goal** - build $\mathbb{R}_{\geq_{0}}$

### What is $\mathbb{R}_{\geq 0}$?

Really just decimal expansions -
$$
\mathbb{R}_{\geq 0} = \{z.d_{1}d_{2}\dots : d_{i}\in \{0,1,2,3,\dots\}\}
$$
with $z.9999999\dots = (z+1).00000$

### Constructing $\mathbb{Q}_{\geq_{0}}$?
$$
\mathbb{Q}_{\geq_{0}} = \{\frac{r}{s} : r,s \in \mathbb{Z}_{\geq_{0}} , s\neq 0\}
$$
with $\frac{r}{s} = \frac{p}{q}$ if $rq=sp$ 

Define addition $\mathbb{Q}_{\geq_{0}} \times \mathbb{Q}_{\geq_{0}} \rightarrow \mathbb{Q}_{\geq_{0}}$ by
$$
\frac{r_{1}}{s_{1}} + \frac{r_{2}}{s_{2}} = \frac{r_{1}s_{2} + s_{1}r_{2}}{s_{1}s_{2}}
$$
Define multiplication $\mathbb{Q}_{\geq_{0}} \times \mathbb{Q}_{\geq_{0}} \rightarrow \mathbb{Q}_{\geq_{0}}$ by
$$
\frac{r_{1}}{s_{1}} \frac{r_{2}}{s_{2}} = \frac{r_{1}r_{2}}{s_{1}s_{2}}
$$
Define an **order** on $\mathbb{Q}_{\geq_{0}}$ by $x\leq y$ if there exists $z \in \mathbb{Q}_{\geq_{0}}$ such that $x+z=y$.

Define the absolute value $|\cdot| : \mathbb{Q}_{\geq_{0}} \rightarrow \mathbb{Q}_{\geq_{0}}$ by $|x| = x$

## The Completion $\hat{\mathbb{Q}}_{\geq_{0}}$

This is the set of Cauchy sequences in $\mathbb{Q}_{\geq_{0}}$

