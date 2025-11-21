# Ex.No:4(E) DESIGN PATTERN  ---- BEHAVIOUR PATTERN

## QUESTION:
Write a DAO class for a Contact model with fields like name and phone. Implement a method to return all contacts starting with a specific letter.

## AIM:

To implement a Data Access Object (DAO) class for managing Contact data.
The program should store multiple contacts and retrieve all contacts whose names begin with a specified letter.

## ALGORITHM :
Start the program.

Create a Contact model class with:

name

phone

Getter methods.

Create a ContactDAO class that contains:

A list to store Contact objects.

addContact(Contact c) to add a contact.

getContactsStartingWith(char ch) to return contacts whose names start with the given letter.

In main():

Read the number of contacts.

For each contact:

Read name and phone.

Store using addContact().

Read a letter from the user.

Call getContactsStartingWith() with the letter.

Print all matching contacts.

End the program.



## PROGRAM:
 ```
/*
Program to implement a Behaviour Pattern using Java
Developed by: SANDHIYA R
RegisterNumber:  212222230129
*/
```

## SOURCE CODE:
```
import java.util.*;

public class ContactDAOExample {

    // ===== Model =====
    static class Contact {
        private String name;
        private String phone;

        public Contact(String name, String phone) {
            this.name = name;
            this.phone = phone;
        }

        public String getName() { return name; }
        public String getPhone() { return phone; }
    }

    // ===== DAO =====
    static class ContactDAO {
        private List<Contact> contacts = new ArrayList<>();

        public void addContact(Contact c) {
            contacts.add(c);
        }

        public List<Contact> getContactsStartingWith(char ch) {
            List<Contact> result = new ArrayList<>();
            for (Contact c : contacts) {
                if (!c.getName().isEmpty() && Character.toUpperCase(c.getName().charAt(0)) == Character.toUpperCase(ch)) {
                    result.add(c);
                }
            }
            return result;
        }
    }

    // ===== Main =====
    public static void main(String[] args) {
        Scanner sc = new Scanner(System.in);
        ContactDAO dao = new ContactDAO();

        int n = sc.nextInt();
        sc.nextLine();

        for (int i = 0; i < n; i++) {
            String name = sc.nextLine();
            String phone = sc.nextLine();
            dao.addContact(new Contact(name, phone));
        }

        String letter = sc.nextLine().trim();
        if (!letter.isEmpty()) {
            List<Contact> filtered = dao.getContactsStartingWith(letter.charAt(0));
            for (Contact c : filtered) {
                System.out.println(c.getName());
                System.out.println(c.getPhone());
            }
        }

        sc.close();
    }
}

```

## OUTPUT:

<img width="493" height="765" alt="image" src="https://github.com/user-attachments/assets/ab5d9348-c58d-47cf-92e0-f996e7c4ba3f" />


## RESULT:
The program successfully demonstrates the DAO pattern by storing Contact objects and retrieving only those whose names start with a given letter. The filtered contacts are displayed correctly based on user input.
