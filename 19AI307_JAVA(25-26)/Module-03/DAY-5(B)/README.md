# Ex.No:3(F) WRAPPER CLASS

## QUESTION:

Write a Java program to check if a number is an Armstrong number using Math.pow() and the Integer wrapper class. Take input from the user.


## AIM:
To determine whether a number is an Armstrong number by calculating the sum of its digits raised to the power of the number of digits using Java’s Math.pow() and Integer wrapper class methods.

## ALGORITHM :
Start the program.

Take an integer input from the user.

Convert the number to a string using Integer.toString() to count the digits.

Extract each digit using modulus (%) and division.

For each digit, compute Math.pow(digit, numberOfDigits) and accumulate the sum.

Compare the sum with the original number:

If equal → Armstrong number.

Else → Not an Armstrong number.

Display the result.

End the program.



## PROGRAM:
 ```
/*
Program to implement a Wrapper Class using Java
Developed by:SANDHIYA R 
RegisterNumber: 212222230129
*/
```

## SOURCE CODE:
```
import java.util.Scanner;

public class Main {
    public static void main(String[] args) {
        Scanner scanner = new Scanner(System.in);

        int num = scanner.nextInt();
        scanner.close();

        int originalNum = num;
        int digits = String.valueOf(num).length();
        double sum = 0;

        while (num != 0) {
            int remainder = num % 10;
            sum += Math.pow(remainder, digits);
            num /= 10;
        }

        if (sum == originalNum) {
            System.out.println(originalNum + " is an Armstrong number.");
        } else {
            System.out.println(originalNum + " is not an Armstrong number.");
        }
    }
}
```




## OUTPUT:


<img width="827" height="246" alt="image" src="https://github.com/user-attachments/assets/1553f4cc-374c-40df-b46d-410bec036a25" />




## RESULT:

The program reads a number, computes the Armstrong sum using Math.pow() and the Integer wrapper class, and correctly identifies whether the number is an Armstrong number.
