# N-Queens Problem

![Screenshot 2024-05-17 222513](https://github.com/athul-2003/WikiSyllabus/assets/128019369/e3d29214-7ae4-49f2-b186-f59a570b4e13)

- For example, the following is a solution for the 4 Queen problem.

![Screenshot 2024-05-17 222900](https://github.com/athul-2003/WikiSyllabus/assets/128019369/8b8955e5-cbf0-459e-b94b-5369c1f8f6d2)


- Consider an \(n * n\) chessboard and try to find all possible ways to place \(n\) non-attacking queens.
- \( (x_1, x_2, ..., x_n) \) be the solution vector. Queen \(i\) is placed in the \(i^{th}\) row and \(x_i^{th}\) column. \(x_i\) will all be distinct since no two queens can be placed in the same column.

- There are 2 types of diagonals:
  - **Positive Diagonal**:
    - Diagonal from upper left to lower right.
    - Every element on the same diagonal has the same row-column value.
    - Suppose 2 queens are placed at position \((i,j)\) and \((k,l)\), then \(i-j = k-l\).
  - **Negative Diagonal**:
    - Diagonal from upper right to lower left.
    - Every element on the same diagonal has the same row+column value.
    - Suppose 2 queens are placed at position \((i,j)\) and \((k,l)\), then \(i+j = k+l\).
    - The 1st equation implies: \(i-k = j-l\).
    - The 2nd equation implies: \(i-k = l-j\).
    - Combining these two, we will get: \(|i-k| = |j-l|\). Absolute value of column difference is equal to the absolute value of row difference.

```cpp
Algorithm NQueens(k,n)
{
    for i=1 to n do
    { 
        if Place(k,i) then
        { 
            x[k] = i
            if(k==n) then write(x[1:n])
            else NQueens(k+1, n)
        }
    }
}
```
```cpp
Algorithm Place(k,i)
{
    for j=1 to k-1 do
    {
        if( (x[j]==i) or ( Abs(j-k)==Abs(x[j]-i) ) then
            Return false
    }
    Return true
}
```

- `Place(k,i)` returns true if the \(k^{th}\) queen can be placed in column \(i\).
  - \(i\) should be distinct from all previous values \(x[1]\), \(x[2]\), ..., \(x[k-1]\).
  - And no 2 queens are to be on the same diagonal.
  - Time complexity of Place() is \(O(k)\).

- `NQueen()` is initially invoked by `NQueen(1,n)`.
  - Time complexity of NQueen() is \(O(n!)\).
 
# Backtracking works on 4-Queens Problem

- If \( (x_1, x_2, ..., x_i) \) is the path to the current E-node, then all children nodes with parent-child labeling \( x_{i+1} \) are such that \( (x_1, x_2, ..., x_{i+1}) \) represents a chessboard configuration in which no two queens are attacking.
- We start with the root node as the only live node. This becomes the E-node and the path is ().
- We generate one child (node 2) and the path is now (1). This corresponds to placing queen 1 on column 1.
- Node 2 becomes the E-node. Node 3 is generated and immediately killed.
- The next node generated is node 8 and the path becomes (1,3). Node 8 becomes the E-node. However, it gets killed as all its children represent board configurations that cannot lead to an answer node.
- We backtrack to node 2 and generate another child node 13. The path is now (1,4). This process continues until it will generate a proper arrangement.


![Screenshot 2024-05-17 223544](https://github.com/athul-2003/WikiSyllabus/assets/128019369/ae28eebb-42ed-405a-8159-e29c729cb4d3)
