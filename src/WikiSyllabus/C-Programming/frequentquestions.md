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

## 2. Write a C program to read the contents of a text file and find the number of characters, lines and words.

### Program

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

### Output
    Enter a filename :file.c
    Lines : 35 
    Words : 225 
    Characters : 787 
    Writing to result.txt



