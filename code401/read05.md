# Linked Lists

### What is a Linked List?


***A Linked List is a sequence of Nodes that are connected/linked to each other. The most defining feature of a Linked List is that each Node references the next Node in the link.***


> There are two types of Linked List - 

- Singly 

- Doubly

*We will be implementing a Singly Linked List in this implementation.*


## Terminology:

- **Linked List** - A data structure that contains nodes that links/points to the next node in the list.

- **Singly** - Singly refers to the number of references the node has. A Singly linked list means that there is only one reference, and the reference points to the Next node in a linked list.

- **Doubly** - Doubly refers to there being two (double) references within the node. A Doubly linked list means that there is a reference to both the Next and Previous node.

- **Node** - Nodes are the individual items/links that live in a linked list. Each node contains the data for each link.

- **Next** - Each node contains a property called Next. This property contains the reference to the next node.

- **Head** - The Head is a reference of type Node to the first node in a linked list.

- **Current** - The Current is a reference of type Node to the node that is currently being looked at. When traversing, you create a new Current variable at the Head to guarantee you are starting from the beginning of the linked list.


### This is what a Singly Linked List looks like:-


![Singly Linked List](https://codefellows.github.io/common_curriculum/data_structures_and_algorithms/Code_401/class-05/resources/images/LinkedList1.PNG)


> **Traversal**


***The best way to approach a traversal is through the use of a while() loop. This allows us to continually check that the Next node in the list is not null. If we accidentally end up trying to traverse on a node that is null, a NullReferenceException gets thrown and our program will crash/end.***



### Let’s talk out what exactly is happening:

> 1- **We are first creating Current at the Head to guarantee we are starting from the beginning. (Remember that Head is always the first node in a Linked List)**

> 2- **We create a while loop. This loop will only run if the node that Current is pointing to is not null. This also means we can guarantee that we are still looking at a Node while the loop is running.**

> 3- **Once we are in the while loop, we are checking if the value of the current node is equal to the value we are looking for. Given the logic, if that condition is true, then we have found the value we were looking for, so we return true.**

> 3- **If the Current node does not contain the value we are looking for, we then must move Current to the next node that is being referenced. Again, because the condition of this while loop is to only run if we are still at a node, we can safely traverse to the next node without fear of getting a NullReferenceException.**

> 4- **At this point, the while loop is re-evaluated. Step 3 & 4 will continue until Current reaches the end of the LinkedList. We will know we are at the last node in the linked list because the current node will be null. Once this condition becomes true, the while loop breaks, and we now know that we are at the end.**

> 5- **Once we hit the end, we know that we did not find the value and return true at any point, so the value is not in the LinkedList. We return false.**




### Prerequisites

> When constructing your code, a few things to keep in mind.

- **When making your Node class, consider requiring a value to be passed in to require that each node has a value.**


