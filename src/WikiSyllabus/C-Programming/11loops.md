# Loops

Looping Statements in C execute the sequence of statements many times until the stated condition becomes false. A loop in C consists of two parts, a body of a loop and a control statement. The control statement is a combination of some conditions that direct the body of the loop to execute until the specified condition becomes false. The purpose of the C loop is to repeat the same code a number of times.

## Types of Loops in C

Depending upon the position of a control statement in a program, looping statement in C is classified into two types:

1. Entry controlled loop

2. Exit controlled loop

### 1. Entry controlled loop

In an entry control loop in C, a condition is checked before executing the body of a loop. It is also called as a pre-checking loop.

In an exit controlled loop, a condition is checked after executing the body of a loop. It is also called as a post-checking loop.

![](assets/entryloopflow.png)

&#39;C&#39; programming language provides us with three types of loop constructs:

1. The while loop

2. The do-while loop

3. The for loop

| **Sr. No.** | **Loop Type** | **Description** |
| --- | --- | --- |
| 1. | While Loop | In while loop, a condition is evaluated before processing a body of the loop. If a condition is true then and only then the body of a loop is executed. |
| --- | --- | --- |
| 2. | Do-While Loop | In a do...while loop, the condition is always executed after the body of a loop. It is also called an exit-controlled loop. |
| 3. | For Loop | In a for loop, the initial value is performed only once, then the condition tests and compares the counter to a fixed value after each iteration, stopping the for loop when false is returned. |

## While Loop in C

A while loop is the most straightforward looping structure. While loop syntax in C programming language is as follows:

Syntax of While Loop in C:

		while (condition) {

		statements;

		}

It is an entry-controlled loop. In while loop, a condition is evaluated before processing a body of the loop. If a condition is true then and only then the body of a loop is executed. After the body of a loop is executed then control again goes back at the beginning, and the condition is checked if it is true, the same process is executed until the condition becomes false. Once the condition becomes false, the control goes out of the loop.

After exiting the loop, the control goes to the statements which are immediately after the loop. The body of a loop can contain more than one statement. If it contains only one statement, then the curly braces are not compulsory. It is a good practice though to use the curly braces even we have a single statement in the body.

Following program illustrates while loop in C programming example:

		#include<stdio.h>
		#include<conio.h>
		int main()
		{
			int num=1;	//initializing the variable
			while(num<=10)	//while loop with condition
			{
				printf("%d\n",num);
				num++;		//incrementing operation
			}
			return 0;
		}
Output:

		1
		2
		3
		4
		5
		6
		7
		8
		9
		10

## **Do-While loop in C**

A do...while loop in C is similar to the while loop except that the condition is always executed after the body of a loop. It is also called an exit-controlled loop.

Syntax of do while loop in C programming language is as follows:

**Syntax of Do-While Loop in C:**

		do {

		statements

		} while (expression);

As we saw in a while loop, the body is executed if and only if the condition is true. In some cases, we have to execute a body of the loop at least once even if the condition is false. This type of operation can be achieved by using a do-while loop.

In the do-while loop, the body of a loop is always executed at least once. After the body is executed, then it checks the condition. If the condition is true, then it will again execute the body of a loop otherwise control is transferred out of the loop.

Similar to the while loop, once the control goes out of the loop the statements which are immediately after the loop is executed.

The following loop program in C illustrates the working of a do-while loop:

Below is a do-while loop in C example to print a table of number 2:

		#include<stdio.h>
		#include<conio.h>
		int main()
		{
			int num=1;	//initializing the variable
			do	//do-while loop 
			{
				printf("%d\n",2*num);
				num++;		//incrementing operation
			}while(num<=10);
			return 0;
		}
Output:

		2
		4
		6
		8
		10
		12
		14
		16
		18
		20


## For loop in C

A for loop is a more efficient loop structure in &#39;C&#39; programming. The general structure of for loop syntax in C is as follows:

### Syntax of For Loop in C:

		for (initial value; condition; incrementation or decrementation )

		{

		statements;

		}

- The initial value of the for loop is performed only once.
- The condition is a Boolean expression that tests and compares the counter to a fixed value after each iteration, stopping the for loop when false is returned.
- The incrementation/decrementation increases (or decreases) the counter by a set value.

Following program illustrates the for loop in C programming example:

		#include<stdio.h>
		int main()
		{
			int number;
			for(number=1;number<=10;number++)	//for loop to print 1-10 numbers
			{
				printf("%d\n",number);		//to print the number
			}
			return 0;
		}
Output:

		1
		2
		3
		4
		5
		6
		7
		8
		9
		10



