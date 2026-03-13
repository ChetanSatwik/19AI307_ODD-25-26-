# Ex.No:1(B) CONDITIONAL STATEMENT

## QUESTION:
A library charges a fine for every book returned late. For first 5 days the fine is 50 paise, for 6-10 days fine is one rupee and above 10 days fine is 5 rupees. If you return the book after 30 days your membership will be cancelled - Print ("Your Membership would be Cancelled.")

Write a program to accept the number of days the member is late to return the book and display the fine or the appropriate message

## AIM:
To write a Java program to accept the number of late days and calculate the library fine or display a membership cancellation message.

## ALGORITHM :
1. Start the program and read the number of late days from the user.

2. If the days are less than or equal to 5, calculate the fine as days × 0.50.

3. Else if the days are between 6 and 10, calculate the fine as days × 1.00.

4. Else if the days are between 11 and 30, calculate the fine as days × 5.00.

5. If the days are more than 30, display the fine and print "Your Membership would be Cancelled." then stop the program.



## PROGRAM:
 ```java
import java.util.Scanner;

public class LibraryFine {
    public static void main(String[] args) {
        Scanner sc = new Scanner(System.in);
        int days = sc.nextInt();
        sc.close();

        double fine = 0.0;

        if (days <= 5) {
            fine = days * 0.50;
            System.out.printf("Fine Amount Pay to Rs :%.2f%n", fine);
        } else if (days <= 10) {
            fine = days * 1.00;
            System.out.printf("Fine Amount Pay to Rs :%.2f%n", fine);
        } else if (days <= 30) {
            fine = days * 5.00;
            System.out.printf("Fine Amount Pay to Rs :%.2f%n", fine);
        } else {
            fine = days * 5.00;
            System.out.printf("Fine Amount Pay to Rs :%.2f%n", fine);
            System.out.println("Your Membership would be Cancelled.");
        }
    }
}
```

## SOURCE CODE:







## OUTPUT:



## RESULT:
The program successfully calculates the library fine based on the number of late days and displays the fine or the membership cancellation message.
