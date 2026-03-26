# Ex.No:4(A) EXCEPTION HANDLING

## QUESTION:
You have a program that reads an integer from the user. The program must reject any negative number by throwing a special error.How would you design a custom exception to handle this? What message would you display if the user enters a negative number?

## AIM:
To design a custom exception in Java that rejects negative numbers entered by the user.

## ALGORITHM :
1. Create a custom exception class by extending Exception.
2. Define a constructor that accepts an error message.
3. In the main program, read an integer input from the user.
4. Check if the number is negative; if yes, throw the custom exception.
5. Catch the exception and display an appropriate error message.




## PROGRAM:
 ```java
/*
Program to implement a Exception Handling using Java
Developed by: N V Chetan Satwik
RegisterNumber:  212224240100
*/
import java.util.Scanner;

class NegativeNumberException extends Exception {
    public NegativeNumberException(String message) {
        super(message);
    }
}

public class Main {
    public static void main(String[] args) {
        Scanner scanner = new Scanner(System.in);
        int number = scanner.nextInt();

        try {
            if (number < 0) {
                throw new NegativeNumberException("Negative numbers are not allowed");
            }
            System.out.println("Valid input: " + number);
        } catch (NegativeNumberException e) {
            System.out.println(e.getMessage());
        }

        scanner.close();
    }
}


```

## SOURCE CODE:







## OUTPUT:
<img width="885" height="306" alt="image" src="https://github.com/user-attachments/assets/c856bdf7-af6c-410e-a83e-0ddee63e49c0" />



## RESULT:
A custom exception successfully handles negative input and displays the message: “Negative numbers are not allowed.”
