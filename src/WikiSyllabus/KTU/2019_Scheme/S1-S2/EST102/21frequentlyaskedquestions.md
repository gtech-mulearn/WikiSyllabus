# Frequently asked C programming Questions

## 1. Write a C program to check whether a given number is palindrome or not using command line arguments.(IMP)


A palindrome is a word, sentence, verse, or even number that reads the same backward or forward.
For example **Racecar** is a palindrome whereas **Wikisyllabus** isn't. **1331** is a palindrome but **2156** isn't.


### Program 
```c
#include<stdio.h>

int main()
{
 int n,r,sum=0,temp; //variable declaration
 printf("Enter number:"); 
 scanf("%d",&n); // get number from user
 temp = n;
 while(n>0) // to reverse the number
 {
  r=n%10;
  sum=(sum*10)+r;
  n=n/10;  
 }
 if(temp==sum) //to check if reversed number equal to input number 
 {
 printf("%d is a palindrome", temp); // 

 } 
 else
 {
 printf("%d is not a palindrome",temp);
 }

}

```
### Output

```c
Enter number: 1331
1331 is a palindrome

Enter number: 1546
1546 is not a palindrome

```

## 2. Write a C program to read the contents of a text file and find the number of characters, lines and words.

### Program
```c
 #include <stdio.h>
 #include <stdlib.h>
 int main()
 {
  FILE *fp; //FILE datatype
  char filename[100]; 
  char ch;
  int lc=0, wc=0, cc=0;
  printf("Enter a filename :");
  gets(filename);
  fp = fopen(filename,"r"); // open existing file or create a new file
  if (fp==NULL) 
  {
printf("The file %s doesn't exist\n",filename);
exit(1);
  }
  else
  {	
while ((ch = fgetc(fp))!= EOF) 
{
 cc++;  
 if (ch == '\n' || ch == '\0')lc++;
 if (ch == ' ' || ch == '\t' || ch == '\n' || ch == '\0')wc++;	
}
fclose(fp);
  }
  printf("Lines : %d \n", lc);
  printf("Words : %d \n", wc);
  printf("Characters : %d \n", cc);
  
  fp=fopen ("result.txt", "w");
  printf("Writing to result.txt\n");
  fprintf (fp, "Lines : %d \n Words : %d \n Characters : %d \n", lc,wc,cc);
  fclose (fp); //close the file opened.
  return 0;
 }
``` 

### Output
```text
 Enter a filename :file.c
 Lines : 35 
 Words : 225 
 Characters : 787 
Writing to result.txt
```


## 3. Develop a C program to generate Fibonacci series.

### Program
```c
#include<stdio.h> 
int main() 
 { 
  int n1=0,n2=1,n3,i,number; 
  printf("Enter the number of elements:"); 
  scanf("%d",&number); 
  printf("\n%d %d",n1,n2);//printing 0 and 1 
  for(i=2;i<number;++i)//loop starts from 2 because 0 and 1 are already printed 
  { 
n3=n1+n2; 
printf(" %d",n3); 
n1=n2; 
n2=n3; 
  }  
  return 0;  
 } 
```
### Output
```text
Enter the number of elements:10
0
1
1
2
3
5
8
13
21
34
```


## 4.  Write a C program to copy a string without using a built in function(IMP)

### Program
```c
#include<stdio.h>

int main()
{
 
 char a[50], b[50], e[50], f[50] ;
 int i,j,c,d;
 printf("String concatenation without using Builtin function\n");
 printf("Enter First string:");
 scanf("%s",a);
 printf("Enter Second string:");
 scanf("%s",b);
 c=strlen(a);
 d=strlen(b);  
for(j=0;j<=d;j++){
  
a[c]=b[j];
c++;
}
printf("The concatenated string is: %s ",a) ; 
}
```
## 5. Write a C program to find largest element in an array 

### Program
```c
 #include<stdio.h>

 int main()
 {
  int a[100], n,i,j;
  printf("Enter number of elements:");
  scanf("%d",&n);
  for(i=0;i<n;i++)
  {
printf("Enter a[%d]:",i);
scanf("%d",&a[i]);
  }
 
  for(i=1;i<n;i++)
  {
if(a[0]<a[i+1])
{
 a[0]=a[i]; // store the largest number to first element of the array
}
  
  }
  printf("The largest number in the array is %d",a[0]);
 }
```
### Output
```
 Enter number of elements:5
 Enter a[0]:2
 Enter a[1]:6
 Enter a[2]:8
 Enter a[3]:7
 Enter a[4]:4
 The largest number in the array is 8
```
## 6. Write a C program to swap the content of two variables using pointers.

### Program
```c
 #include<stdio.h>

 int swap(int *a, int *b)
 {
  int temp;
  temp=*a;
  *a=*b;
  *b=temp;
 }

 int main()
 {
  int a,b,*ap,*bp,s;
  printf("Enter number:");
  scanf("%d",&a);
  printf("Enter number:");
  scanf("%d",&b);
  printf("Before swapping:\n");
  printf("a=%d ",a);
  printf("b=%d ",b);
  printf("\n");
  ap=&a;
  bp=&b;
  swap(ap,bp);
  printf("After swapping:\n");
  printf("a=%d ",a);
  printf("b=%d ",b);
  printf("\n"); 
 }
```
### Output
```
 Enter number:5
 Enter number:6
 Before swapping:
 a=5 b=6 
 After swapping:
 a=6 b=5 
```
## 7. Write a program to print the pattern 101010... using for loop.

### Program
```c  
 #include<stdio.h>
 int main()
 {
 for(;;)
 printf("10");
 
 return 0;
 }
```
### Output
```
 101010101010101010101010101010101010101010101010101010101010101010101010101010101010101010101010101010101010101010101010101010101010101010101010101010101010101010101010101010101010101010101010101010101010101010101010101010101010101010101010101010101010101010101010101010101010101010101010101010101010101010101010101010101010101010101010101010101010101010101010101010101010101010101010101010101010101010101010101010101010101010101010101010101010101010101010101010101010101010101010101010101010101010101010101010101010101010101010101010101010101010101010101010101010101010101010101010101010101010101010101010101010101010101010101010101010101010101010101010101010101010101010101010101010101010101010101010101010101010101010101010101010101010101010101010101010101010101010101010101010101010101010101010101010101010101010101010101010101010101010101010101010101010101010101010101010101010101010101010101010101010101010101010101010101010101010101010101010101010101010101010101010101010101010101010101010101010101010101010101010101010101010101010101010101010101010101010101010101010101010101010101010101010101010101010101010101010101010101010101010101010101010101010101010101010101010101010101010101010101010101010101010101010101010101010101010101010101010101010101010101010101010101010101010101010101010101010101010101010101010101010101010101010101010101010101010101010101010101010101010101010101010101010101010101010101010101010101010101010101010101010101010101010101010101010101010101010101010101010101010101010101010101010101010101010101010101010101010101010101010101010101010101010101010101010101010.............................................................and so on.
```
## 8. Write a C program to check whether a number is Armstrong or not.

## Program
```c
 #include<stdio.h>

 int main()
 {
  int n,num,a,rev=0;
  printf("Enter no:");
  scanf("%d",&num);
  n=num;
  for(num;num!=0;num=num/10){
  a= num % 10;
  rev+=a*a*a;
  }
  if(n==rev)
  {
printf("Amstrong number");
  } 
  
  else
  {
printf("Not an Amstrong number");
  }
  printf("\n");
  return 0; 
 }
```
### Output
```
 Enter no:123
 Not an Amstrong number

 Enter no:153
 Amstrong number
```
## 9. Write a C program to find transpose of a matrix.(IMP)

### Program
```c
 int main()
 {
  int a[10][10];
  int transp[10][10];
  int i,j,r,c;
  printf("First matrix A\n");
  printf("Enter number of rows:");
  scanf("%d",&r);
  printf("Enter number of columns:");
  scanf("%d",&c);
  // Getting the Matrix from user 
  for(i=0;i<r;i++)
  {
for(j=0;j<c;j++)
{
 printf("Enter a[%d][%d]:",i+1,j+1);
 scanf("%d",&a[i][j]);
}
  }
  // Displaying Input Matrix
  printf("The Matrix A is :\n");
  for(i=0;i<r;i++)
  {
for(j=0;j<c;j++)
{
 printf("%d  ",a[i][j]);

}
printf("\n");
  }
  // Transposing the Input Matrix 
  for(i=0;i<r;i++)
  {
for(j=0;j<c;j++)
{
 transp[j][i]=a[i][j];
}
  }  
  // Displaying Transpose Matrix 
  printf("Transpose of Matrix A:\n");  
  for(i=0;i<r;i++)
  {
for(j=0;j<c;j++)
{
 printf("%d  ",transp[i][j]);
}
printf("\n");
  }
 
 }  
```
### Output
```
 Enter number of rows:3 
 Enter number of columns:3
 Enter a[1][1]:5 
 Enter a[1][2]:6
 Enter a[1][3]:9
 Enter a[2][1]:4
 Enter a[2][2]:5
 Enter a[2][3]:6
 Enter a[3][1]:7
 Enter a[3][2]:1
 Enter a[3][3]:6
 The Matrix A is :
 5  6  9  
 4  5  6  
 7  1  6  
 Transpose of Matrix A:
 5  4  7  
 6  5  1  
 9  6  6  
```
## 10. Write a C program to subtract two matrices

### Program 
```c
#include<stdio.h>

int main()
{

int a[10][10];
int b[10][10];
int diff[10][10];
int i,j,r,c;
printf("First matrix A\n");
printf("Enter number of rows:");
  scanf("%d",&r);
  printf("Enter number of columns:");
  scanf("%d",&c);
  
  for(i=0;i<r;i++)
  {
for(j=0;j<c;j++)
{
 printf("Enter a[%d][%d]:",i+1,j+1);
 scanf("%d",&a[i][j]);
}
  }
  

  
  printf("Second matrix B\n");
  printf("Enter number of rows:");
  scanf("%d",&r);
  printf("Enter number of columns:");
  scanf("%d",&c);
  
  for(i=0;i<r;i++)
  {
for(j=0;j<c;j++)
{
 printf("Enter b[%d][%d]:",i+1,j+1);
 scanf("%d",&b[i][j]);
}
  }
  
  printf("The matrix A is :\n");
  for(i=0;i<r;i++)
  {
for(j=0;j<c;j++)
{
 printf("%d\t",a[i][j]);
}
printf("\n");
  }
  printf("The matrix B is :\n");
  for(i=0;i<r;i++)
  {
for(j=0;j<c;j++)
{
 printf("%d\t",b[i][j]);
}
printf("\n");
  }
  for(i=0;i<r;i++)
  {
for(j=0;j<c;j++)
{
 diff[i][j]=a[i][j]-b[i][j];
}
  }
  
  printf("The Difference Matrix is :\n");
  for(i=0;i<r;i++)
  {
for(j=0;j<c;j++)
{
 printf("%d\t",diff[i][j]);
}
printf("\n");
  }
 }
```
### Output 
```
 First matrix A
 Enter number of rows:3
 Enter number of columns:3
 Enter a[1][1]:5
 Enter a[1][2]:6
 Enter a[1][3]:4
 Enter a[2][1]:7
 Enter a[2][2]:8
 Enter a[2][3]:9
 Enter a[3][1]:1
 Enter a[3][2]:3
 Enter a[3][3]:6
 Second matrix B
 Enter number of rows:3
 Enter number of columns:3
 Enter b[1][1]:2
 Enter b[1][2]:5
 Enter b[1][3]:7
 Enter b[2][1]:8
 Enter b[2][2]:9
 Enter b[2][3]:4
 Enter b[3][1]:0
 Enter b[3][2]:3
 Enter b[3][3]:4
 The matrix A is :
 5	6	 4	
 7	8	 9	
 1	3	 6	
 The matrix B is :
 2	5	 7	
 8	9	 4	
 0	3	 4	
 The Difference Matrix is :
 3	 1  -3	
-1  -1	 5	
 1	 0	 2

``` 

## 11. Write a program to Multiply two m x n matrices

### Program
```c

 #include<stdio.h>

 int main()
 {

  int r,c,r1,c1,i,j,k,a[10][10],b[10][10],pro[10][10],sum = 0;
  printf("First Matrix A");
  printf("\nEnter the number of rows:");
  scanf("%d",&r);
  printf("Enter the number of columns:");
  scanf("%d",&c);

  for(i = 0; i < r; i++)
  {  
for(j = 0; j < c; j++){
 printf("Enter a[%d][%d]: ",i+1,j+1);
 scanf("%d", &a[i][j]);
}
  }
  printf("Second Matrix B\n");
  printf("Enter the number of rows:");
  scanf("%d",&r1);
  printf("Enter the number of columns:");
  scanf("%d",&c1);

  for(i = 0; i < r1; i++){  
for(j = 0; j < c1; j++){
 printf("Enter b[%d][%d]: ",i+1,j+1);
 scanf("%d", &b[i][j]);
}
  }  
  for(i = 0; i < r; i++){
  for(j = 0; j < c1; j++){
for(k = 0; k < r1; k++){
sum = sum + a[i][k]*b[k][j];
}
pro[i][j] = sum;
sum=0; 
  }
  }
  
  printf("The matrix A is :\n");
  for(i=0;i<r;i++){
  for(j=0;j<c;j++){
printf("%d  ",a[i][j]);

  }
  printf("\n");
  }
  printf("The matrix is :\n");
for(i=0;i<r1;i++){
for(j=0;j<c1;j++){
 printf("%d  ",b[i][j]);
}
printf("\n");
}
  printf("The product matrix\n");
for(i = 0; i < r; i++){
for(j = 0; j < c1; j++){
 printf("%d", pro[i][j]);
}
 printf("\n"); 
}
 }
```
### Output
```
 First Matrix A
 Enter the number of rows:3
 Enter the number of columns:3
 Enter a[1][1]: 9
 Enter a[1][2]: 1
 Enter a[1][3]: 2
 Enter a[2][1]: 3
 Enter a[2][2]: 4
 Enter a[2][3]: 56
 Enter a[3][1]: 7
 Enter a[3][2]: 8
 Enter a[3][3]: 6
 Second Matrix B
 Enter the number of rows:3
 Enter the number of columns:3
 Enter b[1][1]: 9
 Enter b[1][2]: 7
 Enter b[1][3]: 8
 Enter b[2][1]: 2
 Enter b[2][2]: 6
 Enter b[2][3]: 4
 Enter b[3][1]: 1
 Enter b[3][2]: 3
 Enter b[3][3]: 5
 The matrix A is :
 9  1  2  
 3  4  56  
 7  8  6  
 The matrix is :
 9  7  8  
 2  6  4  
 1  3  5  
 The product matrix
 85 75  86
 91 213 320
 85 115 118
```
## 12. Write a C program to sort an array using Bubble Sort.(IMP)

### Program
```c
#include<stdio.h>

int main()
{
  int n,a[100],i,j,temp;
  printf("Enter no of elements:");
  scanf("%d",&n);
  for(i=0; i<n; i++)
  {
    printf("Enter element:");
    scanf("%d",&a[i]);
  }
  printf("Array before Sorting:");
   for(i=0; i<n; i++)
  {
    printf("%d ",a[i]);
  }  
  for(i=0; i<n-1; i++)
  {
    for(j=0; i<n-1-j; j++)
    {
      if(a[j]>a[j+1])
      {
        temp=a[j];
        a[j]=a[j+1];
        a[j+1]=temp;
      }
    }
  }
   printf("\nArray after Sorting:");
   for(i=0; i<n; i++)
  {
    printf("%d ",a[i]);
  }   
   
}
```

### Output
```
Enter no of elements:5
Enter element:5
Enter element:4
Enter element:6
Enter element:7
Enter element:4
Array before Sorting:5 4 6 7 4 
Array after Sorting:4 4 5 6 7 
```
## 13. Write a C program to perform a linear search on an array of numbers(IMP)

### Program
```c
#include<stdio.h>

int main()
{
  int n,a[100],i,x,temp;
  printf("Enter number of elements:");
  scanf("%d",&n);
  for(i=0; i<n; i++)
  {
    printf("Enter element:");
    scanf("%d",&a[i]);
  }
  printf("Enter the number to be found:");
  scanf("%d",&x);
  int flag=0;
  for(i=0; i<n; i++)
  {
    if(a[i]==x)
    {
      temp=i;
      flag=1;
    }
  }
  if(flag==0)
    printf("Element not found");
  else
    printf("Element found at index %d ",temp);  
}
```
### Output
```
Enter number of elements:5
Enter element:6
Enter element:3
Enter element:4
Enter element:2
Enter element:8
Enter the number to be found:8
Element found at index 4 
```
## 14. Write a C program to find the frequency of vowels and consonants in a string

## Program
```c
#include <stdio.h>
int main() {
    char line[150];
    int vowels, consonant;

    vowels = consonant = 0;

    printf("Enter a line of string: ");
    scanf("%s",line);

    for (int i = 0; line[i] != '\0'; ++i) {
        if (line[i] == 'a' || line[i] == 'e' || line[i] == 'i' ||
            line[i] == 'o' || line[i] == 'u' || line[i] == 'A' ||
            line[i] == 'E' || line[i] == 'I' || line[i] == 'O' ||
            line[i] == 'U') {
            ++vowels;
        } else if ((line[i] >= 'a' && line[i] <= 'z') || (line[i] >= 'A' && line[i] <= 'Z')) {
            ++consonant;
        } 
    }

    printf("Vowels: %d", vowels);
    printf("\nConsonants: %d", consonant);

}
```
### Output
```
Enter a line of string: Cprogramming
Vowels: 3
Consonants: 9
```
## 15. Write a C program to print Floyd's triangle

### Program
```c
#include <stdio.h>

int main() {
int n,i,j,k = 1;

printf("Enter number of rows:");
scanf("%d",&n);

for(i = 1; i <= n; i++) {
for(j = 1;j <= i; j++)
printf("%3d", k++);

printf("\n");
}

return 0;
}
```
### Output
```
  1
  2  3
  4  5  6
  7  8  9 10
  11 12 13 14 15

```

