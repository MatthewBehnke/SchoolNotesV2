#ComputerScience  #IowaStateUniversity  #COMS311


[[Classes/ISU/COM S 311/COM S 311]]

---

# Minimum Spanning Tree


A MST is a [[Greedy Algorithm]] 


## What is a spanning tree

- It has no loop 
- a tree that has no cycle in a graph
- include edges in such a way that there is a path between every vertex with every other vertex


### Examples

Graph: 

![[Drawing 2021-10-19 14.15.11.excalidraw]]


There are 4 spanning trees
- (T2) v0, v2, v3, v1
- (T1) v0, v1, v3, v4
- (T3) v1, v2, v1, v3

wt(T1) = 6


### Information about MST

- Not trying to find the shortest path between every node but tying to find the shortest path between all nodes using a spanning tree. 

### Optimal Substructure property

Given a weighted graph G, Let $T^*$ be a MST for G. Let e = (u. v) be present in $T^*$.  A contraction of e (merge u and v together to form e results in one large vertex with all of edges of v and u) on G to form G/e

If T is a MST of G/e then $T \cup \{e\}$ is a MST of G

very similar to [[Dijkstra's Algorithm]]. 


#### Proof sketch 

***Observation 1***  $T^*$ - $\{e\}$ is a ST for G/e
***Observation 2*** wt(T) $\leq$ wt($T^* - \{e\}$)
  $\leq$ wt($T^*$) - wt(e)

wt($T \cup \{e\}$) = wt(t) + wt(e) $\leq$ wt($T^*$)

### [[Greedy Choice Property]]

Cut: Partition the vertex's in G in two groups.

Cross-edge: e = (v, u) st u $\in A$ and $v \in B$

GCP: For a cut(A,B), the minimum cost cross edge belongs to some MST.


### Proof sketch (GCP)

![[Drawing 2021-10-19 14.50.23.excalidraw]]

- e is min wt cross edge
- Let $T^*$ be a MST which does not contain e
- $e'$ is present in $T^*$
- New ST: T = ($T - \{e'\}) \cup \{e\}$ ( switching out e' and e)
- wt(T) = wt($T^*$) - wt(e') + wt(e)
- $\therefore$ T is a MST

### Another example on how a MST is generated

![[Drawing 2021-10-19 15.03.12.excalidraw]]

Takes the minimum path to each all vertexes. Not always a the MST just a ST

### [[Prim's Algorithm]]