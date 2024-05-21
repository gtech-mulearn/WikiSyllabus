# Operators

C language supports a rich set of built-in operators. An operator is a symbol that tells the compiler to perform a certain mathematical or logical manipulation. Operators are used in programs to manipulate data and variables.

C operators can be classified into following types: 1. Arithmetic operators 2. Relational operators 3. Logical operators 4. Bitwise operators 5. Assignment operators 6. Conditional operators 7. Special operators

## ARITHMETIC OPERATORS

C supports all the basic arithmetic operators. The following table shows all the basic arithmetic operators

| Operator | Description |
| :--- | :--- |
| + | adds two operands |
| - | subtract second operands from first |
| \* | multiply two operand |
| / | divide numerator by denominator |
| % | remainder of division |
| ++ | Increment operator - increases integer value by one |
| -- | Decrement operator - decreases integer value by one |

## RELATIONAL OPERATORS

The following table shows all relation operators supported by C.

| Operator | Description |
| :--- | :--- |
| == | Check if two operand are equal |
| != | Check if two operand are not equal. |
| &gt; | Check if operand on the left is greater than operand on the right |
| &lt; | Check operand on the left is smaller than right operand |
| &gt;= | check left operand is greater than or equal to right operand |
| &lt;= | Check if operand on left is smaller than or equal to right operand |

## LOGICAL OPERATORS

C language supports following 3 logical operators. Suppose a = 1 and b = 0,

| Operator | Description |
| :--- | :--- |
| && | Logical AND |
|  | Logical OR |
| ! | Logical NOT |

## BITWISE OPERATORS

Bitwise operators perform manipulations of data at bit level. These operators also perform shifting of bits from right to left. Bitwise operators are not applied to float or double.

| Operator | Description |
| :--- | :--- |
| & | Bitwise AND |
|  | Bitwise OR |
| ^ | Bitwise exclusive OR |
| &lt;&lt; | left shift |
| &gt;&gt; | right shift |

## ASSIGNMENT OPERATORS

Assignment operators supported by C language are as follows.

| Operator | Description | Example |
| :--- | :--- | :--- |
| = | assigns values from right side operands to left side operand | a=b |
| += | adds right operand to the left operand and assign the result to left | a+=b is same as a=a+b |
| -= | subtracts right operand from the left operand and assign the result to left operand | a-=b is same as a=a-b |
| \*= | mutiply left operand with the right operand and assign the result to left operand | a_=b is same as a=a_b |
| /= | divides left operand with the right operand and assign the result to left operand | a/=b is same as a=a/b |
| %= | calculate modulus using two operands and assign the result to left operand | a%=b is same as a=a%b |

## CONDITIONAL OPERATORS

Conditional operators in C language are known by two more names 1. Ternary Operator 2. ? : Operator

It is actually the if condition that we use in C language decision making, but using conditional operator, we turn the if condition statement into a short and simple operator.

The syntax of a conditional operator is :

```c
expression 1 ? expression 2: expression 3
```

Explanation: 1. The question mark "?" in the syntax represents the if part. 2. The first expression \(expression 1\) generally returns either true or false, based on which it is decided whether \(expression 2\) will be executed or \(expression 3\) 3. If \(expression 1\) returns true then the expression on the left side of " : " i.e \(expression 2\) is executed. 4. If \(expression 1\) returns false then the expression on the right side of " : " i.e \(expression 3\) is executed.

## SPECIAL OPERATORS

| Operator | Description | Example |
| :--- | :--- | :--- |
| sizeof | Returns the size of an variable | sizeof\(x\) return size of the variable x |
| & | Returns the address of an variable | &x ; return address of the variable x |
| \* | Pointer to a variable | \*x ; will be pointer to a variable x |

