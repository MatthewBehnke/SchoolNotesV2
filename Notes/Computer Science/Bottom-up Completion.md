#ComputerScience  #IowaStateUniversity  #COMS311 


[[Classes/ISU/COM S 311/COM S 311]] 

---

# Bottom-up Completion


## Uses 
- [[Dynamic Programming]]

## Online Resources
- Wikipedia https://en.wikipedia.org/wiki/Top-down_and_bottom-up_design

## Examples 

### [[Fibonacci]]

To solve this problem using dynamic programming we can do 

```
fib(n)

	for i = 1 to n
		if i <= 2 
			dist(i) = 1
		else 
			dist[i] = dist[i -1] + dist[i -2]
	return dist[n]

```
