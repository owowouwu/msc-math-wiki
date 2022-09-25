# [[Compact]]

## Counterexamples

### [[Closed]] does not Imply [[Complete]] (Cauchy Compact)

Let $X = \mathbb{R}_{(0,1)}$ and $A = X$. Then $A = X$ so $A$ is closed. But $a_{n} = \frac{1}{n}$ is Cauchy but $0 \notin X$ so $a_{n}$ does not converge in $A$.

### Cauchy Compact does not Imply [[Sequentially Compact]]

Let $X = \mathbb{R}$ and $A = \mathbb{R}$ with the standard metric. We know $\mathbb{R}$ is [[Complete]]. But on the other hand we see that if we let $a_{n}= n$ this sequence has no cluster point.

### [[Bounded]] does not Imply [[Ball Compact]]

Let $X = \mathbb{R}$ with the metrix
$$
d_{X}(x,y) = \min \left\{ |y-x| ,1\right\} 
$$
Let $A = X$. Then $A \subseteq B_{2}(0)$ so $A$ is bounded. But $A$ is not covered by a finite number of balls of radius $\frac{1}{10}$.

### [[Ball Compact]] does not imply [[Cover Compact]].

Let $X = \mathbb{R}$ and $A = \mathbb{R}_{(0,1)}$. $A$ is not closed and bounded so $A$ is not compact by Heine-Borel. But $A$ is certainly ball compact.