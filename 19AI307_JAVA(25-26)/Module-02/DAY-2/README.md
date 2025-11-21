# Ex.No:2(B) METHODS

## QUESTION:
Create two methods:

Get the input for radius from the user.

double getArea(double r) → calculate the area and return the area(Don't print anything in this method).

void printArea(double area) → pass the calculated area to this method and print the area of a circle.

## AIM:
To write a Java program that takes radius as input from the user, calculates the area of a circle using a method that returns the value, and prints the area using another method.

## ALGORITHM :
1.Start the program.

2.Create a method getArea(double r) that:

Calculates the area using the formula
area = 3.14 × r × r

Returns the computed area.

3.Create a method printArea(double area) that:

Accepts the area and prints it.

4.In the main method:

Read the radius from the user.

Call getArea() and store the returned area.

Call printArea() to display the result.

5.End the program.


## PROGRAM:
 ```
/*
Program to implement a Methods using Java
Developed by: 212222230129
RegisterNumber:  Sandhiya R
*/
```

## SOURCE CODE:
```
import java.util.*;
public class Main{
    public static double getArea(double r)
    {
        return 3.14*r*r;
        
    }
   public static void printArea(double r)
    {
        System.out.printf("%.2f",getArea(r));
    }
    public static void main(String arg[])
    {
        Scanner sc=new Scanner(System.in);
        double r=sc.nextDouble();
        printArea(r);
    }
}
```


## OUTPUT:
<img width="396" height="150" alt="image" src="https://github.com/user-attachments/assets/31cfce04-c38c-416e-884c-643199e990da" />

## RESULT:

The program successfully reads the radius, computes the area of the circle using a return-type method, and prints the result using a separate void method.
