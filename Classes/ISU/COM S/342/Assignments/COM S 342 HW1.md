#IowaStateUniversity
#ComputerScience 
#COMS342
#Homework

---

# [[COM S 342]] Homework 1 context free grammar 

### Source 

https://github.com/MatthewBehnke/COM-S-342-Homework-1


### Notes 


## 1

### a
Terminals: 
a, b, c, d, $\epsilon$ 
Non terminals: 
S, X, Y


### b (Left most)


S -> X Y 
   -> a X a Y
   -> a Y a Y
   -> a $\epsilon$ a Y
   -> a $\epsilon$ a c Y 
   -> a $\epsilon$ a c $\epsilon$ 
   -> a a c $\epsilon$
   -> a a c 

### c (right most)

s -> X Y 
   -> X c Y
   -> X c $\epsilon$ 
   -> a X a c $\epsilon$
   -> a Y a c $\epsilon$
   -> a $\epsilon$ a c $\epsilon$
   -> a $\epsilon$ a c 
   -> a a c 

### d (parse tree)


## 2

S -> F
   -> if B then S
   -> if (T E T) then S
   -> if (x E T) then S
   -> if (x > T) then S
   -> if (x > y) then S
   -> if (x > y) then F
   -> if (x > y) then if B then S else S
   -> if (x > y) then if (T E T) then S else S
   -> if (x > y) then if (x E T) then S else S
   -> if (x > y) then if (x < T) then S else S
   -> if (x > y) then if (x < T) then S else S
   -> if (x > y) then if (x < z) then S else S
   -> if (x > y) then if (x < z) then T N T else S
   -> if (x > y) then if (x < z) then x N T else S
   -> if (x > y) then if (x < z) then x = T else S
   -> if (x > y) then if (x < z) then x = 1 else S
   -> if (x > y) then if (x < z) then x = 1 else T N T
   -> if (x > y) then if (x < z) then x = 1 else x N T
   -> if (x > y) then if (x < z) then x = 1 else x = T
   -> if (x > y) then if (x < z) then x = 1 else x = 0


S -> F
   -> if B  then S
   -> if B then F
   -> if B then if B then S else S
   -> if B then if B then S else T N T 
   -> if B then if B then S else T N T    

### a

