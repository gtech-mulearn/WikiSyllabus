# Control Statements

If statements in C are used to control the program flow based on some condition, it is used to execute some statement code block if the expression is evaluated to true. Otherwise, it will get skipped. This is the simplest way to modify the control flow of the program

The if statement in C can be used in various forms depending on the situation and complexity.

There are four different types of if statement in C. These are:

* Simple if Statement
* if-else Statement
* Nested if-else Statement
* else-if Ladder

## Simple if Statement

The basic format of if statement is:

```text
if(test_expression)
{
    statement 1;
    statement 2;
    ...
}
```

'Statement n' can be a statement or a set of statements, and if the test expression is evaluated to true, the statement block will get executed, or it will get skipped.

Flowchart

![](https://github.com/AswinS07/C_programming/tree/82e0997762ed854b7866a18af2d94261b81a2838/_includes/c-if.png)

## if-else Statement

If else statements in C are also used to control the program flow based on some condition, only the difference is: it is used to execute some statement code block if the expression is evaluated to true, otherwise executes else statement code block.

The basic format of if else statement is:

```text
if(test_expression)
{
   //execute your code
}
else
{
   //execute your code
}
```

Flowchart

![](https://github.com/AswinS07/C_programming/tree/82e0997762ed854b7866a18af2d94261b81a2838/_includes/c-if-else.png)

## Nested if-else Statement

Nested if-else statements play an important role in C programming, it means you can use conditional statements inside another conditional statement.

The basic format of Nested if-else statement is:

```text
if(test_expression one)
{
   if(test_expression two) {

      //Statement block Executes when the boolean test expression two is true.
   }
}
else
{
    //else statement block
}
```

## else-if Ladder

else-if statements in C is like another if condition, it's used in a program when if statement having multiple decisions.

The basic format of else-if statement is:

```text
if(test_expression)
{
   //execute your code
}
else if(test_expression n)
{
   //execute your code
}
else
{
   //execute your code
}
```

