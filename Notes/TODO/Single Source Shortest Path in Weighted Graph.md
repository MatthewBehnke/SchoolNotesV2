#ComputerScience  #IowaStateUniversity  #COMS311 


[[Classes/ISU/COM S 311/COM S 311]] 

---

# Single Source Shortest Path in Weighted Graph 

[[Bellman-Ford Algorithm]]


Similar to [[Dijkstra's Algorithm]] but it is more versatile because it can handle negative edge weights. 

Negative edge weights are found in various applications of graphs hence the usefulness of this algorithm shows. If a graph contains a "Negative cycle" that is reachable from the source, then there is no cheapest path: any path that has a point on the negative cycle can be made cheaper by one more walk around the negative cycle. 

So if there is a negative weight cycle then it can determine its existence and and identify the vertices who's shortest path distance is impacted by the negative weight cycles. 

```
**function** BellmanFord(_list_ vertices, _list_ edges, _vertex_ source) **is**

    _// This implementation takes in a graph, represented as_
    _// lists of vertices (represented as integers [0..n-1]) and edges,_
    _// and fills two arrays (distance and predecessor) holding_
    _// the shortest path from the source to each vertex_

    distance := _list_ of size _n_
    predecessor := _list_ of size _n_

    _// Step 1: initialize graph_
    **for each** vertex v **in** vertices **do**

        distance[v] := **inf**             // Initialize the distance to all vertices to infinity
        predecessor[v] := **null**         // And having a null predecessor
    
    distance[source] := 0              // The distance from the source to itself is, of course, zero

    _// Step 2: relax edges repeatedly_
    
    **repeat** |V|−1 **times**:
         **for each** edge (u, v) **with** weight w **in** edges **do**
             **if** distance[u] + w < distance[v] **then**
                 distance[v] := distance[u] + w
                 predecessor[v] := u

    _// Step 3: check for negative-weight cycles_
    **for each** edge (u, v) **with** weight w **in** edges **do**
        **if** distance[u] + w < distance[v] **then**
            **error** "Graph contains a negative-weight cycle"

    **return** distance, predecessor

```



dist(s,t,i) shortest path distance from s to t using at most i edges
sDist(s,t,i) Shortest path distance fom s to t using exactly i edges

OBS1
sDist(s,t,i) = min{D(s,t,0), D(s,t,1) , ... ,D(s,t,i)}

OBS2
sDist^* (s,t) = sortest path distance from s to t 
		   = min{D(s,t,0),D(s,t,1),D(s,t,2),...}	

OBS3
If there is no negative weight cycle sDist^* (s,t)
 = min{dist(s,t,0),..., dist(s,t, |V - 1|)}

sDist(s,t,i) = min{sdist{s,t,i-1}, dist{s,t,i}}


