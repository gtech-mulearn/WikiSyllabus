# File Reader/Writer

```java
import java.io.*;
class FileWriteRead
{
	public static void main(String args[])
	{
		try
		{
			FileWriter fw = new FileWriter("Two.txt");
			FileReader fr = new FileReader("One.txt");
			BufferedReader br = new BufferedReader(fr);
			
			String s;
			
			while((s = br.readLine())!=null)
			{
				fw.write(s);
			}
			
			fr.close();
			fw.close();
		}
		catch(FileNotFoundException e)
		{
			System.out.println(e.getMessage());
		}
		catch(IOException e)
		{
			System.out.println(e.getMessage());
		}
	}
}
```