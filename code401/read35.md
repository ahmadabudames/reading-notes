# Graphs

**A graph is a non-linear data structure that can be looked at as a collection of vertices (or nodes) potentially connected by line segments named edges.**


> **Here is some common terminology used when working with Graphs:**

- **Vertex** - A vertex, also called a “node”, is a data object that can have zero or more adjacent vertices.

- **Edge** - An edge is a connection between two nodes.

- **Neighbor** - The neighbors of a node are its adjacent nodes, i.e., are connected via an edge.

- **Degree** - The degree of a vertex is the number of edges connected to that vertex.

## Directed vs Undirected

**Undirected Graphs**

An Undirected Graph is a graph where each edge is undirected or bi-directional. This means that the undirected graph does not move in any direction.

For example, in the graph below, Node C is connected to Node A, Node E and Node B. There are no “directions” given to point to specific vertices. The connection is bi-directional.

![](https://codefellows.github.io/common_curriculum/data_structures_and_algorithms/Code_401/class-35/resources/assets/UndirectedGraph.PNG)


**Directed Graphs (Digraph)***

A Directed Graph also called a Digraph is a graph where every edge is directed.

Unlike an undirected graph, a Digraph has direction. Each node is directed at another node with a specific requirement of what node should be referenced next.

Compare the visual below with the undirected graph above. Can you see the difference? The Digraph has arrows pointing to specific nodes.

![](https://codefellows.github.io/common_curriculum/data_structures_and_algorithms/Code_401/class-35/resources/assets/DirectedGraph.PNG)


## Complete vs Connected vs Disconnected

**Complete Graphs**


> A complete graph is when all nodes are connected to all other nodes.

![](https://codefellows.github.io/common_curriculum/data_structures_and_algorithms/Code_401/class-35/resources/assets/CompleteGraph.PNG)


**Connected**

> A connected graph is graph that has all of vertices/nodes have at least one edge.

![](https://codefellows.github.io/common_curriculum/data_structures_and_algorithms/Code_401/class-35/resources/assets/ConnectedGraph.PNG)

**Disconnected**

> A disconnected graph is a graph where some vertices may not have edges.

![](https://codefellows.github.io/common_curriculum/data_structures_and_algorithms/Code_401/class-35/resources/assets/DisconnectedGraph.PNG)

## Traversals

> **Here is what the algorithm breadth first traversal looks like:**

- 1-**Enqueue** the declared start node into the Queue.

- 2-Create a loop that will run while the node still has nodes present.

- 3-**Dequeue** the first node from the queue.

- 4-if the **Dequeue‘d** node has unvisited child nodes, add the unvisited children to visited set and insert them into the queue.



### Here is a breakdown of what is going on:

- 1-We have declared that our starting node (or root) is going to be Node A.

- 2-The first thing we want to do is Enqueue the root.

- 3-We also need to add the root to the visited set.

- 4-Next, we enter a while loop. We want this loop to keep running until there are no more nodes in our queue.

- 5-Once we are in the while loop, we want to Dequeue the front node and then check to see if it has any children.

- 6-if there are children of the node we are currently looking at, we want to add them to visited set. This will help us know that we have already seen that node before, and won’t accidently push us into an infinite loop if the graph was cyclic. In addition to tracking each child node as visited, we want to place any of its children that have not yet been visited into the queue.

- 7-The process will complete until the queue is empty.

- 8-Once the while loop breaks, we can then return the list of nodes. This list will contain, in order, all the nodes that were traversed.



