A way of viewing the [[Dirchlet Process]], more specifically the 'rich get richer' aspect of the process i.e the more a component is drawn, the more likely that component will be drawn again.

## Intuition

- Have a restaurant with infinite number of circular tables, indexed. 
- Customer 1 sits at the first table.
- The probability a new customers sits at an occupied table is proportional to the number of customers at that table.
	- i.e they are more likely to sit at a table with many customers

## Formal Definition

A discrete time stochastic process $B_t$ where $B_t$ is a partition (the tables and their customers) of the set $[t]$ (can be thought of as representing each customer), whose probability distribution is determined as follows.

- $B_1 = \{ \{1\} \}$ a.s.
- At time $n+1$, the element $n+1$ is either added to a new singleton block w.p $1/(n+1)$, or to one of the blocks w.p $|b| / (n+1)$ where $|b|$ is the number of elements in the block.

This is similar the the Polya urn scheme / sequential sampling.

## Exchangeability

The partition is [[Exchangability|exchangable]] in the sense that relabelling the customers does not change the distribution of the partition, i.e it does not matter which order the customers sit at the table when determining the probability of the final distribution.

### Relation to DP

The DP exhibits the same clustering properly and can be obtained from the CRP by using [[de Finetti's Theorem]].





