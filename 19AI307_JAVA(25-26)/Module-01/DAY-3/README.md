# Ex.No:1(C) LOOPING STATEMENT

## QUESTION:
Reversing a number means rearranging its digits in the opposite order. For example:

The reverse of 1234 is 4321

The reverse of 9870 is 789 (since leading zeros in the reversed number are not shown)

Write a Java program that takes an integer input from the user and then reverses its digits using a while loop.

The program should repeatedly extract the last digit of the number using the modulus operator (%) and then build the reversed number.

The loop should continue until the number becomes 0.

Finally, display the reversed number as output.

## AIM:
To write a Java program to reverse the digits of a given integer using a while loop.

## ALGORITHM :
1. Start the program and read an integer from the user.

2. Initialize a variable reversed = 0.

3. Repeat while the number is not equal to 0.

4. Extract the last digit using number % 10, update reversed = reversed × 10 + digit, and divide the number by 10.

5. Display the reversed number and stop the program.


## PROGRAM:
 ```java
import java.util.Scanner;

public class ReverseNumber {
    public static void main(String[] args) {
        Scanner sc = new Scanner(System.in);
        int number = sc.nextInt();
        int reversed = 0;
        
        while (number != 0) {
            int digit = number % 10;
            reversed = reversed * 10 + digit;
            number = number / 10;
        }
        
        System.out.println("Reversed number: " + reversed);
        sc.close();
    }
}

```

## SOURCE CODE:







## OUTPUT:
![alt text](image.png)

## RESULT:
The program successfully reverses the digits of the given integer using a while loop and displays the reversed number.

