# Arrays

An array is an **indexed** collection of data elements of the **same type**.
1. **Indexed** means that the array elements are numbered starting from 0.
2.  The restriction of the **same type** is an important one, because arrays are stored in consecutive memory cells. Every cell must be the same data type and therefore, the same size.

```text
Example:
int age[5] = {13, 26, 57, 76, 45};
```
Here the array named 'age' declared with the datatype of integer(int). The array age is given a size of 5 and indexed as,

| index number (of the array) | 0 | 1 |  2 | 3 | 4 |
| :--- | :--- | :--- | :--- | :--- | :--- |
| array elements of age (name of the array) | 13 | 26 | 57 | 76 | 45 |

## **Declaration of Arrays**


An array declaration is similar to the form of a normal declaration [ dataType variableName], but here we add on a size:
```text
  dataType variableName[size]; 
```
This declares an array with the specified size, named variableName, of a particular dataType.
The array is indexed from 0 to size-1. The size in brackets must be an integer literal or a constant variable. The compiler uses the size to determine how much space to allocate.

Examples:
```text
  int list[30];            // an array of 30 integers 
  char name[20];           // an array of 20 characters 
  double nums[50];         // an array of 50 decimals 
  int table[5][10];        // a two dimensional array of integers
```  

The first three examples are one dimensional array containing a single row and meantioned number of columns.
And the last example illustrates a two dimensional array which we often like to think about as a table with both rows and columns specified.

We usually think of the first size as rows, and the second as columns, but it really does not matter, as long as you are consistent!
So, we could think of the last declaration as a table with 5 rows and 10 columns

## **Initializing Arrays**


With normal variables, we could declare on one line, then initialize on the next:
```text
  int x; 
  x = 0;
```
Or, we could simply initialize the variable in the declaration statement itself:
```text
  int x = 0;
```
Can we do the same for arrays? Yes, for the built-in types. Simply list the array values (literals) in set notation { } after the declaration. Here are some examples:
```text
  int list[4] = {1, 2, 3, 4}; 
  char letters[5] = {'a', 'e', 'i', 'o', 'u'}; 
  double numbers[3] = {3.45, 2.39, 9.1}; 
  int table[3][2] = {{2, 5} , {3,1} , {4,9}}; 
```


Array declarations must contain the information about the size of the array. It is possible to leave the size out of the [....] in the declaration as long as you
initialize the array inline, in which case the array is made just large enough to capture the initialized data.
Examples:
```text
  char name[] = "Charlie";        // size is 7
  int list[] = {1, 1, 2, 3, 5};  // size is 5
```
Another shortcut with initializer sets is to use fewer elements than the size specifies. Remaining elements will default to 0.
It is illegal to use a set containing more elements than the allocated size.
```text
  int list[5] = {1, 2};         // array is {1, 2, 0, 0, 0}
  int nums[3] = {1, 2, 3, 4};   // illegal declaration.
```

## **Initializing using For-Loop**


Using initializers on the declaration, as in the examples above, is probably not going to be as desirable with very large arrays.

Another common way to initialize an array is with a **for loop**:
This example initializes the array numList to {1, 1, 2, 3, 5, 8, 13, 21, 34, 55}.
```text
  int numList[10];
  int i;
  for (i = 0; i < 10; i++)
     numList[i] = i * 2;
```

## **Accessing Array elements from the Array**

```text
  int myArray[5];
  int i;

  // Initializing elements of array individually
  for(i=0 ; n < sizeof(myArray) ; i++)
  {
    myArray[i] = i;
  }
```
Once your arrays are declared, you access the elements in an array with the array name and the index number inside brackets[]

```text
  int a = myArray[3]; // Assigning 3rd element of array value to integer 'a'.
```
Here myArray is declared as int myArray[5], then the element with index 3 is referred to as myArray[3]
