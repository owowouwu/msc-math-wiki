An extension of [[Nearest Prototype Classification]] that deals with the issue with labels being scattered.

## Problem Statement

Find a hyperplane that separates two classes.

## Hyperplanes

A hyperplane in $\mathbb{R}^d$ can be defined as

$$ \mathbf{w}^T\mathbf{x} - c = 0$$

where $\mathbf{w}$ is the normal vector, $\mathbf{x}\in\mathbb{R}^d = \{x_1, x_2 ...\}$, and $c$ is an intercept.

We classify points into positive or negative classes. Given a new instance $\mathbf{x}'$, if $\mathbf{x}' \cdot \mathbf{w} - c <0$, it is in one class, and vice versa.

## Finding the Optimal Hyperplane

We want to choose a hyperplane that is stable even under pertubations of inputs. Therefore we want our training data to be as far from the training points as possible.

### Margins

A margin is the minimum distance between the boundary $f(\mathbf{x})$ and the data points $\mathcal{D}$. We want to choose $f$ ($\mathbf{w}$) such that the margin is maximised.

### Optimising

Given the features $X$ and labels $y$, we want to optimise the margin subject to 

$$y_i = 1 : f(x_i) = w^Tx_i + b \geq 1$$
$$y_i = -1 : f(x_i) = w^Tx + b \leq -1$$

for $i = 1,\dots, n$. i.e we want to place features on either side of the those lines to guarantee a margin of $\frac{2}{||w||}$. The so called *support vectors* are the points on these lines. 

In practice we minimise $\frac{w^t w}{2}$. 

## Non-linearly Separate Data

### Soft Margins

For data that is not completely linear separable, i.e has a few points scattered

We have a tradeoff between the size of the margins and proper classification.

![[Pasted image 20220331115514.png]]

#### Penalties / Regularisation

For each incorrectly labelled feature we introduce *slack* variables $\xi_i\geq 0$ and the objective to minimise now becomes

$$
\frac{w^T w}{2} + C||\xi||_1
$$

$C$ is a regularisation parameter, like in LASSO regression. Can use Lagrange multipliers to optimise.

The larger $C$ is, the more errors penalise the model.

### Mapping Functions

For non-linear data,

We change the feature space using a transformation or use [[Kernels | kernels]] without explicitly visiting a higher dimensional feature space.

## Multiclass

### One vs All

For each class $c \in C$, train $c$ against $C -\{c\}$

### One vs One

Produce an SVM for each pair and combine the decision boundaries.

This requires $\binom{C}{2}$ fits for each class label $C$.



