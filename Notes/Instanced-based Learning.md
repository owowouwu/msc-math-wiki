- store labelled examples in memory (also called *memory-based learning*)
- no model being built, just use training instances as they are
	- comparison done based on similarities rather than some input -> output $y=Ax$


## Similarities

Using feature vectors, we can define similarities/distance between them e.g

- Euclidean distance $||v_1 - v_2||$
- $l^1$ norm (Manhattan distance) 
- Cosine similarity $v_1 \cdot v_2 / ||v_1|| ||v_2||$
	- has the advantage of being normalised i.e does not care about magnitudes of vectors

### Dealing with Categorical RVs

above methods deal with continuous data, need different way to deal with categorical data

![[Pasted image 20220324154043.png]]

## Nearest Neighbour Classification

idea - instances similar in the feature space are more likely to have the same label

use labels of $k$ nearest neighbours to predict a label for the test instance

strengths - simple, no model required, incremental (no need to rebuild the model if new instances arrive)
weaknesses - $K$ is quite arbitrary, requires a useful metric, issues with high dimensionality, lazy

### Choosing $k$

- smaller $k$ -> overfitting
- larger $k$ -> gradually worse accuracy and degenerates towards choosing stuff randomly

### Breaking Ties

possible solutions
- use prior probabilities
- use different metric
- change $k$
- random tie breaking
- adding an instance and seeing if it breaks the tie

### Weighted K-NN

rather than taking the majority we weight each train input and choose the label with largest total weight

#### Weighting Strategies

Let $j$ denote a test instance

- inverse distance $w_j = \frac{1}{d_j+\epsilon}$
	- choice of $\epsilon$ matters
- inverse linear distance $w_j = \frac{d_{max}-d_j}{d_{max} - d_{min}}$
	- $1$ is assigned to the closest, with values going between $0$ and $1$

### Implementation

- typically do a brute-force calculation between test instance and every training instance

- depends on $N$ number of training instances and $D$ dimensions (also depends on how norm is computed for $D$)
- complexity $\mathcal{O}(DN)$


