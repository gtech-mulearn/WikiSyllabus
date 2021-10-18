# Frequently asked C programming Questions

## 1. Write a C program to check whether a given number is palindrome or not using command line arguments.


A palindrome is a word, sentence, verse, or even number that reads the same backward or forward.
For example **Racecar** is a palindrome whereas **Wikisyllabus** isn't. **1331** is a palindrome but **2156** isn't.


### Program 
```text
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

```text
Enter number: 1331
1331 is a palindrome

Enter number: 1546
1546 is not a palindrome

```