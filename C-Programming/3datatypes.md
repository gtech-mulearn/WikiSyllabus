# Datatypes

Data types specify how we enter data into our programs and what type of data we enter. C language has some predefined set of data types to handle various kinds of data that we can use in our program. These datatypes have different storage capacities.

There are 4 Data types in C: 1. Basic 2. Derived 3. Void 4. Enumeration

![](assets/datatypes_c.png)

## BASIC DATATYPES

These are also termed as primary or fundamental data types. All the names mean the same thing. Suppose we have to store student details like name, id, group, avg\_marks, interest\_on\_fees.

We can use basic data types to store each of these data:

```c
char name[25];
int id;
char group;
float marks[5];
double interest;
```

### INT DATATYPE

Integers are used to store whole numbers.

| Type | Size\(bytes\) | Range |
| :--- | :--- | :--- |
| int or signed int | 2 | -32,768 to 32767 |
| unsigned int | 2 | 0 to 65535 |
| short int or signed short int | 1 | -128 to 127 |
| unsigned short int | 1 | 0 to 255 |
| long int or signed long int | 4 | -2,147,483,648 to 2,147,483,647 |
| unsigned long int | 4 | 0 to 4,294,967,295 |

Example:

```c
int number = 456;
long prime = 12230234029;
```

### FLOAT DATATYPE

Floating types are used to store real numbers.

| Type | Size\(bytes\) | Range |
| :--- | :--- | :--- |
| float | 4 | 3.4E-38 to 3.4E+38 |

Example:

```c
 float average = 97.665;
 float mark = 67;
 printf("average is %f", average);
 printf(" mark is %f", mark);
```

The result of the mark will be 67.00000.

### DOUBLE DATATYPE

Double is 8 bytes, which means you can have more precision than float. This is useful in scientific programs that require precision. Float is just a single-precision data type; double is the double-precision data type. Long Double is treated the same as double by most compilers; however, it was made for quadruple data precision.

| Type | Size\(bytes\) | Range |
| :--- | :--- | :--- |
| double | 8 | 1.7E-308 to 1.7E+308 |
| long double | 10 | 3.4E-4932 to 1.1E+4932 |

Example:

```c
double average = 679999999.454;
float score = 679999999.454;
printf("average is %lf", average);
printf(", score is %f", score);
```

The outputs are – the average is 679999999.454000, the score is 680000000.000000 Note the difference in outputs – while double prints the exact value, float value is rounded off to the nearest number.

### CHAR DATATYPE

Character types are used to store characters value.

| Type | Size\(bytes\) | Range |
| :--- | :--- | :--- |
| char or signed char | 1 | -128 to 127 |
| unsigned char | 1 | 0 to 255 |

Example:

```c
char group = 'B';
char name[30] = "Student1";
printf("group is %c, name is %s", group, name);
```

## DERIVED DATATYPES

Array, pointers, struct, and union are the derived data types in C.

### ARRAYS

Same as any other language, Array in C stores multiple values of the same data type. That means we can have an array of integers, chars, floats, doubles, etc

```c
int numbers[] = ;
double marks[7];
float interest[5] = ;
```

The array needs to be either initialized, or the size needs to be specified during the declaration.

### POINTERS

A pointer can store the address of variables of any data types. This allows for dynamic memory allocation in C. The pointer is defined by using a ‘\*’ operator.

```c
int *ptr;
```

This indicates ptr stores an address and not a value. To get the address of the variable, we use the dereference operator ‘&.’ The size of a pointer is 2 bytes. Pointers cannot be added, multiplied, or divided. However, we can subtract them. Here is a simple program that illustrates pointer .

```c
#include 
int main(void) {
 int *ptr1;
 int *ptr2;
 int a = 5;
 int b = 10;
 /* address of a is assigned to ptr1*/
 ptr1 = &a;
 /* address of b is assigned to ptr2*/
 ptr2 = &b;
 /* display value of a and b using pointer variables */
 printf("%d", *ptr1); //prints 5
 printf("\n%d", *ptr2); //prints 10 
 //print address of a and b
 printf("\n%d", ptr1); // prints address like -599163656
 printf("\n%d", ptr2); // prints address like -599163652
 // pointer subtraction
 int minus = ptr2 - ptr1;
 printf("\n%d", minus); // prints the difference (in this case 1)
return 0;
}
```

### STRUCTS

A struct is a composite structure that can contain variables of different data types. Here all the basic data types can be put under one structure.

```c
typedef struct{
char name[25];
int id;
char group;
float marks[5];
double interest;
}Student;
```

Structs are simple to use and combine data in a neat way.

### UNION

With a union, you can store different data types in the same memory location. The union can have many members, but only one member can have a value at one time. Union, is thus, a special kind of data type in C.

The union is defined in the same way as a structure but with the keyword union.

```c
union Student{
 char name[25];
 int id;
 char group;
 float marks[5];
 double interest;
 }st1, st2;
```

## ENUMERATION DATATYPE

Enumeration data types enhance the readability of the code. If you have integer constants in the code that can be reused or clubbed together, we can use enums to define the constants.

The most common example of this is the days of the week.

```c
enum weekdays;
enum weekend;
```

Internally, C will store MON as 0, TUE as 1, and so on. We can assign values to the enum as well.

```c
enum weekdays;
If we print each of the enum values, the output will be –
1, 2, 6, 7, 8
```

## VOID DATATYPE

The void is just an empty data type used as a return type for functions. The absence of any other data type is void. When you declare a function as void, it doesn’t have to return anything. Example:

```c
void swapNumbers(int a, int b){
//multiple lines of code here
}
```

