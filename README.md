# Graph ADT – Logistics Route Planner

A modular **Java Graph Abstract Data Type (ADT)** designed to model and optimize logistics and transportation networks. The project demonstrates how graph theory and shortest-path algorithms can be applied to real-world route planning problems.

## Project Overview

Cities or delivery locations are modeled as **vertices**, while roads are represented as **edges** (optionally weighted by distance, cost, or time). The system computes optimal delivery routes using **Dijkstra’s algorithm**, making it suitable for logistics and transport optimization scenarios.

The design emphasizes **scalability, reusability, and clean separation of concerns**, following solid object-oriented principles.

## Key Features

* Generic `Graph<T>` ADT implementation
* Supports:

  * Directed & undirected graphs
  * Weighted & unweighted edges
* Efficient adjacency-list representation
* Shortest-path computation using Dijkstra’s algorithm
* Full route reconstruction via predecessor tracking
* Stress-tested to handle large graphs (1M+ vertices/edges)
* Extensive JUnit test coverage

## Architecture

* **Graph<T>** – Core ADT managing vertices and edges
* **Location** – Domain object representing a city or delivery point
* **LogisticsNetwork** – Builds and maintains the graph structure
* **RoutePlanner** – Computes shortest routes using Dijkstra’s algorithm
* **Dijkstra / DijkstraResult<T>** – Pathfinding logic and results

## Algorithms & Complexity

* **Dijkstra’s Algorithm**:
  Time: `O((V + E) log V)`
  Space: `O(V + E)`

* Graph storage optimized for **sparse networks** using adjacency lists.

## Testing

* JUnit tests validate:

  * Basic graph operations
  * Edge cases and error handling
  * Vertex/edge removal
  * Self-loops and connectivity
  * Large-scale stress testing

All tests pass successfully, ensuring correctness and robustness.

## Example Use Case

```java
planner.findShortestRoute("Satu Mare", "Timisoara");
```

Outputs the shortest distance and path through intermediate cities using weighted edges.

## Future Extensions

* Time-dependent or traffic-aware edge weights
* Alternative algorithms (Bellman-Ford, A*, etc.)
* One-way streets and asymmetric costs
* Delivery constraints (time windows, capacity)

## Academic Context

Developed as part of **COMP47500 – Advanced Data Structures in Java**, showcasing the practical application of graph theory to logistics optimization.
