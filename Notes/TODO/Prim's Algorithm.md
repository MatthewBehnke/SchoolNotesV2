#ComputerScience  #IowaStateUniversity  #COMS311


[[Classes/ISU/COM S 311/COM S 311]] 

---

# Prim's Algorithm 

Very similar to [[Dijkstra's Algorithm]]. 

used on [[Minimum Spanning Tree]]

```

v inTree = false
s inTree = true 

d[v] = inf for all v in V
d[s] = 0 for some arbatrary vertex s in V
Add all vertices to a min heap with a priority value of the d value
	While H != empty
		v  = extract min(H)
		v.inTree = true
		for all v to v' such that v' intree  == false
			if d[v'] < wt (v, v')
				d[v'] = wt(v,v')
				updateHeap(v', d[v'])