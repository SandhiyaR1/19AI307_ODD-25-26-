# Ex.No:2(C) ACCESS SPECIFIERS

## QUESTION:
Write a Java program to create a class called Person with private instance variables name, age. and country. Provide public getter and setter methods to access and modify these variables.

## AIM:

To write a Java program that defines a class Person with private instance variables — name, age, and country — and provides public getter and setter methods to access and modify these variables.

## ALGORITHM :
1.Start the program.

2.Create a class Person with private variables:

name (String)

age (int)

country (String)

3.Write public setter methods to assign values to these variables.

4.Write public getter methods to retrieve the stored values.

5.In the main() method:

 Create an object of the Person class.
 
 Read the values for name, age, and country from the user.
 
 Use setter methods to store these values in the object.
 
 Use getter methods to display the stored information.

6.End the program.




## PROGRAM:
 ```
/*
Program to implement a Access Specifiers using Java
Developed by: Sandhiya R
RegisterNumber:  212222230129
*/
```

## SOURCE CODE:
```
import java.util.*;
class Person{
    private String name;
    private int age;
    private String country;
    
    public String getName()
    {
        return name;
    }
    public void setName(String name)
    {
        this.name=name;
    }
    public int getAge()
    {
        return age;
    }
    public void setAge(int age)
    {
        this.age=age;
    }
    public String getCountry(){
        return country;
    }
    public String setCountry()
    {
        return country;
    }
    public void setCountry(String country)
    {
        this.country=country;
    }
}
public class Main{
    public static void main(String arg[])
{
    Scanner sc=new Scanner(System.in);
    Person p=new Person();
    String name=sc.next();
    int age=sc.nextInt();
    String country=sc.next();
    p.setName(name);
    p.setAge(age);
    p.setCountry(country);
    System.out.println("Person 1");
    System.out.println("Name: "+p.getName());
    System.out.println("Age: "+p.getAge());
    System.out.println("Country: "+p.getCountry());
    
    
}
}
```

## OUTPUT:
<img width="911" height="462" alt="image" src="https://github.com/user-attachments/assets/c992db03-a213-40ac-b849-3be29eab642d" />



## RESULT:
The program successfully creates a Person class with private attributes and uses getter and setter methods to set and retrieve the values of name, age, and country.

