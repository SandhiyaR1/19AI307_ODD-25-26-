# Ex.No:2(E) ACCESS MODIFIERS

## QUESTION:

Create a class Calculator with: One non-static method add(int a, int b) that returns the sum, One static method info() that says "Calculator is ready".
## AIM:
To write a Java program that creates a class Calculator with a non-static method add(int a, int b) to return the sum of two numbers and a static method info() that displays a message indicating the calculator is ready.

## ALGORITHM :

1.Start the program.

2.Create a class Calculator with:

A non-static method add(int a, int b) that returns a + b.

A static method info() that prints "Calculator is ready".

3.In the main() method:

Read two integers from the user.

Call the static method info() using the class name.

Create an object of the Calculator class.

4.Call the non-static method add() using the object and display the result.

5.End the program.




## PROGRAM:
 ```
/*
Program to implement a Access Modifiers using Java
Developed by: Sandhiya R
RegisterNumber:  212222230129
*/
```

## SOURCE CODE:

```

import java.util.Scanner;
class Calculator {
    int a;
    int b;
    
    public int add(int a,int b)
    {
        return a+b;
    }
    public static void info()
    {
        System.out.println("Calculator is ready");
        
    }
}

class prog {
    public static void main(String[] args) {
        Scanner sc=new Scanner(System.in);
        int a=sc.nextInt();
        int b=sc.nextInt();
        Calculator.info();
        Calculator c=new Calculator();
        System.out.print("Sum: "+c.add(a,b));
    }
}

```


## OUTPUT:
<img width="710" height="332" alt="image" src="https://github.com/user-attachments/assets/10b1761a-9f70-490f-b310-b6f1222069be" />



## RESULT:

The program successfully defines a Calculator class with both static and non-static methods. It reads two numbers from the user, displays the readiness message, and prints the correct sum using the non-static add method.
