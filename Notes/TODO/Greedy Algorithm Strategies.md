#ComputerScience  #IowaStateUniversity  #COMS311 


[[COM S 311]] 

---

# [[Greedy Algorithm]] Strategies

![[GreedyAlgoGraphExample.png]]

$G = (V, E, Wt)$, $Wt$ : $E$ $\rightarrow \mathbb{R}$

$Wt$ just means a edge has a weight meaning that it might be cheaper to take more paths with less weight each than one direct path with a high weight. 

wt(u,v) : weight of edge from u to v
wt($\pi(u,v)$) weight of the shortest path $\pi$ from u to v. (lowest weight)

Most of the time there will not be any negative edges but in some cases there are examples where negative numbers do come naturally.

## Properties of Greedy Algorithms 

- Optional substructure property. 
	- Must know the optional solutions to the sub problems.
- [[Greedy Choice Property]]


## Algorithms that are Greedy

- [[Dijkstra's Algorithm]]