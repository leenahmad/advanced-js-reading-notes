# Trees 

A tree data structure can be defined recursively as a collection of nodes, where each node is a data structure consisting of a value and a list of references to nodes. The start of the tree is the "root node" and the reference nodes are the "children". No reference is duplicated and none points to the root.



- Node - A Tree node is a component which may contain its own values, and references to other nodes
+ Root - The root is the node at the beginning of the tree
- K - A number that specifies the maximum number of children any node may have in a k-ary tree. In a binary tree, k = 2.
+ Left - A reference to one child node, in a binary tree
- Right - A reference to the other child node, in a binary tree
+ Edge - The edge in a tree is the link between a parent and child node
- Leaf - A leaf is a node that does not have any children
+ Height - The height of a tree is the number of edges from the root to the furthest leaf


![trees](https://miro.medium.com/max/975/1*PWJiwTxRdQy8A_Y0hAv5Eg.png)



***Given the sample tree above, our traversals would result in different paths:***

+ Pre-order: A, B, D, E, C, F
- In-order: D, B, E, A, F, C
+ Post-order: D, E, B, F, C, A


### Big O

The Big O time complexity of a Binary Search Tree’s insertion and search operations is O(h), or O(height). In the worst case, we will have to search all the way down to a leaf, which will require searching through as many nodes as the tree is tall. In a balanced (or “perfect”) tree, the height of the tree is log(n). In an unbalanced tree, the worst case height of the tree is n.

The Big O space complexity of a BST search would be O(1). During a search, we are not allocating any additional space.


[you can read more about tree here](https://codefellows.github.io/common_curriculum/data_structures_and_algorithms/Code_401/class-15/resources/Trees.html)

