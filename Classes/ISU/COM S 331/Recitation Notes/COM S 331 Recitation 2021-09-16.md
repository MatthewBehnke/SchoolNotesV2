#ComputerScience  #IowaStateUniversity  #COMS331 
#Recitation

[[Classes/ISU/COM S 331/COM S 331]] [[2021-09-16]]

---

# COM S 331 Recitation 2021-09-16

## #15

There will be some strings that will not work.

Two strings that are not divisible by 3

It will be a controdction because the only way to do this problem is with a non deterministic finite automona 

## #16
Prove that for all $x\in\Sigma^*$, the singleton language $\{x\}$is regular.

--- 
a singleton language is regular


## #17
Prove that every finite language $A\subseteq\Sigma^*$ is regular.

---

Build an DFA to prove this. 

Did this in homework 1.

Because we have finite number of strings we can treat the string as a singleton. 

Use the fact that a singleton language is regular and we can combine the dfas. 

Does not work with infinite languages


## #18

Prove / disprove. Every subset of a regular language is regular

### Trying to disprove

need to find a language that has a subset of $\{0^n1^n | \forall n \in \mathbb{N}\}$

$A^*$ ? 

## #19

Long so not going to write it out

|       | [$\frac{0}{0}$] | [$\frac{0}{1}$] | [$\frac{1}{0}$] | [$\frac{1}{1}$] |
| ----- | --------------- | --------------- | --------------- | --------------- |
| $v_1$ | $v_1$           |                 |                 | $v_1$           |
| $v_2$ | $v_2$           |                 |                 | $v_2$           |
| ...   | ...             |                 |                 | ...             |


## #20

go over again

## #21

not hard but just a lot of work. 

7 states? 

(LLRA), 1 = (LRLR)
(LLL), 1 = (LRRA)

use transition table