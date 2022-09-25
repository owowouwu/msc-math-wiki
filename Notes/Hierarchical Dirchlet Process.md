Models distributions with dependencies such as trees.

Idea - model child distribution with a [[Dirchlet Process]] centered (i.e has its mean) at the distribution of its parent.

Example - 

![[Pasted image 20220115174645.png]]

Taking 

$$
\begin{align}
G_1 | H &\sim DP(\alpha, H)\\
G_2 | G_1 &\sim DP(\alpha, G_1)
\end{align}
$$


## Grouped Data

Teh, Jordan et al. 2005

- used in clustering problems where we have *grouped data* and clusters can be shared between groups

we have the following hierarchy

$$
\begin{align}
G_0 &\sim DP(\gamma, H)\\
G_j | G_0 \sim DP(\alpha, G_0)
$$
 
 ![[Pasted image 20220121114925.png]]
 
 - mixture components come from $G_0$ but each $G_j$ has its own mixing proportions

## Chinese Restaurant Franchise

- extension of [[Chinese Restaurant Process]] to the hierarchical model i.e multiple groups
- similarly, also a way of generating HDP


![[Pasted image 20220121122318.png]]

- customers' probabilities of sitting on table $t_{kj}$ in cluster $G_k$ is weighted by 
	- number of customers already present in that table (as is in the usual CRP)
	- also how much the table itself was drawn in $G_0$. 