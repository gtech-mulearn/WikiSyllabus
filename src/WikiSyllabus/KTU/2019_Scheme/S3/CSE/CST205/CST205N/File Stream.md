# File Stream

```java
import java.io.*;
class FileStream
{
	public static void main(String args[])
	{
		try
		{
			FileInputStream fin = new FileInputStream("One.txt");
			FileOutputStream fout = new FileOutputStream("Two.txt");
			
			int i;
			while((i = fin.read())!=-1)
			{
				fout.write(i);
			}
			fin.close();
			fout.close();

		}
		catch(FileNotFoundException e)
		{
			System.out.println(e.getMessage());
		}
		catch(IOException e)
		{
			System.out.println(e.getMessage());
		}
		finally
		{
			System.out.println("Execution Completed");
		}
	}
}
```