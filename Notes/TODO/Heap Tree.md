#ComputerScience  #IowaStateUniversity  #COMS311 


[[Classes/ISU/COM S 311/COM S 311]] 

---

# Heap Tree

Implemented using a [[Binary Search Tree]]

[min max tree](https://en.wikipedia.org/wiki/Min-max_heap)


## Stored within an [[Arrays]]

Parents children
- if odd 2i + 1
- if even 2i + 2

Children's  Parent
-  $\lfloor\frac{i - 1}{2}\rfloor$ (floor)


## Max Heap

The root will contain the highest valued element



## Min Heap

The root will contain the lowest valued element 



### Heapify Down
 If a node is placed in the wrong location because it is not greater then all elements in its sub tree. 

Its job is to move the nodes into place.

It is done by looking at each of the nodes children and swapping places with the child that has the greatest value. Then on the element that was just swapped we check if it is a leaf node or if the node is greater then all elements in its sub tree. If it does not meet the criteria then we run heapify on the node again until the tree holds true.


```

HeapifyDown(i)
	if A[i] is a leaf: return
	if A[i] >= A[2i + 1] and A[i] >= A[2i + 2]: return
	otherwise: j = index of the max child
		swap(A[i], A[j])
		HeapifyDown(j)
		
	  	

```

The runtime of the algo is logn because it is almost a complete binary tree. 

### Heapify Up

If a leaf node has a larger element than its parent and the rest of the tree holds true. 

The function checks if its parent has a larger node if not then it swaps with its parent. This continues until the root node or the parent node is larger.

```

HeapifyUp(i):
	if A[i] is root: return
	if A[i] <= A[(i -1)/2]: return
	otherwise:
		swap(A[i], A[A[(i -1)/2]])
		HeapifyUp(A[(i -1)/2])

```

### Find and extract the highest priority element.

To find

```

return A[o]

```

To remove

```

Replace A[0] with the last element(A[n - 1]). 
Mark A[n - 1] as empty.
HeapifyDown(0)

```

Takes logn time because of HeapifyDown



### Adding new element to the Heap

First make sure we have space in the [[Arrays]] to add the element to. Use a [[Dynamic Arrays]] to have this taken care of for us.

Steps:
- Add the element as a new node at the end of the array
- HeapifyUp(starting from that index probably (n))

```

Add:
	A[n] = (new element)
	HeapifyUp(n)

```

Takes logn because of HeapifyUp.

We will always have the highest priority element at the root because we will always HeapifyUp on the removal of the root node.

### Make heap
- Probably will not need to implement this for our homework assignment but good to know
- Using an existing array that may or may not be a valid heap.

```
makeHeap:
	for i = (n -1)/2 down to 1
 		HeapifyDown(i)
```


### Useful notes about heaps

- The number of nodes at a leaf level are $\frac{n}{2^{l+1}}$ and at the root is = to 1.
- The level or l is 0 at the leaf level and goes up by 1 each level above.

### Heap Sort

Given an [[Arrays]] A of elements
- Make heap A $\rightarrow$ H  . . . O(n)
-  n extracting heap to get the elements in descending order. 
	= O(n log n)
	= logn + log(n -1) ...
	= log(n x (n-1) x (n- 2) x ... 1)
	= log(n!) $\approx$ log(n^n) = nlogn 