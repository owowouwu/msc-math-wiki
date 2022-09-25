If we have labelled data $\mathcal{L}$ and unlabelled data $\mathcal{U}$, we use a classification algorithm based on the labelled data set to classify each point in the unlabelled dataset. Each time we classify a point, we add it to the labelled data.

**Problem** - if $|U| > |L|$ then the estimates are based on entirely on unlabelled data

Propagating labels assumes that the labels are distributed such that points that are nearby are likely to have the same label.

