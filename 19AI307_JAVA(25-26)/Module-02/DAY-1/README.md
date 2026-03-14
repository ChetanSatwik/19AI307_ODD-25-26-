# Ex.No:2(A) CLASS AND OBJECT

## QUESTION:
Create a class Course with attributes code, title, credits.

## AIM:
To create a class Course with attributes code, title, and credits to represent course details using object-oriented programming.

## ALGORITHM :
1.	Start the program.
2.	Import the necessary package 'java.util'
3.	Define a class Course with attributes code, title, and credits, and create a constructor to initialize them.
4.	Create a method printDetails() to display the course information.
5.	In the main method, read course details using Scanner and create a Course object.
6.	Call printDetails() to display the course details and repeat until input ends.


## PROGRAM:
 ```java
/*
Program to implement a Class and Objects using Java
Developed by: N V Chetan Satwik
RegisterNumber: 212224240100
import java.util.Scanner;

class Course {
    String code;
    String title;
    int credits;

    Course(String code, String title, int credits) {
        this.code = code;
        this.title = title;
        this.credits = credits;
    }

    void printDetails() {
        System.out.println(code + " | " + title + " | " + credits + " credits");
    }
}

public class Main {
    public static void main(String[] args) {
        Scanner scanner = new Scanner(System.in);

        while (scanner.hasNext()) {
            String code = scanner.next();
            String title = scanner.next();
            int credits = scanner.nextInt();

            Course course = new Course(code, title, credits);
            course.printDetails();
        }

        scanner.close();
    }
} 
*/
```

## SOURCE CODE:







## OUTPUT:
![alt text](image.png)


## RESULT:
The program successfully creates a Course object and displays the course code, title, and credits entered by the user.
