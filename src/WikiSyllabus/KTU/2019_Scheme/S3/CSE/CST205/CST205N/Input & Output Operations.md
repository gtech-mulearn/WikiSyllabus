# Input & Output Operations

## User Input

In Java, we have mainly two methods or classes for taking input from the user. One is by using the Scanner class, and the other is by using the Buffered Reader class. Both having different set of functions for inputting different data.

### Scanner Class

- Package: java.util
- Data types are read as such without any conversions or typecasting.

![Untitled](Input%20&%20Output%20Operations/Untitled.png)

```java
//Import Statement
import java.util.Scanner;
public class ScannerTest
{
    public static void main(String args[])
    {
        Scanner br = new Scanner(System.in);
        System.out.println("\nEnter a Number: ");
        int n = br.nextInt();
        
        System.out.println("\nEntered Number is: "+n);
    }
}
```

### Buffered Reader Class

- Package: java.io
- User input is read as a String using the.readLine() function and is converted to the data type using the function provided by the Data type classes.

```java
//Import Statement
import java.io.*;
public class BufferedText
{
    public static void main(String args[])
    {
        try
        {
            BufferedReader br = new BufferedReader(new InputStreamReader(System.in));
            System.out.println("Enter a Number: ");
            int n = Integer.parseInt(br.readLine());
						//double m = Double.parseDouble(br.readLine());
						//String s = br.readLine();
        
            System.out.println("Entered Number: "+n);
        }
        catch(IOException e)
        {
            System.out.println(e.getMessage());
        }
    }
}
```

### PrintWriter Class

The print writer class is used as an alternative to the standard System.out.println(””);

```java
import java.io.*;
public class PrintingWriter
{
    public static void main(String args[])
    {
        PrintWriter pw = new PrintWriter(System.out,true);
        pw.println("Hello World");
    }
}
```