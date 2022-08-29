#ComputerScience  #IowaStateUniversity  #COMS311 


[[Classes/ISU/COM S 311/COM S 311]] 

---

# Binary Search Tree

## Uses 
- [[Tree Sort]]
- [[Priority Queue]] operations

## Online Resources

- Wikipedia https://en.wikipedia.org/wiki/Binary_search_tree#Examples_of_applications

## [[Runtime Analysis]]

When the tree is balanced then 
n elements: O(logn) 
- More specific O(h) -
	- The height of the tree
		- The smallest that is possible is (logn)

This is because the tree is sorted meaning that we do not have to search the whole tree but just the height of the tree on the worst case. Because at each level of the tree we get to make a decision if the element that we are looking for is larger or smaller than the element at the current position of the tree.


## Balanced Binary Search Tree

The difference of height of the left and right tree does not exceed one. There can be more elements in one of the trees but the tree still needs to be balanced meaning that there can not be that many more elements in one side of the tree compared to the other side


## Ways of Balancing a Binary Search Tree

- Rotation (AVL Tree)
		<iframe src="https://upload.wikimedia.org/wikipedia/commons/3/31/Tree_rotation_animation_250x250.gif"
height="315" width="560" allowfullscreen="" frameborder="0"></iframe>
