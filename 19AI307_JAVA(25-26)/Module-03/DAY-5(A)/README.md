# Ex.No:3(E) INNER CLASS

## QUESTION:
Write a Java program to create an enum Season with values WINTER, SPRING, SUMMER, and FALL. Use a switch statement to display a custom message based on the current season.

## AIM:
To demonstrate the use of enum types and switch statements in Java by displaying messages for different seasons.

## ALGORITHM :
Start the program.

Create an enum Season with values: WINTER, SPRING, SUMMER, FALL.

Take user input for the current season (as a string).

Convert the input to the corresponding enum value.

Use a switch statement on the Season value:

WINTER → print "It's cold and snowy!"

SPRING → print "Flowers are blooming!"

SUMMER → print "Time for sunshine and beaches!"

FALL → print "Leaves are falling!"

Display the message.

End the program.


## PROGRAM:
 ```
/*
Program to implement a InnerClass using Java
Developed by: SANDHIYA R
RegisterNumber:  212222230129
*/
```

## SOURCE CODE:


```

import java.util.*;

enum Season {
    WINTER, SPRING, SUMMER, FALL
}

public class Main {
    public static void main(String[] args) {
        Scanner sc = new Scanner(System.in);
        String input = sc.nextLine().trim().toUpperCase(); // Convert input to uppercase

        Season season;
        try {
            season = Season.valueOf(input); // Convert string to enum
        } catch (IllegalArgumentException e) {
            System.out.println("Invalid season input.");
            return;
        }

        switch (season) {
            case WINTER:
                System.out.println("It's cold outside. Stay warm!");
                break;
            case SPRING:
                System.out.println("Flowers are blooming. Enjoy the fresh air!");
                break;
            case SUMMER:
                System.out.println("It's sunny and hot. Time for the beach!");
                break;
            case FALL:
                System.out.println("Leaves are falling. Autumn is beautiful!");
                break;
        }
    }
}
```


## OUTPUT:


<img width="953" height="242" alt="image" src="https://github.com/user-attachments/assets/43a3f9e7-6d88-4615-b4d3-06d77c6aab9a" />


## RESULT:

The program accepts a season from the user, maps it to an enum value, and uses a switch case to print a season-specific message successfully.
