# Trees

***Trees are non-linear data structures that represent nodes connected by edges. Each tree consists of a root node as the Parent node, and the left node and right node as Child nodes.***

## Common in the trees:-

- Node:-**A Tree node is a component which may contain it’s own values, and references to other nodes**

- Root:-**The root is the node at the beginning of the tree**

- K:-**A number that specifies the maximum number of children any node may have in a k-ary tree. In a binary tree, k = 2.**

- Left:-**A reference to one child node, in a binary tree**

- Right:-**A reference to the other child node, in a binary tree**

- Edge:-**The edge in a tree is the link between a parent and child node**

- Leaf:-**A leaf is a node that does not have any children**

- Height:-**The height of a tree is the number of edges from the root to the furthest leaf**


# Sample Tree:-

![](https://codefellows.github.io/common_curriculum/data_structures_and_algorithms/Code_401/class-15/resources/images/BinaryTree1.PNG)


## Traversals

- Pre-order: root >> left >> right

- In-order: left >> root >> right

- Post-order: left >> right >> root


![](https://codefellows.github.io/common_curriculum/data_structures_and_algorithms/Code_401/class-15/resources/images/tree-example.png)


# Binary Tree Vs K-ary Trees

***In all of our examples, we’ve been using a Binary Tree. Trees can have any number of children per node, but Binary Trees restrict the number of children to two (hence our left and right children).***

> **There is no specific sorting order for a binary tree. Nodes can be added into a binary tree wherever space allows. Here is what a binary tree looks like:**




![](https://codefellows.github.io/common_curriculum/data_structures_and_algorithms/Code_401/class-15/resources/images/BinaryTree2.PNG)


# K-ary Trees

**If Nodes are able have more than 2 child nodes, we call the tree that contains them a K-ary Tree. In this type of tree we use K to refer to the maximum number of children that each Node is able to have.**


![](https://codefellows.github.io/common_curriculum/data_structures_and_algorithms/Code_401/class-15/resources/images/KaryTree1.png)



### Big O


***The Big O time complexity for inserting a new node is O(n). Searching for a specific node will also be O(n). Because of the lack of organizational structure in a Binary Tree, the worst case for most operations will involve traversing the entire tree. If we assume that a tree has n nodes, then in the worst case we will have to look at n items, hence the O(n) complexity.***

***The Big O space complexity for a node insertion using breadth first insertion will be O(w), where w is the largest width of the tree. For example, in the above tree, w is 4.***

***A “perfect” binary tree is one where every non-leaf node has exactly two children. The maximum width for a perfect binary tree, is 2^(h-1), where h is the height of the tree. Height can be calculated as log n, where n is the number of nodes.***


### Searching a BST


***Searching a BST can be done quickly, because all you do is compare the node you are searching for against the root of the tree or sub-tree. If the value is smaller, you only traverse the left side. If the value is larger, you only traverse the right side.***

***Let’s say we are searching 15. We start by comparing the value 15 to the value of the root, 23.***

***15 < 23, so we traverse the left side of the tree. We then treat 8 as our new “root” to compare against.***

***15 > 8, so we traverse the right side. 16 is our new root.***

***15 < 16, so we traverse the left side. And aha! 15 is our new root and also a match with what we were searching for.***



![](https://codefellows.github.io/common_curriculum/data_structures_and_algorithms/Code_401/class-15/resources/images/BST2.PNG)















