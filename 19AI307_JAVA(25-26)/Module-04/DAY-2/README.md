# Ex.No:4(B)  IMPLEMENT SOLID PRINCIPLES IN JAVA PROGRAM 

## QUESTION:

Write a Java program using the Singleton Design Pattern to create a centralized Logger shared by multiple microservices (like AuthService, UserService, OrderService).

## AIM:
To implement a Singleton Logger that stores and displays logs sent by different services in a microservices architecture. The logger must:

Ensure only one logger instance exists.

Store all log messages in order.

Print all logs every time a new log is added.

## ALGORITHM :
Create a Singleton Logger class

Make the constructor private.

Create a static instance inside the class.

Provide a getInstance() method to return the same instance.

Maintain log history

Use an ArrayList<String> to store all logs.

addLog() method

Add it to the ArrayList.

Print the new log.

Print all previous logs with numbering.

Main program

Read number of logs.

For each input line, split service, level, and message.

Get the Singleton logger using getInstance().

Call addLog().


## PROGRAM:
 ```
/*
Program to implement a SOLID Principles in Java Program
Developed by: SANDHIYA R
RegisterNumber:  212222230129
*/
```

## SOURCE CODE:
```
import java.util.*;

class Logger {
    public static Logger log=new Logger();
    public static  ArrayList<String> currentlogs=new ArrayList<>();
    
    private Logger() {
       //Type your code
    }

    public static Logger getInstance() {
        return log;
    }

    public void addLog(String service, String level, String message) {
        String a=service+" "+level+": "+message;
        currentlogs.add(a);
        System.out.println(service+" "+level+": "+message);
        System.out.println("Current Logs:");
        int i=1;
        for(String c:currentlogs)
        {
            System.out.println(i+". "+c);
            i+=1;
            
        }
        
    }
}
public class prog {
    public static void main(String[] args) {
        Scanner sc = new Scanner(System.in);
        int n = sc.nextInt(); sc.nextLine();

        for (int i = 0; i < n; i++) {
            String[] input = sc.nextLine().split(" ");
            String service = input[0];
            String level = input[1];
            String message = input[2];

            Logger logger = Logger.getInstance();
            logger.addLog(service, level, message);
            System.out.println();
        }
    }
}
```


## OUTPUT:
<img width="1194" height="689" alt="image" src="https://github.com/user-attachments/assets/108481ba-a5d0-44d7-93af-186e182ccc38" />



## RESULT:
The program successfully:

Ensures only one logger instance for the entire system.

Adds each service log to a centralized log list.

Prints full log history every time a new entry is added.

Demonstrates clear use of:
✔ Singleton Pattern
✔ Centralized Logging
✔ String formatting
✔ Collections in Java
