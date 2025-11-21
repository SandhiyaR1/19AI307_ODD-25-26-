# Ex.No:1(C) LOOPING STATEMENT

## QUESTION:
Floyd’s Triangle is a right-angled triangular arrangement of numbers where the numbers start from 1 and increase sequentially row by row.

Write a Java program that:

Prompts the user to enter the number of rows for the triangle.

Uses nested loops to print Floyd’s Triangle.

Ensures that the numbers increase sequentially from the top row to the bottom row.


## AIM:

To write a Java program that takes the number of rows as input and prints Floyd’s Triangle using nested loops, ensuring that the numbers increase sequentially from 1 row by row.


## ALGORITHM :

1.Start the program.

2.Input the number of rows from the user.

3.Initialize a counter variable (e.g., num = 1) to store the next number to print.

4.Use an outer loop to iterate through each row from 1 to the given number of rows.

5.Use an inner loop to print numbers equal to the row number.

6.For each iteration of the inner loop:

7.Print the current value of num.
```
Increment num by 1.

After each row, move to a new line.
```
8.End the program.




## PROGRAM:
 ```
/*
Program to implement a Looping Statement using Java
Developed by: Sandhiya R
RegisterNumber:  212222230129
*/
```

## SOURCE CODE:
```
import java.util.*;
public class Main{
    public static void main(String args[])
    {
        Scanner sc=new Scanner(System.in);
        int n=sc.nextInt();
       int i,j;
       int num=1;
       for(i=0;i<n;i++)
       {
           for(j=0;j<=i;j++)
           {
               System.out.print(num+" ");
               num++;
           }
           System.out.println();
       }
    }
    
}
```


## OUTPUT:

<img width="536" height="461" alt="image" src="https://github.com/user-attachments/assets/33c526c9-d46b-4c43-b907-593de60efdb2" />


## RESULT:

The program successfully generates Floyd’s Triangle for the number of rows entered by the user, displaying sequential numbers in a right-angled triangular format.
