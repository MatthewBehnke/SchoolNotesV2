#ComputerScience  #IowaStateUniversity  #COMS331 
#Recitation

[[Classes/ISU/COM S 331/COM S 331]] [[2021-09-02]]

---

# COM S 331 Recitation 2021-09-02

Main focus of this recitation is questions about homework number one due [[2021-09-07]]

## Homework questions


### #1
Counter example 




### #2
Proof



### #3

use induction

Proof for every positive  int n

$\sum\limits_{k=1}^{n}\frac{1}{k^2}\leq 2 - \frac{1}{n}$

Base case: n = 1

- $\sum\limits_{k=1}^{n}\frac{1}{k^2}\leq 2 - \frac{1}{n}$
- $\frac{1}{1^2} \leq 2 - \frac{1}{1}$
- $1 \leq 2 - 1$ 

Induction hypothesis: assume $\sum\limits_{k=1}^{n}\frac{1}{k^2}\leq 2 - \frac{1}{n}$ holds for n

Induction step 

- $\sum\limits_{k=1}^{n}\frac{1}{k^2}\leq 2 - \frac{1}{n + 1}$
-  $\sum\limits_{k =1}^{n} \frac{1}{k^2} +  \frac{1}{(n + 1)^2}$
-  $\sum\limits_{k =1}^{n} \frac{1}{k^2} +  \frac{1}{(n + 1)^2}$ $\leq 2 - \frac{1}{n} + \frac{1}{(n + 1)^2}$

### #4

o = $\emptyset$ = {}
 n + 1 = n $\cup$ {n}
 
 ###### A
 
- 1 =  0 + 1 = {} $\cup$ {{}} = {{}} = {$\emptyset$}
- 2 = | +| = {{}}  $\cup$ {{} $\cup$ {{}} = 

 ###### B
 - $\forall n \in \mathbb{N}$, $n = \{k \in \mathbb{N}\ | k < n\}$
	 - Base case: 0 = {}
	 - Induction hypothesis: assume n = {k $\in \mathbb{N}\ |\ k < n$ } is true
	 - Induction step: Show 
		 - n + 1 = {k | k < n +1}
		 - n + 1 = n $\cup$ {$n$}
		 
### #5

		 
### #6
		 
### #7
x $\sqsubseteq$ y, x = 00, y=001
s is prefix repetitive if $\exists \infty$ many w st ww $\sqsubseteq$ S, Show P[s is prefix repetitive] = O

let |W| = n

- P [w $\sqsubseteq$ S] = $\frac{1}{2^n}$
- P [w $\sqsubseteq$ S]  = $\frac{1}{2^n} \ \times \frac{1}{2^n}$
