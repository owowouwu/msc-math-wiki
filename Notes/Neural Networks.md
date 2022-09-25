At each layer in the neural network, 

The form of an output to neuron given the input neurons $x_i$ are

$$
f(\mathbf{w}\cdot \mathbf{x}_i + b)
$$

where $b$ is some bias term.

Neural networks train by finding the weights $w$ which minimise errors (e.g  $\ell_2$ error) in the training data. This is done iteratively, and each iteration over the whole dataset is called an epoch. 

A general method for doing this is using gradient descent algorithms

![[Pasted image 20220513103557.png]]

### Universal Approximation Theorem

Neural networks are effective because they are able to approximate any continuous function on $\mathbb{R}$.

Can learn any basis function.