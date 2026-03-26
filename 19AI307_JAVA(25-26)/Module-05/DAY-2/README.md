# Ex.No:5(B) SERIALIZATION AND DESERIALIZATION 

## QUESTION:
Write a Java program to serialize a collection of objects (like ArrayList<Student>) into a file.

## AIM:
To implement serialization and deserialization of Student objects in Java using ObjectOutputStream and ObjectInputStream.

## ALGORITHM :
1. Create a Student class that implements Serializable with fields id, name, and marks.
2. Read multiple student details from the user and store them in an ArrayList.
3. Use ObjectOutputStream to serialize and write the list of students to a file.
4. Use ObjectInputStream to read and deserialize the list from the file.
5. Display the deserialized student details.





## PROGRAM:
 ```
/*
Program to implement a Serialization and Deserialization using Java
Developed by: N V Chetan Satwik
RegisterNumber: 212224240100
*/
```

## SOURCE CODE:
```java
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

public class Main {
    @SuppressWarnings("unchecked")
    public static void main(String[] args) throws Exception {
        Scanner sc = new Scanner(System.in);
        int n = sc.nextInt();
        ArrayList<Student> list = new ArrayList<>();

        for (int i = 0; i < n; i++) {
            int id = sc.nextInt();
            sc.nextLine();
            String name = sc.nextLine();
            double marks = sc.nextDouble();
            list.add(new Student(id, name, marks));
        }

        String file = "students.dat";

        ObjectOutputStream oos = new ObjectOutputStream(new FileOutputStream(file));
        oos.writeObject(list);
        oos.close();
        System.out.println("Students serialized successfully into: " + file);

        ObjectInputStream ois = new ObjectInputStream(new FileInputStream(file));
        ArrayList<Student> result = (ArrayList<Student>) ois.readObject();
        ois.close();
        System.out.println("Students deserialized successfully from: " + file);
        System.out.println();

        System.out.println("Deserialized Students:");
        for (Student s : result) {
            System.out.println(s);
        }
    }
}
```






## OUTPUT:

<img width="1239" height="841" alt="image" src="https://github.com/user-attachments/assets/eabf7706-9d9b-495e-949d-84b52fa6ac05" />


## RESULT:
The program successfully serializes and deserializes Student objects, storing and retrieving their data from a file.
