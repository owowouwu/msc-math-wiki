- classification model
- probabilistic model based on training data -> predicts test data
	- given a new input $T$ we choose label based on the max posterior probability over labels (which is given by frequencies of occurences in data)

- problem - needs many observations of values, especially for high dimensional feature sets

## Naive Bayes

Assume the attributes are conditonally independent on the output class.

Task - classify an unseen instance $T$ into a class $c_j \in C$

$$
\hat{c} = \arg \max_{c_j\in C} P(c_j |T)
$$

with a vector instance $T = (x_1,x_2, \dots)$,  since we asusme conditional independence

$$
P(T|c_j) = \prod_i P(x_i | c_j)
$$

then

$$
\hat{c} = \arg \max_{c_j \in C} P(c_j)\prod_i P(x_i | c_j)
$$

### Computing Prior

$P(c_j)$ and $P(x_i|c_j)$ can be calculated based on the frequencies of classes (empirical dist)

### Zero Values

if we have unobserved values the probabilities will be 0

solution - observe more data, smoothing

#### Smoothing

- replace 0 probablities with a small number $\epsilon >0$, mustbe less than smallest conditional probability
- may need to normalise the probabilities

#### Laplace Smoothing

Increase all counts by 1 (or more generally by some $\alpha>0$)

### Why do assumptions not matter?

- we are only interested in the ranks of the posteriors not the actual estimates
- so even if some attributes are correlated it doesn't matter because it may change probabilities but not rank

### Strengths Weaknesses

- simple fast, interpretable


- inaccurate when data sparse
- assumption becomes problematic for more complex systems,




