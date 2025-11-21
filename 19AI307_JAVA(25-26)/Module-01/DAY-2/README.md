# Ex.No:1(B) CONDITIONAL STATEMENT

## QUESTION:

You are given the lengths of three sides of a triangle. Determine whether the triangle is:

"Equilateral" – all sides equal

"Isosceles" – two sides equal

"Scalene" – all sides different

If the sides don’t form a triangle (triangle inequality fails), print "Not a triangle"


## AIM:
To write a program that reads the lengths of three sides and determines whether the given sides form an Equilateral, Isosceles, Scalene triangle, or not a triangle.

## ALGORITHM :
1.Start the program.

2.Input the three side lengths: a, b, and c.

3.Check the triangle validity using the triangle inequality rule:
```
 a + b > c
 
 b + c > a
 
 a + c > b
```
4.If any condition fails, print "Not a triangle" and stop.

5.If valid, check the type of triangle:
```
 If a == b == c, print "Equilateral"
 
 Else if any two sides are equal, print "Isosceles"
 
 Else, print "Scalene"
```
6.End the program.





## PROGRAM:
 ```
/*
Program to implement a conditional statement using Java
Developed by: Sandhiya R
RegisterNumber:  212222230129
*/
```

## SOURCE CODE:
```
import java.util.*;
public class Main{
    public static void main(String arg[])
    {
        Scanner sc=new Scanner(System.in);
        int a=sc.nextInt();
        int b=sc.nextInt();
        int c=sc.nextInt();
        if((a+b)>c && (a+c)>b && (b+c)>a)
        {
            if(a==b && a==c)
            {
                System.out.print("Equilateral");
            }
            else if(a==b || b==c || a==c)
            {
                System.out.print("Isosceles");
            }
            else if(a!=b && b!=c )
            {
                System.out.print("Scalene");
            }
        }
        else 
        {
            System.out.print("Not a triangle");
        }
    }
}
```



## OUTPUT:

<img width="480" height="167" alt="image" src="https://github.com/user-attachments/assets/ccf5fedc-1551-4444-a7cf-9252b96d95a8" />


## RESULT:
The program successfully checks whether the given sides form a valid triangle and correctly classifies it as Equilateral, Isosceles, Scalene, or Not a triangle.
