# Ex.No:1(E) STRINGS AND MATH FUNCTION

## QUESTION:
Write a Java program to remove all vowels from a given string.

## AIM:
To write a Java program that takes a string as input and removes all vowels (both uppercase and lowercase) from it.

## ALGORITHM :

1.Start the program.

2.Input a string from the user.

3.Initialize an empty result string.

4.Traverse each character of the input string using a loop.

5.For each character, check whether it is a vowel (a, e, i, o, u in both cases).

6.If the character is not a vowel, append it to the result string.

7.After the loop ends, print the string without vowels.

8.End the program.




## PROGRAM:
 ```
/*
Program to implement a Strings and Math Function using Java
Developed by: Sandhiya R
RegisterNumber:  212222230129
*/
```

## SOURCE CODE:

```
import java.util.*;
public class Main
{
    public static void main(String[] args)
    {
        Scanner in=new Scanner(System.in);
        String str=in.next();
        System.out.println("String without vowels: "+str.replaceAll("[AEIOUaeiou]",""));
        
    }
}
```

## OUTPUT:

<img width="841" height="251" alt="image" src="https://github.com/user-attachments/assets/de02b726-47a6-419e-b8a1-399e6a1e61ae" />


## RESULT:

The program successfully reads a string from the user and outputs the same string with all vowels removed.
