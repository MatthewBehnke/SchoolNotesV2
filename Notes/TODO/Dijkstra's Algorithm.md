#ComputerScience  #IowaStateUniversity  #COMS311 #COMS327


[[Classes/ISU/COM S 311/COM S 311]] [[Classes/ISU/COM  S 327/COM S 327]]

---

# Dijkstra's Algorithm


## Example Pseudo code
```

d[u] = inf for all v in V
d[s_n] = 0
Create a PQ and add the vectors w/ priority vales of values

while PQ != empty
	v = extractMin(PQ)
	for all v -> v' in E
		if d[v'] > d[v] + wt(v, v')
			d[v'] =d[v] + wt(v, v')
			update(PQ, v', d[v'])
		
```

If we use a [[Binary Heap]] the runtime of the pseudo code would be O((V + E) + log V) 

If we use a [[Fibonacci Heap]] the runtime would be O(E + V + log V) 