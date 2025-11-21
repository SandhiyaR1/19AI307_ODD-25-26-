# Ex.No:5(C)  FILE HANDLING USING JAVA
## QUESTION:
Write a program to count the number of characters in a file.

## AIM:

To write a program to count the number of characters in a file.

## ALGORITHM :
Start the program.

Read a line of text from the user using Scanner.

Create a file named input.txt using FileWriter.

Write the input text into the file.

Close the file.

Count the number of characters in the input string using length().

Display the character count to the user.

End the program.





## PROGRAM:
 ```
/*
Program to implement a File Handling using Java
Developed by: SANDHIYA R
RegisterNumber:  212222230129
*/
```

## SOURCE CODE:
 ```
import java.io.*;
import java.util.Scanner;

public class CharacterCountInFile {
    public static void main(String[] args) throws IOException {
        Scanner sc = new Scanner(System.in);
        String text = sc.nextLine();

        FileWriter fw = new FileWriter("input.txt");
        fw.write(text);
        fw.close();

        int count = text.length();

        System.out.println("Number of characters written to the file: " + count);
    }
}
```






## OUTPUT:

<img width="1136" height="242" alt="image" src="https://github.com/user-attachments/assets/25671d03-f3fd-498d-b6ec-c3e627c542e1" />


## RESULT:
The program successfully writes the input text to a file and correctly counts and displays the number of characters present in the file.
