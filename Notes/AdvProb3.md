## Using Caratheodory

[[Caratheodory Extension Theorem]]

How do we justify countable additivity and use the theorem?

**Prop** Let $\mathcal{A}$ be an algebra over $\Omega$. Let $\mu : \mathcal{A} \rightarrow [0, \infty]$ satisfy $\mu(\phi) = 0$ and finite additivity. Suppose one of the following conditions hold true:

1. $A_{n} \in \mathcal{A}, A_{n} \downarrow \phi \implies \mu(A_{n}) = 0$ (continuity at the empty set)
2. $A, A_{n} \in \mathcal{A}, A \subseteq \bigcup A_{n} \implies \mu(A) \leq \sum_{n=1}^\infty \mu(A_{n})$ (countable subadditivity)

Then $\mu$ is countably additive on $\mathcal{A}$

**Proof**
Let $A_{n}$ be a disjoint sequence in $\mathcal{A}$. 

#### 1. 
Denote $B_{n} = \bigcup_{k=1}^n A_{k}$. We know from finite additivity that $\mu(A) = \mu(B_{n}) + \mu(A\backslash B_{n}) = \sum_{k=1}^n \mu(A_{k}) + \mu(A\backslash B_{n})$.

Note that $A\backslash B_{n}\downarrow \phi$. So $\mu(A\backslash B_{n})\rightarrow 0$. Which gives $\mu(A) = \sum_{k=1}^\infty \mu(A_{k})$.

#### 2.
We have 

$$
\sum_{k=1}^n \mu(A_{n}) = \mu(B_{n}) \leq \mu(A) \leq \sum_{n=1}^\infty \mu(A_{n})
$$
Taking $n\rightarrow \infty$ we have 
$$
\mu(A) = \sum_{n=1}^\infty \mu(A_{n})
$$

**Example** (Lebesgue Measure)

Let $\Omega = \mathbb{R}$. Consider the algebra - 
$$
\mathcal{A}\left( \{(a,b] : -\infty\leq a<b \leq \infty\} \right)
$$

this is just the finite disjoint unions of intervals of the form $(-\infty, a], (a,b], (b, \infty)$. 

Now define
$$
\mu:\mathcal{A} \rightarrow [0, \infty]
$$
- $\mu((a,b]) = b-a$ 
- $\mu((-\infty, a]) = \mu((b, \infty)) = \infty$

Now extend $\mu$ to $\mathcal{A}$ by finite additivity.

## Random Variables and Integration

[[Random Variable]]

to deal with expectations,

Let $X$ be a [[Random Variable]] on $(\Omega, \mathcal{F}, P)$

1. $X$ is simple i.e a linear combination of indicators
$$
X = \sum_{k=1}^n c_{k}1_{A_{k}}
$$
then
$$
\int X \, dP = \sum_{k=1}^n c_{k}P(A_{k})
$$
2. $X\geq 0$. $\exists X_{n}$ simple such that $0\leq X_{n} \uparrow X$
We take the limit
$$
\int X \, dP = \lim_{n\rightarrow \infty} \int X_{n} \, dP   
$$
3. If $X$ is general we define $X = X^+ X^-$, and use the positive case above
$$
\int X \, dP = \int X^+ \, dP + \int X^- \, dP  
$$
We write that $X$ is integrable, or $X \in L^1$.
