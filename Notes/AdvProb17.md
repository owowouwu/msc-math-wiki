# Conditional Expectation

## Intuition

Given $X$ a [[Random Variable]] on $(\Omega, \mathcal{F}, \mathbb{P})$ and $\mathcal{G } \subseteq \mathcal{F}$ sub-sigma-algebras,

How do we define $\mathbb{E}[X | \mathcal{G}]$?

In the extreme cases -

- $\mathcal{G} = \left\{ \phi, \Omega \right\}$, $\mathbb{E}[X | \mathcal{G}] = \mathbb{E}X$ , <- we have no information
- $\mathcal{G} = \mathcal{F}$, $\mathbb{E}[X | \mathcal{G}] = X$ <- we have total information

It is reasonable to expect that in the intermediate cases, the conditional expectation is a $\mathcal{G}$-measurable random variable (we are conditioning on the information $\mathcal{G}$).

### Building More Intuition
#### Conditioning on an Event

Recall also from elementary probability that we have
$$
\mathbb{P}(B|A) = \frac{\mathbb{P}(A \cap B)}{\mathbb{P}(A)}
$$
We can think of this actually as a probability measure $B \mapsto \mathbb{P}(B|A)$ on $\mathcal{F}$. Then
$$
\mathbb{E}[X | A] = \int_{\Omega} X d\mathbb{P}(\cdot | A) = \frac{\mathbb{E}[X 1_{A}]}{\mathbb{P}(A)}
$$
#### Partitions

Now consider a partition $A_{1}, A_{2}, \dots, A_{n}$ of $\Omega$, and let $\mathcal{G} = \sigma(A_{1}, A_{2}, \dots, A_{n})$. If we want to make a random variable that is $\mathcal{G}$-measurable, it has to be in the form
$$
G = \sum_{i=1}^n g_{i} 1_{A_{i}}
$$
Then what is $\mathbb{E}[X | \mathcal{G}]$?
$$
\mathbb{E}[X | \mathcal{G}] = \sum_{i=1}^n \mathbb{E}[X | A_{i}] 1_{A_{i}}
$$
So how do we generalise this?

Consider
$$
\begin{align}
\int_{A_{i}} \mathbb{E}[X|\mathcal{G}] d\mathbb{P} &= \int_{A_{i}} \sum_{j=1}^n c_{j}1_{A_{j}} d\mathbb{P} \\
&= c_{i} \mathbb{P}(A_{i})  \\
&= \frac{\mathbb{E}[X 1_{A_{i}}]}{\mathbb{P}(A_{i})} \mathbb{P}(A_{i})  \\
&= \int_{A_{i}} X d\mathbb{P} 
\end{align}
$$
and now this becomes true for any $A \in \mathcal{G}$ (by additivity). We use this as our characterising property.

## Formal Definition

[[Conditional Expectation]]

