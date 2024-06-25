# Prime Number

```java
import java.util.Scanner;
class Prime
{
	public static void main(String args[])
	{
		Scanner br = new Scanner(System.in);
		System.out.println("Enter a Number to Check");
		int number = br.nextInt();
		
		int flag = 0;
		
		
		for (int i = 2; i<number/2; i++)
		{
			if(number % i == 0)
			{
				flag = 1;
				break;
			}
		}
		
		if(flag == 1)
		{
			System.out.println(number+" is not a Prime Number");
		}
		else
		{
			System.out.println(number+" is a Prime Number");
		}
		
		
	}
}
```