# continue Statement

Continue is also a loop control statement just like the break statement. Continue statement is opposite to that of break _statement_, instead of terminating the loop, it forces to execute the next iteration of the loop.

As the name suggest the continue statement forces the loop to continue or execute the next iteration. When the continue statement is executed in the loop, the code inside the loop following the continue statement will be skipped and next iteration of the loop will begin.

![](assets/continue_syntax.png)

**Example** :

Consider the situation when you need to write a program which prints number from 1 to 10 and but not 6. It is specified that you have to do this using loop and only one loop is allowed to use.

Here comes the usage of continue statement. What we can do here is we can run a loop from 1 to 10 and every time we have to compare the value of iterator with 6. If it is equal to 6 we will use the _continue_ statement to continue to next iteration without printing anything otherwise we will print the value.

Below is the implementation of the above idea:

![](assets/continue_example.png)

**Output:**

![](assets/continue_ex_output.png)

The _continue_ statement can be used with any other loop also like while or do while in a similar way as it is used with for loop above.

