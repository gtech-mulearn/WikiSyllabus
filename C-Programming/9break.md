# break Statement

The break in C or C++ is a loop control statement which is used to terminate the loop. As soon as the break statement is encountered from within a loop, the loop iterations stops there and control returns from the loop immediately to the first statement after the loop.

**Syntax:**

![](Breaksyntax.png)

Basically break statements are used in the situations when we are not sure about the actual number of iterations for the loop or we want to terminate the loop based on some condition.

![](Breakflowchart.png)

**We will see here the usage of break statement with three different types of loops:**

1. Simple loops
2. Nested loops
3. Infinite loops

Let us now look at the examples for each of the above three types of loops using break statement.

## 1. **Simple loops** : 
Consider the situation where we want to search an element in an array. To do this, use a loop to traverse the array starting from the first index and compare the array elements with the given key.

   Below is the implementation of this idea:

![](breaksimpleloops.png)

**Output:** 
![](Breaksimpleloopsoutput.png)

The above code runs fine with no errors. But the above code is not efficient. The above code completes all the iterations even after the element is found. Suppose there are **1000** elements in the array and the key to be searched is present at 1st position so the above approach will execute **999** iterations which are of no purpose and are useless. To avoid these useless iterations, we can use the break statement in our program. Once the break statement is encountered the control from the loop will return immediately after the condition gets satisfied. So will use the break statement with the if condition which compares the key with array elements as shown below:

![](breaksimpleloops2.png)
**Output:**

![](breaksimpleloops2output.png)

## 2. **Nested Loops** :
 We can also use break statement while working with nested loops. If the break statement is used in the innermost loop. The control will come out only from the innermost loop. Below is the example of using break with nested loops:

![](Breaknestedloops.png) 
**Output:**

![](Breaknestedloopsoutput.png)

In the above code we can clearly see that the inner loop is programmed to execute for 10 iterations. But as soon as the value of **j** becomes greater than 3 the inner loop stops executing which restricts the number of iteration of the inner loop to 3 iterations only. However the iteration of outer loop remains unaffected. **Therefore, break applies to only the loop within which it is present.**

