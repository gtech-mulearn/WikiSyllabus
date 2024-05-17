# Floyd Warshall Algorithm

- The Floyd Warshall Algorithm is for solving the All Pairs Shortest Path problem.
- Negative edge weights are also allowed.
- As a result of this algorithm, it will generate a matrix, which will represent the minimum
distance from any node to all other nodes in the graph.
- Inputs are the adjacency matrix of the given graph and the total number of vertices.

```plaintext
Algorithm FloydWarshall(cost[][], n)
{
    for i = 1 to n do
        for j = 1 to n do
            D[i, j] = cost[i, j]

    for k := 1 to n do
        for i := 1 to n do
            for j := 1 to n do
                D[i, j] = min{D[i, j], D[i, k] + D[k, j]}

    Return D
}
```

## Time Complexity

- Floyd Warshall Algorithm consists of three loops over all the nodes. Each loop has constant complexities.
- Hence, the time complexity of Floyd Warshall algorithm = O(n^3), where n is the number of nodes in the given graph.
  

![Screenshot 2024-05-17 212206](https://github.com/athul-2003/WikiSyllabus/assets/128019369/1c065497-7227-45d6-8fbc-c05a9e86c2df)
![Screenshot 2024-05-17 213114](https://github.com/athul-2003/WikiSyllabus/assets/128019369/45162c03-f3ef-4c7b-b7d8-d3757682791a)
![Screenshot 2024-05-17 213245](https://github.com/athul-2003/WikiSyllabus/assets/128019369/090be10f-0569-4c84-9abe-996d4f852a60)
