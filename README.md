**Shortest Path Algorithm**

This Python script implements a shortest path algorithm to find the shortest path between nodes in a weighted graph. The graph is represented using an adjacency list format, where each node maps to a list of tuples representing its neighbors and corresponding edge weights.

**Usage:**

Before using the script, ensure that you have defined your graph in the form of an adjacency list. The script includes a function `shortest_path(graph, start, target='')` that takes three parameters:

1. `graph`: The graph represented as an adjacency list.
2. `start`: The starting node for finding the shortest paths.
3. `target` (optional): The target node for which the shortest path is to be found. If not specified, the shortest paths from the starting node to all other nodes will be computed.

**Example:**

Suppose you have the following graph defined:

```python
my_graph = {
    'A': [('B', 5), ('C', 3), ('E', 11)],
    'B': [('A', 5), ('C', 1), ('F', 2)],
    'C': [('A', 3), ('B', 1), ('D', 1), ('E', 5)],
    'D': [('C', 1), ('E', 9), ('F', 3)],
    'E': [('A', 11), ('C', 5), ('D', 9)],
    'F': [('B', 2), ('D', 3)]
}
```

You can find the shortest path from node 'A' to node 'F' using the `shortest_path` function:

```python
shortest_path(my_graph, 'A', 'F')
```

This will output the shortest path from node 'A' to node 'F' along with its distance.

**Note:**

- The script utilizes Dijkstra's algorithm to find the shortest path in a weighted graph.
- If the `target` parameter is not specified, the script will compute the shortest paths from the starting node to all other nodes in the graph.
- Ensure that the graph is correctly defined in the adjacency list format, with node names as keys and lists of tuples representing neighbors and edge weights.
