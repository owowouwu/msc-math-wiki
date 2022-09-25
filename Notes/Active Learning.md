Active learning assumes we have some external intervention that allows us to have some say in the selection of training instances.

Instances should be labelled in a way that maximises learning.

Active learners pose queries (unlabelled instances) to an external helper (an oracle, e.g a human annotator). We focus on query points with high uncertainty on their predicted labels.

## Query Strategies

query instances where the classifier is least confident

$$
\hat{x} = \arg \max_x\left(1 - P_\theta (\hat{y} | x) \right)
$$

where $\hat{y} = \arg \max_y P_\theta ( y|x)$

queries where the classifier is unable to distinguish between two labels -

$$
\hat{x} = \arg \min _x \left(P_\theta (\hat{y}_1 | x) - P_\theta (\hat{y}_2 | x)\right)
$$

or use entropy as an uncertainty measure

$$
\hat{x} = \arg \max_x H(P(\cdot |x))
$$

## Practicalities

Is a good, robust strategy, but it is hard to difficult to justify the strategies theoretically.