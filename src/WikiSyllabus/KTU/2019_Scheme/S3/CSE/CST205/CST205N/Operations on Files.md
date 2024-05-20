# Operations on Files

For doing operations on file, we mainly have two ways: one is by using the stream classes, and the other is by using the FileReader and FileWriter Classes.

Package: java.io

Exceptions: FileNotFoundException, IOException

## Reading

- FileInputStream
- FileReader + BufferedReader

## Writing

- FileOutputStream
- FileWriter

## Stream vs Reader/Writer

In the FileInputStream and FileOutStream the string from the file is read and wrote as ASCII values therefore, when used in a program, to read ASCII character has to be first converted into respective character.

### Reading & Writing using Streams

.read

```java
FileInputStream fin = new FileInputStream("One.txt");
FileOutputStream fout = new FileOutputStream("Two.txt");
			
int i;
while((i = fin.read())!=-1)
	{
			fout.write(i);
	}
fin.close();
fout.close();

//While writing the ASCII is automatically converted to characters.
```

### Reading & Writing using Reader/Writer

```java
FileReader fr = new FileReader("A.txt");
BufferedReader br = new BufferedReader(fr);

FileWriter fw = new FileWriter("B.txt");

String s;

while((s = br.readLine())!=null)
	fw.write(s);

fr.close();
fw.close();
```