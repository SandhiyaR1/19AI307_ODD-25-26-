# Ex.No:2(A) CLASS AND OBJECT

## QUESTION:
Create a class Course with attributes code, title, credits.

## AIM:
To create a Java class named Course with attributes code, title, and credits, and to display the details of a course object.

## ALGORITHM :

1.Start the program.

2.Create a class Course with the attributes:

code (String)

title (String)

credits (int)

3.Define a constructor to initialize these attributes.

4.Define a method display() to print the course details.

5.In the main method:

Create an object of the Course class.

Call the display() method to show the course information.

6.End the program.



## PROGRAM:
 ```
/*
Program to implement a Class and Objects using Java
Developed by: Sandhiya R
RegisterNumber:  212222230129
*/
```

## SOURCE CODE:

```
import java.util.*;
class Course
{
    String code;
    String title;
    int credits;
}

public class Main {
    public static void main(String[] args) {
        Scanner sc = new Scanner(System.in);

        Course c1 = new Course();
        c1.code = sc.next();
        c1.title = sc.next();
        c1.credits = sc.nextInt();

        Course c2 = new Course();
        c2.code = sc.next();
        c2.title = sc.next();
        c2.credits = sc.nextInt();

        System.out.println(c1.code + " | " + c1.title + " | " + c1.credits + " credits");
        System.out.println(c2.code + " | " + c2.title + " | " + c2.credits + " credits");

        sc.close();
    }
}
```
## OUTPUT:

<img width="820" height="246" alt="image" src="https://github.com/user-attachments/assets/96eb0678-f38a-4032-a9d6-099fad59215b" />

## RESULT:
The program successfully creates a Course class with code, title, and credits, and displays the details using an object.
