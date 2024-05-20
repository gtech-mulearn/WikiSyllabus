# String Buffer

String Class is an immutable class by default, so new characters cannot be added to an existing string variable. But when it comes to the String Buffer class, it is actually mutable and can be added onto with new characters.

## Reading Character

```java
StringBuffer sb = new StringBuffer("Hello");
        
System.out.println("String Length: " +sb.length());
System.out.println("\nTotal Capacity: " +sb.capacity());

/*
java -cp /tmp/A7PTNkgYqu Test
String Length: 5
Total Capacity: 21
*/
```

- The String Buffer class has an extra 16 locations when initialized, and once the initial allowance is occupied it is added by 10 memory locations.
- .capacity() function is used to get the total capacity of the String Buffer.

## String Buffer Functions

There are several functions available in Java for implementing functionalities like appending, inserting characters into the String Buffer object.

### .insert()

This function can be used to insert the given string in the specified location. In the example shown below, the character b is being inserted to the location 1 of the string.

```java
StringBuffer sb = new StringBuffer("Hello");
        
System.out.println(sb.insert(1,'b'));

/*
java -cp /tmp/A7PTNkgYqu Test
Hbello
*/
```

```java
StringBuffer sb = new StringBuffer("Hello");

System.out.println(sb.insert(4,true));

/*
java -cp /tmp/A7PTNkgYqu Test
Helltrueo
*/
```

### .append()

This function is used to append the give string to the end of the current StringBuffer Object

```java
StringBuffer sb = new StringBuffer("Hello");
        
System.out.println(sb.append("World"));

/*
java -cp /tmp/A7PTNkgYqu Test
HelloWorld
*/
```