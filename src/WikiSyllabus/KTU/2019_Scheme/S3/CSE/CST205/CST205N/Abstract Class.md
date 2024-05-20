# Abstract Class

A class that has been declared abstract using the keyword "abstract” is called an abstract class. Here, in the example shown below, the class shape is an abstract class.

- An abstract class can have both abstract, as can have both abstract and non-abstract methods.
- A method which has been declared as abstract doesn’t have a body and only has the function signature. The class which is inheriting the abstract class should create a body for the abstract function.
    - In our example the function “numberOfSides()” is an abstract function and the classes Rectangle, Triangle and Hexagon inherits it and therefore defines a body for the abstract method inside them.

```java
abstract class Shape
{
	public abstract void numberOfSides();	
}

class Rectangle extends Shape
{
	public void numberOfSides()
	{
		System.out.println("The Number of Sides(Rectangle) is 4");
	}
}

class Triangle extends Shape
{
	public void numberOfSides()
	{
		System.out.println("The Number of Sides(Triangle) is 3");
	}
}

class Hexagon extends Shape
{
	public void numberOfSides()
	{
		System.out.println("The Number of Sides(Hexagon) is 6");
	}
}

class TestShape
{
	public static void main(String args[])
	{
		Triangle t = new Triangle();
		t.numberOfSides();
		
		Rectangle r = new Rectangle();
		r.numberOfSides();
		
		Hexagon h = new Hexagon();
		h.numberOfSides();
	}
}
```