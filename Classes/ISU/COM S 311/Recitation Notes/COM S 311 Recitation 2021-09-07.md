[[Classes/ISU/COM S 311/COM S 311]] [[2021-09-07]]

# COM S 311 Recitation 2021-09-07


## Question 1

Given a sorted list A of ints, and a target int T. Write an algo to verify whether there exists two ints x and y in A, such that x + y = T

because the list is already sorted it can be done in a way that is similar to a binary search algo.

## Question 2

Two sorted lists. A and B of int. Give an algo to find all ints that are common to A and B. There are no repetitions of elements.

its just the union of the two arrays.

Could just brute force or do a double walk comparing each elements.

## Question 3

Given a [[Binary Search Tree]] over ints. Write an algo to find the k-th smallest element in the BST. 
k-th element smallest element is the element that would appear at the k-th position if the elements in the BST are arranged in ascending order. 

Use recursive algo 

## Question 4

remove an element from a BST.

There are three senerios that can come up

1. The node is a leaf.
	Then we can just remove the node
1. The node has one child
	Just replace the node with its child 
1. The node has two child's
	Then  find the next largest element y to x. ( the element that should appear right after x if the elements in BST are arranged in ascending order) Run time for finding such elements is o(logn) if the tree 