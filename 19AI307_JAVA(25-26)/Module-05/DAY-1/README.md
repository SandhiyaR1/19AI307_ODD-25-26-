# Ex.No:5(A) INPUTSTREAMREADER 

## QUESTION:
Write a program to read user input from the keyboard using InputStreamReader 


## AIM:
To write a program to read user input from the keyboard using InputStreamReader 


## ALGORITHM :
Start the program.

Create an InputStreamReader object to read bytes from System.in.

Wrap it inside a BufferedReader to read text efficiently.

Use readLine() to read a string input from the user.

Display a greeting message using the entered input.

Handle possible IOException using a try–catch block.

End the program.



## PROGRAM:
 ```
/*
Program to implement a InputStreamReader using Java
Developed by: SANDHIYA R
RegisterNumber:  212222230129
*/
```

## SOURCE CODE:
```
import java.io.*;

public class Main {
    public static void main(String[] args) {
        try {
            InputStreamReader isr = new InputStreamReader(System.in);
            BufferedReader br = new BufferedReader(isr);
            String name = br.readLine();
            System.out.println("Hello, " + name + "!");
        } catch (IOException e) {
            System.out.println(e);
        }
    }
}
```




## OUTPUT:
<img width="465" height="196" alt="image" src="https://github.com/user-attachments/assets/657f4981-9489-4d46-bc85-2559460aee88" />



## RESULT:

The program successfully reads user input from the keyboard using InputStreamReader and BufferedReader, and prints a greeting message with the entered name.
