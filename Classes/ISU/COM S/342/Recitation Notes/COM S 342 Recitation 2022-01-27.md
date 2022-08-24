#IowaStateUniversity
#ComputerScience 
#COMS342
#Recitation

---

# [[COM S 342]] Recitation [[2022-01-26]]


Started working on problems that should help with homework

### Problems 

1. -

	S -> T U T -> 
	T -> 0 T 1 | $\epsilon$
	U -> 1 U 0 | $\epsilon$


	1100
	0011

	S -> (T) U T
	      -> 0 (T) 1 U T
		  -> 0 0 (T) 1 1 U T
		  -> 00 $\epsilon$ U T
		  -> 0 0 | | $\epsilon$ T
		  -> 0
		  - 0 0 1 1 $\epsilon$
		  - 0 0 1 1

 right

 S -> T U T
    -> T U 0 (T) 1
    -> T U  0 0 (T) 1 1 
    -> T U 0 0 $\epsilon$ 1 1 
    -> T $\epsilon$ 0 0 1  1 
    -> $\epsilon$ 0 0 1 1
    -> 0 0 1 1

   (S)
   /      |    \
(T)      U   T
/  | \    |      | 
0  T 1  $\epsilon$     $\epsilon$ 
    / | \
   0 T  1
      |
	 $\epsilon$ 
	
