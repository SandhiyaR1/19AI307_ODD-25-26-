# Ex.No:3(b) POLYMORPHISM

## QUESTION:
Write a Java program to:

Create a base class Shape with methods draw() and calculateArea().

Create two subclasses:

Circle: overrides draw() and calculateArea() to handle a circle.

Cylinder: overrides draw() and overrides calculateArea() to calculate the total surface area of the cylinder 

Take input from the user to choose between circle and cylinder, and input relevant dimensions.

## AIM:

To write a Java program that implements inheritance by creating a base class Shape with methods draw() and calculateArea(), and two subclasses Circle and Cylinder that override these methods. The program takes user input to choose the shape and calculate its area accordingly.

## ALGORITHM :
1.Start the program.

2.Create a base class Shape with:

Method draw() — displays a general message.

Method calculateArea() — returns 0 by default.

3.Create a subclass Circle extending Shape:

Attribute: radius.

Override draw() to show that a circle is being drawn.

Override calculateArea() using formula:

<img width="226" height="41" alt="image" src="https://github.com/user-attachments/assets/de7182cb-1975-4502-bc85-bbf4633daea9" />


4.Create subclass Cylinder extending Shape:

Attributes: radius, height.

Override draw() to show that a cylinder is being drawn.

Override calculateArea() to compute total surface area of cylinder:

<img width="270" height="44" alt="image" src="https://github.com/user-attachments/assets/e7513524-a6bb-433c-8f0b-e3d60ec0580a" />


5.In the main() method:

Ask the user to choose Circle or Cylinder.

Input required dimensions (radius, height).

Create the corresponding object.

Call the draw() method.

Call and print the result of calculateArea().

6.End the program.


## PROGRAM:
 ```
/*
Program to implement a Polymorphism using Java
Developed by: SANDHIYA R
RegisterNumber:  212222230129
*/
```

## SOURCE CODE:
```
import java.util.*;

class Shape {
    double radius;
    double height;

    Shape(double radius, double height) {
        this.radius = radius;
        this.height = height;
    }

    void draw() {
        System.out.println("Drawing a shape...");
        System.out.printf("Area: %.2f%n", calculateArea());
    }

    double calculateArea() {
        return 0.0;
    }
}

class Circle extends Shape {
    Circle(double radius) {
        super(radius, 0);
    }

    @Override
    void draw() {
        System.out.println("Drawing a circle...");
        System.out.printf("Area: %.2f%n", calculateArea());
    }

    @Override
    double calculateArea() {
        return Math.PI * radius * radius;
    }
}

class Cylinder extends Shape {
    Cylinder(double radius, double height) {
        super(radius, height);
    }

    @Override
    void draw() {
        System.out.println("Drawing a cylinder...");
        System.out.printf("Area: %.2f%n", calculateArea());
    }

    @Override
    double calculateArea() {
        return (2 * Math.PI * radius * height) + (2 * Math.PI * radius * radius);
    }
}

public class Main {
    public static void main(String[] args) {
        Scanner in = new Scanner(System.in);
        String shapeType = in.next().toLowerCase();

        if (shapeType.equals("circle")) {
            double radius = in.nextDouble();
            Shape c = new Circle(radius);
            c.draw();
        } else if (shapeType.equals("cylinder")) {
            double radius = in.nextDouble();
            double height = in.nextDouble();
            Shape cy = new Cylinder(radius, height);
            cy.draw();
        } else {
            System.out.println("Invalid shape type.");
        }

        in.close();
    }
}
```

## OUTPUT:


<img width="633" height="314" alt="image" src="https://github.com/user-attachments/assets/98bbcc7c-2aa7-421e-a295-6a78ff95d3d1" />


## RESULT:
The program successfully demonstrates runtime polymorphism using inheritance. It creates a Shape base class and overrides behaviors in Circle and Cylinder subclasses. Based on user input, the program draws the selected shape and calculates either the area of a circle or the total surface area of a cylinder.

