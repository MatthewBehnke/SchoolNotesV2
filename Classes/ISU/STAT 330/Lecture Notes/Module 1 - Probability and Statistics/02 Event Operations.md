# Event Operations

## Set Theory

### Set Notation

Review Symbols $\in , \not\in, \subset , \subseteq$ etc

- if x is an element of set B, this is denoted $x \in B$
- if y s not an element of set B, this is denoted $y \not\in B$ 
- If every element of set A is also an element of set B, then A is a subset of B. $A \subset B$ 

let A and B be two events 

- Union ($U$): $A \cup B$ is the event consisting of all outcomes in A or in B or in both
	- $A \cup B = \{w | w \in A \text{ or } w \in B \}$ 
- Intersection($\cap$) $A \cap B$ is the event consisting of all outcomes simultaneously in A and in B
	- $A \cap B = \{w | w \in A \text{ and } w \in B\}$ 
- Complement ($\bar A$): The complement of an event A $(\bar A)$ is the event consisting of all outcomes not in A
	- $\bar A = \{w | w \not\in A\}$
	- $A^c = \{w | w \not\in A\}$ ( is also used but in stat 330 use $\bar A$ 
- De Morgan's laws:
	- $(\overline{A \cup B}) = \overline{A} \cap \overline{B}$ 
	- $(\overline{A \cap B}) = \overline{A} \cup \overline{B}$ 
- Empty Set: $(\emptyset)$ is a set containing no element, usually denoted by $\{\}$. the empty set is a subset of every set:
	- $\emptyset \subseteq A$
- Disjoint / mutually exclusive sets: Sets A, B are disjoint if their intersection is empty 
	- $A \cap B = \emptyset$ 
- Pairwise disjoint sets: Sets $A_1, A_2, A_3 ...$ are pairwise disjoint if $A_i \cap A_j = \emptyset$ for any $i \not= j$ 

## Example 7:

$\Omega = \{1,2,3,4,5 \}$
$A = \{1,2,3\}$ 
$B = \{2,3,4\}$ 
$C = \{4,5\}$ 


1. $\overline{A} = \{4,5\}$
2. $A \cup B = \{1, 2,3, 4\}$
3. $A \cap B = \{2,3\}$
4. $A \cup B = \{\}$
5. Are A and B disjoint? No because $A \cap B$ is not empty 
6. Are A and C disjoint? Yes because $A \cap C$ is empty
7. Are A,B,C pairwise disjoint? No because at lease one pair (A and B) are not disjoint 
