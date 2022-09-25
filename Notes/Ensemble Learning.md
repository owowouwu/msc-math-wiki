Idea - we fit multiple models and then take the average, weighted or unweighted.

This can reduce variance.

## Bagging

Bagging stands for bootstrap aggregating and is a way of performing ensemble learning, in which $M$ different bas emodels are fit to different randomly sample versions of the data. This encourages different  models to make diverse predictions (reduce over fitting). 

The datasets are sampled *with replacement* and is done until we have $N$ examples per model, where $N$ is the original number of data points.

## Boosting

Train models sequentially, where each model tries to compensate for the weaknesses of its predecessor by weighting observations that were handled poorly.
