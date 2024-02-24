# Dijkstras-Algorithm
A series of files that work together to establish vertices and edges of a graph as well as connect them to one another, and allow the graph to be searched and a shortest path made between any two vertices. Time complexity of O(E*Log(V)) due to usage of adjacency list.

Each node stores its shortest path in a vector of strings. So if trying to get from A to D, A stores itself, B stores <"A","B">, C stores <"A", "B", "C"> etc. By the end, the goal node will store a vector with the exact path from the start to itself. When assigning this vector of strings, the current node takes the previous node's vector of strings and adds itself onto the end. So for C to assign its shortest_path as <"A", "B", "C">, it would copy B's shortest path, <"A","B">, then add "C" to the end.

Old paths are only overwritten when the current path would be shorter than the established path, so no time is wasted on equal paths.

All nodes must be checked to ensure no faster path is being missed.
