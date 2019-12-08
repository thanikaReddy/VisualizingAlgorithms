## Visualizing Algorithms using D3
This repository contains visualizations of the following algorithms.

### Binary Search 
- This visualization demonstrates how binary search is performed on a sorted array of integers 1 to 400. 
- The 400 vertical lines of varying heights represent the sorted array. The height is proportional to the magnitude of an element in the array.
- Enter a number between 1 to 400 in the search box and click the search button to see the sequence of steps binary search takes. 
- Lines in orange are part of the active array (i.e. the part of the array the element exists within)
- A line in blue represents the middle element of the active array.
- D3 features used: Scale bands, transitions and transformations. 

### Inorder traversal of a Binary Tree
- This visualization shows the sequence of recursive calls made during an inorder traversal. 
- A subtree colored in purple is the one the recursive function is called with. It represents the recusive function call at a certain level of the call stack.
- When a node has blue rings around it, it means it is "visited".
- Enter a comma separated sequence of letters (that represent a binary tree) in the input box. Then click the arrow to render the tree and beigin the animation. An example input is a,b,c,d,e,f,g,h,i,j (which represents a binary tree with 4 levels, the last level is not complete).
- D3 features used: Tree, Heirarchy

### Conversion of an N-ary tree to a Binary Tree
- This is a visualization of the following algorithm to convert an N-ary tree to a binary tree: the left most child of a node stays its left child even in the binary tree. It's right child in the binary tree is its immediate right sibling in the N-ary tree. But when the function to convert an N-ary tree to a binary tree is called recursively, it doesn't know the root node's sibling in the N-ary tree becuase that node isn't part of this subtree. There is thus no way for the recursive funnction to fill in the root's right child. It fills in the left subtree and returns it. The calling function then fills in the right tree (because it knows the right sibling). Butthe right sibling's (N-ary) subtree should first be converted to a binary tree. At any point, there are therefore multiple binary trees in memory and each one is used to build the other. 
- The N-ary tree is shown to the left. The subtree colored in purple is the one with which the recursive function is called or the one whose function the control is presently in. There is one binary tree associated with this particular function (or this particular N-ary subtree) and it is highlighted in yellow. The greyed out binary trees also exist in memory at any point of time, they are just not the binary tree created for the N-ary sub tree in question. Notice that a binary trees to the right gets "plugged into" the tree to its left, i.e. it is returned by the one call to the function and assigned as a subtree in the parent node's function. 
- Enter a string in the following format and click the arrow to render the corresponding N-ary tree and watch how its corresponding binary tree is build: a,#b,c,d,#e,f,#g,#h,i,j,k,#l,m,#n,o,#p,q
