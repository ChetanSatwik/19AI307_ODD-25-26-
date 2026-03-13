# Ex.No:1(E) STRINGS AND MATH FUNCTION

## QUESTION:
Write a Java program to swap two strings without using a third variable.

## AIM:
To write a Java program to swap two strings without using a third variable.

## ALGORITHM :
1.	Start the program.
2.	Import the necessary package 'java.util'
3.	Start the program and read two strings A and B from the user.
4.	Concatenate both strings and store the result in A (A = A + B).
5.	Extract the original first string using substring and assign it to B.
6.	Extract the original second string from A using substring and assign it to A.
7.	Display the swapped values of A and B, then stop the program.


## PROGRAM:
 ```java
import java.util.Scanner;

public class Main {
    public static void main(String[] args) {
        Scanner sc = new Scanner(System.in);

        String a = sc.nextLine();
        String b = sc.nextLine();

        a = a + b;
        b = a.substring(0, a.length() - b.length());
        a = a.substring(b.length());

        System.out.println("After swapping:");
        System.out.println("First string (A): " + a);
        System.out.println("Second string (B): " + b);
    }
}
```

## SOURCE CODE:







## OUTPUT:



## RESULT:
The program successfully swaps the two input strings without using a third variable and displays the swapped strings.
