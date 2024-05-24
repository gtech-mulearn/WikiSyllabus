# Strings

Strings are actually **one-dimensional array** of characters terminated by a null character '\0'. Thus a null-terminated string contains the characters that comprise the string followed by a null.

## Declaring a String

```c
char str_name[size];
```
## Methods of Initializing String

```c
1. char str[] = "Hello World";

2. char str[50] = "Hello World";

3. char str[] = {'H','e','l','l','o',' ','W','o','r','l','d','\0'};

4. char str[12] = {'H','e','l','l','o',' ','W','o','r','l','d','\0'};
```

To hold the null character at the end of the array, the size of the character array containing the string is one more than the number of characters in the word.

## Input / Output a String

The C programming language doesn't provide an inbuilt datatype for Strings, but it has an access specifier `%s`.

### Input a String

```c
#include <stdio.h>

int main () {

   char greeting[100];
   scanf("%s", greeting);
   return 0;
}
```
> Note that scanf can't be used to input string with spaces or newlines.

### Output a String

```c
#include <stdio.h>

int main () {

   char greeting[] = "Hello World";
   printf("%s\n", greeting);
   return 0;
}
```
## String Functions

| No. | Functions         | Used for                                         |
| --- |:-----------------:| :---------                                       |
| 1   | `strcpy(s1, s2);` | Copies string s2 into string s1.                 |
| 2   | `strcat(s1, s2);` | Concatenates string s2 onto the end of string s1.|
| 3   | `strlen(s1);`     | Returns the length of string s1.                 | 
| 4   | `strcmp(s1, s2);` | Returns 0 if s1 and s2 are the same; less than 0 if s1<s2; greater than 0 if s1>s2.|
| 5   | `strchr(s1, ch);` | Returns a pointer to the first occurrence of character ch in string s1.|
| 6   | `strstr(s1, s2);` | Returns a pointer to the first occurrence of string s2 in string s1.|