#ComputerScience  #IowaStateUniversity  #COMS311 


[[COM S 311]] 

---

# RSA
Rivet, Stomir, Adleman in 77



## Asymmetric Key Crypto

Asymmetric means not using the same key but can use the same key 

public key is general shared information



1 Key gen 

a. select two large primes p, q
b. compute n = p x q
c. compute P(n) = (p -1)(q -1)
d. select e < p(n) such that gcd(e, p(n)) = 1
e. compute d such that (e x d) mod P(n) = 1 
f. k_private = (d, n) k_pub = (e, n)

test 

a. p = 7, q = 11
b. n = 77
c. p(n) = 60
d. e = 13 gcd(13, 60) = 1
e. d = 37
k_pub = (13, 77) K_private = (37, 77)


## Euchids GCD Algo 

a >= b

common divisor (a, b) <=> common divisor (b, a mod b) 

Egcd (a, b)
	if b == 0 then return a
	return Egcd(b, a mod b)







