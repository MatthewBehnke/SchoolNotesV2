#ComputerScience  #IowaStateUniversity  #COMS311 


[[COM S 311]] 

---

# Dynamic Programming

- [[Richard Bellmon]] in the 50-60s
- [[Optimization]] type problem

## [[Algorithm Strategies]]
- Divide the problem into [[Subproblems]] 
- Solve the [[Subproblems]]
- Generate the solution of the original problem from the sub problem solutions

## Types of problems
- [[Bottom-up Completion]]
- [[Weighted Interval Scheduling]]

## Examples

### [[Fibonacci]]

a [[Memorization]] type problem

``` 
Fib(n) = Fib(n -1) + Fib(n-2)
Fib(1) = Fib(2) = 1

Fib(n) 
	if n <= 2 return 1
	else return fib(n -1) + fib(n -2)
```

problem with this type of problem 

to solve this we have to solve the same sub problem over and over. If we are able to somehow store the result of the [[Subproblems]] and then use it whenever it comes up again then we will reduce the cost of the program. 

We can just create a dictionary to store the result of fib(i) then we can just check if there exists anything in the i location of the dictionary if so use it else do the recursion.


This problem is not really dynamic programming because it uses recursion it is more of a [[Recursion with Memorization]]

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

This was an example of [[Bottom-up Completion]]
