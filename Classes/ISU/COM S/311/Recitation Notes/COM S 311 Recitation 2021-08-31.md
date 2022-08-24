[[COM S 311]] [[2021-08-31]]

# COM S 311 Recitation 2021-08-31

---

## [[Big-O Notation]] Problems

## Prove / Disprove

### 1.1 

$f(n)$ = $log(n^5)$
$g(n)$ = $log(n) + 5$ 
$f \in O(g)$

#### Proof

$f(n)$ = $log(n^5)$ = $5log(n)$ $<=$ $5(log(n) + 5)$ = $5g(n)$ 

Therefor there exists a c = 5. There exists a $n_o \geq 0$ such that 1 for all n $\geq n_0 : f(n) \leq c \times g(n)$

Hence $f \in O(g)$

### 2 

$f(n)$ = $log(n)$
$g(n) = \sqrt{n}$
$f \in O(g)$


#### Proof

$f(n)$ = $log(n)$ = $log(n^{1/2*2})$ = $2log(n^{1/2}) \leq 2n^{1/2}$

as for all naturals $x: log(x) \leq x$
Therefor $f(n) \leq 2 \sqrt{n}$ i.e
There exists a $c = 2$



#### 2'

For question 2. prove or disprove $g \in O(f)$

##### Disproof

Assume $g(n) \in O(f(n))$

- $\exists c \leq 0.\ n_0 \leq 1.\ \forall n \geq n_0. \sqrt{n} \leq c \times log(n)$
-  $\exists c \leq 0.\ n_0 \leq 1.\ \forall n \geq n_0. \sqrt{n} \leq c \times2 log(\sqrt{n})$
-  $\exists c \leq 0.\ n_0 \leq 1.\ \forall n \geq n_0. \sqrt{n} / 2log(\sqrt(n) \leq c$
-  There exists some  $c\ \geq 0$, which is larger than $x/2 log(x)$ for a number $x$
-  Contradiction
Therefor, the assumption is incorrect

#### 3.
$f(n) = 2^{k log_2(n)}$
$g(n) = n^k$
$f \in O(g)$


##### Proof

$f(n) = 2^{k log_2(n)}$ = $x$

Taking $log_2$ on both sides.
$klog_2(n)$ = $log_2(x)$
- $log_2(n^k)= log_2(x)$
- $n^k = x$

Therefor. $f(n) = g(n)$. i.e $f \in O(g)$. where $c = 1$ and $n_0 \geq 1$

#### 4.

For any $f_1 \in 0(g_1)$ and $f_2 \in O(g_2)$. $f_1(n) = f_2(n) \in O(marg_1(n), g_2(n))$

##### Proof

$f_1(n) \in O(g_1(n)) \Rightarrow exists c_1, n_1 \forall n \leq $




## [[Runtime Analysis]] for loops

#### 1.

````

for (i = 1 to n)
 for (j = 1 to n)
   for (k = 1 to i + j)
   	Some operations

````


$\sum\limits_{i = 1}^{n} \sum\limits_{j = 1}^{n} \sum\limits_{k = 1}^{i + j}$ c =  $\sum\limits_{i = 1}^{n} \sum\limits_{j = 1}^{n}(i + j)$
= $\sum\limits_{i = 1}^{n}(\sum\limits_{j = 1}^{n}  i + \sum\limits_{j = 1}^{n} j)$
= $\sum\limits_{i = 1}^{n}(n \times i + n(n +1)/2)$
= $\sum\limits_{i = 1}^{n} n \times i + \sum\limits_{i =1}^{n} n(n +1)/2$ 
= $n \times n(n +1)/2 + n \times n(n+1)/2 \in O(n^3)$