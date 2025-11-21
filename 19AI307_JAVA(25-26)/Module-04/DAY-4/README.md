# Ex.No:4(D) DESIGN PATTERN -- ABSTRACT FACTORY

## QUESTION:
You’re creating a cross-platform UI tool using the Abstract Factory pattern. Implement factories to create Button and Checkbox for "dark" and "light" themes. Let the user choose the theme, then generate UI components and display their types

## AIM:
To implement the Abstract Factory Design Pattern in Java for generating UI components.
Based on the user’s chosen theme ("dark" or "light"), the program should create and display the corresponding Button and Checkbox types.

## ALGORITHM :
Start the program.

Define Button and Checkbox interfaces with a render() method.

Implement concrete classes:

DarkButton, DarkCheckbox

LightButton, LightCheckbox

Create the UIFactory interface with methods:

createButton()

createCheckbox()

Implement factory classes:

DarkUIFactory

LightUIFactory

In the main() method:

Accept the theme name from the user.

If the theme is "dark", create DarkUIFactory.

If "light", create LightUIFactory.

Use the factory to create Button and Checkbox.

Call render() to display the created UI components.

If the theme is invalid, display an error message.

End the program.


## PROGRAM:
 ```
/*
Program to implement a Abstract Factory Pattern using Java
Developed by: SANDHIYA R
RegisterNumber:  212222230129
*/
```

## SOURCE CODE:
```
import java.util.*;

interface Button {
    void render();
}

interface Checkbox {
    void render();
}

class DarkButton implements Button {
    @Override
    public void render() {
        System.out.println("Dark Button created");
    }
}

class DarkCheckbox implements Checkbox {
    @Override
    public void render() {
        System.out.println("Dark Checkbox created");
    }
}

class LightButton implements Button {
    @Override
    public void render() {
        System.out.println("Light Button created");
    }
}

class LightCheckbox implements Checkbox {
    @Override
    public void render() {
        System.out.println("Light Checkbox created");
    }
}

interface UIFactory {
    Button createButton();
    Checkbox createCheckbox();
}

class DarkUIFactory implements UIFactory {
    public Button createButton() { return new DarkButton(); }
    public Checkbox createCheckbox() { return new DarkCheckbox(); }
}

class LightUIFactory implements UIFactory {
    public Button createButton() { return new LightButton(); }
    public Checkbox createCheckbox() { return new LightCheckbox(); }
}

public class Main {
    public static void main(String[] args) {
        Scanner sc = new Scanner(System.in);
        while (sc.hasNextLine()) {
            String line = sc.nextLine();
            if (line == null) break;
            String theme = line.trim();
            if (theme.isEmpty()) continue;

            String lower = theme.toLowerCase();
            UIFactory factory = null;

            if (lower.equals("dark")) {
                factory = new DarkUIFactory();
            } else if (lower.equals("light")) {
                factory = new LightUIFactory();
            } else {
                System.out.println("Invalid theme");
                continue;
            }
            Button button = factory.createButton();
            Checkbox checkbox = factory.createCheckbox();
            button.render();
            checkbox.render();
        }
        sc.close();
    }
}
```

## OUTPUT:
<img width="716" height="290" alt="image" src="https://github.com/user-attachments/assets/422bd906-6ec4-4205-ab34-c56bfff50380" />

## RESULT:
The program successfully implements the Abstract Factory Pattern, allowing the user to select a theme and generating the appropriate Button and Checkbox components for Dark or Light UI themes.
