# Dynamic Programming

- Dynamic programming is an algorithm design method that can be used when the solution to a problem can be viewed as the result of a sequence of decisions.
- Dynamic Programming is mainly an optimization over plain recursion.
- Wherever we see a recursive solution that has repeated calls for same inputs, we can optimize it using Dynamic Programming.
- The idea is to simply store the results of subproblems, so that we do not have to re-compute them when needed later.
- This simple optimization reduces time complexities from exponential to polynomial.
- For example, if we write simple recursive solution for Fibonacci Numbers, we get exponential time complexity and if we optimize it by storing solutions of subproblems, time complexity reduces to linear.
- In dynamic programming an optimal sequence of decisions is obtained by making explicit appeal to the principle of optimality.

## The Optimality Principle

- **Definition**: The principle of optimality states that an optimal sequence of decisions has the property that whatever the initial state and decision are, the remaining decisions must constitute an optimal decision sequence with regard to the state resulting from the first decision.
- A problem is said to satisfy the Principle of Optimality if the subsolutions of an optimal solution of the problem are themselves optimal solutions for their subproblems.
- **Examples**:
  - The shortest path problem satisfies the Principle of Optimality.
  - This is because if a,x1,x2,...,xn,b is a shortest path from node a to node b in a graph, then the portion of xi to xj on that path is a shortest path from xi to xj.

## Characteristics of Dynamic Programming

1. **Overlapping Subproblems**
   - Subproblems are smaller versions of the original problem. Any problem has overlapping sub-problems if finding its solution involves solving the same subproblem multiple times.
   - Dynamic Programming also combines solutions to sub-problems. It is mainly used where the solution of one sub-problem is needed repeatedly. The computed solutions are stored in a table, so that these don’t have to be re-computed. Hence, this technique is needed where overlapping sub-problem exists.
   - For example, Binary Search does not have overlapping sub-problem. Whereas recursive program of Fibonacci numbers have many overlapping sub-problems.

2. **Optimal Substructure**
   - A given problem has Optimal Substructure Property, if the optimal solution of the given problem can be obtained using optimal solutions of its sub-problems.
   - For example, the Shortest Path problem has the following optimal substructure property: If a node x lies in the shortest path from a source node u to destination node v, then the shortest path from u to v is the combination of the shortest path from u to x, and the shortest path from x to v.

## Steps of Dynamic Programming

- Dynamic programming design involves 4 major steps:
  1. Characterize the structure of an optimal solution.
  2. Recursively define the value of an optimal solution.
  3. Compute the value of an optimal solution, typically in a bottom-up fashion.
  4. Construct an optimal solution from computed information.

## Optimal Matrix Multiplication

- Suppose we wish to compute the product of 4 matrices A1 x A2 x A3 x A4
- The different parenthesizations are:
  - ( A1(A2( A3 A4)))
  - ( A1((A2 A3) A4))
  - ( (A1A2)( A3 A4))
  - (( A1(A2 A3))A4)
  - ((( A1A2) A3)A4)
- We can multiply two matrices A and B if and only if they are compatible: The number of columns of A must be equal to the number of rows of B.
- If A is a pXq matrix and B is a qXr matrix, the resulting matrix C is a pX r matrix.
- The time to compute C is pqr.
- We shall express costs in terms of the number of scalar multiplications.
- **Example**:
  - Consider 3 matrices A1, A2 and A3. Its dimensions are 10X100, 100X5, 5X50 respectively.
  - Number of scalar multiplications for:
    - ((A1A2) A3) is 7500
    - (A1 (A2A3)) is 75000
  - Thus, computing the product according to the first parenthesization is 10 times faster.

### Matrix-Chain Multiplication Problem

- Given a chain (A1, A2, . . . An ) of n matrices, where for i = 1, 2, . . . n, matrix Ai has dimension pi-1 X pi , fully parenthesize the product A1A2. . . An in a way that minimizes the number of scalar multiplications.
- In the matrix-chain multiplication problem, we are not actually multiplying matrices.
- Our goal is only to determine an order for multiplying matrices that has the lowest cost.

### Matrix Chain Multiplication: Dynamic Programming Method

1. **The structure of an optimal parenthesization**
   - Ai. .j denote the matrix that results from evaluating the product AiAi+1 . . . Aj where i <= j.
   - If i < j, we must split the problem into two subproblems (Ai Ai+1 . . . Ak and Ak+1Ai+1 . . . Aj ), for some integer k in the range i <= k < j.
   - That is, for some value of k, we first compute the matrices Ai. .k and Ak+1. .j. Then multiply them together to produce the final product Ai. .j .
   - Total cost = Cost of computing the matrix Ai. .k + Cost of computing Ak+1. .j + Cost of multiplying them together.

2. **A recursive solution**
   - We can define the cost of an optimal solution recursively in terms of the optimal solutions to subproblems.
   - Let m[i, j] be the minimum number of scalar multiplications needed to compute the matrix Ai. .j
   - For the full problem, the lowest cost way to compute A1. .n would thus be m[1, n].
   - Ai. .i = Ai so m[i,i] = 0 for i=1,2,. .. . n
   - s[i,j] be a value of k at which we split the product AiAi+1 . . . Aj in an optimal parenthesization.
   - This will take exponential time.

3. **Computing the optimal costs**
   - Compute the optimal cost by using a tabular, bottom-up approach.

```python
Algorithm Matrix_Chain_Order(p)
{
  n = p.length – 1
  Let m[1..n, 1..n] and s[1..n-1 , 2..n] be new tables
  for i=1 to n do
    m[i,i] = 0
  for l=2 to n do
  {
    for i=1 to n-l+1 do
    {
      j=i+l-1
      m[i,j] = ∞
      for k=i to j-1 do
      {
        q = m[i,k] + m[k+1,j] + pi-1 * pk * pj
        if q < m[i,j] then
        {
          m[i,j] = q
          s[i,j] = k
        }
      }
    }
  }
  return m[][] and s[][]
}
```

4. **Constructing an optimal solution**
   
```python
Algorithm Print_Optimal_Parens(s,i,j)
{
if i==j then
print “A”i
else
print “(“
print_Optimal_Parens(s,i,s[i,j])
print_Optimal_Parens(s,s[i,j]+1,j)
print “)”

}
```

## Time Complexity
- We are generating n(n-1)/2 number of elements in matrix m[].
- To calculate each element it will take atmost n time.
- So the time complexity = O( n.n(n-1)/2) = O(n3)



