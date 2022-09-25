A [[Sequential Monte Carlo]] method in which weights and samples are assigned as follows - 

We take some distribution $\pi(x | y)$ we can sample from, and define the weights as

$$
w(x_{0:t}) = \frac{p(x_{0:t} | y_{1:t})}{\pi(x_{0:t} | y_{1:t})}
$$

we sample particles from $pi$ and assign them the weights as calculated. We do this in an iterative process where at time $1$, we sample from $\pi(x_1|y_1)$, then resample according to the approximation using $w$ to get a new empirical distribution based on the number of times a value is sampled (bootstrap filtering).

we can then compute sequentially the weights as well as importance sampling distribution

$$
\pi(x_{0:t}|y_{1:t}) = \pi(x_0)\prod_{k=1}^t \pi(x_k | x{0:k-1}, y_{1:k})
$$

$$
w_t \propto w_{t-1}\frac{p(y_t|x_t)p(x_t|x_{t-1})}{\pi(x_t|x_{0:t-1},y_{1:t})}
$$

and we use empirical distribution from the previous step for samples of $x$.

