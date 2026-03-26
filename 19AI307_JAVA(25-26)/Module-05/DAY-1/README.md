# Ex.No:5(A) INPUTSTREAMREADER 

## QUESTION:
Write a program to read user input from the keyboard using InputStreamReader

## AIM:
To read user input from the keyboard using InputStreamReader in Java.

## ALGORITHM :
1. Import required classes (InputStreamReader, BufferedReader).
2. Create an InputStreamReader object using System.in.
3. Wrap it with a BufferedReader for efficient reading.
4. Read input from the user using readLine().
5. Display the entered input.





## PROGRAM:
 ```
/*
Program to implement a InputStreamReader using Java
Developed by: N V Chetan Satwik
RegisterNumber: 212224240100
*/
```

## SOURCE CODE:
```java
import java.io.*;

public class Main {
    public static void main(String[] args) throws Exception {
        InputStreamReader isr = new InputStreamReader(System.in);
        BufferedReader br = new BufferedReader(isr);
        
        String name = br.readLine();
        System.out.println("Hello, " + name + "!");
    }
}
```






## OUTPUT:

<img width="489" height="213" alt="image" src="https://github.com/user-attachments/assets/cf6c6bb2-9001-47a9-a9d1-0b7469e0502b" />


## RESULT:
The program successfully reads input from the keyboard using InputStreamReader and displays it.
