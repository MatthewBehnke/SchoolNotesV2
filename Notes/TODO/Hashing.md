#ComputerScience  #IowaStateUniversity  #COMS311 


[[COM S 311]] 

---

# Hashing
Will not need to implement but will use the java lib.

n : elements represented by <ki, vi>
m : bins

##### Hashfunction
f(ki) = integer value = j
 <ki, vi> will be stored in the jth bin
 
 
 if the hashfunction does produce the same value for more than one input we use the chain hashing method to store more than one input in the same bin. We can do this by using an array of lists
 
 
 ##### Get the i'th elemen's value
 
 f($k_i$) = index  = j. Then search for $k_i$ in the list associated by the $j^{th}$ bin
 
 ##### Properties
 1. Each bin index is equally likely to be the [] of hashing
 2. Independence
 3. Expected Runtime O(1 + length of list)
	 1. Expected length of list = n $\times \frac{1}{m}$
	 2. Expected Runtime O(1 + $\frac{n}{m}$) 
		 1. m $\in O(n)$
		 2. $\frac{n}{m} \in O(1)$

