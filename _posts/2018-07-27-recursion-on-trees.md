---
layout: post
title:  "Useful recursive functions for trees"
date:   2017-07-24 10:00:38 -0500
categories: cs

---
A binary tree is a data structure that consists of nodes, which have a maximum of two children referred to as the left child and right child. We can thereby implement a binary tree in Python very easily: 

````
class Node: 
	def __init__(val, left = None, right = None): 
		self.val = val 
		self.left = left 
		self.right = right 

	# Children are set to None by default. We form trees by invoking the constructor: 
	# root = Node(1, Node(2)) - forms a tree with root node 1 and left node 2 
````

By the recursive definition of a binary tree, any binary tree is either empty (a null root node) or consists of a root node together with left and right subtrees, and both of the left and right subtrees are themselves binary trees. This is why recursive algorithms and binary trees go hand in hand. Let's check out some useful recursive functions, starting with simple to more complex.   

In general, a recursive approach to a problem is a procedure that calls itself on smaller subproblems, or smaller input values, and the result for the larger problem is computed by applying some kind of combine operation on the results from the subproblems. For trees, our subproblem will usually be the left and right subtrees, the two recursive calls we would make at any node. The combining or merging of these subproblem solutions can be an addition, a logical operation, etc.- usually this depends on what you want to return. Any recursion always needs a base case which can be thought of as a stopping point for the recursive stack, exiting the recursion; for trees, this will often be leaf nodes. Since our recursive calls will be on left and right subtrees that may not exist, we have to be prepared to handle null nodes. That was a lot, so let's write it out. The general format for recursion on trees will come in handy. 

1. Base case (often leaf or null nodes)
2. Recursive subcalls on left and right subtrees 
3. Combine results of subcalls for the answer 

Often times when doing these problems, the question to ask is, what decision or operation am I making at every node, and how do I combine the results of these decisions? How does the results for the subtrees of a particular node impact the result of that node?

1. Given the root to a binary tree, count the total number of nodes.  
We count the number of nodes in the subtree rooted by any node by counting the node itself, and the size of its subtrees. This directly translates into the Python function below in which, if the node is not a null node (which will be the case when we recurse on a nonexistent left/right child) we add 1 and proceed to count the subtrees. Though the function looks simple, the recursive stack will count every single node in the tree. 
````
def size(root): 
	# base case: null node 
	if root == None: 
		return 0 
	# count this node, then recurse on left and right subtrees, combining results with summation. 
	return 1 + size(root.left) + size(root.right)
````

2. Count the number of leaf nodes in a binary tree. 
We modify the more general count function seen above to count only leaf nodes in the following function. 
````
def count_leaves(root): 
	if root == None: 
		return 0 
	# if leaf node, return 1
	if root.left == None and root.right == None: 
		return 1
	# recurse on left and right subtrees, combine results with addition.
	return count_leaves(root.left) + count_leaves(root.right)

3. Find the height of a binary tree, also known as the height of its root, or the number of edges between the root and the deepest leaf.   
What decision are we making at an arbitrary node if we want to ultimately get the height of the tree? Well, we know each node has two subtrees that may or may not have the same heights. To find the full binary tree's height, we need to consider only the height of the larger subtree at each node. Therefore, we are "combining" the results of the two recursive calls by taking their max, and then adding 1 (representing the current node height itself). This returns the height of the full binary tree. 
````
def get_height(root):
	# base case: null node 
	if root == None: 
		return 0 
	# recursive calls on subtrees to determine their heights
	left_height = get_height(root.left)
	right_height = get_height(root.right)
	# "combine" the results by taking the maximum height of the node's subtrees, and adding 1
	return max(left_height, right_height) + 1
````

4. Check if a binary tree (non-search) contains a specific node. 
What decision are we making at each node? Well, we just want to know if the current node is the key node we are searching for. If it is, we can return True. If it is not, we can recurse on both left and right subtrees to continue the search.   
This time, the way we are combining our recursive calls is with a logical OR operation, as the key can be contained in either subtree. Note that since this is not a binary search tree, we must continue to search both left and right subtrees, instead of being able to know which side to look at. This means that our time complexity will be O(n) where n is the number of nodes in the tree, instead of the O(logn) search provided by binary search trees.
```` 
def contains(root, key): 
	if root == None: 
		return False 
	# Found key?
	if root.val == key: 
		return True 
	# Recurse on left and right subtrees, combine results with logical OR 
	return contains(root.left, key) or contains(root.right, key)
```` 