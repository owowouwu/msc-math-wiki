In [[Multilayer Perceptron]], neurons are fully connected.

Rather than making all neurons connected, we only take a portion of neurons in the previous layer to predict in the next layer. 

Convolutions are defined by a kernel, which is a matrix overlaid on the output which computes an element-wise product of the input. This matrix is shifted along the output matrix.

![[Pasted image 20220513111624.png]]

CNNs are typically used for image recognition.

## Advantages

- more efficient, especially if we only want to recognise a feature of the input.
- preserves spatial relations, i.e we can determine where in the neural network the features are present.
- is a form of regularisation.

## Combining Methods

### Max Pooling

Within a small window of the kernel'soutput map, take the highest output and discard the rest. Adds translation invariance, which makes it so that the network response is the same even if features are in a slightly different position in an image. This allows for reduction in feature space which reduces computational time. 


## Challenges

CNNs can be very sensitive to noise in the data, even if it is small

![[Pasted image 20220513113612.png]]