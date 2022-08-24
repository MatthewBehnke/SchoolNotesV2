#ComputerScience  #IowaStateUniversity  #COMS311 


[[COM S 311]] 

---

# Single Source Shortest Path in Weighted DAG

if we have a shortest path from u to v. Then w is a point in the shortest path and the shortest path from w to u or v is the same as before. 

## Algo non  [[Dynamic Programming]] 
Just use [[Dijkstra's Algorithm]]


## Using [[Dynamic Programming]]

SD(v) = shortest path distance to vertex v from a given vertex s
SD(u) = 0
SD(v) = min (SD (u) + wt(u,v) | u -> v) for all v not = tp s

```
dict[v] store the variation for sd(0)
iterate dict[v] = inf for all v
	for each v in TempOrder(V) [O(v + e)]
		if v == u then dict[v] = 0
		else dict[v] = min{dict[u] + wt(u,v) | u-> v}
	return dict
```
 
 | itr | v0  | v1  | v2  | v3  | v4  | v5  |
 | --- | --- | --- | --- | --- | --- | --- |
 | 1   | inf | inf | inf | inf | inf | inf |
 | 2   | inf | 0   | inf | inf | inf | inf |
 | 3   | inf | 0   | 2   | inf | inf | inf |
 | 4   | inf | 0   | 2   | 6   | inf | inf |
 | 5   | inf | 0   | 2   | 6   | 5   | inf |
 | 6   | inf | 0   | 2   | 6   | 5   | 3   |
