# Vowels & Consonants

```java
import java.util.Scanner;
class vowels
{
    public static void main(String args[])
    {
        Scanner br = new Scanner(System.in);
        System.out.println("Enter a String");
        String s = br.nextLine();
        
        int vowels = 0;
        int consonants = 0;
        int others = 0;
        
        for(int i = 0 ; i<s.length(); i++)
        {
            char ch = s.charAt(i);
            if(ch == 'a' || ch == 'e' || ch == 'i' || ch == 'o' || ch == 'u' || ch == 'A' || ch == 'E'|| ch == 'I' || ch == 'O' || ch == 'U')
            {
                vowels++;
            }
            else if((ch >= 'a' && ch <= 'z') || (ch >= 'A' && ch <= 'Z'))
            {
                consonants++;
            }
            else{
                others++;
            }
        }
        
        System.out.println("Number of Vowels: "+vowels);
        System.out.println("Number of Consonants: "+consonants);
        System.out.println("Number of Other Characters: "+others);
    }
}

/*
java -cp /tmp/atQuukUBgl vowels

Enter a String
Aswin Asok
Number of Vowels: 4
Number of Consonants: 5
Number of Other Characters: 1

*/
```