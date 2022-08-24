#ComputerScience  #IowaStateUniversity  #COMS311 


[[COM S 311]] 

---

# Subset Sum Problem

Given a set of natural numbers  A and a threshold set. $B \subseteq A$  and $B \leq T$. The objective is to find a subset that satisfies the constraint and maximizes the sub of the elements in the subset. 

This is a subset problem of [[Bin Packing]]

## Example

$A : \{2,5,3,7,1\}$
$T : 8$

Maximal Set $\{5,3\}$
$\{2,5,1\} = 8$
$\{3,5\} = 8$
$\{7,1\} = 8$

## [[Brute Force]] Solution 

$A$:  set of elements 
$A_i v$: value of the ith element 
$B$: bound (threshold)


SS(i, B) Max value of subset elements $A_1, A_2, ...,A_i$ such that $A_1 + A_2 +... + A_i \leq B$

SS(i , B) = max {ss($i -1$, $B - A_i$ ) + $A_iv$ if $A_iv \leq B$ SS(i -1, B)}

$SS(0, B) = 0$
$SS(i, 0) = 0$

## Smart [[dynamic programming]] approach 

$dict[x][y]$ = store the values of $SS(x,y)$
- x = last index of the element in a set 
- y = running bound 

| 0   | 1   | 2   | 3   | 4   | 5   | B             |
| --- | --- | --- | --- | --- | --- | --------------- |
| 1   | 0   | 0   | 0   | 0   | 0   | 0               |
| 2   | 0   | ->  | ->  | ->  | ->  | -> $\downarrow$ |
| 3   | 0   | ->  | ->  | ->  | ->  | -> $\downarrow$ |
| 4   | 0   | ->  | ->  | ->  | ->  | -> $\downarrow$ |
| 5   | 0   | ->  | ->  | ->  | ->  | -> $\downarrow$ |
| n | 0   | ->  | ->  | ->  | ->  | -> $\downarrow$ |

```
Input n, B

for X = 0 to n
	dict[x][0] = 0
for y = 0 to B
	dict[0][y] = 0

for x = 1 to A
	for y = 1 to B
		if A_i v <= y
			dict[x][y] = max {dict[x -1][y - A_x v] + A_x v}
							 {dict[i -1][y]}
	 	else 
			dict[x][y]= dict[x -1][y]
return 
	dict[n][B]

```

The runtime of this would be $O(nB)$ also called [[Sudo Polynomical]]

