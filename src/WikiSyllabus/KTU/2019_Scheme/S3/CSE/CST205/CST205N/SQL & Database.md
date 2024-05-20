# SQL & Database

## SQL Commands

SQL is a standard language for accessing and manipulating database, and it stands for **Structured Query Language**

```java
//Creating a Database named marian
> create database marian
//Telling SQL to use the database marian for following actions
> use marian

//creating a table named person in db marian
> create table person(name varchar(10),int age);
> close person

//inserting values into the table
> insert into person values("Aswin", 20);

//query to display all the contents of the table
> select * from person;

//query to display only the name column of the table
> select name from person;

//query to display name of people with age 15
> select * from person where age = 15;

//query to update the age of a person whose name is Aswin
> update person set age = 10 where name= "Aswin";

//adding a new column to the table
> alter table person add(Phoneno);

//altering the existing table column property
> alter table person modify(name varchar(20));

//deleting the rows which has name = Anu
> delete from person where name = "Anu";

//This query deletes the table contents only, but the table exists
> delete from person;

//query to delete the whole table.
> drop table person;
```

## Java Program(SQL & Swing)

Java program to insert values received from the JFrame components onto the SQL database.

```java
import java.awt.event.*;
import javax.swing.*;
import java.sql.*;
class Form extends JFrame implements ActionListener
{
    private JLabel nlabel;
    private JTextField nfield'
    
    public Form()
    {
        setSize(500,400);
        setLayout(null);
        
        //Set Bounds by creating objects for components
        //Add them to the JFrame
        
        sbutton.addActionListener(this);
    }
    
    public static void main(String args[])
    {
        Form f = new Form();
        f.setVisible(true);
    }
    
    public void actionPerformed(ActionEvent e)
    {
        String name = nfield.getText();
        Integer age = new Integer.parseInt(afield.getText());
        
        try
        {
            Class.forName("com.mysql.cj.jdbc.Driver");
            String url = "jdbc:mysql://localhost:3306/marian";
            String user = "root";
            String pwd = "password";
            
            Connection con = DriverManager.getConnection(url,user,pwd);
            Statement stm = con.createStatement();
            
            String sql = "insert into person values(`"+name+"','"+age+"'));
            
            stm.executeUpdate(sql);
            
            con.close
        }
        catch(Exception e)
        {
            System.out.println(e.getMessage());
        }
    }
}
```