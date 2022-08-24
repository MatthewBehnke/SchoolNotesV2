#ComputerScience  #IowaStateUniversity  #COMS311 


[[COM S 311]] 

---

# Graph Algorithms


## [[Graphs]] and [[Graph Algorithms]]

[[Graph Theory]]

Graphs G = (V, E)

directed vs undirected

### [[Reachability]]

Given a vertex $v_0$, can we move from $v_0$ to some other vertex $v_n$ using the edges.

### [[Neighbor Reachability]]

### [[Paths]]

#### [[Simple path]]

No repeating of any vertexes. / cycle free paths

Max length of simple path | v | - 1  


## [[Graph exploration]]

Input: vertex of set of vertexes

### [[Connected Complements]] in graphs

CC is a sub graph in G such that every node in the sub graph can reach every other nodes in the sub graph


### [[Breath First Search]]



Explore from $a\prime$ 
visit $a$
visit $b$ and $c$ (N(a) = {b,c})
visit d (N(b) $\in$ d)
visit e,f (N(d) = {e,f})
visit g (N(f) = {g})

Layers in BFS 

layers are nothing but the step that it takes to reach a vertex



#### Graph Exploration of a BFS

Input for all  v $\in$ V
BFS(v)

```c

v.visited = false
v.layer = -1
v.parent = null

BFS(V)
	v.visited = true
	v.layer = 0
	v.parent = 0
	v.cc =  cnt
	
	add v to Q
	
	while Q is not empty
		u = extracted from Q,
		for all w in N(u)
			if w.visited == false
				w.visited = true, 
				w.layer = u.layer + 1 
				w.parent = u
				w.cc = cnt
				add w to Q

```



```c

ConstructPath($x_1, x_2$)
	BFS(x_1)
	init an empty path list(x)
	add x_2 to path list
	x = x_2 path parent
	add x to pathlist
```


```c

BfsExploration(graph,( V, E ))
	for all v in V
		init v.visited = false
		v.cc -1
		cnt = 0
	for v in V
		if v.visited is false
			BFS(v)
			cnt++
```

### [[Depth First Search]]

```c

Init all v IN V
v.visisted = false
v.st = -1
v.et = -1
v.parent = -1

count = 0
for all v in V
	if v.visted == false
		DFS(v)
	
```

```c
DFS(v)
	v.st = count
	count ++
	v.visted = true
	for all u in N(v)
		if u.visisted == false
			u.parent = v
			DFS(u)
	v.et = count
	count++

```


### Types of edges
Tree Edge: main edge (parent relationship)
- Allowed to be in un-directed graphs

Back Edge ( if start time is after second edge)
- Allowed to be in un-directed graphs

Cross Edge ( crossing two groups)
- Not allowed to be in a un-directed Graph

Forward Edge ( is start time is before second edge)
- Not allowed to be in a un-directed Graph


## Biparhite Testing
Given G = $(V,E)$ does there exist some partition A and B of V such that $\forall u \rightarrow v \in E \Rightarrow u \in A$ and $v \in B$


### Observation 1

If a graph contains a cycle w/ odd number of edges then the graph is non biparhite

### Observation 2 ( BFS )

Given a graph G = (V, E), BFS.exploration of the graph will create layers. L1, L2, L3 there is not edge between vertex in the same layer iff G is bipartile 



## Topological Ordering 
Given a (directed) graph $G = (V, E)$ a topological ordering is a mapping $f : V \rightarrow \{1,2, ..., |v|\}$ such that $\forall u \rightarrow v \in E$ $f(u) < f(u)$

### Observation 1

if we do dfs on the graph the end time $(et(u)) > et(v) \Rightarrow u$ is not dependent on v. 

1. et(u) > et(v) for the tree edge $\Rightarrow$ u does not depend on v
2. et(u) > et(v) for Cross edge $\Rightarrow$ u does not depend on v
3. et(u) > et(v) for forward edge  $\Rightarrow$ u does not depend on v

### Observation 2

A node with highest end time (et) is the first node in the Topological order. 

```c
DEF.exploration G = (V,E)
	init v.visited = false
	for all v in V
		if v.visited = false
				DFS(v)
	output the verticies by poping the stack.
			
DFS(v)
	v.visitted = true
	for all u in N(v)
		if u.visited == false
			DFS(uu)
	add v to a stack		
	add v to a stack		

```