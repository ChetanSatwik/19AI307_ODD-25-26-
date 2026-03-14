# Ex.No:3(E) INNER CLASS

## QUESTION:
Write a Java program to create an inner class and access it from the outer class.

## AIM:
To write a Java program that demonstrates the creation of an inner class and accessing its members from the outer class.

## ALGORITHM :
1.	Start the program.
2.	Import the necessary package 'java.util'
3.	Create an outer class outer containing an inner class inner.
4.	Define a method display() inside the inner class to print a greeting message with the given name.
5.	In the outer class, create a method InnerObj() to create an object of the inner class and call its display() method.
6.	In the main method, read a name from the user using Scanner.
7.	Create an object of the outer class, call InnerObj() with the input name, and display the message.





## PROGRAM:
 ```java
/*
Program to implement a InnerClass using Java
Developed by: N V Chetan Satwik
RegisterNumber: 212224240100
import java.util.Scanner;
class outer{
    class inner{
        void display(String name){
            System.out.println("Hello, "+name+"! This message is from the Inner Class.");
        }
    }
    void InnerObj(String name)
    {
        inner o = new inner();
        o.display(name);
    }
}
public class Main{
    public static void main(String args[]){
        Scanner sc = new Scanner(System.in);
        String name = sc.nextLine();
        outer obj = new outer();
        obj.InnerObj(name);
    }
}
*/
```

## SOURCE CODE:







## OUTPUT:
![alt text](image.png)


## RESULT:
The program successfully creates and accesses an inner class from the outer class and prints a greeting message using the entered name.
