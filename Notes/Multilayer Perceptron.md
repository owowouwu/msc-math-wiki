An extension of the [[Perceptron]] to build a larger [[Neural Networks]].

## Layers

Layers are a group of neurons working in parallel on the same input.

In multilayer perceptron (MLP) we have 

- an input layer
- at least one hidden layer, which receives the previous layer's output as its input
- an output layer which receives input from a hidden layer and outputs the class label

### Hidden Layer

Hidden layers effectively learning intermediate features that are useful for the output layer. These are often difficult to interpret.

## Choosing Number of Neurons and Layers

Depends on the problem, but generally choose a number between the number of features and outputs.

## Backpropagation

How do we deal with the following issues - 

- Gradient descent is a greedy method that can converge to local minima.
- How can we train the hidden layers effectively?

Idea - compute the gradient of loss for a single layer at a time, then iterate backward from the last hidden layer to avoid calculations of immediate terms in the chain rule.


