Form of dimensionality reduction in which we project the higher dimensional data $x \in \mathbb{R}^D$ to a subspace $\mathbb{R}^L$ $L<D$ such that the lower dimensional subspace is still a good approximation in the data.

A good approximation in the sense that, taking $W$ to be the projection matrix, the below

$$ \mathcal{L}(W,Z) := \frac{1}{N}\sum|| X - W^T Z ||^2 =  $$

is small. This is called the *reconstruction error* as we are effectively project $z = Wx$, and then constructing back an estimate for $x = W^T W x$, and we would like this error to be small.

We want to minimise the above under the constrant that $W$ is [[Orthogonal Matrices | orthogonal]].

We set 

$W = U_L$

where $U_L$ contains the $L$ eigenvectors associated with the largest eigenvalue of the empirical covariance matrix

$$\hat{\Sigma}=\sum_{n=1}^N (x_n - \bar{x})(x_n - \bar{x})^T$$

