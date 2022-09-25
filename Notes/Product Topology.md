# Definition

Let $(X, \mathcal{T}_{X})$ and $(Y, \mathcal{T}_{Y})$ be [[Topological Space]]. 

The **product topology** $\mathcal{T}_{X \times Y}$ on $X \times Y$ is the [[Generated Topology]] of $\mathcal{T}_{X} \times \mathcal{T}_{Y}$.

similar to notion of [[Product Sigma Algebra]]

## Characterisation with Continuous Functions

The **product topology** is the minimal topology on $X \times Y$ such that 
$$
X \times Y \to X, (x,y) \mapsto x
$$
$$
X \times Y \to Y, (x,y) \mapsto y
$$
i.e the projections are continuous

## Universal Property

The topological space $(X \times Y, \mathcal{T}_{X \times Y})$ is the unique topological space satisfying

1. $X$
..

The **product** of $X$ and $Y$ is

1. a topological space $(X \times Y, \mathcal{T}_{X \times Y})$ with two continuous functions $p_{1} : X \times Y \to X$, $p_{2} : X \times Y \to Y$
2. if $(Z, \mathcal{T}_{Z})$ is a topological space with two continuous functions $f_{1}, f_{2}$ then there exists $g: Z \to X \times Y$ such that $f_{1} = p_{1}(g)$, $f_{2} = p_{2}(g)$.

