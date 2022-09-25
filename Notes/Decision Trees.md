## Definition

A 'tree' consists of a set of nested decision rules, where at each node $i$ the feature dimension of the input is compared to a threshold value and passed down to the left or right branch, depending on whether it is above or below the threshold.

We associate the output of the node as the average of all output that fall upon that node, i.e for a given decision boundary region $R_i$.

more formally,

$$
w_i = \frac{\sum_{n=1}^N y_n I(x_n \in R_i)}{\sum_{n=1}^N I(x_n \in R_i)}
$$

and the tree is defined by the piecewise function

$$
f(x;\theta) = \sum{j=1}^J w_j I(x\in R_j)
$$

where $J$ is the number of regions formed by the decision tree. If the tree is a balanced binary tree, $J = O(log(N))$.

![[Pasted image 20220228193046.png]]

## Fitting

Because of the discrete tree structure, the loss function is not differentiable. Instead we iteratively grow the tree one node at a time in a greedy approach.

At each node we check the possible set of decision boundaries by considering the value of a cost function on the tree we've constructed so far plus the newly added split.
- for regression we can use MSE
- for classification we can use the [[Gini Index]] after computing the empirical distribution of the class labels at the node


## Advantages and Disadvantages

Advantages
- easy to interpret
- fast to fit
- robust to outliers
- can handle missing input features

Disadvantages
- easy to overfit (especially if we le tthe tree grow)
- unstable - small changes to input can have large effects on the tree
- poorer accuracy due to greedy nature of tree construction


