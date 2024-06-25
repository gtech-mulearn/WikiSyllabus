# Familiarization of Inheritance

![Untitled](Familiarization%20of%20Inheritance/Untitled.png)

```java

class Employee
{
	private String name;
	private int age;
	
	public void setName(String name)
	{
		this.name = name;
	}
	
	public void setAge(int age)
	{
		this.age = age;
	}
	
	public String getName()
	{
		return name;
	}
	
	public int getAge()
	{
		return age;
	}
}

class Manager extends Employee
{
	private String department;
	public void setDepartment(String department)
	{
		this.department = department;
	}
	public String getDepartment()
	{
		return department;
	}
	
}

class Officer extends Employee
{
	private String specialization;
	public void setSpecialization(String specialization)
	{
		this.specialization = specialization;
	}
	public String getSpecialization()
	{
		return specialization;
	}
}

class Inheritance
{
	public static void main(String args[])
	{
	
		//Object Creation for Manager
		Manager m = new Manager();
		m.setName("Manager Aswin Asok");
		m.setAge(19);
		m.setDepartment("CSE");
		
		//Printing Manager Details
		System.out.println("\n\n-------Manager Details---------");
		System.out.println("Name: "+ m.getName());
		System.out.println("Age: "+ m.getAge());
		System.out.println("Department "+ m.getDepartment());
		
		//Object Creation for Officer
		Officer o = new Officer();
		o.setName("Officer Aswin Asok");
		o.setAge(19);
		o.setSpecialization("Java");
		
		//Printing Officer Details
		System.out.println("\n\n-------Officer Details--------");
		System.out.println("Name: "+ o.getName());
		System.out.println("Age: "+ o.getAge());;
		System.out.println("Spcialization "+ o.getSpecialization());
	}
}

/*
-------Manager Details---------
Name: Manager Aswin Asok
Age: 19
Department CSE

-------Officer Details--------
Name: Officer Aswin Asok
Age: 19
Spcialization Java
*/
```

![Untitled](Familiarization%20of%20Inheritance/Untitled%201.png)