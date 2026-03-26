# Ex.No:5(C)  FILE HANDLING USING JAVA
## QUESTION:
Ask the user for name, age, and email address. Write the collected data into a file called userdata.txt in a structured format.

## AIM:
To collect user details (name, age, email) and store them in a file named userdata.txt in a structured format.

## ALGORITHM :
1. Import required classes (Scanner, BufferedWriter, FileWriter).
2. Create a Scanner object to read user input.
3. Read name, age, and email from the user.
4. Use BufferedWriter to write the data into userdata.txt in a structured format.
5. Close the file and display a success message.





## PROGRAM:
 ```
/*
Program to implement a File Handling using Java
Developed by: N V Chetan Satwik
RegisterNumber: 212224240100
*/
```

## SOURCE CODE:
```java
import java.io.*;
import java.util.*;

public class Main {
    public static void main(String[] args) throws Exception {
        Scanner sc = new Scanner(System.in);
        String name = sc.nextLine();
        String age = sc.nextLine();
        String email = sc.nextLine();

        BufferedWriter bw = new BufferedWriter(new FileWriter("userdata.txt"));
        bw.write("User Information");
        bw.newLine();
        bw.write("================");
        bw.newLine();
        bw.write("Name  : " + name);
        bw.newLine();
        bw.write("Age   : " + age);
        bw.newLine();
        bw.write("Email : " + email);
        bw.close();

        System.out.println("User Information");
        System.out.println("================");
        System.out.println("Name  : " + name);
        System.out.println("Age   : " + age);
        System.out.println("Email : " + email);
    }
}
```






## OUTPUT:

<img width="745" height="287" alt="image" src="https://github.com/user-attachments/assets/398505be-13df-407d-b3c8-5632f408e743" />


## RESULT:
The program successfully collects user details and writes them into userdata.txt in a structured format.
