In [[Naive Bayes]], we want to choose a class that maximises the posterior probability

$$
p(c_j | x_i) \propto p(c_j)\prod_i p(x_i|c_j)
$$

in the continuous case this is not valid, but we instead compute its probability density. Distribution different -> different class. We choose the label of the output based on the highest probability density computed.

In the Gaussian case, we estimate the mean and variance as the sample mean and sample variance.

