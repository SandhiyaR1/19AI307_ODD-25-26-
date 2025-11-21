# Ex.No:3(D)    INTERFACE 

## QUESTION:

Write a Java program where two bots (SunBot and RainBot) implement a WeatherBot interface with a method predict(int temperature).
Based on user choice (1 for SunBot, 2 for RainBot) and temperature input, display the weather prediction.

## AIM:
To implement polymorphism using interfaces by creating weather-prediction bots (SunBot and RainBot) that provide predictions based on temperature and user-selected bot type.

## ALGORITHM :
Start.

Create an interface WeatherBot with method String predict(int temperature).

Create class SunBot implementing the interface:

Return "HOT" if temperature > 30

Else return "MODERATE"

Create class RainBot implementing the interface:

Return "COLD" if temperature < 20

Else return "WARM"

Take input:

temperature

botType (1 or 2)

If botType = 1 → create SunBot
If botType = 2 → create RainBot

Call the predict() method using the selected bot.

Display the prediction.

End.



## PROGRAM:
 ```
/*
Program to implement a Interface using Java
Developed by: SANDHIYA R
RegisterNumber:  212222230129
*/
```

## SOURCE CODE:
```
import java.util.Scanner;

interface WeatherBot {
    String predict(int temperature);
}

class SunBot implements WeatherBot {
    public String predict(int temperature) {
        return temperature > 30 ? "HOT" : "MODERATE";
    }
}

class RainBot implements WeatherBot {
    public String predict(int temperature) {
        return temperature < 20 ? "COLD" : "WARM";
    }
}

public class Main {
    public static void main(String[] args) {
        Scanner scanner = new Scanner(System.in);

        int temperature = scanner.nextInt();
        int botType = scanner.nextInt();
        
        WeatherBot bot;
        if (botType == 1) {
            bot = new SunBot();
        } else if (botType == 2) {
            bot = new RainBot();
        } else {
            System.out.println("Invalid botType");
            return;
        }
        
        System.out.println(bot.predict(temperature));
    }
}
```






## OUTPUT:

<img width="440" height="152" alt="image" src="https://github.com/user-attachments/assets/8343776b-edf2-4f10-9cde-4d98870fafe0" />



## RESULT:

The program successfully takes temperature and bot type as input, creates the corresponding bot object, and displays an accurate weather prediction using polymorphism.
