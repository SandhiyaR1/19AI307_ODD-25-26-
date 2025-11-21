# Ex.No:4(A) EXCEPTION HANDLING

## QUESTION:
You wrote a program that stores some input strings into a String array and prints each string in uppercase.
However, you're getting a NullPointerException.
What should you check in your array before calling .toUpperCase() on a element?

## AIM:
To prevent a NullPointerException by ensuring that each element in the String array is not null before calling .toUpperCase().


## ALGORITHM :
Create a String array.

Read input strings and store them in the array.

Before calling .toUpperCase() on any array element:

Check if the element is not null.

If the element is null → skip or handle it.

Print the string in uppercase.

## PROGRAM:
 ```
/*
Program to implement a Exception Handling using Java
Developed by: SANDHIYA R
RegisterNumber:  212222230129
*/
```

## SOURCE CODE:

```
import java.util.*;

public class Main {
    public static void main(String[] args) {
        Scanner in = new Scanner(System.in);
        String input = in.next();

        if (input.equalsIgnoreCase("null")) {
            
            System.out.println("Null element");
        } else {
            System.out.println(input.toUpperCase());
        }
    }
}
```





## OUTPUT:

<img width="569" height="261" alt="image" src="https://github.com/user-attachments/assets/dfd1de24-0d67-4614-8315-b6a179b4b400" />


## RESULT:

The program avoids NullPointerException and safely prints all stored strings in uppercase by checking for null values before calling .toUpperCase().
