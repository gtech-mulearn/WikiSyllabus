# Strings

Strings are a collection of characters. e.g., "coding”, is a string that has six characters in it. String is contained in the package java.util.lang and is imported automatically by the compiler.

Class: **String**

Package: **java.util.lang**

[String Buffer](Strings/String%20Buffer.md)

## Sample Program

[Vowels & Consonants](Strings/Vowels%20&%20Consonants.md)

## Creating a String

There are two methods for creating a string in Java.

- The first method is to directly declare and initialize the String variable at the same time.
    - String s = “Invisible”
- The second method is to create an object for the String class and then initialize it.
    
    ```java
    String s1 = new String();
    s1 = “Invisible”
    
    // These two steps can be combined also.
    String s2 = new String("Coding In The Sea");//Parameterized Constructor
    
    /*String can be also created using the below shown method also.
    But this method is not preffered.
    */
    
    char name[] = {'A','S','W','I','N'}
    String s3 = new String(name);
    
    ```
    

## String Functions

The String class provides a number of functions for converting and manipulating strings. The most commonly used string functions are as follows.

### .length()

- Return Type: int
- Starting Index: 1

Just as the name of this string function implies, it is used to find the length of the string.

```java
String name = "Coding";
System.out.println(name.length());

/*
Output
6
*/
```

### .toUpperCase() & .toLowerCase()

- Return Type: String

To convert a string to uppercase, use.toUpperCase(), and to convert a string to lowercase, use.toLowerCase().

```java
String name = "Coding";
System.out.println(name.toUpperCase());
System.out.println(name.toLowerCase());

/*
Output
CODING
coding
*/
```

### .concat()

- Return Type: String

The concat function is used to merge two strings into a single string.

```java
String name = "Coding";
String name1 = "Java";

System.out.println(name.concat(name1));

/*
Output
CodingJava
*/
```

### .toString()

- Return Type: String

This function is used to convert other data types, such as integers, to strings.

```java
Integer x = 5;

System.out.println(x.toString());  
System.out.println(Integer.toString(12));
```

### Other Common Functions

- .equals()
- .equalsIgnoreCase()
- .compareTo()

## Characters Functions

There are also several character functions available in Java for manipulating characters.

### .charAt()

- Return Type: char
- Start Index: 0

chatAt is one of the most commonly used character functions in Java. It is used in almost every program that demands the programmer to check each character in the string.

```java
public class Test {

   public static void main(String args[]) {
      String s = "Strings are immutable";
      char result = s.charAt(8);
      System.out.println(result);
   }
}
/*
a
*/
```

### .getBytes()

Return Type: **It returns a new byte array storing a series of bytes(ASCII)**

This string function returns the ASCII values of the characters in the string.

```java
String s = "ABCD";
byte barr[] = s.getBytes();
      
for(int i = 0; i<barr.length;i++)
{
   System.out.println(barr[i]);
}

/*
java -cp /tmp/A7PTNkgYqu Test
65
66
67
68
*/
```

### .toCharArray()

Return Type: Character Array

.toCharArray, as the name of the function implies, converts the string to characters, stores them in an array, and returns the array.

```java
class Test {
    public static void main(String args[])
    {
        String s = "Java";
        char[] array = s.toCharArray();
        
        for (int i = 0; i < array.length; i++) 
        {
            System.out.println(array[i]);
        }
    }
}

/*
java -cp /tmp/atQuukUBgl Test
J
a
v
a
*/
```

### Other Functions

- .getChars()