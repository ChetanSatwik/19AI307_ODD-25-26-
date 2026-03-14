# Ex.No:2(C) ACCESS SPECIFIERS

## QUESTION:
Write a Java program to create a class called Rectangle with private instance variables length and width. Provide public getter and setter methods to access and modify these variables

## AIM:
To create a Java class Rectangle with private instance variables length and width, and use public getter and setter methods to access and modify these values.

## ALGORITHM :
1.	Start the program.
2.	Import the necessary package 'java.util'
3.	Create a class Rectangle with private variables length and width.
4.	Define public setter methods setLength() and setWidth() and getter methods getLength() and getWidth().
5.	In the main method, read length and width from the user using Scanner.
6.	Create a Rectangle object, set the values using setters, and display them using getters.


## PROGRAM:
 ```
/*
Program to implement a Access Specifiers using Java
Developed by: N V Chetan Satwik
RegisterNumber:  212224240100
import java.util.Scanner;

class Rectangle {
    private double length;
    private double width;

    public void setLength(double length) {
        this.length = length;
    }

    public void setWidth(double width) {
        this.width = width;
    }

    public double getLength() {
        return length;
    }

    public double getWidth() {
        return width;
    }
}

public class Main {
    public static void main(String[] args) {
        Scanner scanner = new Scanner(System.in);

        double l = scanner.nextDouble();
        double w = scanner.nextDouble();

        Rectangle rect = new Rectangle();
        rect.setLength(l);
        rect.setWidth(w);

        System.out.println("Length: " + rect.getLength());
        System.out.println("Width: " + rect.getWidth());

        scanner.close();
    }
}
*/
```

## SOURCE CODE:







## OUTPUT:
![alt text](image.png)


## RESULT:
The program successfully sets and retrieves the length and width of a rectangle using getter and setter methods.
