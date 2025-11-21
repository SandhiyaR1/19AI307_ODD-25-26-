# Ex.No:1(A) INTRODUCTION TO JAVA PROGRAMMING, DATA TYPES, VARIABLES AND OPERATORS

## QUESTION:
Lovely enters a mystical Power Chamber with 10 doors.
Behind each door is a magic symbol that changes her power in a unique way using compound assignment operators.

She starts with an initial power value, and here's what happens at each door:

Door	Operation	Description
1	+=5	Adds 5 to the power
2	-=3	Subtracts 3
3	*=2	Multiplies power by 2
4	/=4	Divides power by 4
5	%=3	Power mod 3
6	&=7	Bitwise AND with 7
7	^=4	Bitwise XOR with 4
8	<<=1	Left shift by 1
9	>>=1	Right shift by 1


## AIM:
To write a Java program that takes an initial power value and applies a series of compound assignment operations (such as +=, -=, *=, /=, %=, |=, &=, ^=, <<=, >>=) to display how the power changes after passing through each mystical door.


## ALGORITHM :

1.Start the program.

2.Read the initial power value (integer input from the user using Scanner).

3.Display the initial power before entering the doors.

4.Apply each compound assignment operation step-by-step on the power value:

   Add 5
   
   Subtract 3
   
   Multiply by 2
   
   Divide by 4
   
   Modulus with 3
   
   Bitwise OR with 2
   
   Bitwise AND with 7
   
   Bitwise XOR with 4
   
   Left shift by 1
   
   Right shift by 1

5.Display the updated power after each door.

6.Print the final power after all operations are completed.

7.End the program.

## PROGRAM:
 ```
/*
Program to implement variables and Operators using Java
Developed by: Sandhiya R
RegisterNumber:  212222230129
*/
```

## Sourcecode.java:
```
import java.util.*;
public class Main{
    public static void main(String args[])
    {
        Scanner sc=new Scanner(System.in);
        int n=sc.nextInt();
        System.out.println("Initial Power = "+n);
        int a=n+5;
        System.out.println("After Door 1 (+= 5): "+a);
         a=a-3;
        System.out.println("After Door 2 (-= 3): "+a);
         a=a*2;
        System.out.println("After Door 3 (*= 2): "+a);
        a/=4;
        System.out.println("After Door 4 (/= 4): "+a);
        a%=3;
        System.out.println("After Door 5 (%= 3): "+a);
        a|=2;
        System.out.println("After Door 6 (|= 2): "+a);
        a&=7;
        System.out.println("After Door 7 (&= 7): "+a);
        a^=4;
        System.out.println("After Door 8 (^= 4): "+a);
        a<<=1;
        System.out.println("After Door 9 (<<= 1): "+a);
        a>>=1;
        System.out.println("After Door 10 (>>= 1): "+a);
        System.out.println("Final Power = "+a);
    }
}
```
## OUTPUT:
<img width="693" height="729" alt="image" src="https://github.com/user-attachments/assets/b0b555dc-fd55-4b21-9410-df106776fe38" />


## RESULT:

The program successfully demonstrates the use of various compound assignment operators in Java.
The final power value is correctly computed after applying all operations step-by-step.
