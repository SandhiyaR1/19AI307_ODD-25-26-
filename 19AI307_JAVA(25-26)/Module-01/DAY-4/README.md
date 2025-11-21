# Ex.No:1(D) ARRAYS

## QUESTION:
Write a Java program to print all elements in an array that are greater than a given value
## AIM:
To write a Java program that reads an array of numbers and a comparison value, then prints all elements in the array that are greater than the given value.

## ALGORITHM :
1.Start the program.

2.Input the size of the array.

3.Read all array elements from the user.

4.Input the comparison value.

5.Traverse the array using a loop.

6.For each element, check if it is greater than the given value.

7.If true, print the element.

8.End the program.




## PROGRAM:
 ```
/*
Program to implement a Array concept using Java
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
        int n=in.nextInt();
        int arr[]=new int[n];
        for(int i=0;i<n;i++)
        {
            arr[i]=in.nextInt();
        }
        int number=in.nextInt();
        boolean flag=false;
        for(int i=0;i<n;i++)
        {
            if(arr[i]>number)
            {
                System.out.println(arr[i]);
                flag=true;
            }
        }
        if(!flag)
        {
            System.out.println("No elements greater than "+number);
        }
    }
}
```

## OUTPUT:
<img width="779" height="604" alt="image" src="https://github.com/user-attachments/assets/867070b3-e2c1-46ab-9a7e-49445524bb17" />



## RESULT:
The program successfully reads an array and displays all elements that are greater than the specified comparison value.
