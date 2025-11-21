# Ex.No:5(D) THREAD PRIORITY

## QUESTION:
Write a java program for set the priority and name of the current thread.Consider two threads t1 and t2

Note : Read the threadname from the User

set the priority as 4 for t1 and set the priority as 2 for t2

## AIM:
To write a java program for set the priority and name of the current thread.Consider two threads t1 and t2 , set the priority as 4 for t1 and set the priority as 2 for t2

## ALGORITHM :
Start the program.

Read two thread names from the user.

Reference the current thread as t1.

Set:

t1 name using user input.

t1 priority as 4.

Create a new thread t2.

Set:

t2 name using user input.

t2 priority as 2.

Display details of both threads.

End the program.

## PROGRAM:
 ```
/*
Program to implement a Thread Priority Concept using Java
Developed by: SANDHIYA R
RegisterNumber:  212222230129
*/
```

## SOURCE CODE:
```
import java.util.Scanner;

public class TwoThreadsInfo {
    public static void main(String[] args) {
        Scanner sc = new Scanner(System.in);

        String name1 = sc.nextLine();
        String name2 = sc.nextLine();

        Thread t1 = Thread.currentThread();
        t1.setName(name1);
        t1.setPriority(4);
        System.out.println(t1);

        Thread t2 = new Thread();
        t2.setName(name2);
        t2.setPriority(2);
        System.out.println(t2);
    }
}
```






## OUTPUT:

<img width="837" height="251" alt="image" src="https://github.com/user-attachments/assets/b3b91277-aced-4b9b-85de-9e81648ca0e1" />


## RESULT:
The program successfully reads two thread names from the user and assigns:

Thread t1 → priority 4

Thread t2 → priority 2

The thread details are displayed correctly.
