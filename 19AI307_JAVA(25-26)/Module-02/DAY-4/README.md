# Ex.No:2(D) VARIABLE SCOPE AND CONSTRUCTOR

## QUESTION:
Write Java code to create a class Triangle and initialiaze the attributes(base and height) using default constructor and calculate the area of the triangle using user defined function.
## AIM:
To Write Java code to create a class Triangle and initialiaze the attributes(base and height) using default constructor and calculate the area of the triangle using user defined function.
## ALGORITHM :
1.Start the program.

2.Create a class Triangle with attributes:

  base (double)
  
  height (double)

3.Define a default constructor that initializes base and height with fixed default values.

4.Define a user-defined method getArea() to compute the area using the formula:
area = 0.5 × base × height

5.In the main() method:

  Create an object of the Triangle class.
  
  Call the getArea() method to compute the area.
  
  Display the base, height, and calculated area.

6.End the program.



## PROGRAM:
 ```
/*
Program to implement a Variable scope and Constructor using Java
Developed by: Sandhiya R
RegisterNumber:  212222230129
*/
```

## SOURCE CODE:
```
import java.util.*;
class Triangle{
    int base;
    int height;
    
   public Triangle(int base,int height)
   {
       this.base=base;
       this.height=height;
   }
   public double calculateArea()
   {
       return 0.5*base*height;
   }
}
public class Main{
    public static void main(String arg[])
    {
        Scanner sc=new Scanner(System.in);
        int base=sc.nextInt();
        int height=sc.nextInt();
        Triangle t=new Triangle(base,height);
        System.out.print("Area of the triangle is: "+t.calculateArea());
        
    }
}

```

## OUTPUT:

<img width="776" height="325" alt="image" src="https://github.com/user-attachments/assets/4bbe39b3-8d65-43df-bc45-a4430500ad59" />


## RESULT:
The program successfully creates a Triangle class with base and height initialized using a default constructor and correctly calculates the area using a user-defined function.

