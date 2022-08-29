#ComputerScience  #IowaStateUniversity  #COMS311 #COMS228


[[Classes/ISU/COM S 311/COM S 311]]  [[COM S 228]]

---

# Big 0 Notation

Big O notation is useful when [analyzing algorithms](https://en.wikipedia.org/wiki/Analysis_of_algorithms "Analysis of algorithms") for efficiency. For example, the time (or the number of steps) it takes to complete a problem of size n might be found to be T_(_n_) = 4_n_2 − 2_n_ + 2. As n grows large, the _n_2 term will come to dominate, so that all other terms can be neglected—for instance when _n_ = 500, the term 4_n_2 is 1000 times as large as the 2_n_ term. Ignoring the latter would have negligible effect on the expression's value for most purposes. Further, the [coefficients](https://en.wikipedia.org/wiki/Coefficient "Coefficient") become irrelevant if we compare to any other [order](https://en.wikipedia.org/wiki/Orders_of_approximation "Orders of approximation") of expression, such as an expression containing a term _n_3 or _n_4. Even if _T_(_n_) = 1,000,000_n_2, if _U_(_n_) = _n_3, the latter will always exceed the former once n grows larger than 1,000,000 (_T_(1,000,000) = 1,000,0003 = _U_(1,000,000)). Additionally, the number of steps depends on the details of the machine model on which the algorithm runs, but different types of machines typically vary by only a constant factor in the number of steps needed to execute an algorithm. So the big O notation captures what remains: we write either

## Uses 

- Time Complexity
- Space Complexity

## Online Resources
- Wikipedia https://en.wikipedia.org/wiki/Big_O_notation