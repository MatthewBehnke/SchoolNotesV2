#ComputerScience  #IowaStateUniversity  #COMS311 


[[Classes/ISU/COM S 311/COM S 311]] 

---

# Greedy Choice Property

S[V] Shortest distance of v from source vertex.
Lets consider $S \subset V$ for which $\forall v \in S : S[V]$ is known.

$\forall u \in V/s$ d[u] = min($v \in S$){$\delta$[v] + wt(u + v)}

***Claim***:  If $x \in V/S$ has the smallest d[x] values then d[x] = $\delta[x]$. 

This claim is greedy because we can just look at the "S"' that we have. We don't need to consider all of the choices but only the options around us. 

