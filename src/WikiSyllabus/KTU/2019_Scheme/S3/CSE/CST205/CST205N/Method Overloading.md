# Method Overloading

```java
import java.util.Scanner;
class Area
{
	public void area(double radius)
	{
		System.out.println("Area of the Circle is: "+ (3.14*radius*radius));
	}
	
	public void area(double length, double breadth)
	{
		System.out.println("Area of the Rectangle is: "+(length * breadth));
	}
	
	public void area(int base, int height)
	{
		System.out.println("Area of the Triangle is: "+(0.5*base*height));
	}
	
}

class TestArea
{
	public static void main(String args[])
	{
		Scanner br = new Scanner(System.in);
		Area a = new Area();
		System.out.println("\n-------- Circle Parameters ---------");
		System.out.println("\nEnter the Radius of the Circle");
		double radius = br.nextDouble();
		a.area(radius);
		
		System.out.println("\n-------- Rectangle Parameters ---------");
		System.out.println("\nEnter the Length of the Rectangle");
		double length = br.nextDouble();
		System.out.println("Enter the Breath of the Reactangle");
		double breadth = br.nextDouble();
		a.area(length, breadth);
		
		System.out.println("\n-------- Triangle Parameters ---------");
		System.out.println("\nEnter the Base of the Triangle");
		int base = br.nextInt();
		System.out.println("Enter the Height of the Triangle");
		int height = br.nextInt();
		a.area(base,height);
	
	}
	
}
```