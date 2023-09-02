# Bidirectional-Astar
It is an extension of the A* algorithm that aims to improve the efficiency of finding the shortest path between a start node and a goal node in a graph. It employs two simultaneous searches, one starting from the start node and the other starting from the goal node, with the goal of meeting in the middle and minimizing the search space.
Algorithm Description:

1.	Initialization:
•	The algorithm initializes open sets, closed sets, and dictionaries to manage costs and parent nodes for the forward and backward search directions.
•	A variable intersection is established to identify the node where the searches converge.
2.	Bidirectional Search:
•	The algorithm alternates between the forward and backward directions, searching for the node with the lowest f value (incorporating cost and heuristic).
•	Searches continue until an intersection is located or both open sets are exhausted.
3.	Expansion and Update:
•	The algorithm expands nodes by exploring neighbours and calculating tentative g values based on the current path.
•	Nodes in the closed set are bypassed.
•	If a node is absent from the open set or possesses a better g value, it is updated with new parent, g, and f values.
4.	Path Reconstruction:
•	Upon finding the intersection, the algorithm reconstructs the complete path by tracing parents from the source to the intersection and from the intersection to the destination.
•	The resulting path is stored for further analysis.
5.	Output:
•	If no intersection is discovered, the algorithm reports "Path not found!" and returns a None value.
•	In case of successful intersection, the algorithm presents "Path found:" followed by the actual path and returns the path list.
6.	Graph and Heuristic Definition:
•	The graph, represented as an adjacency list, maps each node to its neighbours and respective edge costs.
•	Heuristic h values are supplied to approximate the remaining cost from each node to the destination.
7.	Source and Destination Nodes:
•	The source and destination nodes (src and dst) are specified.
8.	Function Invocation:
•	The Bidirectional A* function is invoked with the source and destination nodes to reveal the shortest path.
