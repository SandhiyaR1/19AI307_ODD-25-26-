# Ex.No:5(B) SERIALIZATION AND DESERIALIZATION 

## QUESTION:

Write a Java program to serialize a collection of objects (like ArrayList<Student>) into a file.


## AIM:
To write a Java program to serialize a collection of objects (like ArrayList<Student>) into a file.



## ALGORITHM :
Start the program.

Create a Student class that implements Serializable with fields:

id

name

marks

Read the number of students from the user.

For each student:

Read id, name, and marks.

Create a Student object and add it to an ArrayList<Student>.

Create a file named students.dat.

Use ObjectOutputStream to serialize the entire list into the file.

Close the output stream.

Use ObjectInputStream to read the file and deserialize the list of students.

Close the input stream.

Print the deserialized student details.

End the program.




## PROGRAM:
 ```
/*
Program to implement a Serialization and Deserialization using Java
Developed by: SANDHIYA R
RegisterNumber:  212222230129
*/
```

## SOURCE CODE:
```
import java.io.*;
import java.util.*;

class Student implements Serializable {
    int id;
    String name;
    double marks;

    Student(int id, String name, double marks) {
        this.id = id;
        this.name = name;
        this.marks = marks;
    }

    public String toString() {
        return "Student{id=" + id + ", name='" + name + "', marks=" + marks + "}";
    }
}

public class SerializeStudentList {
    @SuppressWarnings("unchecked")
    public static void main(String[] args) throws Exception {
        Scanner sc = new Scanner(System.in);

        int n = Integer.parseInt(sc.nextLine());
        List<Student> list = new ArrayList<>();

        for (int i = 0; i < n; i++) {
            int id = Integer.parseInt(sc.nextLine());
            String name = sc.nextLine();
            double marks = Double.parseDouble(sc.nextLine());
            list.add(new Student(id, name, marks));
        }

        String filename = "students.dat";

        ObjectOutputStream oos = new ObjectOutputStream(new FileOutputStream(filename));
        oos.writeObject(list);
        oos.close();

        System.out.println("Students serialized successfully into: " + filename);

        ObjectInputStream ois = new ObjectInputStream(new FileInputStream(filename));
        List<Student> deserializedList = (List<Student>) ois.readObject();
        ois.close();

        System.out.println("Students deserialized successfully from: " + filename);
        System.out.println();
        System.out.println("Deserialized Students:");
        for (Student s : deserializedList) {
            System.out.println(s);
        }
    }
}
```





## OUTPUT:
<img width="1174" height="361" alt="image" src="https://github.com/user-attachments/assets/992afe25-fa27-4484-a3bc-2962537e4963" />



## RESULT:
The program successfully serializes a list of Student objects into a file (students.dat) and accurately deserializes the list back into Java objects. The deserialized student data is displayed correctly, confirming that object serialization and deserialization work as intended.
