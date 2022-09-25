Given a feature $X$ and class label $C$,

$$
PMI = \log_2 \frac{p(x,c)}{p(x)p(c)}
$$

This gives a value in $\mathbb{R}$, with $0$ meaning $X$ and $c$ are independent, and the higher the magnitude the more correlated the features are.