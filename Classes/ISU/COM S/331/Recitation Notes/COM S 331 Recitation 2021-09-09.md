#ComputerScience  #IowaStateUniversity  #COMS331 
#Recitation

[[COM S 331]] [[2021-09-09]]

---

# COM S 331 Recitation 2021-09-09

## Review

###  [[Deterministic Finite Automaton]]

M = ($Q, \sum, \delta, s, F$)

Q = Set of states
$\sum$ = alphabet
$\delta$ = transition
s = start set
F = set of accepting states


### Examples


##### 1
A = {$x \in \{a,b\}^*\ |\ \#(a, b)\ \text{is odd}$}

Q = {even, odd}
$\sum$ = {a, b}
s = even
F = {odd}
$\delta$ = 
- $\delta$(even, a) = odd
- $\delta$(odd,  a) = even
- $\delta$(even, b) = even
- $\delta$(odd,  b) = odd

$\hat{\delta}$(even, aa) = even

##### 2

$A = \{ x0^n | x \in \{0,1\}^*, n \in \mathbb{N}\}$ = $\sum^*$

##### 3

$A = \{ x0^n | x \in \{0,1\}^*, n \in \mathbb{Z}^+\}$

Q = 
$\sum$ = 
s =
F = 
$\delta$ = 

## HW problems

8. only need the state diagram
9. only need the state diagram
10. only need the state diagram
	need to think in base 3
11. only need the state diagram


### 12.

M = ($Q, \sum, \delta, s, F$)

prove $\hat{\delta}(q, xy) = \hat{\delta}(\hat{\delta}(q,x),y))$
by induction on y

Base case: y = $\lambda$

$\hat{\delta}(q, x \lambda) = \hat{\delta}(q,x)$

$\hat{\delta}(q, \lambda) = q$

$\hat{\delta}(\hat{\delta}(q,n), \lambda) = \hat{\delta}(q,n)$


IH: assume $\hat{\delta}(q,ny)$ = $\hat{\delta}(\hat{\delta}(q,x),y)$ is true for y

IS: show that $\uparrow$ is true for $y^\prime = ya$

a $\in \sum$

### 13.

Prove every full prefix free language (PFL) is maximal

We know: A is full if $\sum\limits_{x \in a}^{} 2^{-|x|} = 1$

A is a PFL if $\sum\limits_{x \in a}^{} 2^{-|x|} \leq 1$

Let A be some PFL that is not maximal
	$\sum\limits_{x \in a}^{} 2^{-|x|} = 1$ (***we know this is true***)
	
A is maximal if A is not a proper subset of any PFL. 


... 
Some other prefix free language B  = A $\cup\ {y}$ $\sum\limits_{Z \in B}^{} 2^{-|z|}$

ALL PFL has to be maximal 

The controdiction is that it is not maximal becaise there could be another string that it is a subset of that ...

If B is greater that one then it is not prefix free

becomes: ...

prove that B is greater than 1

....

### 14.

How many DFAs  M = ($Q, \sum, \delta, s, F$) are there with $\sum = \{0,1\}$ and $Q = \{1,2,...,n\}$

Start states: n
final states : $2^n$ $\leftarrow$ P(Q)   (P means power set in this case)
Transitions: ___

### 15. 

Prove there is a language A $\subseteq \{0,1\}^*$ with both of the following properties

i. $\forall x \in A, |X| $\leq 5$
ii. Every DFA that decides A has more than 8 states. 

$\sum$ of the sets all the way to 5


\#A : $2^0 + 2^1 +\ ...$

There must be some DFA that is $\leq$ 5 that does not have 8 sets ? is this right?