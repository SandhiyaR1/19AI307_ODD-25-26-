# Ex.No:4(C)  COMPOSITION IN JAVA

## QUESTION:

A Department contains Professor objects, but professors can exist independently.
If no inputs gets passed, print "No professors assigned."

## AIM:
To write a Java program that demonstrates Aggregation, where a Department contains multiple Professor objects.

## ALGORITHM :
Start the program.

Create the Professor class

Include a private variable name.

Create a constructor to initialize the name.

Provide a getter method getName().

Create the Department class

Store the department name.

Maintain a List<Professor> to hold professors.

Implement addProfessor() to add a professor to the list.

Implement printDetails():

Print department name.

If the professor list is empty:

Print "No professors assigned."

Else, print the list of professors.

In the main method

Create a Department object with a predefined name.

Check if the user enters an integer (number of professors).

If yes:

Read the number of professors.

Use a loop to input each professor’s name.

Add each to the department.

Call printDetails() to show the output.

End the program.



## PROGRAM:
 ```
/*
Program to implement a Composition Concepts in Java
Developed by: SANDHIYA R
RegisterNumber:  212222230129
*/
```

## SOURCE CODE:

```
import java.util.ArrayList;
import java.util.List;
import java.util.Scanner;

class Professor {
    private String name;

    public Professor(String name) {
        this.name = name;
    }

    public String getName() {
        return name;
    }
}

class Department {
    private String name;
    private List<Professor> professors;

    public Department(String name) {
        this.name = name;
        this.professors = new ArrayList<>();
    }

    public void addProfessor(Professor professor) {
        professors.add(professor);
    }

    public void printDetails() {
        System.out.println("Department: " + name);

        if (professors.isEmpty()) {
            System.out.println("No professors assigned.");
            return;
        }

        for (Professor p : professors) {
            System.out.println("- " + p.getName());
        }
    }
}

public class Main {
    public static void main(String[] args) {
        Scanner sc = new Scanner(System.in);

        Department dept = new Department("Computer Science");

        if (sc.hasNextInt()) {
            int n = sc.nextInt();
            sc.nextLine(); // consume newline

            for (int i = 0; i < n; i++) {
                if (sc.hasNextLine()) {
                    String profName = sc.nextLine();
                    dept.addProfessor(new Professor(profName));
                }
            }
        }

        dept.printDetails();
    }
}

```

## OUTPUT:

<img width="841" height="209" alt="image" src="https://github.com/user-attachments/assets/31783a9a-138b-4368-ac42-82c69d191366" />

## RESULT:

The program successfully demonstrates Aggregation by linking professors to a department and correctly displays "No professors assigned." when no professor data is provided.
