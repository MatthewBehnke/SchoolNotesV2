#ComputerScience  #IowaStateUniversity  #COMS311 


[[COM S 311]] 

---

# Weighted Interval Scheduling

## Using [[Dynamic Programming]]

- s(i): start of the i-th job
- e(i): end of the i-th job
- v(i): value / weight  (wt) of the i-th job



This solution uses [[Bottom-up Completion]] and [[Memorization]] 
```

dict[0] = 0
for i = 1 tot n
	dict[i] max{v(A[i]) + dict[p(1)], dict[i +1]}
return dict[i]
```

```
FindSetSolution(i)
	if i == 0
		return empty set
	else if dict[i] > dict[p(i)] + v(A[i])
		return FindSetSolutiion(i -1)
	else
		return A[i] union FindSetSolutiion(p(i))


```




## [[Recursion]] with [[Memorization]]

```
WI(1...i):	max value of the jobs A[1] ... A[i] that are scheduled
	if dict[i] < undefined
		if i == 0 i
			dict[i] = 0
		else if i = 1 
			dict[i] = v(A[i])
		else 
			dict[i] = max{v(A[i]) + Wi(1, p(i)), Wi(1, i +1)}
	return dict[i]
```


## [[Optimization]] Objective 

Schedule some subset of non-overlapping jobs such that the sub of the values of the scheduling jobs is maximal 

## No [[Greedy Algorithm]] Solution 

There exists a proof (will not cover) that there exists no known greedy solution to this problem 

## Brute force way to solve this problem 

For every job we have two choices (yes and no). If we choose yes ($OPT_1$) then it will be the set of jobs in A that does not overlap with $J_i$. If we choose no ($OPT_2$) then it will be the set of jobs in A without $J_i$.

The OPT is $Max\{OPT_1 + v(J_i), OPT_2\}$

