# Ex.No:2(E) ACCESS MODIFIERS

## QUESTION:
Create a class Employee with method display(). Inside display(), return the current object using this. Create another method that calls display().printName()

## AIM:
To create a Java class Employee that returns the current object using this in the display() method and calls another method using display().printName().

## ALGORITHM :
1.	Start the program.
2.	Import the necessary package 'java.util'
3.	Create a class Employee with a variable name and a method setName() to assign the name.
4.	Define a method display() that returns the current object using this.
5.	Create a method printName() to display the employee name.
6.	In the main method, read the name, create an Employee object, set the name, call display().printName(), and end the program.





## PROGRAM:
 ```java
/*
Program to implement a Access Modifiers using Java
Developed by: N V Chetan Satwik
RegisterNumber: 212224240100
import java.util.*;
class Employee
{
    String name;
    void setName(String name)
    {
        this.name=name;
    }
    Employee display()
    {
        return this;
    }
    void printName()
    {
        System.out.println("Employee Name: "+name);
    }
}
class prog
{
    public static void main(String[] args)
    {
        Scanner sc=new Scanner(System.in);
        String name=sc.nextLine();
        Employee e=new Employee();
        e.setName(name);
        e.display().printName();
        sc.close();
    }
}
*/
```

## SOURCE CODE:







## OUTPUT:



## RESULT:
The program reads the employee name from the user and displays it using method chaining with this reference.
