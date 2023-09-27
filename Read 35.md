# Graphs

A graph is a fundamental data structure in computer science and mathematics that models relationships between objects. It's a versatile tool used in various applications, including computer networks, social networks, routing algorithms, and more.

## Terminology

Vertex (Node): A vertex, often called a node, represents an object or entity in the graph. Each vertex can have zero or more connections to other vertices.

Edge: An edge is a connection between two vertices, indicating a relationship or interaction.

Neighbor: Neighbors of a vertex are other vertices connected to it through edges.

Degree: The degree of a vertex is the number of edges connected to it. In an undirected graph, it's the number of neighbors.

Directed vs. Undirected Graphs

Undirected Graph: In an undirected graph, edges have no direction, and connections are bi-directional. It's like a friendship on social media; if you're friends with someone, they are also friends with you.

Directed Graph (Digraph): In a directed graph, each edge has a direction, indicating a one-way relationship. It's like following someone on social media; you can follow them without them following you back.

Types of Graphs

Complete Graph: In a complete graph, every vertex is connected to every other vertex. It's like a tightly knit community where everyone knows everyone.

Connected Graph: A connected graph has a path between every pair of vertices. It's like a web of connections where you can reach any person through mutual friends.

Disconnected Graph: A disconnected graph has isolated components with no connection between them. It's like several separate islands in a vast ocean.

## Acyclic vs. Cyclic Graphs

Acyclic Graph (DAG - Directed Acyclic Graph): An acyclic graph has no cycles, meaning you can't start from a vertex and follow edges to return to the same vertex. It's like a family tree with no loops.

Cyclic Graph: A cyclic graph contains cycles, allowing you to follow edges and return to the same vertex. It's like a loop in a social network where you can follow friends and eventually come back to yourself.

Graph Representation

 ## Graphs can be represented in two main ways:

Adjacency Matrix: An adjacency matrix is a 2D array where each row and column represent vertices. A value at (i, j) indicates an edge between vertex i and vertex j.

Adjacency List: An adjacency list is a collection of linked lists or arrays. Each vertex has a list of its neighboring vertices, representing its connections.

## Weighted Graphs

In weighted graphs, edges have associated values or weights. These weights can represent distances, costs, or any other relevant metric. Weighted graphs are used in applications like route planning and optimization.

 ## Graph Traversals

Traversing a graph means visiting its vertices and edges in a systematic way. There are two common methods:

Breadth-First Traversal: Start at a vertex and visit all its neighbors before moving to their neighbors. It's like exploring all immediate friends before moving to friends of friends.

Depth-First Traversal: Start at a vertex and explore as far as possible along each branch before backtracking. It's like diving deep into a topic before switching to another.

Real-World Uses of Graphs

Graphs are used extensively in real-world applications:

GPS and Mapping: Graphs help find the shortest route between locations on maps.

Driving Directions: Algorithms use graphs to provide step-by-step driving directions.

Social Networks: Friendships and connections on social media are represented using graphs.

Airline Traffic: Flight routes and connections between airports form a graph.

Recommendation Systems: Services like Netflix use graphs to recommend movies or products based on user preferences.

This overview provides a solid foundation for understanding graphs and their significance in various domains.