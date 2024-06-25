# Method Overriding

```java
class Person
{
    private String name;
    private int age;
        
    public Person() //Parent Default Constructor
    {
        name = "Aswin Asok";
        age = 20;
    }
        
    public void display()
    {
        System.out.println("\nName: "+ name);
        System.out.println("\nAge: "+ age);
    }
    
}

class Employee extends Person
{
    private double salary;
    
    public Employee() //Child Default Constructor
    {
        salary = 1000.00;
    }
    
    public void display()
    {
        // super.display();
        System.out.println("\nSalary: "+salary);
    }
}

class Test
{
    public static void main(String args[])
    {
        Employee e = new Employee();
        e.display();
    }
}

/*
Program Output

java -cp /tmp/qql6TGTs9y Test
Name: Aswin Asok
Age: 20
Salary: 1000.0
*/
```

## Flow of Program

![Untitled](Method%20Overriding/Untitled.png)