# Function Arguments

#### While calling a function, the arguments can be passed to a function in two ways, Call by value and c

```text
Type               Description

Call by Value          The actual parameter is passed to a function
                      New memory area created for the passed parameters, can be used only within the function.
                      The actual parameters cannot be modified here.

Call by Reference     Instead of copying variable; an address is passed to function as parameters.
                      Address operator(&) is used in the parameter of the called function.
                      Changes in function reflect the change of the original variables.
```

## Call by Value

### Example:

```text
  #include<stdio.h>

  /* function declaration */int addition(int num1, int num2);

  int main()
  {
      /* local variable definition */    int answer;
      int num1 = 10;
      int num2 = 5;

      /* calling a function to get addition value */    answer = addition(num1,num2);

      printf("The addition of two numbers is: %d\n",answer);
      return 0;
  }

  /* function returning the addition of two numbers */int addition(int a,int b)
  {
      return a + b;
  }
```

Program output:

The addition of two numbers is: 15

## Call by Reference

### Example:

```text
  #include<stdio.h>

  /* function declaration */int addition(int *num1, int *num2);

  int main()
  {
      /* local variable definition */    int answer;
      int num1 = 10;
      int num2 = 5;

      /* calling a function to get addition value */    answer = addition(&num1,&num2);

      printf("The addition of two numbers is: %d\n",answer);
      return 0;
  }

  /* function returning the addition of two numbers */int addition(int *a,int *b)
  {
      return *a + *b;
  }
```

Program output:

The addition of two numbers is: 15

